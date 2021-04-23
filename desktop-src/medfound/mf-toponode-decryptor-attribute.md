---
description: Указывает, является ли базовый объект топологии узлами дешифрованием.
ms.assetid: 211789d8-5e51-485c-b8f1-cd0ae3e39250
title: Атрибут MF_TOPONODE_DECRYPTOR (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a8129e82fc2ebc01ee8cf21aabda77dc26970e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703077"
---
# <a name="mf_toponode_decryptor-attribute"></a><span data-ttu-id="fdbf0-103">\_ \_ Атрибут расшифровки MF топоноде</span><span class="sxs-lookup"><span data-stu-id="fdbf0-103">MF\_TOPONODE\_DECRYPTOR attribute</span></span>

<span data-ttu-id="fdbf0-104">Указывает, является ли базовый объект узла топологии расшифровывается.</span><span class="sxs-lookup"><span data-stu-id="fdbf0-104">Specifies whether a toplogy node's underlying object is a decrypter.</span></span>

## <a name="data-type"></a><span data-ttu-id="fdbf0-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fdbf0-105">Data type</span></span>

<span data-ttu-id="fdbf0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fdbf0-106">**UINT32**</span></span>

<span data-ttu-id="fdbf0-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="fdbf0-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdbf0-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fdbf0-108">Remarks</span></span>

<span data-ttu-id="fdbf0-109">Этот атрибут применяется ко всем типам узлов.</span><span class="sxs-lookup"><span data-stu-id="fdbf0-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="fdbf0-110">Если значение этого атрибута не равно нулю, то базовый объект узла является расшифрованным.</span><span class="sxs-lookup"><span data-stu-id="fdbf0-110">If the value of this attribute is nonzero, the node's underlying object is a decrypter.</span></span>

<span data-ttu-id="fdbf0-111">Обычно приложения не используют этот атрибут напрямую.</span><span class="sxs-lookup"><span data-stu-id="fdbf0-111">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="fdbf0-112">Сеанс мультимедиа задает этот атрибут при создании узла для расшифровки, полученного из метода [**имфинпуттрустаусорити::-дешифратора**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) .</span><span class="sxs-lookup"><span data-stu-id="fdbf0-112">The Media Session sets this attribute when it creates a node for a decrypter, obtained from the [**IMFInputTrustAuthority::GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) method.</span></span>

<span data-ttu-id="fdbf0-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="fdbf0-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdbf0-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fdbf0-114">Requirements</span></span>



| <span data-ttu-id="fdbf0-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fdbf0-115">Requirement</span></span> | <span data-ttu-id="fdbf0-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fdbf0-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fdbf0-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdbf0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fdbf0-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fdbf0-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fdbf0-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdbf0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fdbf0-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fdbf0-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fdbf0-121">Header</span><span class="sxs-lookup"><span data-stu-id="fdbf0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdbf0-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdbf0-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fdbf0-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdbf0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdbf0-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fdbf0-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fdbf0-125">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="fdbf0-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="fdbf0-126">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="fdbf0-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="fdbf0-127">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="fdbf0-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="fdbf0-128">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="fdbf0-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




