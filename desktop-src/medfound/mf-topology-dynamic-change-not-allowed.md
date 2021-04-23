---
description: Указывает, пытается ли сеанс мультимедиа изменить топологию при изменении формата потока.
ms.assetid: 8272ded7-9d27-4652-877b-40fc76426ffc
title: Атрибут MF_TOPOLOGY_DYNAMIC_CHANGE_NOT_ALLOWED (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ade7308c4fadef315fae0828a5c2cb29575b03a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497355"
---
# <a name="mf_topology_dynamic_change_not_allowed-attribute"></a><span data-ttu-id="148f5-103">\_Атрибут " \_ Динамическое изменение топологии MF" \_ \_ не \_ разрешен</span><span class="sxs-lookup"><span data-stu-id="148f5-103">MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute</span></span>

<span data-ttu-id="148f5-104">Указывает, пытается ли сеанс мультимедиа изменить топологию при изменении формата потока.</span><span class="sxs-lookup"><span data-stu-id="148f5-104">Specifies whether the Media Session attempts to modify the topology when the format of a stream changes.</span></span>

## <a name="data-type"></a><span data-ttu-id="148f5-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="148f5-105">Data type</span></span>

<span data-ttu-id="148f5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="148f5-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="148f5-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="148f5-107">Get/set</span></span>

<span data-ttu-id="148f5-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="148f5-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="148f5-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="148f5-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="148f5-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="148f5-110">Applies to</span></span>

[<span data-ttu-id="148f5-111">**имфтопологи**</span><span class="sxs-lookup"><span data-stu-id="148f5-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="148f5-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="148f5-112">Remarks</span></span>

<span data-ttu-id="148f5-113">Этот атрибут управляет реакцией сеанса мультимедиа при изменении формата потока во время потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="148f5-113">This attribute controls how the Media Session responds if the format of a stream changes during streaming.</span></span>

<span data-ttu-id="148f5-114">Если в результате изменения формата и \_ атрибута " \_ Динамическое изменение топологии MF" \_ \_ \_ указано **значение false**, сеанс мультимедиа может вставить новые узлы в топологию в соответствии с новым форматом.</span><span class="sxs-lookup"><span data-stu-id="148f5-114">If the format changes and the MF\_TOPOLOGY\_DYNAMIC\_CHANGE\_NOT\_ALLOWED attribute is **FALSE**, the Media Session might insert new nodes into the topology to match the new format.</span></span> <span data-ttu-id="148f5-115">Например, при изменении размера видео сеанс мультимедиа может добавить Media Foundation преобразование (MFT), которое изменяет размер видео.</span><span class="sxs-lookup"><span data-stu-id="148f5-115">For example, if the video size changes, the Media Session might add a Media Foundation transform (MFT) that resizes the video.</span></span> <span data-ttu-id="148f5-116">В противном случае, если атрибут имеет **значение true**, сеанс мультимедиа не изменит топологию.</span><span class="sxs-lookup"><span data-stu-id="148f5-116">Otherwise, if the attribute is **TRUE**, the Media Session will not modify the topology.</span></span>

<span data-ttu-id="148f5-117">Значение этого атрибута по умолчанию равно **false**.</span><span class="sxs-lookup"><span data-stu-id="148f5-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="148f5-118">Рекомендуемое значение — **false**.</span><span class="sxs-lookup"><span data-stu-id="148f5-118">The recommended value is **FALSE**.</span></span>

<span data-ttu-id="148f5-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="148f5-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="148f5-120">Требования</span><span class="sxs-lookup"><span data-stu-id="148f5-120">Requirements</span></span>



| <span data-ttu-id="148f5-121">Требование</span><span class="sxs-lookup"><span data-stu-id="148f5-121">Requirement</span></span> | <span data-ttu-id="148f5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="148f5-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="148f5-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="148f5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="148f5-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="148f5-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="148f5-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="148f5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="148f5-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="148f5-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="148f5-127">Header</span><span class="sxs-lookup"><span data-stu-id="148f5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="148f5-128"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="148f5-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="148f5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="148f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="148f5-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="148f5-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="148f5-131">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="148f5-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




