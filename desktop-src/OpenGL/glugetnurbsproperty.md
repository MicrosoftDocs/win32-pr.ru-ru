---
title: Функция Глужетнурбспроперти (GLU. h)
description: Функция Глужетнурбспроперти возвращает неравномерное рациональное свойство B-сплайна (НУРБС).
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- Функция Глужетнурбспроперти OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135659"
---
# <a name="glugetnurbsproperty-function"></a>Функция Глужетнурбспроперти

Функция **глужетнурбспроперти** возвращает неравномерное рациональное свойство B-сплайна ([нурбс](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*нобж* 
</dt> <dd>

Объект НУРБС (созданный с помощью [**глуневнурбсрендерер**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Свойство, значение которого необходимо извлечь. Допустимы следующие значения: допустимость \_ выборки Glu \_ , \_ режим экрана Glu \_ , GLUное извлечение \_ , Glu \_ автоматической \_ загрузки \_ матрицы, \_ GLU \_ нечувствительность, \_ Glu \_ метод выборки, Glu \_ U \_ Step и Glu \_ V \_ Step.

</dd> <dt>

*value* 
</dt> <dd>

Указатель на расположение, в которое записывается значение именованного свойства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Используйте **глужетнурбспроперти** для получения свойств, хранящихся в объекте нурбс. Эти свойства влияют на способ отрисовки НУРБС кривых и поверхностей. Дополнительные сведения о свойствах НУРБС см. в разделе [**глунурбспроперти**](glunurbsproperty.md).

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

[**глуневнурбсрендерер**](glunewnurbsrenderer.md)
</dt> <dt>

[**глунурбспроперти**](glunurbsproperty.md)
</dt> </dl>

 

 





