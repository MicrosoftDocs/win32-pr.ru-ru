---
description: Метод получения \_ заголовка извлекает заголовок текущего окна.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: Метод CBaseControlWindow.get_Caption (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f05501adbd486eaa60e939aacfdd5896c0fbcae059673029f04fcca8aeb742a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640893"
---
# <a name="cbasecontrolwindowget_caption-method"></a>Метод Кбасеконтролвиндов. Get \_ Caption

`get_Caption`Метод извлекает заголовок текущего окна.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстркаптион* 
</dt> <dd>

Указатель на заголовок текущего окна.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

большинство окон верхнего уровня на рабочем столе на основе Windows имеют заголовок (заголовок), связанный с ними. Это свойство можно запрашивать и задавать с помощью интерфейса [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) . Любой набор заголовков будет виден только в том случае, если для окна \_ применен стиль «заголовок WS». Если это не так, заголовок можно по-прежнему задать (и получить), хотя он не будет виден пользователю.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




