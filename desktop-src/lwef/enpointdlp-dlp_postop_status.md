---
description: Указывает сведения о состоянии операции DLP конечной точки.
title: Структура DLP_POSTOP_STATUS (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495825"
---
# <a name="dlp_postop_status-structure"></a><span data-ttu-id="4e68c-103">Структура DLP_POSTOP_STATUS</span><span class="sxs-lookup"><span data-stu-id="4e68c-103">DLP_POSTOP_STATUS structure</span></span>

<span data-ttu-id="4e68c-104">Указывает сведения о состоянии операции DLP конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4e68c-104">Specifies status information about an endpoint DLP operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e68c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e68c-105">Syntax</span></span>


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a><span data-ttu-id="4e68c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="4e68c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4e68c-107">*Версия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e68c-107">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e68c-108">Значение типа DWORD, указывающее версию API.</span><span class="sxs-lookup"><span data-stu-id="4e68c-108">A DWORD specifying the API version.</span></span> <span data-ttu-id="4e68c-109">Это значение всегда должно быть **DLP_POSTOP_STATUS_V_LATEST**.</span><span class="sxs-lookup"><span data-stu-id="4e68c-109">This value should always be **DLP_POSTOP_STATUS_V_LATEST**.</span></span> <span data-ttu-id="4e68c-110">Эта константа определена в файле заголовка образца ендпоинтдлп. h, приведенном в статье [Защита от потери данных в конечной точке](endpointdlp-endpoint-data-loss-prevention.md)</span><span class="sxs-lookup"><span data-stu-id="4e68c-110">This constant is defined in the endpointdlp.h sample header file listing in the article [Endpoint data loss prevention](endpointdlp-endpoint-data-loss-prevention.md)</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="4e68c-111">*Оператионсукцесс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e68c-111">*OperationSuccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e68c-112">Логическое значение, указывающее, была ли операция открытия успешной.</span><span class="sxs-lookup"><span data-stu-id="4e68c-112">A BOOL indicating whether the open operation was successful.</span></span>

</dd> </dl>





## <a name="remarks"></a><span data-ttu-id="4e68c-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="4e68c-113">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="4e68c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4e68c-114">Requirements</span></span>



| <span data-ttu-id="4e68c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4e68c-115">Requirement</span></span>          |    <span data-ttu-id="4e68c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4e68c-116">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e68c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e68c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4e68c-118">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="4e68c-118">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
