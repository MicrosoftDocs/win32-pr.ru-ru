---
description: Возвращает значение неустановленного аппаратного кодека.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf310ae3dafee7823119b2d5d5bd2c6b61fe822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263507"
---
# <a name="opm_get_codec_info"></a><span data-ttu-id="f091b-103">ОПМ \_ получить \_ \_ сведения о кодека</span><span class="sxs-lookup"><span data-stu-id="f091b-103">OPM\_GET\_CODEC\_INFO</span></span>

<span data-ttu-id="f091b-104">Возвращает значение неустановленного аппаратного кодека.</span><span class="sxs-lookup"><span data-stu-id="f091b-104">Gets the merit value of a hardware codec.</span></span>



| <span data-ttu-id="f091b-105">Требование</span><span class="sxs-lookup"><span data-stu-id="f091b-105">Requirement</span></span> | <span data-ttu-id="f091b-106">Значение</span><span class="sxs-lookup"><span data-stu-id="f091b-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f091b-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="f091b-107">Request GUID</span></span> | <span data-ttu-id="f091b-108">**ОПМ \_ получить \_ \_ сведения о кодека**</span><span class="sxs-lookup"><span data-stu-id="f091b-108">**OPM\_GET\_CODEC\_INFO**</span></span>                                                                 |
| <span data-ttu-id="f091b-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="f091b-109">Input data</span></span>   | <span data-ttu-id="f091b-110">Структура [**\_ \_ \_ \_ параметров получения кодека ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)</span><span class="sxs-lookup"><span data-stu-id="f091b-110">An [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure</span></span>   |
| <span data-ttu-id="f091b-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="f091b-111">Return data</span></span>  | <span data-ttu-id="f091b-112">Структура [**\_ \_ \_ \_ сведений о кодека ОПМ Get**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)</span><span class="sxs-lookup"><span data-stu-id="f091b-112">An [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f091b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f091b-113">Remarks</span></span>

<span data-ttu-id="f091b-114">Хотя эта команда использует интерфейс [Output Protection Manager](output-protection-manager.md) (ОПМ), она применяется только к аппаратным кодировщикам и декодерам.</span><span class="sxs-lookup"><span data-stu-id="f091b-114">Although this command uses the [Output Protection Manager](output-protection-manager.md) (OPM) interface, it applies only to hardware encoders and decoders.</span></span> <span data-ttu-id="f091b-115">Он не применяется к устройствам вывода видео.</span><span class="sxs-lookup"><span data-stu-id="f091b-115">It does not apply to video output devices.</span></span>

<span data-ttu-id="f091b-116">Как правило, эту команду не следует использовать напрямую.</span><span class="sxs-lookup"><span data-stu-id="f091b-116">Generally, you should not use this command directly.</span></span> <span data-ttu-id="f091b-117">Чтобы получить ценность для аппаратного кодека, вызовите функцию [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .</span><span class="sxs-lookup"><span data-stu-id="f091b-117">To get the merit value for a hardware codec, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span> <span data-ttu-id="f091b-118">Эта функция выполняет все вызовы ОПМ, необходимые для отправки команды **ОПМ \_ Get \_ кодек \_ info** .</span><span class="sxs-lookup"><span data-stu-id="f091b-118">This function performs all of the OPM calls needed to send the **OPM\_GET\_CODEC\_INFO** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="f091b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f091b-119">Requirements</span></span>



| <span data-ttu-id="f091b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f091b-120">Requirement</span></span> | <span data-ttu-id="f091b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f091b-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f091b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f091b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f091b-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f091b-123">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f091b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f091b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f091b-125">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f091b-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f091b-126">Header</span><span class="sxs-lookup"><span data-stu-id="f091b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f091b-127"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f091b-127"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f091b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f091b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f091b-129">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="f091b-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> <dt>

[<span data-ttu-id="f091b-130">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="f091b-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="f091b-131">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="f091b-131">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




