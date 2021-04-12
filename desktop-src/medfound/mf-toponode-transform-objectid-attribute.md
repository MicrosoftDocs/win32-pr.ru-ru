---
description: Идентификатор класса (CLSID) преобразования Media Foundation (MFT), связанного с этим узлом топологии.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: Атрибут MF_TOPONODE_TRANSFORM_OBJECTID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543250"
---
# <a name="mf_toponode_transform_objectid-attribute"></a><span data-ttu-id="b8866-103">\_ \_ Атрибут ObjectID преобразования топоноде MF \_</span><span class="sxs-lookup"><span data-stu-id="b8866-103">MF\_TOPONODE\_TRANSFORM\_OBJECTID attribute</span></span>

<span data-ttu-id="b8866-104">Идентификатор класса (CLSID) преобразования Media Foundation (MFT), связанного с этим узлом топологии.</span><span class="sxs-lookup"><span data-stu-id="b8866-104">The class identifier (CLSID) of the Media Foundation transform (MFT) associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="b8866-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b8866-105">Data type</span></span>

<span data-ttu-id="b8866-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b8866-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b8866-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8866-107">Remarks</span></span>

<span data-ttu-id="b8866-108">Этот атрибут применяется к узлам преобразования (**\_ \_ \_ узел преобразования топологии MF**).</span><span class="sxs-lookup"><span data-stu-id="b8866-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="b8866-109">Приложения могут использовать этот атрибут для инициализации узла, производного от.</span><span class="sxs-lookup"><span data-stu-id="b8866-109">Applications can use this attribute to initialize a transfrom node.</span></span> <span data-ttu-id="b8866-110">Если задать этот атрибут, не нужно вызывать [**имфтопологиноде:: setObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) с указателем на таблицу MFT или объект активации.</span><span class="sxs-lookup"><span data-stu-id="b8866-110">If you set this attribute, you do not have to call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) with a pointer to an MFT or activation object.</span></span> <span data-ttu-id="b8866-111">И наоборот, при вызове **setObject** не нужно задавать этот атрибут.</span><span class="sxs-lookup"><span data-stu-id="b8866-111">Conversely, if you call **SetObject**, you do not need to set this attribute.</span></span> <span data-ttu-id="b8866-112">Дополнительные сведения см. в разделе [Создание топологий](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="b8866-112">For more information, see [Creating Topologies](creating-topologies.md).</span></span>

<span data-ttu-id="b8866-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="b8866-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8866-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b8866-114">Requirements</span></span>



| <span data-ttu-id="b8866-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b8866-115">Requirement</span></span> | <span data-ttu-id="b8866-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b8866-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8866-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8866-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b8866-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8866-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b8866-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8866-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b8866-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8866-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b8866-121">Header</span><span class="sxs-lookup"><span data-stu-id="b8866-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8866-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8866-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8866-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8866-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8866-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b8866-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b8866-125">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="b8866-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="b8866-126">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="b8866-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="b8866-127">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="b8866-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b8866-128">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b8866-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b8866-129">Создание топологий</span><span class="sxs-lookup"><span data-stu-id="b8866-129">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="b8866-130">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="b8866-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




