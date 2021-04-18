---
description: В Windows Vista Microsoft Media Foundation предоставляет метаданные через интерфейс Имфметадата.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: Поставщики метаданных в Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1726e04058a7b15e387fca4f3faa94fce7c91c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673344"
---
# <a name="metadata-providers-in-windows-vista"></a>Поставщики метаданных в Windows Vista

В Windows Vista Microsoft Media Foundation предоставляет метаданные через интерфейс [**имфметадата**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .

## <a name="reading-metadata"></a>Чтение метаданных

Чтобы прочитать метаданные из источника мультимедиа, выполните следующие действия.

1.  Получение указателя на интерфейс [**имфмедиасаурце**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) источника мультимедиа. Для получения указателя **имфмедиасаурце** можно использовать интерфейс [**имфсаурцересолвер**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .
2.  Вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) , чтобы получить дескриптор представления источника мультимедиа.
3.  Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) в источнике мультимедиа, чтобы получить указатель на интерфейс [**имфметадатапровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) . В параметре *гуидсервице* объекта **мфжетсервице** укажите значение **\_ \_ \_ служба поставщика метаданных MF**. Если источник не поддерживает интерфейс **имфметадатапровидер** , **мфжетсервице** возвращает **MF \_ \_ неподдерживаемую \_ службу**.
4.  Вызовите [**имфметадатапровидер:: жетмфметадата**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) и передайте указатель на дескриптор представления. Этот метод возвращает указатель на интерфейс [**имфметадата**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .
    -   Чтобы получить метаданные уровня потока, сначала вызовите [**имфстреамдескриптор:: жетстреамидентифиер**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) , чтобы получить идентификатор потока. Затем передайте идентификатор потока в параметре *двстреамидентифиер* объекта [**жетмфметадата**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).
    -   Чтобы получить метаданные уровня представления, задайте для *двстреамидентифиер* значение 0.
5.  \[Необязательный \] вызов [**имфметадата:: жеталллангуажес**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) для получения списка языков, на которых доступны метаданные. Языки определяются с помощью тегов языка, соответствующих стандарту RFC 1766.
6.  \[Необязательный \] вызов [**имфметадата:: сетлангуаже**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) для выбора языка.
7.  \[Необязательный \] вызов [**имфметадата:: жеталлпропертинамес**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) для получения списка имен всех свойств метаданных для этого потока или презентации.
8.  Вызовите [**имфметадата::-Property**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) , чтобы получить определенное значение свойства метаданных, передав имя свойства.

В следующем коде показаны шаги 2 – 4.


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



В следующем коде показаны шаги 7 – 8. Предположим, что `DisplayProperty` является функцией, которая отображает значение **пропвариант** .


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Метаданные мультимедиа](media-metadata.md)
</dt> <dt>

[Поставщики метаданных оболочки](shell-metadata-providers.md)
</dt> </dl>

 

 



