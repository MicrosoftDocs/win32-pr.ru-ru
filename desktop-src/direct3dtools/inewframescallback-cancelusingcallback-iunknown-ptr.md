---
description: Обратный вызов, уведомляющий узел об отмене запроса.
MS-HAID: vspixengine.INewFramesCallback\_CancelUsingCallback\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иневфрамескаллбакк:: Канцелусингкаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 291B2F85-1437-4704-8971-4B7C25B693F8
api_name:
- INewFramesCallback.CancelUsingCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0f5e6ef8a7e2533ce4a78109f2d4d2aa4b5eb845
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627744"
---
# <a name="span-idvspixengineinewframescallback_cancelusingcallback_iunknown_ptrspaninewframescallbackcancelusingcallback-method"></a><span id="vspixengine.inewframescallback_cancelusingcallback_iunknown_ptr"></span>Метод Иневфрамескаллбакк:: Канцелусингкаллбакк

Обратный вызов, уведомляющий узел об отмене запроса.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CancelUsingCallback(
   IUnknown * requestCallback
);
```

## <a name="parameters"></a>Параметры

*рекуесткаллбакк*   
Адрес отмененного запроса.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иневфрамескаллбакк**](/windows/desktop/direct3dtools/inewframescallback)

 

 
