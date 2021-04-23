---
description: Указывает, является ли поток взаимоисключающим с другими потоками того же типа.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: Атрибут MF_SD_MUTUALLY_EXCLUSIVE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712399"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a><span data-ttu-id="866ee-103">\_Атрибут, \_ \_ взаимоисключающий MF SD</span><span class="sxs-lookup"><span data-stu-id="866ee-103">MF\_SD\_MUTUALLY\_EXCLUSIVE attribute</span></span>

<span data-ttu-id="866ee-104">Указывает, является ли поток взаимоисключающим с другими потоками того же типа.</span><span class="sxs-lookup"><span data-stu-id="866ee-104">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span>

## <a name="data-type"></a><span data-ttu-id="866ee-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="866ee-105">Data type</span></span>

<span data-ttu-id="866ee-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="866ee-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="866ee-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="866ee-107">Get/set</span></span>

<span data-ttu-id="866ee-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="866ee-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="866ee-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="866ee-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="866ee-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="866ee-110">Applies to</span></span>

[<span data-ttu-id="866ee-111">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="866ee-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="866ee-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="866ee-112">Remarks</span></span>

<span data-ttu-id="866ee-113">Если этот атрибут имеет **значение true** (отличное от нуля), поток является взаимоисключающим с другими потоками того же типа, например аудио или видео, в той же презентации.</span><span class="sxs-lookup"><span data-stu-id="866ee-113">If this attribute is **TRUE** (nonzero), the stream is mutually exclusive with other streams of the same type, such as audio or video, within the same presentation.</span></span> <span data-ttu-id="866ee-114">Например, если AVI-файл содержит несколько звуковых потоков, они помечаются как взаимоисключающие, так как только один звуковой поток должен воспроизводиться за один раз.</span><span class="sxs-lookup"><span data-stu-id="866ee-114">For example, if an AVI file contains multiple audio streams, they are marked as mutually exclusive, because only one audio stream should be played at one time.</span></span>

<span data-ttu-id="866ee-115">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="866ee-115">The default value is **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="866ee-116">Этот атрибут не используется для файлов ASF, которые имеют более сложный способ представления условий взаимного исключения.</span><span class="sxs-lookup"><span data-stu-id="866ee-116">This attribute is not used for Advanced Systems Format (ASF) files, which have a more sophisticated way to represent mutual exclusion criteria.</span></span> <span data-ttu-id="866ee-117">Дополнительные сведения см. в разделе [**имфасфмутуалексклусион**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="866ee-117">For more information, see [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span></span>

 

<span data-ttu-id="866ee-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="866ee-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="866ee-119">Требования</span><span class="sxs-lookup"><span data-stu-id="866ee-119">Requirements</span></span>



| <span data-ttu-id="866ee-120">Требование</span><span class="sxs-lookup"><span data-stu-id="866ee-120">Requirement</span></span> | <span data-ttu-id="866ee-121">Значение</span><span class="sxs-lookup"><span data-stu-id="866ee-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="866ee-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="866ee-122">Minimum supported client</span></span><br/> | <span data-ttu-id="866ee-123">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="866ee-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="866ee-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="866ee-124">Minimum supported server</span></span><br/> | <span data-ttu-id="866ee-125">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="866ee-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="866ee-126">Header</span><span class="sxs-lookup"><span data-stu-id="866ee-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="866ee-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="866ee-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="866ee-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="866ee-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="866ee-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="866ee-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="866ee-130">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="866ee-130">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




