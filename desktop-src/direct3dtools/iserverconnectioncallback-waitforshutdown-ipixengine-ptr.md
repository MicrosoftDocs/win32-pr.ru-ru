---
description: Ожидание завершения работы указанного обработчика (вызов блокировки).
MS-HAID: vspixengine.IServerConnectionCallback\_WaitForShutdown\_IPixEngine\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Исерверконнектионкаллбакк:: Ваитфоршутдовн'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B70229D5-3C41-4B50-8336-A1271A9EBE81
api_name:
- IServerConnectionCallback.WaitForShutdown
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65ea49e01d6635ea73f5740ebf05a1fb65122291
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625770"
---
# <a name="span-idvspixengineiserverconnectioncallback_waitforshutdown_ipixengine_ptrspaniserverconnectioncallbackwaitforshutdown-method"></a><span id="vspixengine.iserverconnectioncallback_waitforshutdown_ipixengine_ptr"></span>Метод Исерверконнектионкаллбакк:: Ваитфоршутдовн

Ожидание завершения работы указанного обработчика (вызов блокировки).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WaitForShutdown(
   IPixEngine * pEngine
);
```

## <a name="parameters"></a>Параметры

*пенгине*   
Подсистема для завершения работы.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**исерверконнектионкаллбакк**](/windows/desktop/direct3dtools/iserverconnectioncallback)

 

 
