---
description: Указывает тип действия для операции защиты от потери данных конечной точки (DLP).
title: Перечисление Длпактионтипе (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495954"
---
# <a name="dlpactiontype-enumeration"></a><span data-ttu-id="f821b-103">Перечисление Длпактионтипе</span><span class="sxs-lookup"><span data-stu-id="f821b-103">DlpActionType enumeration</span></span>

<span data-ttu-id="f821b-104">Указывает тип действия для операции защиты от потери данных конечной точки (DLP).</span><span class="sxs-lookup"><span data-stu-id="f821b-104">Specifies the action type of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f821b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f821b-105">Syntax</span></span>


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a><span data-ttu-id="f821b-106">Константы</span><span class="sxs-lookup"><span data-stu-id="f821b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f821b-107">*длпактионтипекопиторемоваблемедиа*</span><span class="sxs-lookup"><span data-stu-id="f821b-107">*DlpActionTypeCopyToRemovableMedia*</span></span>
</dt> <dd>

<span data-ttu-id="f821b-108">Операция копирования на съемный носитель.</span><span class="sxs-lookup"><span data-stu-id="f821b-108">A copy operation to removable media.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="f821b-109">*длпактионтипекопитонетворкшаре*</span><span class="sxs-lookup"><span data-stu-id="f821b-109">*DlpActionTypeCopyToNetworkShare*</span></span>
</dt> <dd>

<span data-ttu-id="f821b-110">Операция копирования в общую сетевую папку.</span><span class="sxs-lookup"><span data-stu-id="f821b-110">A copy operation to a shared network folder.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="f821b-111">*длпактионтипекопитоклипбоард*</span><span class="sxs-lookup"><span data-stu-id="f821b-111">*DlpActionTypeCopyToClipboard*</span></span>
</dt> <dd>

<span data-ttu-id="f821b-112">Операция копирования в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="f821b-112">A copy operation to the clipboard.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="f821b-113">*длпактионтипепринт*</span><span class="sxs-lookup"><span data-stu-id="f821b-113">*DlpActionTypePrint*</span></span>
</dt> <dd>

<span data-ttu-id="f821b-114">Операция печати.</span><span class="sxs-lookup"><span data-stu-id="f821b-114">A print operation.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="f821b-115">*длпактионтипескринклип*</span><span class="sxs-lookup"><span data-stu-id="f821b-115">*DlpActionTypeScreenClip*</span></span>
</dt> <dd>

<span data-ttu-id="f821b-116">Операция снимка экрана.</span><span class="sxs-lookup"><span data-stu-id="f821b-116">A screen capture operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="f821b-117">*длпактионтипеакцессбюналловедапп*</span><span class="sxs-lookup"><span data-stu-id="f821b-117">*DlpActionTypeAccessByUnallowedApp*</span></span>
</dt> <dd>

<span data-ttu-id="f821b-118">Операция, выполняемая неразрешенным приложением.</span><span class="sxs-lookup"><span data-stu-id="f821b-118">An operation performed by an unallowed app.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="f821b-119">*длпактионтипеклаудаппегресс*</span><span class="sxs-lookup"><span data-stu-id="f821b-119">*DlpActionTypeCloudAppEgress*</span></span>
</dt> <dd>

<span data-ttu-id="f821b-120">Операция, нацеленная на облачное расположение.</span><span class="sxs-lookup"><span data-stu-id="f821b-120">An operation targeted to a cloud location.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="f821b-121">*длпактионтипеакцессбиблуетусапп*</span><span class="sxs-lookup"><span data-stu-id="f821b-121">*DlpActionTypeAccessByBluetoothApp*</span></span>
</dt> <dd>

<span data-ttu-id="f821b-122">Операция, включающая доступ приложения Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="f821b-122">An operation that includes access by a bluetooth app.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="f821b-123">*длпактионтипеакцессбирдпапп*</span><span class="sxs-lookup"><span data-stu-id="f821b-123">*DlpActionTypeAccessByRDPApp*</span></span>
</dt> <dd>

<span data-ttu-id="f821b-124">Операция, которая включает доступ к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="f821b-124">An operation that includes access by a remote desktop.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="f821b-125">*длпактионтипекаунт*</span><span class="sxs-lookup"><span data-stu-id="f821b-125">*DlpActionTypeCount*</span></span>
</dt> <dd>

<span data-ttu-id="f821b-126">Максимальное значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="f821b-126">The maximum value of the enumeration.</span></span>

</dd> </dl>
 

## <a name="remarks"></a><span data-ttu-id="f821b-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="f821b-127">Remarks</span></span>

<span data-ttu-id="f821b-128">Значения из этого перечисления используются структурой [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .</span><span class="sxs-lookup"><span data-stu-id="f821b-128">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f821b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="f821b-129">Requirements</span></span>



| <span data-ttu-id="f821b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="f821b-130">Requirement</span></span>          |    <span data-ttu-id="f821b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="f821b-131">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f821b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f821b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f821b-133">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="f821b-133">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

