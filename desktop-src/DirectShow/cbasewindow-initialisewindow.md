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
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675469"
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

Обработчик для окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

По умолчанию этот метод получает маркер для контекста устройства (DC) окна и создает совместимый контроллер памяти. Однако если значение флага [**кбасевиндов:: m \_ Бдожетдк**](cbasewindow-m-bdogetdc.md) равно **false**, этот метод не извлекает контексты устройств. КОНТРОЛЛЕР памяти может использоваться для выбора точечных рисунков, прежде чем блиттинг их в окно.

Метод [**кбасевиндов::D окреатевиндов**](cbasewindow-docreatewindow.md) вызывает этот метод.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасевиндов**](cbasewindow.md)
</dt> </dl>

 

 




