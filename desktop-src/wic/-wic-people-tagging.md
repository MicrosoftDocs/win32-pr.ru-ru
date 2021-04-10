---
description: В этом разделе рассказывается о новой схеме с расширенной платформой метаданных (XMP) и свойстве Photo. photo. Пеопленамес Windows 7, которая позволяет размечать людей в цифровой фотографии.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Общие сведения о разметке пользователей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156739"
---
# <a name="people-tagging-overview"></a>Общие сведения о разметке пользователей

В этом разделе рассказывается о новой схеме с расширенной платформой метаданных (XMP) и свойстве Photo [. photo. Пеопленамес](../properties/props-system-photo-peoplenames.md) Windows 7, которая позволяет размечать людей в цифровой фотографии. В этом разделе также обсуждается использование API компонента Windows Imaging Component (WIC) для чтения и записи метаданных, необходимых для добавления тегов к пользователям.

В этом разделе содержатся следующие подразделы.

-   [Предварительные условия](#prerequisites)
-   [Введение](#introduction)
-   [Теги для людей](#people-tagging-overview)
    -   [Имена людей](#people-names)
    -   [Прямоугольники людей](#people-rectangles)
-   [Справочник по схемам](#schema-reference)
    -   [Схема Microsoft Photo 1,2](#microsoft-photo-12-schema)
    -   [Схема Microsoft Photo RegionInfo](#microsoft-photo-regioninfo-schema)
    -   [Схема области фотографии (Майкрософт)](#microsoft-photo-regioninfo-schema)
    -   [Образцы метаданных](#sample-metadata)
-   [См. также](#related-topics)

## <a name="prerequisites"></a>Предварительные условия

Чтобы понять этот раздел, необходимо ознакомиться с интерфейсами декодера WIC и связанными с ним компонентами модели COM, как описано в разделе [Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md). Кроме того, он позволяет получить общее представление о метаданных изображений, особенно XMP.

## <a name="introduction"></a>Введение

Корпорация Майкрософт создала новую схему XMP для тегирования людей в цифровом изображении. Эта схема позволяет приложениям хранить имена и расположения пользователей, которые находятся в образе, в виде метаданных в образе. В дополнение к новой схеме в Windows 7 доступно новое свойство Photo [System. photo. пеопленамес](../properties/props-system-photo-peoplenames.md) . Это новое свойство позволяет приложениям считывать имена отдельных пользователей, хранящиеся в метаданных образа. WIC использует эти новые функции, позволяя приложениям легко считывать и записывать в цифровые фотографии метаданные тегов.

## <a name="people-tagging"></a>Теги для людей

Компонент WIC предоставляет разработчикам приложений COM-компоненты, считывающие данные изображений, а также метаданные изображений. Для чтения и записи метаданных, таких как новая функция тегирования людей, компонент WIC предоставляет интерфейсы [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) и [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Эти интерфейсы позволяют приложениям использовать [язык запросов метаданных](-wic-codec-metadataquerylanguage.md) для записи метаданных в отдельные кадры изображения. В следующем разделе показано, как считывать и записывать метаданные тегов людей в метаданные изображения с помощью средств чтения и записи запросов WIC.

### <a name="people-names"></a>Имена людей

Часть функции тегирования людей — это возможность просто получить список имен людей, помеченных в изображении. Эта часть функции поддерживается обработчиками метаданных [System. photo. пеопленамес](../properties/props-system-photo-peoplenames.md) и WIC. Интерфейс [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) в сочетании со свойством System. photo. пеопленамес используется для чтения имен людей, определенных в образе и хранимых в метаданных образа.

В следующем примере кода показано, как средство чтения запросов, полученное из кадра изображения, запрашивает метаданные изображения для именованных тегов свойства [System. photo. пеопленамес](../properties/props-system-photo-peoplenames.md) .


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



Выражение запроса System. photo. Пеопленамес запрашивает кадр для свойства. Если метаданные тегов людей существуют и содержат имена людей, значение [пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) будет установлено VT \_ LPWSTR, а значение данных будет содержать список имен с тегами. Дополнительные сведения о чтении метаданных изображения см. в разделе [Общие сведения о чтении и записи метаданных изображения](-wic-codec-readingwritingmetadata.md).

Запрос к тегу "имена людей" полезен только в том случае, если изображение фактически содержит метаданные тегов для людей. Чтобы это произошло, приложение должно сначала записать его. Чтобы записать метаданные имен людей, используйте [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) и ЯВНЫЙ путь XMP к метаданным. В следующем примере кода показано использование средства записи запроса для записи имени в путь запроса.


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



Обратите внимание на шаг, создающий структуру XMP и задавая ее в разделе `MPRI:Regions/{ulong=0}` . Без этого шага компонент WIC не сможет выяснить, где разместить `PersonDisplayName` позже. Также обратите внимание, что вместо [System. photo. пеопленамес](-wic-photoprop-system-photo-peoplenames.md)используется явный путь запроса, политика метаданных которой не поддерживает запись метаданных.

### <a name="people-rectangles"></a>Прямоугольники людей

Однако имена людей являются только частью функции добавления тегов. В дополнение к хранению имен людей в метаданных схема также поддерживает сведения о регионах, определяющие конкретную область (прямоугольник), которую пользователь показывает в изображении.

Сведения о прямоугольнике представлены четырьмя десятичными значениями, разделенными запятой, например "0,25, 0,25, 0,25, 0,25". Первые два значения указывают координату верхнего левого угла; последние два указывают высоту и ширину прямоугольника. Размеры изображения в целях определения прямоугольников людей нормализованы до 1, что означает, что в примере "0,25, 0,25, 0,25, 0,25" прямоугольник начинается с 1/4 расстояния от верхнего края и от 1/4 на расстоянии от левого края изображения. Высота и ширина прямоугольника равна 1/4 размера соответствующих размеров изображения.

Сведения о прямоугольнике, определяющие отдельных лиц, записываются так же, как и имена пользователей в одной и той же структуре. Чтобы записать метаданные прямоугольника, используйте [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) и ЯВНЫЙ путь XMP к метаданным. Следующий пример кода возобновляет предыдущий пример и добавляет прямоугольник, представляющий "John Петрова", в метаданные изображения. Обратите внимание, что он использует тот же `{ulong=0}` индекс для связывания этого прямоугольника с "Джон Петров".


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a>Справочник по схеме

Схемы Microsoft XMP для тегирования пользователей определяют набор свойств для обозначения лиц в цифровых фотографиях.

В следующих разделах приводятся определения схемы, необходимые для добавления тегов к пользователям. Там, где это возможно, определения схемы используют соглашения, предоставляемые [спецификациями расширяемой платформы метаданных (XMP) Adobe](https://www.adobe.com/devnet/xmp/). Определения схемы в этом разделе показывают универсальный код ресурса (URI) пространства имен XML, который идентифицирует схему и префикс пространства имен предпочтительной схемы, за которым следует таблица со списком всех свойств, определенных для схемы. Каждая таблица содержит следующие столбцы.

-   **Property** — имя свойства, включая предпочтительный префикс пространства имен.

-   **Тип значения** — тип значения свойства. Схемы поддержки тегов людей используют типы значений XMP везде, где это возможно, включая дату и текст. Перед типами массивов следует тип контейнера: `alt` , `bag` или `seq` .

-   **Категория** — свойства схемы являются внутренними или внешними:

    -   Внутренние метаданные должны быть заданы приложением.

    -   Внешние метаданные должны быть заданы пользователем и не зависеть от содержимого документа.

-   **Описание** — описание свойства.

### <a name="microsoft-photo-12-schema"></a>Схема Microsoft Photo 1,2

Схема Microsoft Photo 1,2 предоставляет набор свойств для областей изображения.

-   URI-код пространства имен схемы — `https://ns.microsoft.com/photo/1.2/` .
-   Предпочтительным префиксом пространства имен схемы является `MP` .



| Свойство      | Тип значения | Категория | Описание                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Пакет управления: RegionInfo | RegionInfo | Внутренние | **обязательный** : сохраняет корень метаданных тегов людей. См. раздел Схема фотоколлажа Майкрософт, который приведен ниже. |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Схема Microsoft Photo RegionInfo

Схема Microsoft Photo RegionInfo 1,2 содержит набор свойств для сведений о регионе.

-   URI-код пространства имен схемы — `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .
-   Предпочтительным префиксом пространства имен схемы является `MPRI` .



| Свойство              | Тип значения | Категория | Описание                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| МПРИ: Датерегионсвалид | Дата       | External | **необязательно** : Дата создания последней области.                                                          |
| МПРИ: регионы          | Регион сумки | External | **Обязательное** : сохраняет области тегов пользователей. См. раздел Схема области фотографии Майкрософт, который приведен ниже. |



 

### <a name="microsoft-photo-region-schema"></a>Схема области фотографии (Майкрософт)

Схема Microsoft Photo Region 1,2 содержит набор свойств для областей изображения.

-   URI-код пространства имен схемы — `https://ns.microsoft.com/photo/1.2/t/Region#` .
-   Предпочтительным префиксом пространства имен схемы является `MPReg` .



| Мпрег: свойство          | Тип значения | Категория | Описание                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Мпрег: Персондисплайнаме | Текст       | External | **обязательный** : хранит имя пользователя в заданном прямоугольнике.                                                                                                                                                                                                                                            |
| Мпрег: прямоугольник         | Текст       | External | ( **необязательно** .) содержит прямоугольник, идентифицирующий пользователя в фотографии. Прямоугольник хранится в виде четырех десятичных значений с разделителями-запятыми. Первые два значения указывают верхнюю левую координату. последние два указывают высоту и ширину прямоугольника. Десятичные значения должны быть нормализованы до 1. |
| Мпрег: Персонемаилдижест | Текст       | External | ( **необязательно** .) хранит хэш зашифрованного сообщения SHA-1 для адреса электронной почты пользователя.                                                                                                                                                                                                                     |
| Мпрег: ПерсонливеидЦид   | Текст       | External | **необязательно** : сохраняет десятичное представление целого числа со знаком для действительной CID, 64-разрядное целое число, которое общедоступно определяет действующее удостоверение.                                                                                                                                                                     |



 

### <a name="sample-metadata"></a>Образцы метаданных

Ниже приведено представление метаданных XMP для тегов пользователей.

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Общие сведения о метаданных компонента WIC](-wic-about-metadata.md)
</dt> <dt>

[Общие сведения о чтении и записи метаданных изображений](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Общие сведения о языке запросов метаданных](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
