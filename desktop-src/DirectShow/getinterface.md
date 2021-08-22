---
description: Функция "интерфейс" получает указатель интерфейса.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: Функция-интерфейс (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 289c6e56d4b5387fe9224e476c69865107102141b687825cdfd9a717f482632c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537034"
---
# <a name="getinterface-function"></a>Функция "интерфейс

`GetInterface`Функция получает указатель интерфейса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pUnk* 
</dt> <dd>

Указатель на интерфейс **IUnknown** .

</dd> <dt>

*ппв* 
</dt> <dd>

Адрес указателя на полученный интерфейс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

Эта функция-член выполняет поточно-ориентированное приращение счетчика ссылок. Чтобы получить интерфейс и добавить ссылку, вызовите эту функцию из переопределяющей реализации метода **инонделегатингункновн:: нонделегатингкуеринтерфаце** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>комбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Вспомогательные функции COM**](com-helper-functions.md)
</dt> <dt>

[**инонделегатингункновн**](inondelegatingunknown.md)
</dt> </dl>

 

 




