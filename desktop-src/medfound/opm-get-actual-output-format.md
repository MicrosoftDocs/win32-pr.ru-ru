---
description: Возвращает описание видеосигнала, передаваемого через соединитель.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344422"
---
# <a name="opm_get_actual_output_format"></a><span data-ttu-id="d1fa3-103">ОПМ \_ получить \_ фактический \_ выходной \_ Формат</span><span class="sxs-lookup"><span data-stu-id="d1fa3-103">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>

<span data-ttu-id="d1fa3-104">Возвращает описание видеосигнала, передаваемого через соединитель.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-104">Returns a description of the video signal that is being transmitted over the connector.</span></span>



| <span data-ttu-id="d1fa3-105">Требование</span><span class="sxs-lookup"><span data-stu-id="d1fa3-105">Requirement</span></span> | <span data-ttu-id="d1fa3-106">Значение</span><span class="sxs-lookup"><span data-stu-id="d1fa3-106">Value</span></span> |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d1fa3-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="d1fa3-107">Request GUID</span></span> | <span data-ttu-id="d1fa3-108">ОПМ \_ получить \_ фактический \_ выходной \_ Формат</span><span class="sxs-lookup"><span data-stu-id="d1fa3-108">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>                                             |
| <span data-ttu-id="d1fa3-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d1fa3-109">Input data</span></span>   | <span data-ttu-id="d1fa3-110">Нет</span><span class="sxs-lookup"><span data-stu-id="d1fa3-110">None</span></span>                                                                         |
| <span data-ttu-id="d1fa3-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="d1fa3-111">Return data</span></span>  | <span data-ttu-id="d1fa3-112">Структура [**\_ реального \_ \_ формата выходных данных ОПМ**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)</span><span class="sxs-lookup"><span data-stu-id="d1fa3-112">An [**OPM\_ACTUAL\_OUTPUT\_FORMAT**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d1fa3-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1fa3-113">Remarks</span></span>

<span data-ttu-id="d1fa3-114">Видеосигнал, передаваемый через соединитель, не обязательно имеет тот же формат, что и режим экрана рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-114">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="d1fa3-115">Например, режим экрана рабочего стола может быть 1024 x 768 пикселей по 85 Гц, а соединитель может быть соединителем S-Video, передающий видеосигналы в 720 x 480 пикселей, 60/1.01 Гц с чередованием.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-115">For example, the desktop display mode might be 1024 x 768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720 x 480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="d1fa3-116">В этом случае драйвер вернет разрешение видеосигнала S-Video, а не разрешение рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-116">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

<span data-ttu-id="d1fa3-117">Этот запрос эквивалентен \_ запросу дксва коппкуеридисплайдата, используемому в сертифицированном протоколе защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="d1fa3-117">This query is equivalent to the DXVA\_COPPQueryDisplayData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1fa3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d1fa3-118">Requirements</span></span>



| <span data-ttu-id="d1fa3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d1fa3-119">Requirement</span></span> | <span data-ttu-id="d1fa3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d1fa3-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d1fa3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1fa3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1fa3-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1fa3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d1fa3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1fa3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1fa3-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1fa3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d1fa3-125">Header</span><span class="sxs-lookup"><span data-stu-id="d1fa3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1fa3-126"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1fa3-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1fa3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1fa3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1fa3-128">**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**</span><span class="sxs-lookup"><span data-stu-id="d1fa3-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="d1fa3-129">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="d1fa3-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="d1fa3-130">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="d1fa3-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




