---
description: Отключает использование преобразований Media Foundation на основе оборудования (МФТС) в подсистеме записи.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: Атрибут MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711559"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a><span data-ttu-id="8e4fa-103">\_Атрибут MF \_ \_ Отключить \_ аппаратные \_ преобразования для ядра записи</span><span class="sxs-lookup"><span data-stu-id="8e4fa-103">MF\_CAPTURE\_ENGINE\_DISABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="8e4fa-104">Отключает использование преобразований Media Foundation на основе оборудования (МФТС) в подсистеме записи.</span><span class="sxs-lookup"><span data-stu-id="8e4fa-104">Disables the use of hardware-based Media Foundation transforms (MFTs) in the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="8e4fa-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8e4fa-105">Data type</span></span>

<span data-ttu-id="8e4fa-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="8e4fa-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8e4fa-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e4fa-107">Remarks</span></span>

<span data-ttu-id="8e4fa-108">По умолчанию подсистема отслеживания использует аппаратные декодеры или кодировщики.</span><span class="sxs-lookup"><span data-stu-id="8e4fa-108">By default, the capture engine uses hardware decoders or encoders.</span></span> <span data-ttu-id="8e4fa-109">Чтобы отключить использование оборудования МФТС, установите для этого атрибута значение **true** при создании подсистемы захвата.</span><span class="sxs-lookup"><span data-stu-id="8e4fa-109">To disable the use of hardware MFTs, set this attribute to **TRUE** when you create the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e4fa-110">Требования</span><span class="sxs-lookup"><span data-stu-id="8e4fa-110">Requirements</span></span>



| <span data-ttu-id="8e4fa-111">Требование</span><span class="sxs-lookup"><span data-stu-id="8e4fa-111">Requirement</span></span> | <span data-ttu-id="8e4fa-112">Значение</span><span class="sxs-lookup"><span data-stu-id="8e4fa-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e4fa-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e4fa-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8e4fa-114">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8e4fa-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="8e4fa-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e4fa-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8e4fa-116">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8e4fa-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8e4fa-117">Header</span><span class="sxs-lookup"><span data-stu-id="8e4fa-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e4fa-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e4fa-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e4fa-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8e4fa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e4fa-120">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8e4fa-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8e4fa-121">Атрибуты подсистемы захвата</span><span class="sxs-lookup"><span data-stu-id="8e4fa-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="8e4fa-122">**Имфкаптурингине:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="8e4fa-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




