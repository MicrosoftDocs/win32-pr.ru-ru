---
description: Начиная с Windows 7 Microsoft Media Foundation предоставляет метаданные через интерфейс Ипропертисторе.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Поставщики метаданных оболочки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35488e750531a5ee7bac7dc915990593ecee1d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711394"
---
# <a name="shell-metadata-providers"></a>Поставщики метаданных оболочки

Начиная с Windows 7 Microsoft Media Foundation предоставляет метаданные через интерфейс [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

Метаданные, полученные с помощью процесса, определенного в этом разделе, следует использовать только для доступа только для чтения. Запись данных с помощью этого процесса не поддерживается. Вы можете создать объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) для написания целей с помощью идентификатора класса (CLSID), полученного из [**пслукуппропертихандлерклсид**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).

## <a name="reading-metadata"></a>Чтение метаданных

Чтобы прочитать метаданные из источника мультимедиа, выполните следующие действия.

1.  Получение указателя на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника мультимедиа. Для получения указателя **имфмедиасаурце** можно использовать интерфейс [**имфсаурцересолвер**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .
2.  Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) в источнике мультимедиа, чтобы получить указатель на интерфейс [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . В параметре *гуидсервице* объекта **мфжетсервице** укажите значение **\_ \_ \_ службы обработчика свойства MF**. Если источник не поддерживает интерфейс **ипропертисторе** , **мфжетсервице** возвращает **MF \_ \_ неподдерживаемую \_ службу**.
3.  Вызовите методы [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы перечислить свойства метаданных.

Эти действия показаны в следующем коде. Предположим, что `DisplayProperty` является функцией, которая отображает значение **пропвариант** .


```C++
HRESULT EnumerateMetadata(IMFMediaSource *pSource)
{
    IPropertyStore *pProps = NULL;

    HRESULT hr = MFGetService(
        pSource, MF_PROPERTY_HANDLER_SERVICE, IID_PPV_ARGS(&pProps));

    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cProps;

    hr = pProps->GetCount(&cProps);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cProps; i++)
    {
        PROPERTYKEY key;
        hr = pProps->GetAt(i, &key);
        if (FAILED(hr))
        {
            goto done;
        }

        PROPVARIANT pv;

        hr = pProps->GetValue(key, &pv);
        if (FAILED(hr))
        {
            goto done;
        }

        DisplayProperty(key, pv);
        PropVariantClear(&pv);
    }

done:
    SafeRelease(&pProps);
    return hr;
}
```



Список ключей свойств метаданных см. в разделе [Свойства метаданных для файлов мультимедиа](metadata-properties-for-media-files.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Метаданные мультимедиа](media-metadata.md)
</dt> </dl>

 

 
