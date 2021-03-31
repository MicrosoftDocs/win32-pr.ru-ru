---
title: Функции обратного вызова клиентских приложений
description: Два типа сигнатур обратного вызова.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411251"
---
# <a name="client-application-callback-functions"></a><span data-ttu-id="6c731-103">Функции обратного вызова клиентских приложений</span><span class="sxs-lookup"><span data-stu-id="6c731-103">Client Application Callback Functions</span></span>

<span data-ttu-id="6c731-104">Биометрическая платформа Windows поддерживает два типа сигнатур ответного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c731-104">The Windows Biometric Framework supports two types of callback signatures.</span></span> <span data-ttu-id="6c731-105">Начиная с Windows 8, поддерживается следующий обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="6c731-105">Beginning with Windows 8, the following callback is supported.</span></span> <span data-ttu-id="6c731-106">Рекомендуется реализовать этот обратный вызов для всех новых приложений.</span><span class="sxs-lookup"><span data-stu-id="6c731-106">We recommend that you implement this callback for all new applications.</span></span> <span data-ttu-id="6c731-107">Однако этот обратный вызов не может использоваться в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6c731-107">This callback cannot, however, be used in Windows 7.</span></span>



| <span data-ttu-id="6c731-108">Обратный вызов</span><span class="sxs-lookup"><span data-stu-id="6c731-108">Callback</span></span>                                                                                     | <span data-ttu-id="6c731-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6c731-109">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c731-110">**\_ \_ обратный вызов асинхронного завершения пвинбио \_**</span><span class="sxs-lookup"><span data-stu-id="6c731-110">**PWINBIO\_ASYNC\_COMPLETION\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | <span data-ttu-id="6c731-111">Уведомляет клиентское приложение о том, что асинхронная операция, запущенная с помощью [**винбиоасинкопенсессион**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) или [**винбиоасинкопенфрамеворк**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) , завершилась.</span><span class="sxs-lookup"><span data-stu-id="6c731-111">Notifies the client application that an asynchronous operation started by using [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) or [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) has completed.</span></span><br/> |



 

<span data-ttu-id="6c731-112">В Windows 7 появились следующие функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6c731-112">The following callback functions were introduced in Windows 7.</span></span> <span data-ttu-id="6c731-113">Не рекомендуется реализовывать их для новых приложений, предназначенных для операционных систем Windows 8 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="6c731-113">We recommend that you do not implement them for new applications that target Windows 8 and later operating systems.</span></span>



| <span data-ttu-id="6c731-114">Обратный вызов</span><span class="sxs-lookup"><span data-stu-id="6c731-114">Callback</span></span>                                                                                 | <span data-ttu-id="6c731-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6c731-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6c731-116">**\_ \_ обратный вызов записи пвинбио**</span><span class="sxs-lookup"><span data-stu-id="6c731-116">**PWINBIO\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | <span data-ttu-id="6c731-117">Возвращает результаты асинхронной функции [**винбиокаптуресамплевискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) .</span><span class="sxs-lookup"><span data-stu-id="6c731-117">Returns results from the asynchronous [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="6c731-118">**\_ \_ обратный вызов записи регистрации пвинбио \_**</span><span class="sxs-lookup"><span data-stu-id="6c731-118">**PWINBIO\_ENROLL\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | <span data-ttu-id="6c731-119">Возвращает результаты асинхронной функции [**винбиоенроллкаптуревискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) .</span><span class="sxs-lookup"><span data-stu-id="6c731-119">Returns results from the asynchronous [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="6c731-120">**\_ \_ обратный вызов события пвинбио**</span><span class="sxs-lookup"><span data-stu-id="6c731-120">**PWINBIO\_EVENT\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | <span data-ttu-id="6c731-121">Возвращает результаты асинхронной функции [**винбиорегистеревентмонитор**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) .</span><span class="sxs-lookup"><span data-stu-id="6c731-121">Returns results from the asynchronous [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function.</span></span><br/>           |
| [<span data-ttu-id="6c731-122">**\_ \_ обратный вызов пвинбио Identify**</span><span class="sxs-lookup"><span data-stu-id="6c731-122">**PWINBIO\_IDENTIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | <span data-ttu-id="6c731-123">Возвращает результаты асинхронной функции [**винбиоидентифивискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) .</span><span class="sxs-lookup"><span data-stu-id="6c731-123">Returns results from the asynchronous [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) function.</span></span><br/>           |
| [<span data-ttu-id="6c731-124">**ПВИНБИОный \_ \_ \_ обратный вызов датчика**</span><span class="sxs-lookup"><span data-stu-id="6c731-124">**PWINBIO\_LOCATE\_SENSOR\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | <span data-ttu-id="6c731-125">Возвращает результаты асинхронной функции [**винбиолокатесенсорвискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) .</span><span class="sxs-lookup"><span data-stu-id="6c731-125">Returns results from the asynchronous [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) function.</span></span><br/>   |
| [<span data-ttu-id="6c731-126">**\_ \_ обратный вызов пвинбио проверки**</span><span class="sxs-lookup"><span data-stu-id="6c731-126">**PWINBIO\_VERIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | <span data-ttu-id="6c731-127">Возвращает результаты асинхронной функции [**винбиоверифивискаллбакк**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) .</span><span class="sxs-lookup"><span data-stu-id="6c731-127">Returns results from the asynchronous [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) function.</span></span><br/>               |



 

## <a name="related-topics"></a><span data-ttu-id="6c731-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6c731-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c731-129">Справочник по клиентскому приложению</span><span class="sxs-lookup"><span data-stu-id="6c731-129">Client Application Reference</span></span>](client-application-reference.md)
</dt> </dl>

 

 





