---
title: Функция gluBuild2DMipmaps (GLU. h)
description: Функция gluBuild2DMipmaps создает 2-D MIP-карты.
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- Функция gluBuild2DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92402792e41701711e99f469ead67410d6a8c1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988356"
---
# <a name="glubuild2dmipmaps-function"></a>Функция gluBuild2DMipmaps

Функция **gluBuild2DMipmaps** создает 2-D MIP-карты.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*target* 
</dt> <dd>

Целевая текстура. Должно быть \_ 2D-текстура GL \_ .

</dd> <dt>

*компонента* 
</dt> <dd>

Число компонентов цвета в текстуре. Должно быть равно 1, 2, 3 или 4.

</dd> <dt>

*width* 
</dt> <dd>

Ширина изображения текстуры.

</dd> <dt>

*height* 
</dt> <dd>

Высота изображения текстуры.

</dd> <dt>

*format* 
</dt> <dd>

Формат точечных данных. Должно быть одним из следующих: индекс цвета GL, красный, зеленый, GL, GL, ГК, красное, GL, GL, GL, ГК, BGR ext, GL, BGRA, GL или цветная \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ светимость GL \_ .

</dd> <dt>

*type* 
</dt> <dd>

Тип данных для *данных*. Значение должно быть одним из следующих: \_ НЕподписанный \_ байт, байт ГК \_ , \_ точечный рисунок GL, GL \_ без знака \_ Short, краткое название GL, \_ \_ Неподписанное \_ целое число без знака, GL \_ или GL \_ .

</dd> <dt>

*data* 
</dt> <dd>

Указатель на данные изображения в памяти.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Функция **gluBuild2DMipmaps** получает входной образ и создает все образы mipmap (с помощью [**глускалеимаже**](gluscaleimage.md)), поэтому входной образ можно использовать в качестве изображения текстуры мипмаппед. Чтобы загрузить каждое изображение, вызовите [**glTexImage2D**](glteximage2d.md). Если размеры входного изображения не являются степенями двух, то изображение масштабируется таким образом, чтобы ширина и высота были степенями двух до создания MIP-карты.

Возвращаемое значение, равное нулю, указывает на успешное выполнение. В противном случае возвращается код ошибки GLU (см. [**глуеррорстринг**](gluerrorstring.md)).

Описание допустимых значений параметра *Format* см. в разделе **glTexImage2D**. Описание допустимых значений для *типа* см. в разделе [**глдравпикселс**](gldrawpixels.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**глдравпикселс**](gldrawpixels.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**глускалеимаже**](gluscaleimage.md)
</dt> </dl>

 

 





