---
description: Для формата 3D-видео указывает, какое представление является базовым представлением.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: Атрибут MF_MT_VIDEO_3D_LEFT_IS_BASE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674191"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a><span data-ttu-id="1c5e2-103">\_Полевой \_ \_ 3D-ролик MF \_ \_ — \_ базовый атрибут</span><span class="sxs-lookup"><span data-stu-id="1c5e2-103">MF\_MT\_VIDEO\_3D\_LEFT\_IS\_BASE attribute</span></span>

<span data-ttu-id="1c5e2-104">Для формата 3D-видео указывает, какое представление является базовым представлением.</span><span class="sxs-lookup"><span data-stu-id="1c5e2-104">For a 3D video format, specifies which view is the base view.</span></span>

## <a name="data-type"></a><span data-ttu-id="1c5e2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1c5e2-105">Data type</span></span>

<span data-ttu-id="1c5e2-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="1c5e2-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1c5e2-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c5e2-107">Remarks</span></span>

<span data-ttu-id="1c5e2-108">По умолчанию левое представление в трехмерной видеопоследовательности является базовым представлением.</span><span class="sxs-lookup"><span data-stu-id="1c5e2-108">By default, the left view in a 3D video sequence is the base view.</span></span> <span data-ttu-id="1c5e2-109">Если в правильном представлении используется базовое представление, присвойте этому атрибуту **значение false**.</span><span class="sxs-lookup"><span data-stu-id="1c5e2-109">If the right view is the base view, set this attribute to **FALSE**.</span></span>

<span data-ttu-id="1c5e2-110">Чтобы преобразовать видео стереоскопик в 2D, следует сохранить базовое представление и отменить другое представление.</span><span class="sxs-lookup"><span data-stu-id="1c5e2-110">To convert stereoscopic video to 2D, keep the base view and discard the other view.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c5e2-111">Требования</span><span class="sxs-lookup"><span data-stu-id="1c5e2-111">Requirements</span></span>



| <span data-ttu-id="1c5e2-112">Требование</span><span class="sxs-lookup"><span data-stu-id="1c5e2-112">Requirement</span></span> | <span data-ttu-id="1c5e2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="1c5e2-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c5e2-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c5e2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1c5e2-115">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="1c5e2-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="1c5e2-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c5e2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1c5e2-117">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="1c5e2-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="1c5e2-118">Header</span><span class="sxs-lookup"><span data-stu-id="1c5e2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c5e2-119"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c5e2-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c5e2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c5e2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c5e2-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c5e2-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




