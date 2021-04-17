---
title: Функция gluBuild1DMipmaps (GLU. h)
description: Функция gluBuild1DMipmaps создает 1-D MIP-карты.
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- Функция gluBuild1DMipmaps OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089357488c7eae18e26258018473e9008fb29d24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672596"
---
# <a name="glubuild1dmipmaps-function"></a>Функция gluBuild1DMipmaps

Функция **gluBuild1DMipmaps** создает 1-D MIP-карты.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*target* 
</dt> <dd>

Целевая текстура. Должен быть \_ \_ одномерной текстурой GL.

</dd> <dt>

*компонента* 
</dt> <dd>

Число компонентов цвета в текстуре. Должно быть равно 1, 2, 3 или 4.

</dd> <dt>

*width* 
</dt> <dd>

Ширина изображения текстуры.

</dd> <dt>

*format* 
</dt> <dd>

Формат точечных данных. Допустимы следующие значения: " \_ индекс цвета GL" \_ , " \_ Красная \_ \_ строка \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ ", "красный", "зеленый", "синий", "голубой", "GL", "красное", "GL", "GL", "BGR", "Расш.

</dd> <dt>

*type* 
</dt> <dd>

Тип данных для *данных*. Допустимы следующие значения: \_ НЕподписанный байт, байт GL, формат GL, формат GL \_ \_ \_ \_ без знака \_ Short, краткое название GL, \_ \_ Неподписанное целое число без знака, значение GL, \_ \_ а также тип \_ float.

</dd> <dt>

*data* 
</dt> <dd>

Указатель на данные изображения в памяти.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Функция **gluBuild1DMipmaps** получает входной образ и создает все образы mipmap (с помощью [**глускалеимаже**](gluscaleimage.md)), чтобы входной образ можно было использовать в качестве изображения текстуры мипмаппед. Затем вызывается функция [**glTexImage1D**](glteximage1d.md) для загрузки каждого изображения. Если ширина входного изображения не является степенью двух, то изображение масштабируется до ближайшей степени числа двух перед созданием MIP-карты.

Возвращаемое значение, равное нулю, указывает на успешное выполнение. В противном случае возвращается код ошибки GLU (см. [**глуеррорстринг**](gluerrorstring.md)).

Описание допустимых значений параметра *Format* см. в разделе **glTexImage1D**. Описание допустимых значений параметра *типа* см. в разделе [**глдравпикселс**](gldrawpixels.md).

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**глускалеимаже**](gluscaleimage.md)
</dt> </dl>

 

 





