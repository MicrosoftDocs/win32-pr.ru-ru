---
description: Указывает, является ли базовый объект узлов топологии декодером.
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: Атрибут MF_TOPONODE_DECODER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab16d14a91608fb6b21c901e3fb055ce5e4dfbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272379"
---
# <a name="mf_toponode_decoder-attribute"></a><span data-ttu-id="35f07-103">\_ \_ Атрибут декодера MF топоноде</span><span class="sxs-lookup"><span data-stu-id="35f07-103">MF\_TOPONODE\_DECODER attribute</span></span>

<span data-ttu-id="35f07-104">Указывает, является ли базовый объект узла топологии декодером.</span><span class="sxs-lookup"><span data-stu-id="35f07-104">Specifies whether a topology node's underlying object is a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="35f07-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="35f07-105">Data type</span></span>

<span data-ttu-id="35f07-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="35f07-106">**UINT32**</span></span>

<span data-ttu-id="35f07-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="35f07-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35f07-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35f07-108">Remarks</span></span>

<span data-ttu-id="35f07-109">Этот атрибут применяется ко всем типам узлов.</span><span class="sxs-lookup"><span data-stu-id="35f07-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="35f07-110">Если значение этого атрибута не равно нулю, то базовый объект узла является декодером.</span><span class="sxs-lookup"><span data-stu-id="35f07-110">If the value of this attribute is nonzero, the node's underlying object is a decoder.</span></span>

<span data-ttu-id="35f07-111">Загрузчик топологии задает этот атрибут при создании узла декодера.</span><span class="sxs-lookup"><span data-stu-id="35f07-111">The topology loader sets this attribute when it creates a decoder node.</span></span> <span data-ttu-id="35f07-112">Приложение должно установить этот атрибут, если приложение вручную добавляет декодер в топологию.</span><span class="sxs-lookup"><span data-stu-id="35f07-112">An application should set this attribute if the application manually adds a decoder to the topology.</span></span>

<span data-ttu-id="35f07-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="35f07-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="35f07-114">Требования</span><span class="sxs-lookup"><span data-stu-id="35f07-114">Requirements</span></span>



| <span data-ttu-id="35f07-115">Требование</span><span class="sxs-lookup"><span data-stu-id="35f07-115">Requirement</span></span> | <span data-ttu-id="35f07-116">Значение</span><span class="sxs-lookup"><span data-stu-id="35f07-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35f07-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35f07-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35f07-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35f07-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="35f07-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35f07-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35f07-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35f07-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="35f07-121">Header</span><span class="sxs-lookup"><span data-stu-id="35f07-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="35f07-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="35f07-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f07-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35f07-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f07-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35f07-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="35f07-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="35f07-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="35f07-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="35f07-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="35f07-127">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="35f07-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="35f07-128">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="35f07-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




