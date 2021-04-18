---
description: Указывает, может ли конвейер удалять образцы из узла топологии.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: Атрибут MF_TOPONODE_DISCARDABLE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719702"
---
# <a name="mf_toponode_discardable-attribute"></a><span data-ttu-id="1d497-103">\_Атрибут MF топоноде \_</span><span class="sxs-lookup"><span data-stu-id="1d497-103">MF\_TOPONODE\_DISCARDABLE attribute</span></span>

<span data-ttu-id="1d497-104">Указывает, может ли конвейер удалять образцы из узла топологии.</span><span class="sxs-lookup"><span data-stu-id="1d497-104">Specifies whether the pipeline can drop samples from a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="1d497-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1d497-105">Data type</span></span>

<span data-ttu-id="1d497-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="1d497-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="1d497-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1d497-107">Remarks</span></span>

<span data-ttu-id="1d497-108">Этот атрибут применяется ко всем типам узлов.</span><span class="sxs-lookup"><span data-stu-id="1d497-108">This attribute applies to all node types.</span></span> <span data-ttu-id="1d497-109">Обычно этот атрибут устанавливается на узлах tee, чтобы указать, что вторичные выходные данные не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="1d497-109">Typically you would set this attribute on tee nodes, to indicate that the secondary outputs are not essential.</span></span>

<span data-ttu-id="1d497-110">Значение атрибута представляет собой массив индексов для вывода потоков на узле.</span><span class="sxs-lookup"><span data-stu-id="1d497-110">The value of the attribute is an array of indexes to output streams on the node.</span></span>

<span data-ttu-id="1d497-111">Если этот атрибут задан, конвейер может удалить образцы из указанных выходных потоков, если поток не находится позади.</span><span class="sxs-lookup"><span data-stu-id="1d497-111">If this attribute is set, the pipeline might drop samples from the specified output streams, if the stream is falling behind.</span></span>

<span data-ttu-id="1d497-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="1d497-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d497-113">Требования</span><span class="sxs-lookup"><span data-stu-id="1d497-113">Requirements</span></span>



| <span data-ttu-id="1d497-114">Требование</span><span class="sxs-lookup"><span data-stu-id="1d497-114">Requirement</span></span> | <span data-ttu-id="1d497-115">Значение</span><span class="sxs-lookup"><span data-stu-id="1d497-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d497-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d497-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1d497-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d497-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1d497-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d497-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1d497-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1d497-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1d497-120">Header</span><span class="sxs-lookup"><span data-stu-id="1d497-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d497-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d497-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d497-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d497-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d497-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d497-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d497-124">**Имфаттрибутес:: BLOB**</span><span class="sxs-lookup"><span data-stu-id="1d497-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="1d497-125">**Имфаттрибутес:: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="1d497-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="1d497-126">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="1d497-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="1d497-127">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="1d497-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




