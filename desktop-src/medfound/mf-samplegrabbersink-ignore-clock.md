---
description: Указывает, использует ли приемник выборочного захвата часы презентации для планирования образцов.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: Атрибут MF_SAMPLEGRABBERSINK_IGNORE_CLOCK (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712252"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a><span data-ttu-id="b0e4e-103">\_ \_ Атрибут часов пропуска MF самплеграбберсинк \_</span><span class="sxs-lookup"><span data-stu-id="b0e4e-103">MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute</span></span>

<span data-ttu-id="b0e4e-104">Указывает, использует ли приемник выборочного захвата часы презентации для планирования образцов.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-104">Specifies whether the sample-grabber sink uses the presentation clock to schedule samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="b0e4e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b0e4e-105">Data type</span></span>

<span data-ttu-id="b0e4e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b0e4e-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b0e4e-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="b0e4e-107">Get/set</span></span>

<span data-ttu-id="b0e4e-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b0e4e-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b0e4e-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b0e4e-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e4e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b0e4e-110">Remarks</span></span>

<span data-ttu-id="b0e4e-111">Этот атрибут можно задать для объекта активации, созданного функцией [**мфкреатесамплеграбберсинкактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="b0e4e-111">You can set this attribute on the activation object created by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="b0e4e-112">Задайте атрибут перед вызовом метода [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) для объекта активации.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-112">Set the attribute before calling the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method on the activation object.</span></span>

<span data-ttu-id="b0e4e-113">По умолчанию, когда приемник выборки получает пример, он ждет, пока время презентации примера не вызовет обратный вызов приложения.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-113">By default, when the sample-grabber sink receives a sample, it waits until the presentation time of the sample to invoke the application's callback.</span></span> <span data-ttu-id="b0e4e-114">Если атрибут MF \_ самплеграбберсинк \_ Ignore \_ не равен нулю, приемник выборки игнорирует часы презентации и вызывает обратный вызов, как только он получает каждый пример.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-114">If the MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute is nonzero, the sample-grabber sink ignores the presentation clock and invokes the callback as soon as it receives each sample.</span></span>

<span data-ttu-id="b0e4e-115">Рекомендуемое использование:</span><span class="sxs-lookup"><span data-stu-id="b0e4e-115">Recommended usage:</span></span>

-   <span data-ttu-id="b0e4e-116">Если требуется как можно быстрее обрабатывать примеры, установите для этого атрибута **значение true**.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-116">If you want to process samples as quickly as possible, set this attribute to **TRUE**.</span></span>
-   <span data-ttu-id="b0e4e-117">Если нужно, чтобы вызовы метода обратного вызова синхронизировались с часами, не устанавливайте этот атрибут или присвойте ему значение **false**.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-117">If you want the calls to the callback method to be synchronized with the clock, either do not set this attribute or set it to **FALSE**.</span></span> <span data-ttu-id="b0e4e-118">Вы можете получить образцы несколько раз в часы, сохраняя их синхронизацию, установив атрибут [**\_ \_ \_ \_ смещения Самплеграбберсинк выборки**](mf-samplegrabbersink-sample-time-offset-attribute.md) в формате MF.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-118">You can get samples slightly ahead of the clock, while still remaining synchronized, by setting the [**MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET**](mf-samplegrabbersink-sample-time-offset-attribute.md) attribute.</span></span>

<span data-ttu-id="b0e4e-119">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="b0e4e-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e4e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b0e4e-120">Requirements</span></span>



| <span data-ttu-id="b0e4e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b0e4e-121">Requirement</span></span> | <span data-ttu-id="b0e4e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b0e4e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e4e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b0e4e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e4e-124">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b0e4e-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b0e4e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b0e4e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e4e-126">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0e4e-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b0e4e-127">Header</span><span class="sxs-lookup"><span data-stu-id="b0e4e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e4e-128"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e4e-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0e4e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0e4e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e4e-130">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0e4e-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b0e4e-131">Атрибуты Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b0e4e-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




