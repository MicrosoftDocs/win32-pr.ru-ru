---
title: ID2D1RenderTarget Креатебитмапфромвикбитмап методы
description: Создает ID2D1Bitmap, копируя указанный точечный рисунок компонента Microsoft Windows Imaging Component (WIC).
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
ms.openlocfilehash: 23ad055beab9f24c39f032a3e28456c231480c68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674856"
---
# <a name="id2d1rendertargetcreatebitmapfromwicbitmap-methods"></a>Методы ID2D1RenderTarget:: Креатебитмапфромвикбитмап

Создает [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , копируя указанный точечный рисунок компонента Microsoft Windows Imaging Component (WIC).

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                              | Описание                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**Креатебитмапфромвикбитмап (IWICBitmapSource \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_id2d1bitmap))                                                       | Создает [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , копируя указанный точечный рисунок компонента Microsoft Windows Imaging Component (WIC).<br/>  |
| [**Креатебитмапфромвикбитмап (IWICBitmapSource \* , \_ Свойства точечного рисунка D2D1 \_&, ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1))  | Создает [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , копируя указанный точечный рисунок компонента Microsoft Windows Imaging Component (WIC).<br/> |
| [**Креатебитмапфромвикбитмап (IWICBitmapSource \* , \_ Свойства точечного рисунка D2D1 \_ \* , ID2D1Bitmap \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) | Создает [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , копируя указанный точечный рисунок компонента Microsoft Windows Imaging Component (WIC).<br/> |



## <a name="remarks"></a>Комментарии

Прежде чем Direct2D сможет загрузить образ WIC, его необходимо преобразовать в поддерживаемый формат пикселей и альфа-режим. Список поддерживаемых форматов пикселей и альфа-режимов см. в разделе [Поддерживаемые форматы пикселей и альфа-режимы](supported-pixel-formats-and-alpha-modes.md).

## <a name="examples"></a>Примеры

Примеры см. в разделе [Загрузка растрового изображения из файла](how-to-load-a-direct2d-bitmap-from-a-file.md) и [Загрузка растрового изображения из ресурса](how-to-load-a-bitmap-from-a-resource.md).

## <a name="requirements"></a>Требования



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

 

