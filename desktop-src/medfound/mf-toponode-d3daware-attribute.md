---
description: Указывает, поддерживает ли преобразование, связанное с узлом топологии, поддержку ускорения видео DirectX (ДКСВА).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: Атрибут MF_TOPONODE_D3DAWARE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498111"
---
# <a name="mf_toponode_d3daware-attribute"></a><span data-ttu-id="7f687-103">\_Атрибут MF топоноде \_ D3DAWARE</span><span class="sxs-lookup"><span data-stu-id="7f687-103">MF\_TOPONODE\_D3DAWARE attribute</span></span>

<span data-ttu-id="7f687-104">Указывает, поддерживает ли преобразование, связанное с узлом топологии, поддержку ускорения видео DirectX (ДКСВА).</span><span class="sxs-lookup"><span data-stu-id="7f687-104">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA).</span></span>

## <a name="data-type"></a><span data-ttu-id="7f687-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7f687-105">Data type</span></span>

<span data-ttu-id="7f687-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7f687-106">**UINT32**</span></span>

<span data-ttu-id="7f687-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="7f687-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f687-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f687-108">Remarks</span></span>

<span data-ttu-id="7f687-109">Этот атрибут применяется к узлам преобразования (**\_ \_ \_ узел преобразования топологии MF**).</span><span class="sxs-lookup"><span data-stu-id="7f687-109">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="7f687-110">Обычно приложения не используют этот атрибут напрямую.</span><span class="sxs-lookup"><span data-stu-id="7f687-110">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="7f687-111">Сеанс мультимедиа задает этот атрибут на узле преобразования, если в базовом преобразовании Media Foundation имеется атрибут [**MF \_ SA с \_ \_ поддержкой D3D**](mf-sa-d3d-aware-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="7f687-111">The Media Session sets this attribute on a transform node if the underlying Media Foundation transform has the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute.</span></span>

<span data-ttu-id="7f687-112">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="7f687-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f687-113">Требования</span><span class="sxs-lookup"><span data-stu-id="7f687-113">Requirements</span></span>



| <span data-ttu-id="7f687-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7f687-114">Requirement</span></span> | <span data-ttu-id="7f687-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7f687-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f687-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f687-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7f687-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f687-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7f687-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f687-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7f687-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f687-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7f687-120">Header</span><span class="sxs-lookup"><span data-stu-id="7f687-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f687-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f687-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f687-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f687-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f687-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f687-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f687-124">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="7f687-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7f687-125">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7f687-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7f687-126">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="7f687-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="7f687-127">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="7f687-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




