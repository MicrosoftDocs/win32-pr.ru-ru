---
title: Структура TSMF_SUPPORT_NODEDATA_OUT
description: Используется в \_ \_ структуре out данных поддержки тсмф \_ для хранения сведений о поддерживаемых форматах мультимедиа.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT структуры службы удаленных рабочих столов
- PTSMF_SUPPORT_NODEDATA_OUT службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892193"
---
# <a name="tsmf_support_nodedata_out-structure"></a><span data-ttu-id="35c75-105">\_Структура тсмф поддержки \_ нодедата \_ out</span><span class="sxs-lookup"><span data-stu-id="35c75-105">TSMF\_SUPPORT\_NODEDATA\_OUT structure</span></span>

<span data-ttu-id="35c75-106">Используется в структуре [**\_ \_ \_ out данных поддержки тсмф**](tsmf-support-data-out.md) для хранения сведений о поддерживаемых форматах мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="35c75-106">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c75-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35c75-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a><span data-ttu-id="35c75-108">Члены</span><span class="sxs-lookup"><span data-stu-id="35c75-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="35c75-109">**nodeId**</span><span class="sxs-lookup"><span data-stu-id="35c75-109">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="35c75-110">Узел.</span><span class="sxs-lookup"><span data-stu-id="35c75-110">The node.</span></span>

</dd> <dt>

<span data-ttu-id="35c75-111">**хрсуппортстатус**</span><span class="sxs-lookup"><span data-stu-id="35c75-111">**hrSupportStatus**</span></span>
</dt> <dd>

<span data-ttu-id="35c75-112">Поддерживается ли приемник, идентифицируемый параметром *клсидневсинк* .</span><span class="sxs-lookup"><span data-stu-id="35c75-112">Whether the sink identified by the *clsidNewSink* parameter is supported.</span></span>

<span data-ttu-id="35c75-113">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="35c75-113">The possible values are.</span></span>

<dt>

<span data-ttu-id="35c75-114">0</span><span class="sxs-lookup"><span data-stu-id="35c75-114">0</span></span>
</dt> <dd>

<span data-ttu-id="35c75-115">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="35c75-115">Not supported</span></span>

</dd> <dt>

<span data-ttu-id="35c75-116">1</span><span class="sxs-lookup"><span data-stu-id="35c75-116">1</span></span>
</dt> <dd>

<span data-ttu-id="35c75-117">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="35c75-117">Supported</span></span>

</dd> </dl>

<span data-ttu-id="35c75-118">Другие значения не определены.</span><span class="sxs-lookup"><span data-stu-id="35c75-118">Other values are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="35c75-119">**клсидневсинк**</span><span class="sxs-lookup"><span data-stu-id="35c75-119">**clsidNewSink**</span></span>
</dt> <dd>

<span data-ttu-id="35c75-120">Приемник, связанный с типом носителя.</span><span class="sxs-lookup"><span data-stu-id="35c75-120">The sink associated with the media type.</span></span>

</dd> <dt>

<span data-ttu-id="35c75-121">**суппортедмедиатипеиндекс**</span><span class="sxs-lookup"><span data-stu-id="35c75-121">**supportedMediaTypeIndex**</span></span>
</dt> <dd>

<span data-ttu-id="35c75-122">Отсчитываемый от нуля индекс типа носителя, поддерживаемого приемником.</span><span class="sxs-lookup"><span data-stu-id="35c75-122">The zero-based index of the media type supported by the sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35c75-123">Требования</span><span class="sxs-lookup"><span data-stu-id="35c75-123">Requirements</span></span>



| <span data-ttu-id="35c75-124">Требование</span><span class="sxs-lookup"><span data-stu-id="35c75-124">Requirement</span></span> | <span data-ttu-id="35c75-125">Значение</span><span class="sxs-lookup"><span data-stu-id="35c75-125">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="35c75-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35c75-126">Minimum supported client</span></span><br/> | <span data-ttu-id="35c75-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="35c75-127">None supported</span></span><br/>         |
| <span data-ttu-id="35c75-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35c75-128">Minimum supported server</span></span><br/> | <span data-ttu-id="35c75-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35c75-129">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35c75-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35c75-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c75-131">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="35c75-131">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="35c75-132">**\_Исходящие \_ данные поддержки тсмф \_**</span><span class="sxs-lookup"><span data-stu-id="35c75-132">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> </dl>

 

 





