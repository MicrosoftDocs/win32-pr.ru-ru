---
title: Изменение свойства Scale
description: Изменение свойства Scale
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- проигрыватель Windows Media подключаемых модулей, свойства образца Echo
- подключаемые модули, свойства образца Echo
- подключаемые модули обработки цифровых сигналов, свойства образца эха
- Подключаемые модули DSP, свойства образца Echo
- Пример подключаемого модуля Echo DSP, свойство Scale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10073e01213469dcb6a85ddffd378421fddb6ae8f2fd432b9822c3a5046fdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574621"
---
# <a name="modifying-the-scale-property"></a>Изменение свойства Scale

Реализация мастера по умолчанию предоставляет свойство Scale. Вместо этого можно изменить существующую реализацию, чтобы предоставить свойство времени задержки.

Во-первых, используйте следующий пример, чтобы изменить прототипы функций для получения \_ масштабирования и разместить \_ масштаб в Echo. h. Измените имя методов и типы данных для параметров:


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



Затем измените реализации \_ методов Get Scale и разместить \_ Scale в Echo. cpp. Убедитесь, что код соответствует следующим примерам:


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



В предыдущем примере кода изменяются имена методов и типы данных параметров. Имя переменной члена должно быть изменено ранее. Не забудьте изменить комментарии, которые также посвящены каждому методу.

Теперь измените определение интерфейса. Следующий код заменяет код в объявлении интерфейса Иечо в Echo. IDL:


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Свойства образца Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




