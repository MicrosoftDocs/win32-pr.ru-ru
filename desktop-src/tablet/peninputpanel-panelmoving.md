---
description: Не рекомендуется. Пенинпутпанел был заменен панелью ввода текста (TIP). Происходит при перемещении объекта Пенинпутпанел.
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: Событие Пенинпутпанел. Панелмовинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4a152afdef9fcd10fb92fdec55d9a460faf58ca91536e96c9876203fbad44c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596604"
---
# <a name="peninputpanelpanelmoving-event"></a>Пенинпутпанел. Панелмовинг, событие

Не рекомендуется. [**Пенинпутпанел**](peninputpanel-class.md) был заменен [панелью ввода текста (TIP)](text-input-panel-reference.md).

Происходит при перемещении объекта [**пенинпутпанел**](peninputpanel-class.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

По *левому краю* \[ в, out\]
</dt> <dd>

Новая горизонтальная ось, или оси x, Расположение левого края объекта [**пенинпутпанел**](peninputpanel-class.md) в экранных координатах.

</dd> <dt>

В *Начало* \[ в, out\]
</dt> <dd>

Новая вертикальная ось, или оси y, Расположение левого края объекта [**пенинпутпанел**](peninputpanel-class.md) в экранных координатах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если это событие завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Событие **панелмовинг** предназначено для изменения расположения панели ввода с помощью пера путем изменения параметров *Left* и *Top* .

Методы [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) и [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) приводят к тому, что объект [**пенинпутпанел**](peninputpanel-class.md) вызывает его код автоматического позиционирования, который активирует событие **панелмовинг** . Следовательно, вызов этих методов внутри обработчика **панелмовинг** может привести к созданию рекурсивного бесконечного цикла.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Заголовок<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также

<dl> <dt>

[**пенинпутпанел**](peninputpanel-class.md)
</dt> </dl>

 

 




