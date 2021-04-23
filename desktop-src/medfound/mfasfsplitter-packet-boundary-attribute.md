---
description: Указывает, содержит ли буфер начало пакета расширенного системного формата (ASF).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: Атрибут MFASFSPLITTER_PACKET_BOUNDARY (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 044fd3ed635dc7cb45db1cb9e5c480481b06cd31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647204"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a><span data-ttu-id="402b6-103">\_ \_ Атрибут границы пакета мфасфсплиттер</span><span class="sxs-lookup"><span data-stu-id="402b6-103">MFASFSPLITTER\_PACKET\_BOUNDARY attribute</span></span>

<span data-ttu-id="402b6-104">Указывает, содержит ли буфер начало пакета расширенного системного формата (ASF).</span><span class="sxs-lookup"><span data-stu-id="402b6-104">Specifies whether a buffer contains the start of an Advanced Systems Format (ASF) packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="402b6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="402b6-105">Data type</span></span>

<span data-ttu-id="402b6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="402b6-106">**UINT32**</span></span>

<span data-ttu-id="402b6-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="402b6-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="402b6-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="402b6-108">Remarks</span></span>

<span data-ttu-id="402b6-109">Если буфер мультимедиа предоставляет интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) через **QueryInterface**, а значение этого атрибута не равно нулю, разделитель ASF рассматривает буфер как начало нового пакета.</span><span class="sxs-lookup"><span data-stu-id="402b6-109">If a media buffer exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface through **QueryInterface**, and the value of this attribute is nonzero, the ASF splitter treats the buffer as the start of a new packet.</span></span>

<span data-ttu-id="402b6-110">Этот атрибут применяется, если для анализа данных ASF используется разделитель ASF.</span><span class="sxs-lookup"><span data-stu-id="402b6-110">This attribute applies if you are using the ASF splitter to parse ASF data.</span></span> <span data-ttu-id="402b6-111">Если данные ASF имеют переменную длину пакетов, необходимо установить этот атрибут для буферов мультимедиа, передаваемых в метод [**имфасфсплиттер::P арседата**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="402b6-111">If your ASF data has variable packet lengths, you must set this attribute on the media buffers that you pass to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="402b6-112">Присвойте атрибуту **значение true** , если в буфере содержится начало нового пакета.</span><span class="sxs-lookup"><span data-stu-id="402b6-112">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="402b6-113">Если буфер содержит продолжение предыдущего пакета, присвойте атрибуту **значение false**.</span><span class="sxs-lookup"><span data-stu-id="402b6-113">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="402b6-114">Буферы не могут охватывать несколько пакетов.</span><span class="sxs-lookup"><span data-stu-id="402b6-114">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="402b6-115">Для данных ASF с фиксированными размерами пакетов этот атрибут не является обязательным, а буфер может охватывать несколько пакетов.</span><span class="sxs-lookup"><span data-stu-id="402b6-115">For ASF data with fixed packet sizes, this attribute is not required, and a buffer can can span multiple packets.</span></span>

<span data-ttu-id="402b6-116">Обратите внимание, что стандартные реализации [**имфмедиабуффер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) , предоставляемые Media Foundation, не предоставляют [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span><span class="sxs-lookup"><span data-stu-id="402b6-116">Note that the standard implementations of the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) provided by Media Foundation do not expose [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).</span></span> <span data-ttu-id="402b6-117">Чтобы использовать этот атрибут, необходимо предоставить собственную реализацию **имфмедиабуффер**; Например, путем заключения буферов, возвращаемых функцией [**мфкреатемеморибуффер**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span><span class="sxs-lookup"><span data-stu-id="402b6-117">To use this attribute, you must provide your own implementation of **IMFMediaBuffer**; for example, by wrapping the buffers returned by [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).</span></span>

## <a name="requirements"></a><span data-ttu-id="402b6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="402b6-118">Requirements</span></span>



| <span data-ttu-id="402b6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="402b6-119">Requirement</span></span> | <span data-ttu-id="402b6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="402b6-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="402b6-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="402b6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="402b6-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="402b6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="402b6-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="402b6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="402b6-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="402b6-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="402b6-125">Header</span><span class="sxs-lookup"><span data-stu-id="402b6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="402b6-126"><dt>Вмконтаинер. h</dt></span><span class="sxs-lookup"><span data-stu-id="402b6-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="402b6-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="402b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="402b6-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="402b6-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="402b6-129">Атрибуты ASF</span><span class="sxs-lookup"><span data-stu-id="402b6-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="402b6-130">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="402b6-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="402b6-131">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="402b6-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="402b6-132">**имфмедиабуффер**</span><span class="sxs-lookup"><span data-stu-id="402b6-132">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




