---
description: Указывает, включает ли загрузчик топологии ускорение видео Microsoft DirectX (ДКСВА) в топологии.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: Атрибут MF_TOPOLOGY_DXVA_MODE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701465"
---
# <a name="mf_topology_dxva_mode-attribute"></a><span data-ttu-id="79780-103">\_ \_ Атрибут режима ДКСВА топологии MF \_</span><span class="sxs-lookup"><span data-stu-id="79780-103">MF\_TOPOLOGY\_DXVA\_MODE attribute</span></span>

<span data-ttu-id="79780-104">Указывает, включает ли загрузчик топологии ускорение видео Microsoft DirectX (ДКСВА) в топологии.</span><span class="sxs-lookup"><span data-stu-id="79780-104">Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="79780-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="79780-105">Data type</span></span>

<span data-ttu-id="79780-106">**[**Мфтопологи \_ \_Режим дксва**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** , хранящийся как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="79780-106">**[**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="79780-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="79780-107">Get/set</span></span>

<span data-ttu-id="79780-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="79780-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="79780-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="79780-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="79780-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="79780-110">Applies to</span></span>

[<span data-ttu-id="79780-111">**имфтопологи**</span><span class="sxs-lookup"><span data-stu-id="79780-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="79780-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79780-112">Remarks</span></span>

<span data-ttu-id="79780-113">Значением этого атрибута является константа перечисления [**мфтопологи \_ дксва \_ mode**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) .</span><span class="sxs-lookup"><span data-stu-id="79780-113">The value of this attribute is an [**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) enumeration constant.</span></span> <span data-ttu-id="79780-114">Значение по умолчанию — **мфтопологи \_ дксва \_ по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="79780-114">The default value is **MFTOPOLOGY\_DXVA\_DEFAULT**.</span></span>

<span data-ttu-id="79780-115">Этот атрибут определяет, какой МФТС получает указатель на диспетчер устройств Direct3D.</span><span class="sxs-lookup"><span data-stu-id="79780-115">This attribute controls which MFTs receive a pointer to the Direct3D device manager.</span></span> <span data-ttu-id="79780-116">Чтобы включить полное ускорение видео, присвойте параметру значение **мфтопологи \_ дксва \_ Full**.</span><span class="sxs-lookup"><span data-stu-id="79780-116">To enable full video acceleration, set the value to **MFTOPOLOGY\_DXVA\_FULL**.</span></span> <span data-ttu-id="79780-117">Значение **мфтопологи \_ дксва \_ по умолчанию** определено для обеспечения обратной совместимости. оно соответствует поведению всех более ранних версий Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="79780-117">The value **MFTOPOLOGY\_DXVA\_DEFAULT** is defined for backward compatibility; it matches the behavior of all earlier versions of Microsoft Media Foundation.</span></span>

<span data-ttu-id="79780-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="79780-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="79780-119">Требования</span><span class="sxs-lookup"><span data-stu-id="79780-119">Requirements</span></span>



| <span data-ttu-id="79780-120">Требование</span><span class="sxs-lookup"><span data-stu-id="79780-120">Requirement</span></span> | <span data-ttu-id="79780-121">Значение</span><span class="sxs-lookup"><span data-stu-id="79780-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79780-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79780-122">Minimum supported client</span></span><br/> | <span data-ttu-id="79780-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="79780-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="79780-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79780-124">Minimum supported server</span></span><br/> | <span data-ttu-id="79780-125">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="79780-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="79780-126">Header</span><span class="sxs-lookup"><span data-stu-id="79780-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="79780-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="79780-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79780-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79780-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79780-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79780-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="79780-130">диспетчер устройств Direct3D</span><span class="sxs-lookup"><span data-stu-id="79780-130">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="79780-131">Атрибуты топологии</span><span class="sxs-lookup"><span data-stu-id="79780-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




