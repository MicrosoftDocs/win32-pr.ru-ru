---
description: Запросы состояния ОПМ
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Запросы состояния ОПМ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811585"
---
# <a name="opm-status-requests"></a><span data-ttu-id="0787f-103">Запросы состояния ОПМ</span><span class="sxs-lookup"><span data-stu-id="0787f-103">OPM Status Requests</span></span>

<span data-ttu-id="0787f-104">В этом разделе перечислены доступные запросы состояния для [Output Protection Manager](output-protection-manager.md) (ОПМ).</span><span class="sxs-lookup"><span data-stu-id="0787f-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="0787f-105">Чтобы отправить запрос состояния ОПМ, вызовите [**иопмвидеуутпут:: i Information**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span><span class="sxs-lookup"><span data-stu-id="0787f-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="0787f-106">Для каждого запроса перечислены следующие сведения.</span><span class="sxs-lookup"><span data-stu-id="0787f-106">For each request, the following information is listed.</span></span>



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0787f-107">GUID запроса</span><span class="sxs-lookup"><span data-stu-id="0787f-107">Request GUID</span></span> | <span data-ttu-id="0787f-108">Идентифицирует запрос.</span><span class="sxs-lookup"><span data-stu-id="0787f-108">Identifies the request.</span></span> <span data-ttu-id="0787f-109">Задайте для элемента **гуидсеттинг** структуры [**\_ \_ \_ Parameters получения сведений ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) значение, равное этому значению.</span><span class="sxs-lookup"><span data-stu-id="0787f-109">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="0787f-110">Входные данные</span><span class="sxs-lookup"><span data-stu-id="0787f-110">Input data</span></span>   | <span data-ttu-id="0787f-111">Указывает способ интерпретации массива **абпараметерс** в структуре [**параметров ОПМ \_ Get \_ info \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) .</span><span class="sxs-lookup"><span data-stu-id="0787f-111">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="0787f-112">Выходные данные</span><span class="sxs-lookup"><span data-stu-id="0787f-112">Output data</span></span>  | <span data-ttu-id="0787f-113">Указывает способ интерпретации массива **абрекуестединформатион** в структуре [**\_ запрашиваемой \_ информации ОПМ**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .</span><span class="sxs-lookup"><span data-stu-id="0787f-113">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="0787f-114">Определены следующие запросы состояния:</span><span class="sxs-lookup"><span data-stu-id="0787f-114">The following status requests are defined:</span></span>



| <span data-ttu-id="0787f-115">Запрос состояния</span><span class="sxs-lookup"><span data-stu-id="0787f-115">Status request</span></span>                                                                                      | <span data-ttu-id="0787f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0787f-116">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0787f-117">**ОПМ \_ Получение \_ \_ сигнала ACP и \_ кгмса \_**</span><span class="sxs-lookup"><span data-stu-id="0787f-117">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="0787f-118">Возвращает следующие сведения о выходе видео:</span><span class="sxs-lookup"><span data-stu-id="0787f-118">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="0787f-119">**ОПМ \_ получить \_ фактический \_ выходной \_ Формат**</span><span class="sxs-lookup"><span data-stu-id="0787f-119">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="0787f-120">Возвращает описание видеосигнала, передаваемого через соединитель.</span><span class="sxs-lookup"><span data-stu-id="0787f-120">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="0787f-121">**ОПМ \_ получить \_ фактический \_ \_ уровень защиты**</span><span class="sxs-lookup"><span data-stu-id="0787f-121">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="0787f-122">Возвращает глобальный уровень защиты для указанного механизма защиты.</span><span class="sxs-lookup"><span data-stu-id="0787f-122">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="0787f-123">**ОПМ \_ получить \_ \_ Тип шины \_ адаптера**</span><span class="sxs-lookup"><span data-stu-id="0787f-123">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="0787f-124">Возвращает тип шины ввода-вывода, используемой выходными данными видео.</span><span class="sxs-lookup"><span data-stu-id="0787f-124">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="0787f-125">**ОПМ \_ получить \_ \_ сведения о кодека**</span><span class="sxs-lookup"><span data-stu-id="0787f-125">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="0787f-126">Возвращает значение неустановленного аппаратного кодека.</span><span class="sxs-lookup"><span data-stu-id="0787f-126">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="0787f-127">**ОПМ \_ получить \_ \_ \_ сведения о подключенном устройстве HDCP \_**</span><span class="sxs-lookup"><span data-stu-id="0787f-127">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="0787f-128">Возвращает сведения о High-Bandwidth устройстве цифровой Защита содержимого (HDCP), подключенном к выходным данным видео.</span><span class="sxs-lookup"><span data-stu-id="0787f-128">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="0787f-129">Возвращаются следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="0787f-129">The following information is returned:</span></span> |
| [<span data-ttu-id="0787f-130">**ОПМ \_ получить \_ \_ Тип соединителя**</span><span class="sxs-lookup"><span data-stu-id="0787f-130">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="0787f-131">Возвращает тип физического соединителя для выходного видео.</span><span class="sxs-lookup"><span data-stu-id="0787f-131">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="0787f-132">**ОПМ \_ получить \_ текущую \_ \_ версию СРМ \_ HDCP**</span><span class="sxs-lookup"><span data-stu-id="0787f-132">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="0787f-133">Возвращает номер версии сообщения об обновлении системы (СРМ), используемого в настоящий момент выходными данными видео.</span><span class="sxs-lookup"><span data-stu-id="0787f-133">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="0787f-134">**ОПМ \_ Получение \_ \_ характеристик DVI**</span><span class="sxs-lookup"><span data-stu-id="0787f-134">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="0787f-135">Запрашивает, поддерживает ли соединитель цифрового видео DVI версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="0787f-135">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="0787f-136">**ОПМ \_ получить \_ \_ идентификатор выхода**</span><span class="sxs-lookup"><span data-stu-id="0787f-136">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="0787f-137">Возвращает уникальный идентификатор монитора, связанного с этим выходным видео.</span><span class="sxs-lookup"><span data-stu-id="0787f-137">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="0787f-138">**ОПМ \_ получить \_ поддерживаемые \_ \_ типы защиты**</span><span class="sxs-lookup"><span data-stu-id="0787f-138">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="0787f-139">Возвращает список механизмов защиты, поддерживаемых соединителем.</span><span class="sxs-lookup"><span data-stu-id="0787f-139">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="0787f-140">**ОПМ \_ получить \_ \_ уровень защиты \_ виртуальной системы**</span><span class="sxs-lookup"><span data-stu-id="0787f-140">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="0787f-141">Возвращает уровень виртуальной защиты для указанного механизма защиты.</span><span class="sxs-lookup"><span data-stu-id="0787f-141">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="0787f-142">См. также</span><span class="sxs-lookup"><span data-stu-id="0787f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0787f-143">Справочник по программированию ОПМ</span><span class="sxs-lookup"><span data-stu-id="0787f-143">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="0787f-144">Диспетчер выходной защиты</span><span class="sxs-lookup"><span data-stu-id="0787f-144">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



