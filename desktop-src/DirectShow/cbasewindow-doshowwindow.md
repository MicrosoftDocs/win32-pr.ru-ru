---
description: Метод Дошоввиндов задает режим отображения окна.
ms.assetid: 4180de9d-ef40-40e3-aa37-be54283b1f97
title: Кбасевиндов. Дошоввиндов, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoShowWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fef63e04d0e04f2fe0daa78cd6b33a22fa7c8fa14c57b1e022703dea0914dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074636"
---
# <a name="cbasewindowdoshowwindow-method"></a>Кбасевиндов. Дошоввиндов, метод

Метод **дошоввиндов** задает режим отображения окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DoShowWindow(
   LONG ShowCmd
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*шовкмд* 
</dt> <dd>

Флаг, указывающий способ отображения окна. Значением может быть любая константа, определенная для параметра *нкмдшов* функции [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

