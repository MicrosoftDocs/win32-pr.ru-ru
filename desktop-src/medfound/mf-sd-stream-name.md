---
description: Содержит имя потока.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: Атрибут MF_SD_STREAM_NAME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734c2d20390ba1a450a40c03054b4c67c5c0409a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349122"
---
# <a name="mf_sd_stream_name-attribute"></a><span data-ttu-id="67fc3-103">\_ \_ Атрибут имени потока MF SD \_</span><span class="sxs-lookup"><span data-stu-id="67fc3-103">MF\_SD\_STREAM\_NAME attribute</span></span>

<span data-ttu-id="67fc3-104">Содержит имя потока.</span><span class="sxs-lookup"><span data-stu-id="67fc3-104">Contains the name of a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="67fc3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="67fc3-105">Data type</span></span>

<span data-ttu-id="67fc3-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="67fc3-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="67fc3-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="67fc3-107">Get/set</span></span>

<span data-ttu-id="67fc3-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="67fc3-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="67fc3-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="67fc3-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="67fc3-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="67fc3-110">Applies to</span></span>

[<span data-ttu-id="67fc3-111">**имфстреамдескриптор**</span><span class="sxs-lookup"><span data-stu-id="67fc3-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="67fc3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="67fc3-112">Remarks</span></span>

<span data-ttu-id="67fc3-113">Источник AVI Media устанавливает этот атрибут, если AVI-файл содержит фрагмент «стрн».</span><span class="sxs-lookup"><span data-stu-id="67fc3-113">The AVI media source sets this attribute if the AVI file contains a 'strn' chunk.</span></span>

<span data-ttu-id="67fc3-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="67fc3-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="67fc3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="67fc3-115">Requirements</span></span>



| <span data-ttu-id="67fc3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="67fc3-116">Requirement</span></span> | <span data-ttu-id="67fc3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="67fc3-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67fc3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67fc3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="67fc3-119">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="67fc3-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="67fc3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67fc3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="67fc3-121">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="67fc3-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="67fc3-122">Header</span><span class="sxs-lookup"><span data-stu-id="67fc3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="67fc3-123"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="67fc3-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67fc3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="67fc3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67fc3-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="67fc3-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="67fc3-126">Атрибуты дескриптора потока</span><span class="sxs-lookup"><span data-stu-id="67fc3-126">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




