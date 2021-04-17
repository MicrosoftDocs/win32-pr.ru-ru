---
description: Метод Саурцесреадканваит удерживает или освобождает поток потоковой передачи.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Кбасерендерер. Саурцесреадканваит, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657991"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a>Кбасерендерер. Саурцесреадканваит, метод

`SourceThreadCanWait`Метод удерживает или освобождает поток потоковой передачи.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бканваит* 
</dt> <dd>

Логическое значение, указывающее, следует ли хранить поток потоковой передачи. Если **значение равно true**, поток потоковой передачи блокируется, пока фильтр ожидает отображения следующих выборок. Если **значение равно false**, поток потоковой передачи освобождается.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК.

## <a name="remarks"></a>Комментарии

Вызов `SourceThreadCanWait` метода со значением **false** приводит к тому, что фильтр возвращается из заблокированного вызова [**имеминпутпин:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) . Когда фильтр работает, он блокирует **Получение** вызовов до времени презентации в текущем примере. Если фильтр приостановлен, он блокирует **Получение** вызовов на неопределенное время. Это поведение регулирует поток данных в потоке. Однако если фильтр остановлен или сброшен, он не должен блокироваться.

Блокировка управляется методом [**кбасерендерер:: ваитфоррендертиме**](cbaserenderer-waitforrendertime.md) , который ожидает два события: [**кбасерендерер:: m \_ рендеревент**](cbaserenderer-m-renderevent.md) и [**кбасерендерер:: m \_ среадсигнал**](cbaserenderer-m-threadsignal.md). Событие **m \_ рендеревент** сигнализирует о получении времени презентации. Событие **m \_ среадсигнал** сигнализирует, когда `SourceThreadCanWait` вызывается со значением **false**. Вызов `SourceThreadCanWait` со значением **true** сбрасывает событие.

Методы [**кбасерендерер:: останавливают**](cbaserenderer-stop.md) и [**Кбасерендерер:: бегинфлуш**](cbaserenderer-beginflush.md) вызывают `SourceThreadCanWait` со значением **false** (освобождая поток потоковой передачи). Методы [**кбасерендерер::P Аусе**](cbaserenderer-pause.md), [**Кбасерендерер:: Run**](cbaserenderer-run.md)и [**кбасерендерер:: ендфлуш**](cbaserenderer-endflush.md) вызывают `SourceThreadCanWait` значение **true**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




