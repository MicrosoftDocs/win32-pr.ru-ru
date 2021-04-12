---
description: Указывает, имеют ли звуковые потоки в презентации переменную скорость.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: Атрибут MF_PD_AUDIO_ISVARIABLEBITRATE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a34d3dd64f9100050dc9aae37e811d00c9d58af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265358"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a><span data-ttu-id="dba08-103">\_ \_ Атрибут аудиоподсистемы MF PD Audio \_ исвариаблебитрате</span><span class="sxs-lookup"><span data-stu-id="dba08-103">MF\_PD\_AUDIO\_ISVARIABLEBITRATE attribute</span></span>

<span data-ttu-id="dba08-104">Указывает, имеют ли звуковые потоки в презентации переменную скорость.</span><span class="sxs-lookup"><span data-stu-id="dba08-104">Specifies whether the audio streams in a presentation have a variable bit rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="dba08-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="dba08-105">Data type</span></span>

<span data-ttu-id="dba08-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dba08-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="dba08-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="dba08-107">Get/set</span></span>

<span data-ttu-id="dba08-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="dba08-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="dba08-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="dba08-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="dba08-110">Применение</span><span class="sxs-lookup"><span data-stu-id="dba08-110">Applies To</span></span>

[<span data-ttu-id="dba08-111">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="dba08-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="dba08-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dba08-112">Remarks</span></span>

<span data-ttu-id="dba08-113">Это необязательный атрибут для дескрипторов представления.</span><span class="sxs-lookup"><span data-stu-id="dba08-113">This is an optional attribute for presentation descriptors.</span></span> <span data-ttu-id="dba08-114">Если атрибут имеет **значение true** (не равно нулю), то в презентации содержится по крайней мере один звуковой поток с переменной СКОРОСТЬЮ (VBR).</span><span class="sxs-lookup"><span data-stu-id="dba08-114">If the attribute is **TRUE** (nonzero), the presentation contains at least one variable-bit-rate (VBR) audio stream.</span></span> <span data-ttu-id="dba08-115">Если атрибут имеет **значение false**, то все звуковые потоки имеют постоянную скорость.</span><span class="sxs-lookup"><span data-stu-id="dba08-115">If the attribute is **FALSE**, all of the audio streams have a constant bit rate.</span></span>

<span data-ttu-id="dba08-116">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="dba08-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="dba08-117">Требования</span><span class="sxs-lookup"><span data-stu-id="dba08-117">Requirements</span></span>



| <span data-ttu-id="dba08-118">Требование</span><span class="sxs-lookup"><span data-stu-id="dba08-118">Requirement</span></span> | <span data-ttu-id="dba08-119">Значение</span><span class="sxs-lookup"><span data-stu-id="dba08-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dba08-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dba08-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dba08-121">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="dba08-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="dba08-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dba08-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dba08-123">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="dba08-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="dba08-124">Header</span><span class="sxs-lookup"><span data-stu-id="dba08-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dba08-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="dba08-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dba08-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dba08-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dba08-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dba08-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="dba08-128">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="dba08-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




