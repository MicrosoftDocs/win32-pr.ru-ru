---
description: Функция обратного вызова, используемая для уведомления узла о ходе выполнения модулей. Это также позволяет основному приложению определить, что ядро все еще работает.
title: 'Метод Истатускаллбакк:: Status'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: edf48e62389224a01af7e52aa7e87f3db63b3740
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622310"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>Метод Истатускаллбакк:: Status

Функция обратного вызова, используемая для уведомления узла о ходе выполнения модуля. Это также позволяет основному приложению определить, что ядро все еще работает.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a>Параметры

*двмиллисекондселапсед*   
Время, прошедшее с момента последнего вызова состояния, в миллисекундах.

*двфрамескаптуред*   
Число кадров, записанных с момента последнего вызова Status.

*двфрамеселапсед*   
Число кадров, истекших с момента последнего вызова состояния.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается с ошибкой, возвращается **S_OK**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**истатускаллбакк**](/windows/desktop/direct3dtools/istatuscallback)

 

 
