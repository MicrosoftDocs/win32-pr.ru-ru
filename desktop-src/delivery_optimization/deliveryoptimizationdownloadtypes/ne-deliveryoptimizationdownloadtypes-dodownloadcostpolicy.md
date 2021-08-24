---
title: Перечисление Додовнлоадкостполици
description: Указывает идентификатор параметров политик затрат, связанных со свойством **DODownloadProperty_CostPolicy** .
keywords:
- Перечисление Додовнлоадкостполици, Додовнлоадкостполици
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 763042ed6d0df6fa287fbe66d23528a199a73041cb3500c6a2812e6db86cb698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677884"
---
# <a name="dodownloadcostpolicy-enumeration"></a>Перечисление Додовнлоадкостполици

Перечисление **додовнлоадкостполици** указывает идентификатор параметров политик затрат, связанных со свойством **DODownloadProperty_CostPolicy** .

## <a name="syntax"></a>Синтаксис

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a>Константы

| Требование | Значение |
|-|-|
| DODownloadCostPolicy_Always | Загрузка выполняется независимо от стоимости. |
| DODownloadCostPolicy_Unrestricted | Загрузка выполняется, если не накладывает затраты или лимиты трафика. |
| DODownloadCostPolicy_Standard | Загрузка выполняется, если не взимается ни плата, ни исчерпание. |
| DODownloadCostPolicy_NoRoaming | Загрузка выполняется, если в связи с нагрузкой не взимается плата за роуминг. |
| DODownloadCostPolicy_NoSurcharge | Загрузка выполняется, если не взимается плата. |
| DODownloadCostPolicy_NoCellular | Загрузка выполняется, если сеть не подключена к сотовой сети. |

## <a name="requirements"></a>Requirements (Требования)

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, версия 1809 \[ Только приложения Win32\] |
| **Минимальная версия сервера** | Windows Сервер, \[ только приложения Win32 версии 1809\] |
| **Header** | Деливерйоптимизатиондовнлоадтипес. h |
