---
description: Указывает, использует ли источник аппаратного устройства Системное время для меток времени.
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: Атрибут MFT_HW_TIMESTAMP_WITH_QPC_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f6f7d50db89e99e76e7b7ea509f444c3998bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692790"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a><span data-ttu-id="03a3b-103">\_ \_ Метка времени в MFT HW \_ с \_ \_ атрибутом атрибута QPC</span><span class="sxs-lookup"><span data-stu-id="03a3b-103">MFT\_HW\_TIMESTAMP\_WITH\_QPC\_Attribute attribute</span></span>

<span data-ttu-id="03a3b-104">Указывает, использует ли источник аппаратного устройства Системное время для меток времени.</span><span class="sxs-lookup"><span data-stu-id="03a3b-104">Specifies whether a hardware device source uses the system time for time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="03a3b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="03a3b-105">Data type</span></span>

<span data-ttu-id="03a3b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="03a3b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="03a3b-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="03a3b-107">Get/set</span></span>

<span data-ttu-id="03a3b-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="03a3b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="03a3b-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="03a3b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="03a3b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03a3b-110">Remarks</span></span>

<span data-ttu-id="03a3b-111">Если этот атрибут имеет **значение true**, источник устройства использует системное время, возвращаемое **QueryPerformanceCounter**, для меток времени.</span><span class="sxs-lookup"><span data-stu-id="03a3b-111">If this attribute is **TRUE**, the device source uses the system time, as returned by the **QueryPerformanceCounter**, for time stamps.</span></span> <span data-ttu-id="03a3b-112">В противном случае источник устройства использует часы устройства.</span><span class="sxs-lookup"><span data-stu-id="03a3b-112">Otherwise, the device source uses the device's clock.</span></span> <span data-ttu-id="03a3b-113">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="03a3b-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="03a3b-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="03a3b-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="03a3b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="03a3b-115">Requirements</span></span>



| <span data-ttu-id="03a3b-116">Требование</span><span class="sxs-lookup"><span data-stu-id="03a3b-116">Requirement</span></span> | <span data-ttu-id="03a3b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="03a3b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="03a3b-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03a3b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="03a3b-119">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="03a3b-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="03a3b-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03a3b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="03a3b-121">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="03a3b-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="03a3b-122">Header</span><span class="sxs-lookup"><span data-stu-id="03a3b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="03a3b-123"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="03a3b-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03a3b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03a3b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a3b-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="03a3b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="03a3b-126">Запись атрибутов устройства</span><span class="sxs-lookup"><span data-stu-id="03a3b-126">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




