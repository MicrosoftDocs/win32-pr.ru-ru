---
description: Функция обратного вызова, используемая для уведомления узла о том, какие кадры были захвачены.
MS-HAID: vspixengine.IFrameListCallback\_ResultCallback\_DWORD\_DWORD\_arr\_DWORD\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Ифрамелисткаллбакк:: Ресулткаллбакк'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AEB340C6-74AA-4F8B-86D0-9C0366ECDE70
api_name:
- IFrameListCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 79edccd587d0109767fd0e1661f76d3e1830ee072610296ac389acaac177cfc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094824"
---
# <a name="span-idvspixengineiframelistcallback_resultcallback_dword_dword_arr_dword_arrspaniframelistcallbackresultcallback-method"></a><span id="vspixengine.iframelistcallback_resultcallback_dword_dword_arr_dword_arr"></span>Метод Ифрамелисткаллбакк:: Ресулткаллбакк

Функция обратного вызова, используемая для уведомления узла о том, какие кадры были захвачены.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResultCallback(
   DWORD    numFrames,
   DWORD [] count0_frameNumbers,
   DWORD [] count0_frameEventIDs
);
```

## <a name="parameters"></a>Параметры

*нумфрамес*   
Число захваченных кадров.

*count0 \_ фраменумберс*   
Номера кадров захваченных кадров.

*count0 \_ фрамивентидс*   
Завершающее событие, связанное с каждым кадром.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**ифрамелисткаллбакк**](/windows/desktop/direct3dtools/iframelistcallback)

 

 
