---
title: Функция Глужеттесспроперти (GLU. h)
description: Функция Глужеттесспроперти возвращает свойство объекта тесселяции.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- Функция Глужеттесспроперти OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d12e7ca8099197b663893b1edcf04dd8fa98348fe4f6d3d324b54f33904e026a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554244"
---
# <a name="glugettessproperty-function"></a>Функция Глужеттесспроперти

Функция **глужеттесспроперти** возвращает свойство объекта тесселяции.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тесс* 
</dt> <dd>

Объект тесселяции (созданный с помощью [**глуневтесс**](glunewtess.md)).

</dd> <dt>

*какую* 
</dt> <dd>

Свойство, значение которого необходимо извлечь. Допустимы следующие значения: GLU \_ Тесс \_ обмотка \_ , Glu \_ Тесс \_ \_ only и Glu \_ Тесс \_ .

</dd> <dt>

*value* 
</dt> <dd>

Указатель на расположение, в которое записывается значение именованного свойства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Используйте **глужеттесспроперти** для извлечения свойств, хранящихся в объекте тесселяции. Эти свойства влияют на способ интерпретации и отрисовки объектов тесселяции. Сведения о свойствах и их возможностях см. в разделе [**глутесспроперти**](glutessproperty.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Библиотека<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**глуневтесс**](glunewtess.md)
</dt> <dt>

[**глутесспроперти**](glutessproperty.md)
</dt> </dl>

 

 





