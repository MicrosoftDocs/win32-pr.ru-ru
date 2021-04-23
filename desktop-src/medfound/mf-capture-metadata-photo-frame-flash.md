---
description: Указывает, активирована ли флэш-память для захваченного кадра.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: Атрибут MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692666"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a><span data-ttu-id="dcb6e-103">\_ \_ \_ \_ \_ Атрибут флеш-кадра фото захвата метаданных записи MF</span><span class="sxs-lookup"><span data-stu-id="dcb6e-103">MF\_CAPTURE\_METADATA\_PHOTO\_FRAME\_FLASH attribute</span></span>

<span data-ttu-id="dcb6e-104">Указывает, активирована ли флэш-память для захваченного кадра.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-104">Indicates if a flash was triggered for the captured frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="dcb6e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="dcb6e-105">Data type</span></span>

<span data-ttu-id="dcb6e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dcb6e-106">**UINT32**</span></span>



| <span data-ttu-id="dcb6e-107">Значение</span><span class="sxs-lookup"><span data-stu-id="dcb6e-107">Value</span></span>                                                                               | <span data-ttu-id="dcb6e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="dcb6e-108">Meaning</span></span>                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dcb6e-109"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dcb6e-109"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="dcb6e-110">Флэш-память не активирована в этом кадре.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-110">A flash was not triggered on this frame.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="dcb6e-111"><dt>ненулевое значение</dt></span><span class="sxs-lookup"><span data-stu-id="dcb6e-111"><dt>non-zero</dt></span></span> </dl> | <span data-ttu-id="dcb6e-112">В этом кадре активирована флэш-память.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-112">A flash was triggered on this frame.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="dcb6e-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dcb6e-113"><dt>1</dt></span></span> </dl>        | <span data-ttu-id="dcb6e-114">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="dcb6e-114">Reserved</span></span><br/> <span data-ttu-id="dcb6e-115">Не следует явно проверять значение 1.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-115">Do not explicitly check for a value of 1.</span></span> <span data-ttu-id="dcb6e-116">Приложения должны проверять наличие! = 0, чтобы указать, была ли запущена флэш-память.</span><span class="sxs-lookup"><span data-stu-id="dcb6e-116">Applications should only check for !=0 to indicate if a flash was triggered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dcb6e-117">Требования</span><span class="sxs-lookup"><span data-stu-id="dcb6e-117">Requirements</span></span>



| <span data-ttu-id="dcb6e-118">Требование</span><span class="sxs-lookup"><span data-stu-id="dcb6e-118">Requirement</span></span> | <span data-ttu-id="dcb6e-119">Значение</span><span class="sxs-lookup"><span data-stu-id="dcb6e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb6e-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dcb6e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb6e-121">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dcb6e-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="dcb6e-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dcb6e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb6e-123">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="dcb6e-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="dcb6e-124">Header</span><span class="sxs-lookup"><span data-stu-id="dcb6e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcb6e-125"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcb6e-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcb6e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcb6e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb6e-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dcb6e-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




