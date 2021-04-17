---
title: Структура TSMF_SUPPORT_NODEDATA_IN
description: Используется в \_ данных поддержки тсмф \_ \_ в структуре для хранения сведений о поддерживаемых форматах мультимедиа.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN структуры службы удаленных рабочих столов
- PTSMF_SUPPORT_NODEDATA_IN службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681918"
---
# <a name="tsmf_support_nodedata_in-structure"></a><span data-ttu-id="92e3f-105">\_Нодедата поддержки \_ тсмф \_ в структуре</span><span class="sxs-lookup"><span data-stu-id="92e3f-105">TSMF\_SUPPORT\_NODEDATA\_IN structure</span></span>

<span data-ttu-id="92e3f-106">Используется в [**\_ данных поддержки тсмф \_ \_ в**](tsmf-support-data-in.md) структуре для хранения сведений о поддерживаемых форматах мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="92e3f-106">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="92e3f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92e3f-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a><span data-ttu-id="92e3f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="92e3f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="92e3f-109">**byteCount**</span><span class="sxs-lookup"><span data-stu-id="92e3f-109">**byteCount**</span></span>
</dt> <dd>

<span data-ttu-id="92e3f-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="92e3f-110">The size of the structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="92e3f-111">**nodeId**</span><span class="sxs-lookup"><span data-stu-id="92e3f-111">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="92e3f-112">Узел.</span><span class="sxs-lookup"><span data-stu-id="92e3f-112">The node.</span></span>

</dd> <dt>

<span data-ttu-id="92e3f-113">**нуммедиатипес**</span><span class="sxs-lookup"><span data-stu-id="92e3f-113">**numMediaTypes**</span></span>
</dt> <dd>

<span data-ttu-id="92e3f-114">Число структур формата мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="92e3f-114">The number of media format structures.</span></span>

</dd> <dt>

<span data-ttu-id="92e3f-115">**...**</span><span class="sxs-lookup"><span data-stu-id="92e3f-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="92e3f-116">Переменное число структур, определяющих форматы аудио-или видеоклипа.</span><span class="sxs-lookup"><span data-stu-id="92e3f-116">A variable number of structures defining audio or video media formats.</span></span> <span data-ttu-id="92e3f-117">**Форматтипе** может иметь **Формат \_ Вавеформатекс** для аудио или **формата \_ мфвидеоформат** для видео.</span><span class="sxs-lookup"><span data-stu-id="92e3f-117">The **FormatType** is either **FORMAT\_WaveFormatEx** for audio or **FORMAT\_MFVideoFormat** for video.</span></span>

<span data-ttu-id="92e3f-118">Дополнительные сведения об этой структуре см. в разделе [TS \_ AM \_ Media \_ Type Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span><span class="sxs-lookup"><span data-stu-id="92e3f-118">For details of this structure, see [TS\_AM\_MEDIA\_TYPE Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92e3f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="92e3f-119">Requirements</span></span>



| <span data-ttu-id="92e3f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="92e3f-120">Requirement</span></span> | <span data-ttu-id="92e3f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="92e3f-121">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="92e3f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92e3f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="92e3f-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="92e3f-123">None supported</span></span><br/>         |
| <span data-ttu-id="92e3f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92e3f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="92e3f-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="92e3f-125">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92e3f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92e3f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e3f-127">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="92e3f-127">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="92e3f-128">**ТСМФ \_ Поддержка \_ данных \_ в**</span><span class="sxs-lookup"><span data-stu-id="92e3f-128">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> </dl>

 

