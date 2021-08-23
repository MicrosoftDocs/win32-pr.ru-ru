---
title: Функция Глдепсмаск (GL. h)
description: Функция Глдепсмаск включает или отключает запись в буфер глубины.
ms.assetid: 067b18e2-f21a-4dde-8fa6-dd975746e189
keywords:
- Функция Глдепсмаск OpenGL
topic_type:
- apiref
api_name:
- glDepthMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0e774917d47cecdbb276b19dbc97a7c8c7620e04e0a044cf6932aa83167e325
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625724"
---
# <a name="gldepthmask-function"></a>Функция Глдепсмаск

Функция **глдепсмаск** включает или отключает запись в буфер глубины.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI glDepthMask(
   GLboolean flag
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*flag* 
</dt> <dd>

Указывает, разрешена ли запись в буфер глубины. Если *флаг* равен нулю, запись в буфер глубины отключена. В противном случае он будет включен. Изначально запись в буфере глубины включена.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.



| Имя                                                                                                  | Значение                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Недопустимая \_ Операция GL**</dt> </dl> | Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).<br/> |



## <a name="remarks"></a>Remarks

Следующая функция получает сведения, связанные с **глдепсмаск**:

**глжет** с аргументом GL \_ Depth \_ вритемаск

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Библиотека<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**глбегин**](glbegin.md)
</dt> <dt>

[**глколормаск**](glcolormask.md)
</dt> <dt>

[**глдепсфунк**](gldepthfunc.md)
</dt> <dt>

[**глдепсранже**](gldepthrange.md)
</dt> <dt>

[**гленд**](glend.md)
</dt> <dt>

[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**глиндексмаск**](glindexmask.md)
</dt> <dt>

[**глстенЦилмаск**](glstencilmask.md)
</dt> </dl>

 

 





