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
ms.openlocfilehash: 2ac6838e7103970d588814bdc5a39e9e26fd4a33
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710587"
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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ирунексперименткаллбакк**](/windows/desktop/direct3dtools/irunexperimentcallback)

 

 
