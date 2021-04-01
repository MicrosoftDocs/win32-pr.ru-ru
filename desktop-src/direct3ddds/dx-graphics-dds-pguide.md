---
title: Руководством по программированию для DDS
description: Direct3D реализует формат файлов DDS для хранения несжатых или сжатых текстур (Дкстн).
ms.assetid: 39f9847e-3b1c-4401-a253-74c183ffcc83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4940db5ec40e6ec0b907aa4ee7ce725cd585e961
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414161"
---
# <a name="programming-guide-for-dds"></a>Руководством по программированию для DDS

Direct3D реализует формат файлов DDS для хранения несжатых или сжатых текстур (Дкстн). Формат файла реализует несколько разных типов, предназначенных для хранения различных типов данных, и поддерживает однослойные текстуры, текстуры с MIP-карты, карты кубов, карты томов и массивы текстур (в Direct3D 10/11). В этом разделе описывается компоновка файла DDS.

Сведения о создании текстуры в Direct3D 11 см. в разделе [как создать текстуру](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create). Справку по Direct3D 9 см. [в разделе Поддержка текстур в D3DX (Direct3D 9)](/windows/desktop/direct3d9/texture-support-in-d3dx).

-   [Макет файла DDS](#dds-file-layout)
-   [Варианты DDS](#dds-variants)
-   [Использование массивов текстур в Direct3D 10/11](#using-texture-arrays-in-direct3d-1011)
-   [Общие форматы файловых ресурсов DDS и связанное содержимое заголовка](#common-dds-file-resource-formats-and-associated-header-content)
-   [См. также](#related-topics)

## <a name="dds-file-layout"></a>Макет файла DDS

DDS-файл — это двоичный файл, который содержит следующую информацию:

-   Параметр DWORD (контрольное число), содержащий четырехсимвольное кодовое значение «DDS « (0x20534444).

-   Описание данных, содержащихся в файле.

    Данные описаны с описанием заголовка с помощью [**\_ заголовка DDS**](dds-header.md). формат пикселей определяется с помощью [**DDS \_ PIXELFORMAT**](dds-pixelformat.md). Обратите внимание, что структуры **DDS \_** и **DDS \_ PIXELFORMAT** заменяют нерекомендуемые структуры DDSURFACEDESC2, DDSCAPS2 и ддпикселформат DirectDraw 7. **DDS \_ ЗАГОЛОВОК** является двоичным эквивалентом DDSURFACEDESC2 и DDSCAPS2. **DDS \_ PIXELFORMAT** является двоичным эквивалентом ддпикселформат.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
            
    ```

    

    Если для DDS \_ PIXELFORMAT dwFlags задано значение ддпф \_ FourCC, а двфауркк имеет значение "содержимым DX10", то для размещения массивов текстур или форматов DXGI будет использоваться дополнительная структура [**\_ заголовков DDS \_ DXT10**](dds-header-dxt10.md) , которая не может быть выражена в формате пикселей RGB, например в форматах с плавающей запятой, форматах sRGB и т. д. При наличии **структуры \_ \_ DXT10 заголовков DDS** полное описание данных будет выглядеть следующим образом.

    ```
    DWORD               dwMagic;
    DDS_HEADER          header;
    DDS_HEADER_DXT10    header10;
    ```

    

-   Указатель на массив байтов, содержащий сведения о главной плоскости.
    ```
    BYTE bdata[]
    ```

    

-   Указатель на массив байтов, содержащий сведения об остальных плоскостях, например об уровнях MIP, гранях в кубической текстуре, глубин в объемной текстуре. В статьях, ссылки на которые приведены ниже, представлены дополнительные сведения о структуре DDS-файлов для [текстуры](dds-file-layout-for-textures.md), [кубической текстуры](dds-file-layout-for-cubic-environment-maps.md) или [объемной текстуры](dds-file-layout-for-volume-textures.md).

    ```
    BYTE bdata2[]
    ```

    

Для широкой поддержки оборудования рекомендуется использовать [**\_ Формат DXGI \_ R8G8B8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), в [**\_ формате DXGI \_ R8G8B8A8 \_ UNORM \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), в [**\_ формате DXGI \_ R8G8B8A8 \_ снорм**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), в [**\_ формате DXGI \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), в [**формате DXGI \_ \_ R16G16 \_ снорм**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**формате DXGI \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)R8G8 снорм, в [**формате DXGI. UNORM, формате DXGI BC1 UNORM, формате \_ DXGI BC1 \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)UNORM sRGB, в формате DXGI BC2 UNORM, формате DXGI BC2 sRGB, формат DXGI UNORM BC3 или в формате DXGI UNORM BC3 sRGB. [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**\_ \_ \_ \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Дополнительные сведения о форматах сжатых текстур см. [в разделе Сжатие блочного блока в Direct3D 11](/windows/desktop/direct3d11/texture-block-compression-in-direct3d-11) и [блочное сжатие (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression).

Библиотека D3DX (например, D3DX11. lib) и другие аналогичные библиотеки ненадежно или неодинаково предоставляют значение высоты в элементе **двпитчорлинеарсизе** структуры [**\_ заголовков DDS**](dds-header.md) . Поэтому при чтении и записи в файлы DDS рекомендуется вычислять шаг одним из следующих способов для указанных форматов:

-   Для форматов, сжатых в виде блоков, вычислите тон следующим образом:

    Max (1, ((ширина + 3)/4)) \* блочный размер

    Размер блока составляет 8 байт для форматов DXT1, BC1 и BC4 и 16 байт для других форматов, сжатых в виде блока.

-   Для R8G8 \_ B8G8, G8R8 \_ G8B8, устаревших UYVY-упакованных и устаревших форматов YUY2-Упакованные, вычисляют шаг как:

    ((ширина + 1)  >> 1) \* четырех

-   Для других форматов Вычислите шаг как:

    (ширина, \* бит на пиксель + 7)/8

    Для выравнивания байтов можно разделить на 8.

> [!Note]  
> Вычисленное значение высоты не всегда равно пошаговому вызываемому средой выполнения, которое в некоторых ситуациях и в других ситуациях выдается в виде DWORD. Поэтому рекомендуется копировать строку сканирования за раз, а не пытаться копировать весь образ в одну копию.

 

## <a name="dds-variants"></a>Варианты DDS

Существует множество средств для создания и использования файлов DDS, но они могут различаться в зависимости от того, что они требуют в заголовке. Модули записи должны заполнять заголовки как можно более полно, а читатели должны проверить минимальное значение для обеспечения максимальной совместимости. Чтобы проверить файл DDS, читатель должен убедиться, что размер файла не менее 128 байт для размещения магического значения и основного заголовка, магическое значение — 0x20534444 ("DDS"), \_ размер заголовка DDS — 124, а DDS \_ PIXELFORMAT в заголовке — 32. Если для DDS \_ PIXELFORMAT dwFlags задано значение ддпф \_ FourCC, а для двфауркк задано значение "содержимым DX10", общий размер файла должен составлять не менее 148 байт.

Существуют некоторые распространенные варианты использования, где формат пикселей задан как код ДДПФ FourCC, \_ где двфауркк имеет значение ПЕРЕЧИСЛЕНИЯ D3DFORMAT или DXGI \_ . Невозможно определить, является ли значение перечисления D3DFORMAT или \_ форматом DXGI, поэтому настоятельно рекомендуется использовать вместо него заголовок DXT10 "содержимым DX10" и заголовков \_ заголовков DDS, \_ чтобы хранить дксгиформат, когда базовый набор DDS \_ PIXELFORMAT не может выразить этот формат.

Стандартный PIXELFORMAT DDS \_ должен быть предпочтительным для обеспечения максимальной совместимости для хранения несжатых данных RGB и данных DXT1-5, так как не все средства DDS поддерживают расширение содержимым DX10.

## <a name="using-texture-arrays-in-direct3d-1011"></a>Использование массивов текстур в Direct3D 10/11

Новые структуры DDS ([**\_ заголовком**](dds-header.md) DDS [**и \_ заголовком dds \_ DXT10**](dds-header-dxt10.md)) в Direct3D 10/11 расширяют формат файлов DDS для поддержки массива текстур, который является новым типом ресурсов в Direct3D 10/11. Ниже приведен пример кода, в котором показано, как получить доступ к различным уровням mipmap в массиве текстур с помощью новых заголовков.


```
DWORD               dwMagic;
DDS_HEADER          header;
DDS_HEADER_DXT10    header10;
   
for (int iArrayElement = 0; iArrayElement < header10.arraySize; iArrayElement++)
{
   for (int iMipLevel = 0; iMipLevel < header.dwMipMapCount; iMipLevel++)
   {
     ...
   }
}       
```



## <a name="common-dds-file-resource-formats-and-associated-header-content"></a>Общие форматы файловых ресурсов DDS и связанное содержимое заголовка



| Формат ресурса                                                                            | dwFlags        | двргббиткаунт | дврбитмаск | двгбитмаск | двббитмаск | двабитмаск |
|--------------------------------------------------------------------------------------------|----------------|---------------|------------|------------|------------|------------|
| \_Формат DXGI \_ R8G8B8A8 \_ UNORM<br/> D3DFMT \_ A8B8G8R8<br/>                       | RGBA для DDS \_      | 32            | 0xFF       | 0xff00     | 0xff0000   | 0xff000000 |
| \_Формат DXGI \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | RGBA для DDS \_      | 32            | 0xFFFF     | 0xffff0000 |            |            |
| \*\*<br/> \_Формат DXGI \_ R10G10B10A2 \_ UNORM<br/> D3DFMT \_ A2B10G10R10<br/> | RGBA для DDS \_      | 32            | 0x3ff      | 0xffc00    | 0x3ff00000 |            |
| \_Формат DXGI \_ R16G16 \_ UNORM<br/> D3DFMT \_ G16R16<br/>                           | заdds \_ RGB       | 32            | 0xFFFF     | 0xffff0000 |            |            |
| \_Формат DXGI \_ B5G5R5A1 \_ UNORM<br/> D3DFMT \_ A1R5G5B5<br/>                       | RGBA для DDS \_      | 16            | 0x7c00     | 0x3e0      | 0x1F       | 0x8000     |
| \_Формат DXGI \_ B5G6R5 \_ UNORM<br/> D3FMT \_ R5G6B5<br/>                            | заdds \_ RGB       | 16            | 0xf800     | 0x7e0      | 0x1F       |            |
| DXGI \_ a8 \_ UNORM<br/> D3DFMT \_ A8<br/>                                           | заdds \_ Alpha     | 8             |            |            |            | 0xFF       |
| D3DFMT \_ A8R8G8B8<br/>                                                                | RGBA для DDS \_      | 32            | 0xff0000   | 0xff00     | 0xFF       | 0xff000000 |
| D3DFMT \_ X8R8G8B8<br/>                                                                | заdds \_ RGB       | 32            | 0xff0000   | 0xff00     | 0xFF       |            |
| D3DFMT \_ X8B8G8R8<br/>                                                                | заdds \_ RGB       | 32            | 0xFF       | 0xff00     | 0xff0000   |            |
| \*\*<br/> D3DFMT \_ A2R10G10B10<br/>                                             | RGBA для DDS \_      | 32            | 0x3ff00000 | 0xffc00    | 0x3ff      | 0xc0000000 |
| D3DFMT \_ R8G8B8<br/>                                                                  | заdds \_ RGB       | 24            | 0xff0000   | 0xff00     | 0xFF       |            |
| D3DFMT \_ X1R5G5B5<br/>                                                                | заdds \_ RGB       | 16            | 0x7c00     | 0x3e0      | 0x1F       |            |
| D3DFMT \_ A4R4G4B4<br/>                                                                | RGBA для DDS \_      | 16            | 0xf00      | 0xf0       | 0xF        | число 0xF000 не     |
| D3DFMT \_ X4R4G4B4<br/>                                                                | заdds \_ RGB       | 16            | 0xf00      | 0xf0       | 0xF        |            |
| D3DFMT \_ A8R3G3B2<br/>                                                                | RGBA для DDS \_      | 16            | 0xE0       | 0x1c       | 0x3        | 0xff00     |
| D3DFMT \_ A8L8<br/>                                                                    | \_светимость DDS | 16            | 0xFF       |            |            | 0xff00     |
| D3DFMT \_ L16<br/>                                                                     | \_светимость DDS | 16            | 0xFFFF     |            |            |            |
| D3DFMT \_ 8<br/>                                                                      | \_светимость DDS | 8             | 0xFF       |            |            |            |
| D3DFMT \_ A4L4<br/>                                                                    | \_светимость DDS | 8             | 0xF        |            |            | 0xf0       |



 



| Формат ресурса                                                                             | dwFlags     | двфауркк |
|---------------------------------------------------------------------------------------------|-------------|----------|
| \_Формат DXGI \_ BC1 \_ UNORM<br/> D3DFMT \_ DXT1<br/>                                 | DDS \_ FourCC | "DXT1"   |
| \_Формат DXGI \_ BC2 \_ UNORM<br/> D3DFMT \_ DXT3<br/>                                 | DDS \_ FourCC | "DXT3"   |
| \_Формат DXGI \_ BC3 \_ UNORM<br/> D3DFMT \_ DXT5<br/>                                 | DDS \_ FourCC | "DXT5"   |
| \*<br/> \_Формат DXGI \_ BC4 \_ UNORM<br/>                                           | DDS \_ FourCC | "BC4U"   |
| \*<br/> \_Формат DXGI \_ BC4 \_ снорм<br/>                                           | DDS \_ FourCC | "BC4S"   |
| \*<br/> \_Формат DXGI \_ Bc5 \_ UNORM<br/>                                           | DDS \_ FourCC | "ATI2"   |
| \*<br/> \_Формат DXGI \_ Bc5 \_ снорм<br/>                                           | DDS \_ FourCC | "BC5S"   |
| \_Формат DXGI \_ R8G8 \_ B8G8 \_ UNORM<br/> D3DFMT \_ R8G8 \_ B8G8<br/>                    | DDS \_ FourCC | "РГБГ"   |
| \_Формат DXGI \_ G8R8 \_ G8B8 \_ UNORM<br/> D3DFMT \_ G8R8 \_ G8B8<br/>                    | DDS \_ FourCC | "ГРГБ"   |
| \*<br/> \_Формат DXGI \_ R16G16B16A16 \_ UNORM<br/> D3DFMT \_ A16B16G16R16<br/>  | DDS \_ FourCC | 36       |
| \*<br/> \_Формат DXGI \_ R16G16B16A16 \_ снорм<br/> D3DFMT \_ Q16W16V16U16<br/>  | DDS \_ FourCC | 110      |
| \*<br/> \_Формат DXGI \_ R16 \_ float<br/> D3DFMT \_ R16F<br/>                   | DDS \_ FourCC | 111      |
| \*<br/> \_Формат DXGI \_ R16G16 \_ float<br/> D3DFMT \_ G16R16F<br/>             | DDS \_ FourCC | 112      |
| \*<br/> \_Формат DXGI \_ R16G16B16A16 \_ float<br/> D3DFMT \_ A16B16G16R16F<br/> | DDS \_ FourCC | 113      |
| \*<br/> \_Формат DXGI \_ R32 \_ float<br/> D3DFMT \_ R32F<br/>                   | DDS \_ FourCC | 114      |
| \*<br/> \_Формат DXGI \_ R32G32 \_ float<br/> D3DFMT \_ G32R32F<br/>             | DDS \_ FourCC | 115      |
| \*<br/> \_Формат DXGI \_ R32G32B32A32 \_ float<br/> D3DFMT \_ A32B32G32R32F<br/> | DDS \_ FourCC | 116      |
| D3DFMT \_ DXT2<br/>                                                                     | DDS \_ FourCC | "DXT2"   |
| D3DFMT \_ DXT4<br/>                                                                     | DDS \_ FourCC | "DXT4"   |
| D3DFMT \_ UYVY<br/>                                                                     | DDS \_ FourCC | UYVY   |
| D3DFMT \_ YUY2<br/>                                                                     | DDS \_ FourCC | "YUY2"   |
| D3DFMT \_ CxV8U8<br/>                                                                   | DDS \_ FourCC | 117      |
| Любой формат DXGI                                                                             | DDS \_ FourCC | СОДЕРЖИМЫМ DX10   |



 

\* = Надежный модуль чтения DDS должен иметь возможность обрабатывать эти коды устаревших форматов. Тем не менее такой модуль чтения DDS должен предпочесть использовать расширение заголовка СОДЕРЖИМЫМ DX10 при записи этих кодов форматов, чтобы избежать неоднозначности.

\*\* = Из-за некоторых долгосрочных проблем в распространенных реализациях модулей чтения и записи DDS, самым надежным способом записи данных 10:10:10:2-Type является использование расширения заголовка СОДЕРЖИМЫМ DX10 с кодом [**\_ формата DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) "24" (то есть \_ форматом DXGI \_ R10G10B10A2 \_ UNORM Value). \_Данные A2R10G10B10 D3DFMT должны быть преобразованы в данные типа 10:10:10:2 перед их записью в виде \_ \_ файла DDS формата DXGI R10G10B10A2 \_ UNORM.

## <a name="related-topics"></a>См. также

<dl> <dt>

[НАБОРА](dx-graphics-dds.md)
</dt> </dl>

 

