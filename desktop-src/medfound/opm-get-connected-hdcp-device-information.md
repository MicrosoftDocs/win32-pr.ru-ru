---
description: 'Дополнительные сведения: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION'
ms.assetid: 71fa9a99-83e4-4b27-9fd1-5a9dc3070820
title: OPM_GET_CONNECTED_HDCP_DEVICE_INFORMATION (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7561a348588b1244a6763eb447affa2b330e9c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543871"
---
# <a name="opm_get_connected_hdcp_device_information"></a><span data-ttu-id="6383f-103">ОПМ \_ получить \_ \_ \_ сведения о подключенном устройстве HDCP \_</span><span class="sxs-lookup"><span data-stu-id="6383f-103">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>

<span data-ttu-id="6383f-104">Возвращает сведения о High-Bandwidth устройстве цифровой Защита содержимого (HDCP), подключенном к выходным данным видео.</span><span class="sxs-lookup"><span data-stu-id="6383f-104">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="6383f-105">Возвращаются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="6383f-105">The following information is returned:</span></span>

-   <span data-ttu-id="6383f-106">Вектор выбора ключа HDCP устройства (КСВ).</span><span class="sxs-lookup"><span data-stu-id="6383f-106">The device's HDCP key selection vector (KSV).</span></span>
-   <span data-ttu-id="6383f-107">Является ли устройство повторителем HDCP.</span><span class="sxs-lookup"><span data-stu-id="6383f-107">Whether the device is an HDCP repeater.</span></span>



| <span data-ttu-id="6383f-108">Требование</span><span class="sxs-lookup"><span data-stu-id="6383f-108">Requirement</span></span> | <span data-ttu-id="6383f-109">Значение</span><span class="sxs-lookup"><span data-stu-id="6383f-109">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6383f-110">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="6383f-110">Request GUID</span></span> | <span data-ttu-id="6383f-111">ОПМ \_ получить \_ \_ \_ сведения о подключенном устройстве HDCP \_</span><span class="sxs-lookup"><span data-stu-id="6383f-111">OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION</span></span>                                                          |
| <span data-ttu-id="6383f-112">Входные данные</span><span class="sxs-lookup"><span data-stu-id="6383f-112">Input data</span></span>   | <span data-ttu-id="6383f-113">Нет</span><span class="sxs-lookup"><span data-stu-id="6383f-113">None</span></span>                                                                                                    |
| <span data-ttu-id="6383f-114">Возвращать данные</span><span class="sxs-lookup"><span data-stu-id="6383f-114">Return data</span></span>  | <span data-ttu-id="6383f-115">Структура [**\_ \_ \_ \_ сведений о подключенном устройстве HDCP ОПМ**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)</span><span class="sxs-lookup"><span data-stu-id="6383f-115">An [**OPM\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6383f-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6383f-116">Remarks</span></span>

<span data-ttu-id="6383f-117">Этот запрос можно использовать только с *режимом эмуляции Копп*.</span><span class="sxs-lookup"><span data-stu-id="6383f-117">This query can be used only with *COPP emulation mode*.</span></span> <span data-ttu-id="6383f-118">Если интерфейс [**иопмвидеуутпут**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) использует семантику исходящего Protection Manager (ОПМ), этот запрос состояния не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6383f-118">If the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface uses Output Protection Manager (OPM) semantics, this status request is not supported.</span></span>

<span data-ttu-id="6383f-119">КСВ — это идентификатор, предоставленный изготовителю устройства и используемый в процессе проверки подлинности и установки HDCP.</span><span class="sxs-lookup"><span data-stu-id="6383f-119">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="6383f-120">В режиме эмуляции Копп приложение использует КСВ, чтобы определить, отозвано ли устройство HDCP.</span><span class="sxs-lookup"><span data-stu-id="6383f-120">In COPP emulation mode, the application uses the KSV to determine whether the HDCP device is revoked.</span></span> <span data-ttu-id="6383f-121">Если это так, приложение не должно воспроизводить защищенное содержимое.</span><span class="sxs-lookup"><span data-stu-id="6383f-121">If it is, the application should not play protected content.</span></span> <span data-ttu-id="6383f-122">Кроме того, приложение не должно воспроизводить защищенное содержимое, если устройство является повторителем HDCP, так как Копп не поддерживает повторители HDCP.</span><span class="sxs-lookup"><span data-stu-id="6383f-122">Also, the application should not play protected content if the device is an HDCP repeater, because COPP does not support HDCP repeaters.</span></span>

<span data-ttu-id="6383f-123">Этот запрос не требуется, если используется семантика ОПМ, так как ОПМ поддерживает отзыв устройств и повторители HDCP.</span><span class="sxs-lookup"><span data-stu-id="6383f-123">This query is not needed when OPM semantics are used, because OPM supports device revocation and HDCP repeaters.</span></span>

<span data-ttu-id="6383f-124">Этот запрос эквивалентен \_ запросу дксва коппкуерихдкпкэйдата, используемому в сертифицированном протоколе защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="6383f-124">This query is equivalent to the DXVA\_COPPQueryHDCPKeyData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="6383f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6383f-125">Requirements</span></span>



| <span data-ttu-id="6383f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6383f-126">Requirement</span></span> | <span data-ttu-id="6383f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6383f-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6383f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6383f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6383f-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6383f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6383f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6383f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6383f-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6383f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6383f-132">Header</span><span class="sxs-lookup"><span data-stu-id="6383f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6383f-133"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="6383f-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6383f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6383f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6383f-135">**Иопмвидеуутпут:: Коппкомпатиблежетинформатион**</span><span class="sxs-lookup"><span data-stu-id="6383f-135">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="6383f-136">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="6383f-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




