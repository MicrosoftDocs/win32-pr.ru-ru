---
description: Указывает, какие выходные данные являются основными выходными данными на узле Tee.
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: Атрибут MF_TOPONODE_PRIMARYOUTPUT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344165"
---
# <a name="mf_toponode_primaryoutput-attribute"></a><span data-ttu-id="dbe6a-103">\_Атрибут MF топоноде \_ PRIMARYOUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbe6a-103">MF\_TOPONODE\_PRIMARYOUTPUT attribute</span></span>

<span data-ttu-id="dbe6a-104">Указывает, какие выходные данные являются основными выходными данными на узле Tee.</span><span class="sxs-lookup"><span data-stu-id="dbe6a-104">Indicates which output is the primary output on a tee node.</span></span>

## <a name="data-type"></a><span data-ttu-id="dbe6a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="dbe6a-105">Data type</span></span>

<span data-ttu-id="dbe6a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dbe6a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dbe6a-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbe6a-107">Remarks</span></span>

<span data-ttu-id="dbe6a-108">Этот атрибут применяется к узлам tee (**\_ \_ \_ узел топологии MF tee**).</span><span class="sxs-lookup"><span data-stu-id="dbe6a-108">This attribute applies to tee nodes (**MF\_TOPOLOGY\_TEE\_NODE**).</span></span>

<span data-ttu-id="dbe6a-109">Значением этого атрибута является отсчитываемый от нуля индекс выходного соединения на этом tee узле.</span><span class="sxs-lookup"><span data-stu-id="dbe6a-109">The value of this attribute is the zero-based index of an output connection on this tee node.</span></span> <span data-ttu-id="dbe6a-110">Это значение указывает, какие выходные данные являются основным выходным потоком.</span><span class="sxs-lookup"><span data-stu-id="dbe6a-110">This value indicates which output is the primary output stream.</span></span> <span data-ttu-id="dbe6a-111">Конвейер ожидает запрос от основного выхода перед обработкой запросов из других выходных данных.</span><span class="sxs-lookup"><span data-stu-id="dbe6a-111">The pipeline waits for a request from the primary output before processing requests from the other outputs.</span></span>

<span data-ttu-id="dbe6a-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="dbe6a-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe6a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="dbe6a-113">Requirements</span></span>



| <span data-ttu-id="dbe6a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="dbe6a-114">Requirement</span></span> | <span data-ttu-id="dbe6a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="dbe6a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe6a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbe6a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe6a-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbe6a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dbe6a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbe6a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe6a-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbe6a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dbe6a-120">Header</span><span class="sxs-lookup"><span data-stu-id="dbe6a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbe6a-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6a-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe6a-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbe6a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe6a-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dbe6a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dbe6a-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="dbe6a-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="dbe6a-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="dbe6a-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="dbe6a-126">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="dbe6a-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="dbe6a-127">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="dbe6a-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




