---
title: Поиск и открытие компрессоров и декомпрессоров
description: Поиск и открытие компрессоров и декомпрессоров
ms.assetid: ed931f01-dbfc-4fdc-b725-c062302b037b
keywords:
- Диспетчер сжатия видео (ВКМ), открытие компрессоров
- ВКМ (диспетчер сжатия видео), открытие компрессоров
- Функция Иклокате
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45b07c619095b4d50bdbdde5c3d2b1ca9209471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067692"
---
# <a name="locating-and-opening-compressors-and-decompressors"></a>Поиск и открытие компрессоров и декомпрессоров

В следующем примере функция [**иклокате**](/windows/desktop/api/Vfw/nf-vfw-iclocate) используется для поиска компрессора, который может сжимать точечный рисунок размером 8 бит на пиксель.


```C++
BITMAPINFOHEADER bih; 
HIC              hIC 
 
// Initialize the bitmap structure. 
bih.biSize = sizeof(BITMAPINFOHEADER); 
bih.biWidth = bih.biHeight = 0; 
bih.biPlanes = 1; 
bih.biCompression = BI_RGB;      // standard RGB bitmap 
bih.biBitcount = 8;              // 8 bits-per-pixel format 
bih.biSizeImage = 0; 
bih.biXPelsPerMeter = bih.biYPelsPerMeter = 0; 
bih.biClrUsed = bih.biClrImportant = 256; 
 
hIC = ICLocate (ICTYPE_VIDEO, 0L, (LPBITMAPINFOHEADER) &bih, 
    NULL, ICMODE_COMPRESS); 
 
```



В следующем примере выполняется перечисление декомпрессоров в системе, чтобы найти тот, который может работать с форматом его изображений. В этом примере **используется \_ видео иктипе** (которое эквивалентно 4-символьному коду "vidc") и макрос [**икдекомпресскуери**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) для определения того, поддерживает ли программа сжатия или распаковку формат изображения.


```C++
for (i=0; ICInfo(fccType, i, &icinfo); i++) 
{ 
    hic = ICOpen(icinfo.fccType, icinfo.fccHandler, ICMODE_QUERY); 
    if (hic) 
    { 
        // Skip this compressor if it can't handle the format. 
        if (fccType == ICTYPE_VIDEO && pvIn != NULL && 
            ICDecompressQuery(hic, pvIn, NULL) != ICERR_OK) 
        { 
            ICClose(hic); 
            continue; 
        } 
 
        // Find out the compressor name. 
        ICGetInfo(hic, &icinfo, sizeof(icinfo)); 
 
        // Add it to the combo box. 
        n = ComboBox_AddString(hwndC,icinfo.szDescription); 
        ComboBox_SetItemData(hwndC, n, hic); 
    } 
} 
 
```



В следующем примере предпринимается попытка указать конкретный компрессор для сжатия 8-разрядного формата RGB до 8-разрядного формата RLE.


```C++
BITMAPINFOHEADER    bihIn, bihOut; 
HIC                 hIC 
 
// Initialize the bitmap structure. 

biSize = bihOut.biSize = sizeof(BITMAPINFOHEADER); 
bihIn.biWidth = bihIn.biHeight = bihOut.biWidth = bihOut.biHeight = 0; 
bihIn.biPlanes = bihOut.biPlanes= 1; 
bihIn.biCompression = BI_RGB;        // standard RGB bitmap for input 
bihOut.biCompression = BI_RLE8;      // 8-bit RLE for output format 
bihIn.biBitcount = bihOut.biBitCount = 8;  // 8 bits-per-pixel format 
bihIn.biSizeImage = bihOut.biSizeImage = 0; 
bihIn.biXPelsPerMeter = bih.biYPelsPerMeter = 
    bihOut.biXPelsPerMeter = bihOut.biYPelsPerMeter = 0; 
bihIn.biClrUsed = bih.biClrImportant = 
    bihOut.biClrUsed = bihOut.biClrImportant = 256; 

hIC = ICLocate (ICTYPE_VIDEO, 0L, 
    (LPBITMAPINFOHEADER)&bihIn, 
    (LPBITMAPINFOHEADER)&bihOut, ICMODE_COMPRESS); 
 
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование диспетчера сжатия видео](using-the-video-compression-manager.md)
</dt> </dl>

 

 




