---
description: 'Дополнительные сведения: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711437"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a><span data-ttu-id="b6d3d-103">ОПМ \_ Получение \_ \_ сигнала ACP и \_ кгмса \_</span><span class="sxs-lookup"><span data-stu-id="b6d3d-103">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="b6d3d-104">Возвращает следующие сведения о выходе видео:</span><span class="sxs-lookup"><span data-stu-id="b6d3d-104">Returns the following information about a video output:</span></span>

-   <span data-ttu-id="b6d3d-105">Список стандартов защиты телевизионных передач, поддерживаемых драйвером.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-105">A list of television protection standards supported by the driver.</span></span>
-   <span data-ttu-id="b6d3d-106">Стандартный, который активен в данный момент.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-106">The standard that is currently active.</span></span>
-   <span data-ttu-id="b6d3d-107">Текущие пропорции или другие сигнальные данные.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-107">The current aspect ratio or other signaling data.</span></span>



| <span data-ttu-id="b6d3d-108">Требование</span><span class="sxs-lookup"><span data-stu-id="b6d3d-108">Requirement</span></span> | <span data-ttu-id="b6d3d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="b6d3d-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d3d-110">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="b6d3d-110">Request GUID</span></span> | <span data-ttu-id="b6d3d-111">ОПМ \_ Получение \_ \_ сигнала ACP и \_ кгмса \_</span><span class="sxs-lookup"><span data-stu-id="b6d3d-111">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                |
| <span data-ttu-id="b6d3d-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="b6d3d-112">Input data</span></span>   | <span data-ttu-id="b6d3d-113">Нет</span><span class="sxs-lookup"><span data-stu-id="b6d3d-113">None</span></span>                                                                                |
| <span data-ttu-id="b6d3d-114">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="b6d3d-114">Return data</span></span>  | <span data-ttu-id="b6d3d-115">Структура [**\_ \_ \_ \_ сигнализации ОПМ и кгмса**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)</span><span class="sxs-lookup"><span data-stu-id="b6d3d-115">An [**OPM\_ACP\_AND\_CGMSA\_SIGNALING**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b6d3d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6d3d-116">Remarks</span></span>

<span data-ttu-id="b6d3d-117">Этот запрос эквивалентен \_ запросу дксва коппкуерисигналинг, используемому в сертифицированном протоколе защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="b6d3d-117">This query is equivalent to the DXVA\_COPPQuerySignaling query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6d3d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b6d3d-118">Requirements</span></span>



| <span data-ttu-id="b6d3d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b6d3d-119">Requirement</span></span> | <span data-ttu-id="b6d3d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b6d3d-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d3d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6d3d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b6d3d-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6d3d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b6d3d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6d3d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b6d3d-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6d3d-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b6d3d-125">Header</span><span class="sxs-lookup"><span data-stu-id="b6d3d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6d3d-126"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6d3d-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6d3d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6d3d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6d3d-128">**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**</span><span class="sxs-lookup"><span data-stu-id="b6d3d-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="b6d3d-129">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="b6d3d-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="b6d3d-130">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="b6d3d-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




