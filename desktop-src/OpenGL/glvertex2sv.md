---
title: Функция glVertex2sv (GL. h)
description: Указывает вершину. | Функция glVertex2sv (GL. h)
ms.assetid: 4e13356a-a74b-4fb6-a001-1fffc28dd7a1
keywords:
- Функция glVertex2sv OpenGL
topic_type:
- apiref
api_name:
- glVertex2sv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e865ab8999e08f9c13ad46443ba039be1cda9e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684908"
---
# <a name="glvertex2sv-function"></a>Функция glVertex2sv

Указывает вершину.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glVertex2sv(
   const GLshort *v
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*3,3* 
</dt> <dd>

Указатель на массив из двух элементов. Элементы являются координатами x и y вершины.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Библиотека<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**глбегин**](glbegin.md)
</dt> <dt>

[**глкалллист**](glcalllist.md)
</dt> <dt>

[**глколор**](glcolor-functions.md)
</dt> <dt>

[**гледжефлаг**](gledgeflag-functions.md)
</dt> <dt>

[**гленд**](glend.md)
</dt> <dt>

[**глевалкурд**](glevalcoord-functions.md)
</dt> <dt>

[**глиндекс**](glindex-functions.md)
</dt> <dt>

[**глматериал**](glmaterial-functions.md)
</dt> <dt>

[**глнормал**](glnormal-functions.md)
</dt> <dt>

[**глрект**](glrect-functions.md)
</dt> <dt>

[**глтекскурд**](gltexcoord-functions.md)
</dt> </dl>

 

 





