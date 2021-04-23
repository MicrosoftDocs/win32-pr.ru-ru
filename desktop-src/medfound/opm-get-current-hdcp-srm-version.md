---
description: Возвращает номер версии сообщения об обновлении системы (СРМ), используемого в настоящий момент выходными данными видео.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711433"
---
# <a name="opm_get_current_hdcp_srm_version"></a><span data-ttu-id="799fb-103">ОПМ \_ получить \_ текущую \_ \_ версию СРМ \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="799fb-103">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>

<span data-ttu-id="799fb-104">Возвращает номер версии сообщения об обновлении системы (СРМ), используемого в настоящий момент выходными данными видео.</span><span class="sxs-lookup"><span data-stu-id="799fb-104">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>



| <span data-ttu-id="799fb-105">Требование</span><span class="sxs-lookup"><span data-stu-id="799fb-105">Requirement</span></span> | <span data-ttu-id="799fb-106">Значение</span><span class="sxs-lookup"><span data-stu-id="799fb-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="799fb-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="799fb-107">Request GUID</span></span> | <span data-ttu-id="799fb-108">ОПМ \_ получить \_ текущую \_ \_ версию СРМ \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="799fb-108">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>                                       |
| <span data-ttu-id="799fb-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="799fb-109">Input data</span></span>   | <span data-ttu-id="799fb-110">Нет</span><span class="sxs-lookup"><span data-stu-id="799fb-110">None</span></span>                                                                        |
| <span data-ttu-id="799fb-111">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="799fb-111">Return data</span></span>  | <span data-ttu-id="799fb-112">[**\_ Стандартная \_ информационная структура ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="799fb-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="799fb-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="799fb-113">Remarks</span></span>

<span data-ttu-id="799fb-114">Если этот запрос выполнен, элемент **улинформатион** в [**информационной структуре ОПМ \_ Standard \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) содержит номер версии СРМ в формате с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="799fb-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains the SRM version number, in little-endian format.</span></span>

<span data-ttu-id="799fb-115">Срмс используются для обновления списка отозванных High-Bandwidth устройств цифровой Защита содержимого (HDCP).</span><span class="sxs-lookup"><span data-stu-id="799fb-115">SRMs are used to update the list of revoked High-Bandwidth Digital Content Protection (HDCP) devices.</span></span> <span data-ttu-id="799fb-116">Срмс доставляются с видеоматериалом.</span><span class="sxs-lookup"><span data-stu-id="799fb-116">SRMs are delivered with the video content.</span></span> <span data-ttu-id="799fb-117">Чтобы задать СРМ, отправьте команду [**ОПМ \_ Set \_ HDCP \_ СРМ**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="799fb-117">To set the SRM, send the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="799fb-118">Этот запрос может вызвать метод [**иопмвидеуутпут::**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) noreturn, возвращающий любой из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="799fb-118">This query can cause the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method to return any of the following error codes.</span></span>



| <span data-ttu-id="799fb-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="799fb-119">Return code</span></span>                                            | <span data-ttu-id="799fb-120">Описание</span><span class="sxs-lookup"><span data-stu-id="799fb-120">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="799fb-121">Ошибка \_ Graphics \_ ОПМ \_ HDCP \_ СРМ \_ не \_ задана</span><span class="sxs-lookup"><span data-stu-id="799fb-121">ERROR\_GRAPHICS\_OPM\_HDCP\_SRM\_NEVER\_SET</span></span>            | <span data-ttu-id="799fb-122">Приложение не установило СРМ.</span><span class="sxs-lookup"><span data-stu-id="799fb-122">The application did not set an SRM.</span></span>     |
| <span data-ttu-id="799fb-123">\_вывод ошибок Graphics \_ ОПМ не \_ \_ \_ \_ поддерживает \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="799fb-123">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="799fb-124">Выходные данные видео не поддерживают HDCP.</span><span class="sxs-lookup"><span data-stu-id="799fb-124">The video output does not support HDCP.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="799fb-125">Требования</span><span class="sxs-lookup"><span data-stu-id="799fb-125">Requirements</span></span>



| <span data-ttu-id="799fb-126">Требование</span><span class="sxs-lookup"><span data-stu-id="799fb-126">Requirement</span></span> | <span data-ttu-id="799fb-127">Значение</span><span class="sxs-lookup"><span data-stu-id="799fb-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="799fb-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="799fb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="799fb-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="799fb-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="799fb-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="799fb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="799fb-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="799fb-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="799fb-132">Header</span><span class="sxs-lookup"><span data-stu-id="799fb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="799fb-133"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="799fb-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="799fb-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="799fb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="799fb-135">**Иопмвидеуутпут:: о.**</span><span class="sxs-lookup"><span data-stu-id="799fb-135">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="799fb-136">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="799fb-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




