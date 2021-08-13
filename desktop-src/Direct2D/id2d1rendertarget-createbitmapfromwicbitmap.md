---
title: ID2D1RenderTarget Креатебитмапфромвикбитмап методы
description: создает ID2D1Bitmap путем копирования указанного точечного рисунка Microsoft Windows imaging Component (WIC).
ms.assetid: 463fc2f9-8ec6-47e8-8d48-a9015616e656
keywords:
- Методы Креатебитмапфромвикбитмап Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 3d023db69afdc3cc69535d310cb21fb841c2f1bbe981df98e0aaa22074a46db0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119304344"
---
# <a name="id2d1rendertargetcreatebitmapfromwicbitmap-methods"></a>Методы ID2D1RenderTarget:: Креатебитмапфромвикбитмап

создает [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) путем копирования указанного точечного рисунка Microsoft Windows imaging Component (WIC).

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                              | Описание                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**Креатебитмапфромвикбитмап (IWICBitmapSource \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_id2d1bitmap))                                                       | создает [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) путем копирования указанного точечного рисунка Microsoft Windows imaging Component (WIC).<br/>  |
| [**Креатебитмапфромвикбитмап (IWICBitmapSource \* , \_ Свойства точечного рисунка D2D1 \_&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1))  | создает [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) путем копирования указанного точечного рисунка Microsoft Windows imaging Component (WIC).<br/> |
| [**Креатебитмапфромвикбитмап (IWICBitmapSource \* , \_ Свойства точечного рисунка D2D1 \_ \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) | создает [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) путем копирования указанного точечного рисунка Microsoft Windows imaging Component (WIC).<br/> |



## <a name="remarks"></a>Remarks

Прежде чем Direct2D сможет загрузить образ WIC, его необходимо преобразовать в поддерживаемый формат пикселей и альфа-режим. Список поддерживаемых форматов пикселей и альфа-режимов см. в разделе [Поддерживаемые форматы пикселей и альфа-режимы](supported-pixel-formats-and-alpha-modes.md).

## <a name="examples"></a>Примеры

Примеры см. в разделе [Загрузка растрового изображения из файла](how-to-load-a-direct2d-bitmap-from-a-file.md) и [Загрузка растрового изображения из ресурса](how-to-load-a-bitmap-from-a-resource.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[Как загрузить точечный рисунок из файла](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> <dt>

[Поддерживаемые форматы пикселей и режимы альфа-канала](supported-pixel-formats-and-alpha-modes.md)
</dt> </dl>

 

