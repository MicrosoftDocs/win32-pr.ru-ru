---
description: Функция обратного вызова, используемая для уведомления узла о завершении считывания значения шаг текселя.
MS-HAID: vspixengine.IPixEngine5Callbacks\_ReadTexelValueComplete\_UINT\_BSTR\_arr\_double\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Метод IPixEngine5Callbacks:: Реадтекселвалуекомплете'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3CAC08D8-0E4F-40B5-B91C-5C9159665C96
api_name:
- IPixEngine5Callbacks.ReadTexelValueComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7069d286cf65d87ba7bf4c576de3692b2a51d1a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537577"
---
# <a name="span-idvspixengineipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arrspanipixengine5callbacksreadtexelvaluecomplete-method"></a><span id="vspixengine.ipixengine5callbacks_readtexelvaluecomplete_uint_bstr_arr_double_arr"></span>Метод IPixEngine5Callbacks:: Реадтекселвалуекомплете

Функция обратного вызова, используемая для уведомления узла о завершении считывания значения шаг текселя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ReadTexelValueComplete(
   UINT      numChannels,
   BSTR []   count0_channelNames,
   double [] count0_channelValues
);
```

## <a name="parameters"></a>Параметры

*нумчаннелс*   
Число каналов, которые имеет шаг текселя.

*count0 \_ чаннелнамес*   
Строки COM, содержащие имена каналов.

*count0 \_ чаннелвалуес*   
Значения каналов.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span> См. также

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
