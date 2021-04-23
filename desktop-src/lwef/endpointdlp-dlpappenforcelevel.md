---
description: Задает уровень принудительной операции защиты от потери данных в конечной точке.
title: Перечисление Длпаппенфорцелевел (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495953"
---
# <a name="dlpappenforcelevel-enumeration"></a><span data-ttu-id="c8c74-103">Перечисление Длпаппенфорцелевел</span><span class="sxs-lookup"><span data-stu-id="c8c74-103">DlpAppEnforceLevel enumeration</span></span>

<span data-ttu-id="c8c74-104">Задает уровень принудительной операции защиты от потери данных в конечной точке.</span><span class="sxs-lookup"><span data-stu-id="c8c74-104">Specifies the enforcement level of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c74-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8c74-105">Syntax</span></span>


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a><span data-ttu-id="c8c74-106">Константы</span><span class="sxs-lookup"><span data-stu-id="c8c74-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c8c74-107">*Длпаппенфорцелевелноне* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8c74-107">*DlpAppEnforceLevelNone* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c74-108">Приложение не принудительно применено.</span><span class="sxs-lookup"><span data-stu-id="c8c74-108">No enforcement by the app.</span></span> <span data-ttu-id="c8c74-109">Система DLP принудительно применит операцию.</span><span class="sxs-lookup"><span data-stu-id="c8c74-109">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c8c74-110">*Длпаппенфорцелевелнотифи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8c74-110">*DlpAppEnforceLevelNotify* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c74-111">Приложение кнопка будет использовать API DLP для уведомления системы DLP об операции.</span><span class="sxs-lookup"><span data-stu-id="c8c74-111">Tne app will use the DLP APIs to notify the DLP system about the operation.</span></span> <span data-ttu-id="c8c74-112">Система DLP принудительно применит операцию.</span><span class="sxs-lookup"><span data-stu-id="c8c74-112">The DLP system will enforce the operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c8c74-113">*Длпаппенфорцелевелпревент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8c74-113">*DlpAppEnforceLevelPrevent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c74-114">Не поддерживается в текущей версии.</span><span class="sxs-lookup"><span data-stu-id="c8c74-114">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c8c74-115">*Длпаппенфорцелевелфулл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8c74-115">*DlpAppEnforceLevelFull* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c74-116">Не поддерживается в текущей версии.</span><span class="sxs-lookup"><span data-stu-id="c8c74-116">Not supported in the current version.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c8c74-117">*Длпаппенфорцелевелкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8c74-117">*DlpAppEnforceLevelCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8c74-118">Максимальное значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="c8c74-118">The maximum value of the enumeration.</span></span>

</dd> </dl>



## <a name="remarks"></a><span data-ttu-id="c8c74-119">Remarks</span><span class="sxs-lookup"><span data-stu-id="c8c74-119">Remarks</span></span>

<span data-ttu-id="c8c74-120">Значения из этого перечисления используются структурой [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .</span><span class="sxs-lookup"><span data-stu-id="c8c74-120">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>


## <a name="requirements"></a><span data-ttu-id="c8c74-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c8c74-121">Requirements</span></span>



| <span data-ttu-id="c8c74-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c8c74-122">Requirement</span></span>          |    <span data-ttu-id="c8c74-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c8c74-123">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c74-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8c74-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c8c74-125">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="c8c74-125">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

