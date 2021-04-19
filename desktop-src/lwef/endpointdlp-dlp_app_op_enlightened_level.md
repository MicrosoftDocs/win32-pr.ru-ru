---
description: Связывает действие защиты от потери данных (DLP) конечной точки с уровнем применения.
title: Структура DLP_APP_OP_ENLIGHTENED_LEVEL (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495965"
---
# <a name="dlp_app_op_enlightened_level-structure"></a><span data-ttu-id="a02a1-103">Структура DLP_APP_OP_ENLIGHTENED_LEVEL</span><span class="sxs-lookup"><span data-stu-id="a02a1-103">DLP_APP_OP_ENLIGHTENED_LEVEL structure</span></span>

<span data-ttu-id="a02a1-104">Связывает действие защиты от потери данных (DLP) конечной точки с уровнем применения.</span><span class="sxs-lookup"><span data-stu-id="a02a1-104">Associates an endpoint Data Loss Prevention (DLP) action with an enforcement level.</span></span>

## <a name="syntax"></a><span data-ttu-id="a02a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a02a1-105">Syntax</span></span>


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a><span data-ttu-id="a02a1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a02a1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a02a1-107">*Операция* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a02a1-107">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a02a1-108">Значение из перечисления [длпактионтипе](endpointdlp-dlpactiontype.md) , указывающее тип действия DLP конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a02a1-108">A value from the [DlpActionType](endpointdlp-dlpactiontype.md) enumeration specifying the endpoint DLP action type.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="a02a1-109">*Аппенфорцементлевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a02a1-109">*AppEnforcementLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a02a1-110">Значение из [длпаппенфорцелевел](endpointdlp-dlpappenforcelevel.md) , указывающее уровень принудительного применения для соответствующего типа действия DLP конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a02a1-110">A value from the [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) specifying the level of enforcement for the associated endpoint DLP action type.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="a02a1-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="a02a1-111">Remarks</span></span>

<span data-ttu-id="a02a1-112">Передайте массив этих структур в [длпинитиализинфорцементмоде](endpointdlp-dlpinitializeenforcementmode.md) , чтобы установить режим принудительного применения для набора операций DLP в конечной точке.</span><span class="sxs-lookup"><span data-stu-id="a02a1-112">Pass an array of these structures into [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) to set the enforcement mode for a set of endpoint DLP operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="a02a1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a02a1-113">Requirements</span></span>



| <span data-ttu-id="a02a1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a02a1-114">Requirement</span></span>          |    <span data-ttu-id="a02a1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a02a1-115">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a02a1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a02a1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a02a1-117">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="a02a1-117">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

