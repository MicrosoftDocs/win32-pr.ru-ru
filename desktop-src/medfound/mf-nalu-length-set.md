---
description: Указывает, что сведения о длине налу будут отправляться в виде большого двоичного объекта в каждом сжатом образце H. 264.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: Атрибут MF_NALU_LENGTH_SET (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693666"
---
# <a name="mf_nalu_length_set-attribute"></a><span data-ttu-id="72881-103">\_ \_ Атрибут задания длины MF налу \_</span><span class="sxs-lookup"><span data-stu-id="72881-103">MF\_NALU\_LENGTH\_SET attribute</span></span>

<span data-ttu-id="72881-104">Указывает, что сведения о длине налу будут отправляться в виде **большого двоичного объекта** в каждом сжатом образце H. 264.</span><span class="sxs-lookup"><span data-stu-id="72881-104">Indicates that NALU length information will be sent as a **BLOB** with each compressed H.264 sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="72881-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="72881-105">Data type</span></span>

<span data-ttu-id="72881-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="72881-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="72881-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72881-107">Remarks</span></span>

<span data-ttu-id="72881-108">Задайте этот атрибут для входного типа носителя МЕДИАСУБТИПЕ \_ H264 Single bitrate.</span><span class="sxs-lookup"><span data-stu-id="72881-108">Set this attribute on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="72881-109">Задайте \_ длину MF \_ налу \_ , установленную для типа входного носителя декодера H. 264, указывая, что для каждого входного образца доступна длина налу, и каждый входной пример содержит одну полную основную картину.</span><span class="sxs-lookup"><span data-stu-id="72881-109">Set MF\_NALU\_LENGTH\_SET on input media type of H.264 decoder, indicating each input sample will have a NALU length available and each input sample contains one complete primary picture.</span></span>

<span data-ttu-id="72881-110">**Большой двоичный объект** , содержащий сведения о ДЛИНе налу, можно получить из атрибута [ \_ \_ \_ сведений о длине MF налу](mf-nalu-length-information.md) в образце входных данных.</span><span class="sxs-lookup"><span data-stu-id="72881-110">The **BLOB** containing the NALU length information can be retrieved from [MF\_NALU\_LENGTH\_INFORMATION](mf-nalu-length-information.md) attribute on the input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="72881-111">Требования</span><span class="sxs-lookup"><span data-stu-id="72881-111">Requirements</span></span>



| <span data-ttu-id="72881-112">Требование</span><span class="sxs-lookup"><span data-stu-id="72881-112">Requirement</span></span> | <span data-ttu-id="72881-113">Значение</span><span class="sxs-lookup"><span data-stu-id="72881-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="72881-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72881-114">Minimum supported client</span></span><br/> | <span data-ttu-id="72881-115">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="72881-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="72881-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72881-116">Minimum supported server</span></span><br/> | <span data-ttu-id="72881-117">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="72881-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="72881-118">Header</span><span class="sxs-lookup"><span data-stu-id="72881-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="72881-119"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="72881-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72881-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72881-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72881-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="72881-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="72881-122">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="72881-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




