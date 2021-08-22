---
title: Функция Глислист (GL. h)
description: Функция Гллслист проверяет наличие списка отображений.
ms.assetid: 86ef3684-8047-4ee4-befd-ec26bcd036c3
keywords:
- Функция Глислист OpenGL
topic_type:
- apiref
api_name:
- glIsList
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562eb4040323452379659a068dbc4844a2e84c51009cb0ac843b2e5aa1b641a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493374"
---
# <a name="glislist-function"></a>Функция Глислист

Функция **гллслист** проверяет наличие списка отображений.

## <a name="syntax"></a>Синтаксис


```C++
GLboolean WINAPI glIsList(
   GLuint list
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*list* 
</dt> <dd>

Потенциальное имя списка дисплеев.

</dd> </dl>

## <a name="error-codes"></a>Коды ошибок

С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.



| Имя                                                                                                  | Значение                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Недопустимая \_ Операция GL**</dt> </dl> | Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).<br/> |



## <a name="remarks"></a>Remarks

Функция **гллслист** ВОЗВРАЩАЕТ значение GL \_ true, если *List* является именем списка отображаемых данных, и возвращает \_ значение GL false в противном случае.

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

[**глкалллист**](glcalllist.md)
</dt> <dt>

[**глкалллистс**](glcalllists.md)
</dt> <dt>

[**глделетелистс**](gldeletelists.md)
</dt> <dt>

[**гленд**](glend.md)
</dt> <dt>

[**глженлистс**](glgenlists.md)
</dt> <dt>

[**глневлист**](glnewlist.md)
</dt> </dl>

 

 





