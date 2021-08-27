---
description: Метод Инитиалисевиндов инициализирует окно.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Iniметод Тиалисевиндов (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f260f60111f715bfce357e264b65bb4b821c5ca890d39d4d54e7269a191df303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954663"
---
# <a name="cbasewindowinitialisewindow-method"></a>CBaseWindow.Iniметод Тиалисевиндов

`InitialiseWindow`Метод инициализирует окно.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Дескриптор для окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Remarks

По умолчанию этот метод получает маркер для контекста устройства (DC) окна и создает совместимый контроллер памяти. Однако если значение флага [**кбасевиндов:: m \_ Бдожетдк**](cbasewindow-m-bdogetdc.md) равно **false**, этот метод не извлекает контексты устройств. КОНТРОЛЛЕР памяти может использоваться для выбора точечных рисунков, прежде чем блиттинг их в окно.

Метод [**кбасевиндов::D окреатевиндов**](cbasewindow-docreatewindow.md) вызывает этот метод.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




