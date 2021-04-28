---
description: Метод конструктора Кбасевиндов. Кбасевиндов.
ms.assetid: 9f0b91c4-0364-4c73-b97f-86703ca3ef74
title: Конструктор Кбасевиндов. Кбасевиндов (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CBaseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 05205750810294076bf005d0e5b73fda6b2143d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095822"
---
# <a name="cbasewindowcbasewindow-constructor"></a>Кбасевиндов. Кбасевиндов, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseWindow(
   BOOL bDoGetDC = TRUE,
   BOOL bPostToDestroy = FALSE
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бдожетдк* 
</dt> <dd>

Логическое значение, указывающее, следует ли извлекать контекст устройства.

</dd> <dt>

*бпосттодестрой* 
</dt> <dd>

Логическое значение, указывающее переменную члена [**кбасевиндов:: m \_ бдопосттодестрой**](cbasewindow-m-bdoposttodestroy.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

После создания объекта вызовите метод [**кбасевиндов::P репаревиндов**](cbasewindow-preparewindow.md) , чтобы создать окно. **Препаревиндов** является виртуальным методом. Он вызывает [**кбасевиндов:: инитиалисевиндов**](cbasewindow-initialisewindow.md), а также виртуальный метод. Эти методы отделены от конструктора, чтобы производные классы могли переопределять их при необходимости.

Если значение параметра *бдожетдк* равно **true**, `CBaseWindow` объект получает маркер для контекста устройства (DC) окна и сохраняет его в переменной члена [**кбасевиндов:: m \_ HDC**](cbasewindow-m-hdc.md) . Объект также создает совместимый с памятью контроллер домена, который хранится в переменной-члене [**кбасевиндов:: m \_ меморидк**](cbasewindow-m-memorydc.md) . Эти действия выполняются в методе **инитиалисевиндов** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




