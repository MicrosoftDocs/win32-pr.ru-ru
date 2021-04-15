---
description: Шаг 2.
ms.assetid: 8be83564-07ad-47cf-9538-73136f42ba79
title: Шаг 2. Реализация ИспеЦифипропертипажес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3125230c8e28c6bd6b8593839d7175bb43d39674
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683990"
---
# <a name="step-2-implement-ispecifypropertypages"></a>Шаг 2. Реализация ИспеЦифипропертипажес

Затем реализуйте интерфейс **испеЦифипропертипажес** в фильтре. Этот интерфейс содержит один метод, а **-страницы**, который ВОЗВРАЩАЕТ массив идентификаторов CLSID для страниц свойств, поддерживаемых фильтром. В этом примере фильтр содержит одну страницу свойств. Начните с создания идентификатора CLSID и объявления его в файле заголовка:


```C++
// Always create new GUIDs! Never copy a GUID from an example.
DEFINE_GUID(CLSID_SaturationProp, 0xa9bd4eb, 0xded5, 
0x4df0, 0xba, 0xf6, 0x2c, 0xea, 0x23, 0xf5, 0x72, 0x61);
```



Теперь реализуйте **метод WebMethod** :


```C++
class CGrayFilter : public ISaturation,
                    public ISpecifyPropertyPages, 
                    /* Other inherited classes. */
{
public:
    STDMETHODIMP GetPages(CAUUID *pPages)
    {
        if (pPages == NULL) return E_POINTER;
        pPages->cElems = 1;
        pPages->pElems = (GUID*)CoTaskMemAlloc(sizeof(GUID));
        if (pPages->pElems == NULL) 
        {
            return E_OUTOFMEMORY;
        }
        pPages->pElems[0] = CLSID_SaturationProp;
        return S_OK;
    }
};

/* ... */

}
```



Выделите память для массива с помощью функции **CoTaskMemAlloc**. Вызывающий объект выполнит освобождение памяти.

Далее. [Шаг 3. Поддержка QueryInterface](step-3--support-queryinterface.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание страницы свойств фильтра](creating-a-filter-property-page.md)
</dt> </dl>

 

 



