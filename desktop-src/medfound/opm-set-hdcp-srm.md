---
description: Обновляет сообщение о возобновлении системы (СРМ) для High-Bandwidth Digital Защита содержимого (HDCP).
ms.assetid: ea18baba-0e03-4471-af0e-a588773c98d2
title: OPM_SET_HDCP_SRM (Опмапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9283c493598f22a1715f687eccea985a27e0e6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263501"
---
# <a name="opm_set_hdcp_srm"></a><span data-ttu-id="feffe-103">ОПМ \_ Set \_ HDCP \_ СРМ</span><span class="sxs-lookup"><span data-stu-id="feffe-103">OPM\_SET\_HDCP\_SRM</span></span>

<span data-ttu-id="feffe-104">Обновляет сообщение о возобновлении системы (СРМ) для High-Bandwidth Digital Защита содержимого (HDCP).</span><span class="sxs-lookup"><span data-stu-id="feffe-104">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span>



| <span data-ttu-id="feffe-105">Требование</span><span class="sxs-lookup"><span data-stu-id="feffe-105">Requirement</span></span> | <span data-ttu-id="feffe-106">Значение</span><span class="sxs-lookup"><span data-stu-id="feffe-106">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="feffe-107">Идентификатор GUID команды</span><span class="sxs-lookup"><span data-stu-id="feffe-107">Command GUID</span></span> | <span data-ttu-id="feffe-108">ОПМ \_ Set \_ HDCP \_ СРМ</span><span class="sxs-lookup"><span data-stu-id="feffe-108">OPM\_SET\_HDCP\_SRM</span></span>                                                                 |
| <span data-ttu-id="feffe-109">Входные данные</span><span class="sxs-lookup"><span data-stu-id="feffe-109">Input data</span></span>   | <span data-ttu-id="feffe-110">Структура [**\_ \_ \_ \_ параметров СРМ ОПМ Set HDCP**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)</span><span class="sxs-lookup"><span data-stu-id="feffe-110">An [**OPM\_SET\_HDCP\_SRM\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) structure</span></span> |



 

<span data-ttu-id="feffe-111">Параметр *Пбаддитионалпараметерс* [**Иопмвидеуутпут:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) должен указывать на буфер, содержащий СРМ.</span><span class="sxs-lookup"><span data-stu-id="feffe-111">The *pbAdditionalParameters* parameter of [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) must point to a buffer that contains the SRM.</span></span> <span data-ttu-id="feffe-112">Формат HDCP СРМ описан в спецификации HDCP.</span><span class="sxs-lookup"><span data-stu-id="feffe-112">The format of an HDCP SRM is documented in the HDCP specification.</span></span> <span data-ttu-id="feffe-113">Установите параметр *уладдитионалпараметерссизе* равным размеру буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="feffe-113">Set the *ulAdditionalParametersSize* parameter equal to the size of the buffer, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="feffe-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="feffe-114">Remarks</span></span>

<span data-ttu-id="feffe-115">Срмс используются для обновления списка отозванных устройств HDCP.</span><span class="sxs-lookup"><span data-stu-id="feffe-115">SRMs are used to update the list of revoked HDCP devices.</span></span> <span data-ttu-id="feffe-116">Срмс доставляются с видеоматериалом.</span><span class="sxs-lookup"><span data-stu-id="feffe-116">SRMs are delivered with the video content.</span></span>

<span data-ttu-id="feffe-117">Эта команда обновляет текущий СРМ вывода видео.</span><span class="sxs-lookup"><span data-stu-id="feffe-117">This command updates the video output's current SRM.</span></span> <span data-ttu-id="feffe-118">Если в момент выполнения команды включена функция HDCP, в видеоролике используется новый СРМ для проверки того, отозвано ли какое-либо из подключенных устройств HDCP.</span><span class="sxs-lookup"><span data-stu-id="feffe-118">If HDCP is enabled at the time of the command, the video output uses the new SRM to check whether any of the connected HDCP devices are revoked.</span></span> <span data-ttu-id="feffe-119">Если видеоизображение обнаруживает отозванное устройство, оно прекращает отображать видео.</span><span class="sxs-lookup"><span data-stu-id="feffe-119">If the video output detects a revoked device, it stops displaying video.</span></span> <span data-ttu-id="feffe-120">При отправке этой команды при отключенной HDCP видеозапись проверяет СРМ и сохраняет его.</span><span class="sxs-lookup"><span data-stu-id="feffe-120">If you send this command while HDCP is disabled, the video output validates the SRM and stores it.</span></span> <span data-ttu-id="feffe-121">Позже, если приложение включит HDCP, в видеоролике будет использоваться новый СРМ для проверки состояния отзыва устройства.</span><span class="sxs-lookup"><span data-stu-id="feffe-121">Later, if the application enables HDCP, the video output uses the new SRM to check the device's revocation status.</span></span>

<span data-ttu-id="feffe-122">Эта команда может привести к возврату метода **Configure** любого из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="feffe-122">This command can cause the **Configure** method to return any of the following error codes.</span></span>



| <span data-ttu-id="feffe-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="feffe-123">Return code</span></span>                                            | <span data-ttu-id="feffe-124">Описание</span><span class="sxs-lookup"><span data-stu-id="feffe-124">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="feffe-125">Ошибка \_ графики \_ ОПМ \_ Недопустимая \_ СРМ</span><span class="sxs-lookup"><span data-stu-id="feffe-125">ERROR\_GRAPHICS\_OPM\_INVALID\_SRM</span></span>                     | <span data-ttu-id="feffe-126">Недопустимый СРМ.</span><span class="sxs-lookup"><span data-stu-id="feffe-126">The SRM is not valid.</span></span>                   |
| <span data-ttu-id="feffe-127">\_вывод ошибок Graphics \_ ОПМ не \_ \_ \_ \_ поддерживает \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="feffe-127">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="feffe-128">Выходные данные видео не поддерживают HDCP.</span><span class="sxs-lookup"><span data-stu-id="feffe-128">The video output does not support HDCP.</span></span> |



 

<span data-ttu-id="feffe-129">Эта команда не поддерживается, если интерфейс **иопмвидеуутпут** эмулирует сертифицированный протокол защиты выходных данных (Копп).</span><span class="sxs-lookup"><span data-stu-id="feffe-129">This command is not supported when the **IOPMVideoOutput** interface emulates Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="feffe-130">Если используется семантика Копп, приложение отвечает за анализ Срмс и проверку состояния отзыва устройства HDCP.</span><span class="sxs-lookup"><span data-stu-id="feffe-130">When COPP semantics are used, the application is responsible for parsing SRMs and checking the revocation status of the HDCP device.</span></span> <span data-ttu-id="feffe-131">Используйте запрос [состояния \_ \_ \_ \_ \_ сведений об устройстве ОПМ Get Connected HDCP](opm-get-connected-hdcp-device-information.md) , чтобы получить вектор выбора ключа устройства (КСВ), необходимый для проверки состояния отзыва.</span><span class="sxs-lookup"><span data-stu-id="feffe-131">Use the [OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION](opm-get-connected-hdcp-device-information.md) status request to get the device's key selection vector (KSV), which is needed to check the revocation status.</span></span> <span data-ttu-id="feffe-132">Дополнительные сведения о Срмс см. в спецификации HDCP.</span><span class="sxs-lookup"><span data-stu-id="feffe-132">For more information about SRMs, refer to the HDCP specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="feffe-133">Требования</span><span class="sxs-lookup"><span data-stu-id="feffe-133">Requirements</span></span>



| <span data-ttu-id="feffe-134">Требование</span><span class="sxs-lookup"><span data-stu-id="feffe-134">Requirement</span></span> | <span data-ttu-id="feffe-135">Значение</span><span class="sxs-lookup"><span data-stu-id="feffe-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="feffe-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="feffe-136">Minimum supported client</span></span><br/> | <span data-ttu-id="feffe-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="feffe-137">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="feffe-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="feffe-138">Minimum supported server</span></span><br/> | <span data-ttu-id="feffe-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="feffe-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="feffe-140">Header</span><span class="sxs-lookup"><span data-stu-id="feffe-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="feffe-141"><dt>Опмапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="feffe-141"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feffe-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="feffe-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feffe-143">**Иопмвидеуутпут:: Configure**</span><span class="sxs-lookup"><span data-stu-id="feffe-143">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="feffe-144">Команды ОПМ</span><span class="sxs-lookup"><span data-stu-id="feffe-144">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




