---
description: Указывает, разрешено ли приложению доступ к несжатым видеокадрам.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: Атрибут MFPROTECTION_VIDEO_FRAMES (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702035"
---
# <a name="mfprotection_video_frames-attribute"></a><span data-ttu-id="fea21-103">\_Атрибут "кадры видео мфпротектион" \_</span><span class="sxs-lookup"><span data-stu-id="fea21-103">MFPROTECTION\_VIDEO\_FRAMES attribute</span></span>

<span data-ttu-id="fea21-104">Указывает, разрешено ли приложению доступ к несжатым видеокадрам.</span><span class="sxs-lookup"><span data-stu-id="fea21-104">Specifies if an application is allowed access to uncompressed video frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="fea21-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fea21-105">Data type</span></span>

<span data-ttu-id="fea21-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="fea21-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="fea21-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fea21-107">Remarks</span></span>

<span data-ttu-id="fea21-108">Значение 0 указывает, что приложению разрешен доступ к кадрам.</span><span class="sxs-lookup"><span data-stu-id="fea21-108">A value of 0 indicates that the application is allowed access to the frames.</span></span> <span data-ttu-id="fea21-109">Это может быть определено в результате применения частного соглашения между приложением и определенной системой защиты содержимого.</span><span class="sxs-lookup"><span data-stu-id="fea21-109">This might be determined as a result of a private agreement between the application and the particular content protection system in use.</span></span>

<span data-ttu-id="fea21-110">Значение 1 указывает, что приложению разрешен доступ к кадрам, если приложение предоставляет действительный сертификат приложения (см. раздел [**имфмедиаенгинепротектедконтент:: сетаппликатионцертификате**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span><span class="sxs-lookup"><span data-stu-id="fea21-110">A value of 1 indicates that the application is allowed access to frames if a valid application certificate is provided by the application (see [**IMFMediaEngineProtectedContent::SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).</span></span>

<span data-ttu-id="fea21-111">Значение 0xFFFFFFFF, которое является значением по умолчанию, указывает, что приложениям не разрешен доступ к несжатым кадрам.</span><span class="sxs-lookup"><span data-stu-id="fea21-111">A value of 0xFFFFFFFF, which is the default value, indicates no applications are allowed access to uncompressed frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="fea21-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fea21-112">Requirements</span></span>



| <span data-ttu-id="fea21-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fea21-113">Requirement</span></span> | <span data-ttu-id="fea21-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fea21-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fea21-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fea21-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fea21-116">\[Только приложения UWP Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fea21-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fea21-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fea21-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fea21-118">Только приложения UWP для Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fea21-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fea21-119">Header</span><span class="sxs-lookup"><span data-stu-id="fea21-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="fea21-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="fea21-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fea21-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fea21-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fea21-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fea21-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fea21-123">Атрибуты типа мультимедиа</span><span class="sxs-lookup"><span data-stu-id="fea21-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




