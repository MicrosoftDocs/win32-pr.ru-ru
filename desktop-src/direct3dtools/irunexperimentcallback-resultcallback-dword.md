---
description: Запросы на запуск эксперимента (записи) в указанном процессе.
MS-HAID: vspixengine.IRunExperimentCallback\_ResultCallback\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ирунексперименткаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C00034DF-5F51-49A2-B49A-62F98EA48F46
api_name:
- IRunExperimentCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a8eac603821c546f79734a615afb31dcb92fe0ac
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625590"
---
# <a name="span-idvspixengineirunexperimentcallback_resultcallback_dwordspanirunexperimentcallbackresultcallback-method"></a><span id="vspixengine.irunexperimentcallback_resultcallback_dword"></span>Метод Ирунексперименткаллбакк:: Ресулткаллбакк

Запросы на запуск эксперимента (записи) в указанном процессе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResultCallback(
   DWORD processId
);
```

## <a name="parameters"></a>Параметры

*processId*   
Указанный процесс.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ирунексперименткаллбакк**](/windows/desktop/direct3dtools/irunexperimentcallback)

 

 
