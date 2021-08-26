---
description: Функция обратного вызова, используемая для уведомления узла о том, какие интерфейсы поддерживаются.
MS-HAID: vspixengine.IVersionCallback\_VersionTableReady\_GUID\_arr\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод Иверсионкаллбакк:: Версионтаблереади'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 58D5E6B4-2CF8-4C13-9A62-93418D46CBCF
api_name:
- IVersionCallback.VersionTableReady
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 680a9db6fe72dcf11dc6ecb13cf64fede9cf375e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626540"
---
# <a name="span-idvspixengineiversioncallback_versiontableready_guid_arr_uintspaniversioncallbackversiontableready-method"></a><span id="vspixengine.iversioncallback_versiontableready_guid_arr_uint"></span>Метод Иверсионкаллбакк:: Версионтаблереади

Функция обратного вызова, используемая для уведомления узла о том, какие интерфейсы поддерживаются.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT VersionTableReady(
   GUID [] count1_interfaceIds,
   UINT    count
);
```

## <a name="parameters"></a>Параметры

*count1 \_ интерфацеидс*   
Массив, содержащий идентификаторы GUID поддерживаемых идентификаторов интерфейса.

*расчета*   
Число идентификаторов GUID, переданных в count1 \_ интерфацеидс.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Заголовок</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**иверсионкаллбакк**](/windows/desktop/direct3dtools/iversioncallback)

 

 
