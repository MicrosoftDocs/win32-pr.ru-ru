---
description: Задает смещение для границ полезных данных в кадре для защищенных выборок.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: Атрибут MFSampleExtension_PacketCrossOffsets (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416f41fef9caab3d73c2bdd015d345452ccbd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719423"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a><span data-ttu-id="d2641-103">Мфсампликстенсион \_ паккеткроссоффсетс, атрибут</span><span class="sxs-lookup"><span data-stu-id="d2641-103">MFSampleExtension\_PacketCrossOffsets attribute</span></span>

<span data-ttu-id="d2641-104">Задает смещение для границ полезных данных в кадре для защищенных выборок.</span><span class="sxs-lookup"><span data-stu-id="d2641-104">Specifies the offsets to the payload boundaries in a frame for protected samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="d2641-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d2641-105">Data type</span></span>

<span data-ttu-id="d2641-106">массив байтов;</span><span class="sxs-lookup"><span data-stu-id="d2641-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="d2641-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="d2641-107">Get/set</span></span>

<span data-ttu-id="d2641-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="d2641-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="d2641-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="d2641-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d2641-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="d2641-110">Applies to</span></span>

[<span data-ttu-id="d2641-111">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="d2641-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="d2641-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2641-112">Remarks</span></span>

<span data-ttu-id="d2641-113">Этот атрибут применяется к примерам мультимедиа, защищенным цифровыми Rights Management Windows Media (DRM).</span><span class="sxs-lookup"><span data-stu-id="d2641-113">This attribute applies to media samples protected by Windows Media Digital Rights Management (DRM).</span></span> <span data-ttu-id="d2641-114">Значение атрибута является массивом **DWORD** s.</span><span class="sxs-lookup"><span data-stu-id="d2641-114">The value of the attribute is an array of **DWORD** s.</span></span> <span data-ttu-id="d2641-115">Каждая запись в массиве является смещением границы полезной нагрузки относительно начала кадра.</span><span class="sxs-lookup"><span data-stu-id="d2641-115">Each entry in the array is the offset of a payload boundary, relative to the start of the frame.</span></span> <span data-ttu-id="d2641-116">Приложение может использовать эти значения при расшифровке и перестроении кадров.</span><span class="sxs-lookup"><span data-stu-id="d2641-116">An application can use these values when decrypting and reconstructing the frames.</span></span>

<span data-ttu-id="d2641-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="d2641-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2641-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d2641-118">Requirements</span></span>



| <span data-ttu-id="d2641-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d2641-119">Requirement</span></span> | <span data-ttu-id="d2641-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d2641-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2641-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2641-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d2641-122">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="d2641-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="d2641-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2641-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d2641-124">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="d2641-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d2641-125">Header</span><span class="sxs-lookup"><span data-stu-id="d2641-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2641-126"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2641-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2641-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2641-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2641-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d2641-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d2641-129">Разделитель ASF</span><span class="sxs-lookup"><span data-stu-id="d2641-129">ASF Splitter</span></span>](asf-splitter.md)
</dt> <dt>

[<span data-ttu-id="d2641-130">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="d2641-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="d2641-131">Примеры носителей</span><span class="sxs-lookup"><span data-stu-id="d2641-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




