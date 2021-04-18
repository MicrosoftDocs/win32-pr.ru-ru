---
description: Шаг 1.
ms.assetid: 1912af22-11dc-4864-8c20-91675d4f45d9
title: Шаг 1. Определение механизма установки свойства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a1845cfb3cdf5642378a2321e827e52720a83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673994"
---
# <a name="step-1-define-a-mechanism-for-setting-the-property"></a>Шаг 1. Определение механизма установки свойства

Фильтр должен поддерживать связь со страницей свойств, чтобы страница свойств могла устанавливать и получать свойства фильтра. К возможным механизмам относятся следующие.

-   Предоставление пользовательского COM-интерфейса.
-   Поддержка свойств автоматизации через **IDispatch**.
-   Предоставьте интерфейс **ипропертибаг** и определите набор именованных свойств.

В этом примере используется пользовательский COM-интерфейс с именем Исатуратион. Это не реальный интерфейс DirectShow. он определен только для этого примера. Начните с объявления интерфейса в файле заголовка вместе с идентификатором интерфейса (IID):


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(IID_ISaturation, 0x19412d6e, 0x6401, 
0x475c, 0xb0, 0x48, 0x7a, 0xd2, 0x96, 0xe1, 0x6a, 0x19);

interface ISaturation : public IUnknown
{
    STDMETHOD(GetSaturation)(long *plSat) = 0;
    STDMETHOD(SetSaturation)(long lSat) = 0;
};
```



Можно также определить интерфейс с помощью IDL и использовать компилятор MIDL для создания файла заголовка. Затем реализуйте пользовательский интерфейс в фильтре. В этом примере для значения насыщенности фильтра используются методы get и Set. Обратите внимание, что оба метода защищают \_ элемент m лсатуратион с помощью критической секции.


```C++
class CGrayFilter : public ISaturation, /* Other inherited classes. */
{
private:
    CCritSec  m_csShared;    // Protects shared data.
    long      m_lSaturation; // Saturation level.
public:
    STDMETHODIMP GetSaturation(long *plSat)
    {
        if (!plSat) return E_POINTER;
        CAutoLock lock(&m_csShared);
        *plSat = m_lSaturation;
        return S_OK;
    }
    STDMETHODIMP SetSaturation(long lSat)
    {
        CAutoLock lock(&m_csShared);
        if (lSat < SATURATION_MIN || lSat > SATURATION_MAX)
        {
            return E_INVALIDARG;
        }
        m_lSaturation = lSat;
        return S_OK;
    }
};
```



Разумеется, сведения о собственной реализации будут отличаться от приведенного здесь примера.

Далее. [Шаг 2. Реализуйте ИспеЦифипропертипажес](step-2--implement-ispecifypropertypages.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Класс Ккритсек**](ccritsec.md)
</dt> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 



