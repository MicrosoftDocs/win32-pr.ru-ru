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
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414873"
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

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Минимальная версия клиента** | Windows 10, \[ только приложения Win32 версии 1809\] |
| **Минимальная версия сервера** | Windows Server, \[ только приложения Win32 версии 1809\] |
| **Header** | Деливерйоптимизатиондовнлоадтипес. h |
