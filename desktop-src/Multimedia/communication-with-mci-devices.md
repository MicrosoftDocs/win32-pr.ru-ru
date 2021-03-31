---
title: Связь с устройствами MCI
description: Связь с устройствами MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Устройства MCI, Обмен данными
- Макрос МЦивнджетдевицеид
- Функция МЦисендкомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336908"
---
# <a name="communication-with-mci-devices"></a><span data-ttu-id="11357-106">Связь с устройствами MCI</span><span class="sxs-lookup"><span data-stu-id="11357-106">Communication with MCI Devices</span></span>

<span data-ttu-id="11357-107">Для каждого устройства MCI можно использовать один или несколько следующих идентификаторов:</span><span class="sxs-lookup"><span data-stu-id="11357-107">It is possible for each MCI device to use one or more of the following as identifiers:</span></span>

-   <span data-ttu-id="11357-108">идентификатор устройства</span><span class="sxs-lookup"><span data-stu-id="11357-108">a device identifier</span></span>
-   <span data-ttu-id="11357-109">имя устройства</span><span class="sxs-lookup"><span data-stu-id="11357-109">a device name</span></span>
-   <span data-ttu-id="11357-110">псевдоним</span><span class="sxs-lookup"><span data-stu-id="11357-110">an alias</span></span>
-   <span data-ttu-id="11357-111">имя файла загруженного в данный момент содержимого.</span><span class="sxs-lookup"><span data-stu-id="11357-111">the filename of the currently loaded content.</span></span>

<span data-ttu-id="11357-112">МЦивнд предоставляет макросы, которые можно использовать для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="11357-112">MCIWnd provides macros you can use to retrieve this information.</span></span> <span data-ttu-id="11357-113">Затем эти сведения можно использовать для связи через MCI напрямую с устройствами MCI, связанными с МЦивнд Windows.</span><span class="sxs-lookup"><span data-stu-id="11357-113">You can then use this information to communicate through MCI directly with MCI devices associated with MCIWnd windows.</span></span>

<span data-ttu-id="11357-114">Идентификатор текущего устройства MCI можно получить с помощью макроса [**мЦивнджетдевицеид**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .</span><span class="sxs-lookup"><span data-stu-id="11357-114">You can retrieve the identifier of the current MCI device by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span> <span data-ttu-id="11357-115">Идентификатор устройства MCI — это числовое значение, идентифицирующее экземпляр устройства MCI, используемого приложением.</span><span class="sxs-lookup"><span data-stu-id="11357-115">The MCI device identifier is a numerical value that identifies the instance of the MCI device your application is using.</span></span> <span data-ttu-id="11357-116">Приложение может использовать этот идентификатор при взаимодействии с устройством MCI с помощью функции [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="11357-116">Your application can use this identifier when communicating with an MCI device by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="11357-117">Чтобы получить имя текущего устройства MCI, используйте макрос [**мЦивнджетдевице**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) .</span><span class="sxs-lookup"><span data-stu-id="11357-117">To retrieve the name of the current MCI device, use the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span> <span data-ttu-id="11357-118">Имя устройства MCI является строкой, завершающейся нулем и определяющей тип устройства, связанный с окном МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="11357-118">The MCI device name is a null-terminated string that identifies the device type associated with an MCIWnd window.</span></span> <span data-ttu-id="11357-119">Приложение может использовать это имя при взаимодействии с устройством MCI с помощью **мЦисендкомманд**.</span><span class="sxs-lookup"><span data-stu-id="11357-119">Your application can use this name when communicating with an MCI device by using **mciSendCommand**.</span></span>

<span data-ttu-id="11357-120">Псевдоним текущего устройства MCI можно получить с помощью макроса [**мЦивнджеталиас**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) .</span><span class="sxs-lookup"><span data-stu-id="11357-120">You can retrieve the alias of the current MCI device by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span> <span data-ttu-id="11357-121">Приложение может использовать этот псевдоним при взаимодействии с устройством MCI с помощью функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="11357-121">Your application can use this alias when communicating with an MCI device by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>

<span data-ttu-id="11357-122">Наконец, можно получить имя файла, используемое устройством MCI, с помощью макроса [**мЦивнджетфиленаме**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) .</span><span class="sxs-lookup"><span data-stu-id="11357-122">Finally, you can retrieve the filename used by an MCI device by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span> <span data-ttu-id="11357-123">Имя файла определяет содержимое, которое в настоящее время связано с окном МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="11357-123">The filename identifies the content currently associated with an MCIWnd window.</span></span> <span data-ttu-id="11357-124">Приложение может использовать это имя файла при взаимодействии с устройством MCI с помощью **мЦисендкомманд** или **mciSendString**.</span><span class="sxs-lookup"><span data-stu-id="11357-124">Your application can use this filename when communicating with a MCI device by using **mciSendCommand** or **mciSendString**.</span></span>

 

 