---
description: Возвращает уникальный идентификатор монитора, связанного с этим выходным видео.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701799"
---
# <a name="opm_get_output_id"></a><span data-ttu-id="d6468-103">ОПМ \_ получить \_ \_ идентификатор выхода</span><span class="sxs-lookup"><span data-stu-id="d6468-103">OPM\_GET\_OUTPUT\_ID</span></span>

<span data-ttu-id="d6468-104">Возвращает уникальный идентификатор монитора, связанного с этим выходным видео.</span><span class="sxs-lookup"><span data-stu-id="d6468-104">Returns the unique identifier of the monitor associated with this video output.</span></span>



| <span data-ttu-id="d6468-105">Требование</span><span class="sxs-lookup"><span data-stu-id="d6468-105">Requirement</span></span> | <span data-ttu-id="d6468-106">Значение</span><span class="sxs-lookup"><span data-stu-id="d6468-106">Value</span></span> |
|--------------|------------------------------------------------------------------|
| <span data-ttu-id="d6468-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="d6468-107">Request GUID</span></span> | <span data-ttu-id="d6468-108">ОПМ \_ получить \_ \_ идентификатор выхода</span><span class="sxs-lookup"><span data-stu-id="d6468-108">OPM\_GET\_OUTPUT\_ID</span></span>                                             |
| <span data-ttu-id="d6468-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="d6468-109">Input data</span></span>   | <span data-ttu-id="d6468-110">Нет</span><span class="sxs-lookup"><span data-stu-id="d6468-110">None</span></span>                                                             |
| <span data-ttu-id="d6468-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="d6468-111">Return data</span></span>  | <span data-ttu-id="d6468-112">Структура [**\_ \_ \_ данных идентификатора выхода ОПМ**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)</span><span class="sxs-lookup"><span data-stu-id="d6468-112">An [**OPM\_OUTPUT\_ID\_DATA**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d6468-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6468-113">Remarks</span></span>

<span data-ttu-id="d6468-114">Драйвер видеоадаптера назначает уникальный идентификатор каждому монитору.</span><span class="sxs-lookup"><span data-stu-id="d6468-114">The video driver assigns a unique identifier to each monitor.</span></span> <span data-ttu-id="d6468-115">Этот запрос возвращает идентификатор монитора, связанного с текущим указателем [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) .</span><span class="sxs-lookup"><span data-stu-id="d6468-115">This query returns the identifier for the monitor that is associated with the current [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6468-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d6468-116">Requirements</span></span>



| <span data-ttu-id="d6468-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d6468-117">Requirement</span></span> | <span data-ttu-id="d6468-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d6468-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d6468-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6468-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d6468-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6468-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d6468-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6468-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d6468-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6468-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d6468-123">Header</span><span class="sxs-lookup"><span data-stu-id="d6468-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6468-124"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6468-124"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6468-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6468-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6468-126">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="d6468-126">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="d6468-127">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="d6468-127">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




