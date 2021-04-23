---
description: Указывает сведения о видеосигнале, отличном от уровня защиты.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543858"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a><span data-ttu-id="2a8ac-103">ОПМ \_ Установка \_ \_ сигнала ACP и \_ кгмса \_</span><span class="sxs-lookup"><span data-stu-id="2a8ac-103">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="2a8ac-104">Указывает сведения о видеосигнале, отличном от уровня защиты.</span><span class="sxs-lookup"><span data-stu-id="2a8ac-104">Specifies information about the video signal, other than the protection level.</span></span>



| <span data-ttu-id="2a8ac-105">Требование</span><span class="sxs-lookup"><span data-stu-id="2a8ac-105">Requirement</span></span> | <span data-ttu-id="2a8ac-106">Значение</span><span class="sxs-lookup"><span data-stu-id="2a8ac-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a8ac-107">Идентификатор GUID команды</span><span class="sxs-lookup"><span data-stu-id="2a8ac-107">Command GUID</span></span> | <span data-ttu-id="2a8ac-108">ОПМ \_ Установка \_ \_ сигнала ACP и \_ кгмса \_</span><span class="sxs-lookup"><span data-stu-id="2a8ac-108">OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                                                |
| <span data-ttu-id="2a8ac-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="2a8ac-109">Input data</span></span>   | <span data-ttu-id="2a8ac-110">Структура [**\_ \_ \_ \_ \_ \_ параметров сигнализации ОПМ Set ACP и кгмса**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters)</span><span class="sxs-lookup"><span data-stu-id="2a8ac-110">An [**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="2a8ac-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a8ac-111">Remarks</span></span>

<span data-ttu-id="2a8ac-112">Эта команда эквивалентна \_ команде дксва коппсетсигналинг, используемой в протоколе сертифицированной защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="2a8ac-112">This command is equivalent to the DXVA\_COPPSetSignaling command used in Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="2a8ac-113">В случае с CGMS-A для некоторых стандартов защиты требуется, чтобы ТВ-сигнал содержал информацию в тех же пакетах ВБИ звукозаписи, что и для битов с ЗАЩИТой от имени A.</span><span class="sxs-lookup"><span data-stu-id="2a8ac-113">For CGMS-A, certain protection standards require that the television signal contain information within the same VBI waveform packets as the CGMS-A bits.</span></span> <span data-ttu-id="2a8ac-114">Помимо прочего, эта информация включает в себя пропорции изображения.</span><span class="sxs-lookup"><span data-stu-id="2a8ac-114">Among other things, this information includes the picture aspect ratio.</span></span> <span data-ttu-id="2a8ac-115">Телевизоры могут плохо отображаться, если сведения о пропорции не соответствуют потоку видео.</span><span class="sxs-lookup"><span data-stu-id="2a8ac-115">Televisions may display poorly if the aspect ratio information is not consistent with the video stream.</span></span> <span data-ttu-id="2a8ac-116">Приложение может использовать эту команду, чтобы задать пропорции, чтобы графический драйвер мог формировать правильные пакеты ВБИ.</span><span class="sxs-lookup"><span data-stu-id="2a8ac-116">The application can use this command to specify the aspect ratio so that the graphics driver can generate the correct VBI packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a8ac-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2a8ac-117">Requirements</span></span>



| <span data-ttu-id="2a8ac-118">Требование</span><span class="sxs-lookup"><span data-stu-id="2a8ac-118">Requirement</span></span> | <span data-ttu-id="2a8ac-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2a8ac-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2a8ac-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a8ac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a8ac-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a8ac-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2a8ac-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a8ac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a8ac-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a8ac-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2a8ac-124">Header</span><span class="sxs-lookup"><span data-stu-id="2a8ac-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a8ac-125"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a8ac-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a8ac-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2a8ac-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a8ac-127">**Иопмвидеуутпут:: Configure**</span><span class="sxs-lookup"><span data-stu-id="2a8ac-127">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="2a8ac-128">Команды ОПМ</span><span class="sxs-lookup"><span data-stu-id="2a8ac-128">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




