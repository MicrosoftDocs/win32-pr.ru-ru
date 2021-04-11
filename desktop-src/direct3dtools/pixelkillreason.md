---
description: Перечисление, используемое для указания причины отклонения пикселя.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Перечисление ПИКСЕЛКИЛЛРЕАСОН
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341822"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>Перечисление ПИКСЕЛКИЛЛРЕАСОН

Перечисление, используемое для указания причины отклонения пикселя.

## <a name="syntax"></a>Синтаксис


```C++
};
```

## <a name="constants"></a>Константы

<span id="PKR_NONE"></span><span id="pkr_none"></span>**ПКР \_ None**  
Значение, указывающее, что пиксель не был отклонен.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**ПКР \_ шадеркилл**  
Значение, указывающее, что точка была отклонена из-за того, что шейдер не выполнялся.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**ПКР \_ сЦиссортест**  
Значение, указывающее, что точка была отклонена из-за сбоя выножницного теста.

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**ПКР \_ алфатест**  
Значение, указывающее, что точка была отклонена из-за сбоя при проверке альфа-канала.

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**ПКР \_ стенЦилтест**  
Значение, указывающее, что точка была отклонена из-за сбоя теста набора элементов.

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**ПКР \_ депстест**  
Значение, указывающее, что точка была отклонена из-за сбоя теста глубины.

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**ПКР \_ ноткомпутабле**  
Значение, указывающее, что невозможно вычислить Журнал пикселей.

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**ПКР, \_ Ошибка**  
Значение, указывающее, что точка была отклонена из-за общей ошибки.

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**ПКР, не \_ ПЕРЕсечение**  
Значение, указывающее, что точка была отклонена, поскольку вызов Draw не пересекает пиксел.

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**ПКР \_ перекрыто**  
Значение, указывающее, что точка была отклонена, поскольку Draw была перекрыто.

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**ПКР \_ депсстенЦилтест**  
Значение, указывающее, что точка была отклонена из-за сбоя теста глубины и трафарета.

## <a name="requirements"></a>Требования

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Вспиксенгине. h</td></tr></tbody></table>

 

 



