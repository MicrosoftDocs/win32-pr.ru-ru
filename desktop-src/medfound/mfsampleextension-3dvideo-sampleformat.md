---
description: Указывает, как трехмерный видеокадр хранится в примере носителя.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: Атрибут MFSampleExtension_3DVideo_SampleFormat (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155974"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a><span data-ttu-id="b230a-103">Мфсампликстенсион \_ 3DVideo \_ самплеформат, атрибут</span><span class="sxs-lookup"><span data-stu-id="b230a-103">MFSampleExtension\_3DVideo\_SampleFormat attribute</span></span>

<span data-ttu-id="b230a-104">Указывает, как трехмерный видеокадр хранится в примере носителя.</span><span class="sxs-lookup"><span data-stu-id="b230a-104">Specifies how a 3D video frame is stored in a media sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="b230a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b230a-105">Data type</span></span>

<span data-ttu-id="b230a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b230a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b230a-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b230a-107">Remarks</span></span>

<span data-ttu-id="b230a-108">Значение этого атрибута является членом перечисления [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .</span><span class="sxs-lookup"><span data-stu-id="b230a-108">The value of this attribute is a member of the [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) enumeration.</span></span>

<span data-ttu-id="b230a-109">Компонент, создающий трехмерные видеокадры, должен установить для этого атрибута **значение true** на каждом образце носителя, содержащем трехмерный кадр.</span><span class="sxs-lookup"><span data-stu-id="b230a-109">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span> <span data-ttu-id="b230a-110">Атрибут игнорируется, если атрибут [мфсампликстенсион \_ 3DVideo](mfsampleextension-3dvideo.md) имеет **значение false** или не задан.</span><span class="sxs-lookup"><span data-stu-id="b230a-110">The attribute is ignored if the [MFSampleExtension\_3DVideo](mfsampleextension-3dvideo.md) attribute is **FALSE** or not set.</span></span>

## <a name="requirements"></a><span data-ttu-id="b230a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="b230a-111">Requirements</span></span>



| <span data-ttu-id="b230a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="b230a-112">Requirement</span></span> | <span data-ttu-id="b230a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="b230a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b230a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b230a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b230a-115">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="b230a-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b230a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b230a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b230a-117">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="b230a-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b230a-118">Header</span><span class="sxs-lookup"><span data-stu-id="b230a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b230a-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b230a-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b230a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b230a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b230a-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b230a-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b230a-122">Мфсампликстенсион \_ 3DVideo</span><span class="sxs-lookup"><span data-stu-id="b230a-122">MFSampleExtension\_3DVideo</span></span>](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




