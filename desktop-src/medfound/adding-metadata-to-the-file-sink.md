---
description: Дополнительные сведения о добавлении метаданных в приемник файлов ASF, которые приложение может использовать для архивации данных ASF Media в файл.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Добавление метаданных в приемник файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65e25ddc12b406987de4ec95d3183309e8453696d1bb5b2816054407f1ced4b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606724"
---
# <a name="adding-metadata-to-the-file-sink"></a>Добавление метаданных в приемник файлов

Приемник ASF-файлов — это реализация [**имфмедиасинк**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , предоставляемая Media Foundation, которую приложение может использовать для архивации данных ASF Media в файл. Сведения об объектной модели приемников ASF Media и общем использовании см. в статье [приемники мультимедиа ASF](asf-media-sinks.md).

После [создания приемника файлов ASF](creating-the-asf-file-sink.md)его необходимо настроить с помощью сведений о потоках и кодировке в выходном файле. Эти процедуры описаны в разделе [Добавление сведений о потоке в приемник файлов ASF](adding-stream-information-to-the-asf-file-sink.md) и [Задание свойств в приемнике файла](setting-properties-in-the-file-sink.md). Кроме того, можно добавить сведения о метаданных, включая пары «имя-значение», такие как «Author», «Title». В этом разделе описывается процесс добавления метаданных к приемнику файла, чтобы он появился в окончательном [объекте заголовка ASF](asf-file-structure.md).

Перед созданием топологии кодирования можно добавить сведения о метаданных в приемник файлов ASF. Объект ASF Контентинфо для приемника файлов отслеживает свойства метаданных и предоставляется приложению через интерфейс [**имфметадата**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) . Некоторые из этих свойств, например "Исвбр", которые указывают, содержит ли файл потоки с переменной скоростью (VBR), устанавливаются автоматически приемником файла путем анализа заданных свойств кодировки потока.

Полный список свойств см. в разделе «Список атрибутов» документации по формату пакета SDK.

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a>Использование интерфейса Имфметадата в приемнике файлов ASF

1.  Запросите объект приемника ASF-файла, чтобы получить указатель на его реализацию интерфейса [**имфметадатапровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .
2.  Вызовите [**имфметадатапровидер:: жетмфметадата**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) , чтобы получить указатель [**имфметадата**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .

    Параметр *ппресентатиондескриптор* игнорируется, и приложение может передать **значение NULL**. Если приложение передает ноль в качестве идентификатора потока в параметре *двстреамидентифиер* , метод извлекает метаданные, которые применяются ко всему файлу ASF. В противном случае извлекается только метаданные для потока.

3.  Вызовите метод [**имфметадата:: жеталлпропертинамес**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) , чтобы получить список свойств кодирования файла, заданных для мультимедийного содержимого.
4.  Вызовите [**имфметадата:: Property**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) , чтобы получить значения свойств.

## <a name="example"></a>Пример

В следующем примере кода показано, как перечислить имена и значения свойств, заданные для файла ASF.


```C++
/////////////////////////////////////////////////////////////////////
// Name: ListASFProperties
//
// Enumerates the metadata properties of the ASF file. 
//
// pContentInfo: Pointer to the ASF ContentInfo object.
/////////////////////////////////////////////////////////////////////

HRESULT ListASFProperties(IMFASFContentInfo *pContentInfo)
{
    HRESULT hr = S_OK;
    
    PROPVARIANT varNames;
    PropVariantInit(&varNames);

    PROPVARIANT varValue;
    PropVariantInit(&varValue);

    IMFMetadataProvider* pProvider = NULL;
    IMFMetadata* pMetadata = NULL;

    // Query the ContentInfo object for IMFMetadataProvider.
    CHECK_HR(hr = pContentInfo->QueryInterface(IID_IMFMetadataProvider,
        (void**)&pProvider));

    // Get a pointer to IMFMetadata for file-wide metadata.
    CHECK_HR(hr = pProvider->GetMFMetadata(NULL, 0, 0, &pMetadata));

    // Get the property names that are stored in the metadata object.
    CHECK_HR(hr = pMetadata->GetAllPropertyNames(&varNames));

    // Loop through the properties and get their values.
    if (varNames.vt == (VT_VECTOR | VT_LPWSTR))
    {
        ULONG cElements = varNames.calpwstr.cElems;
        for (ULONG i = 0; i < cElements; i++)
        {
            const WCHAR* sName = varNames.calpwstr.pElems[i];
            CHECK_HR(hr = pMetadata->GetProperty(sName, &varValue));
            //Use the property values. Not shown.
            PropVariantClear(&varValue);
        }
    }
done:
    PropVariantClear(&varNames);
    PropVariantClear(&varValue);
    SAFE_RELEASE (pMetaData);
    SAFE_RELEASE (pProvider);
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Приемники мультимедиа ASF](asf-media-sinks.md)
</dt> <dt>

[Компоненты ASF уровня конвейера](pipeline-layer-asf-components.md)
</dt> <dt>

[Поддержка ASF в Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



