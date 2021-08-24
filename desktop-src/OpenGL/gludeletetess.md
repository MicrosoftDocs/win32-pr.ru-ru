---
title: Функция Глуделететесс (GLU. h)
description: Функция Глуделететесс уничтожает объект тесселяции.
ms.assetid: 7e1540f7-5e7d-4a3b-8c94-5a6800b17411
keywords:
- Функция Глуделететесс OpenGL
topic_type:
- apiref
api_name:
- gluDeleteTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72d00d2ab10df54b5f4b3869f1d573167ee1f35f5d0b3991af14ece867c5a19e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777694"
---
# <a name="gludeletetess-function"></a>Функция Глуделететесс

Функция **глуделететесс** уничтожает объект тесселяции.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI gluDeleteTess(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тесс* 
</dt> <dd>

Объект тесселяции для уничтожения (создается с помощью [**глуневтесс**](glunewtess.md)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Remarks

Функция **глуделететесс** уничтожает указанный объект тесселяции и освобождает используемую память.

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

[**глутессбегинполигон**](glubeginpolygon.md)
</dt> <dt>

[*глутесскаллбакк*](glutess.md)
</dt> </dl>

 

 





