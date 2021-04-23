---
title: Подключение окна записи к драйверу записи
description: Подключение окна записи к драйверу записи
ms.assetid: 78d4aaf5-6216-4eec-84d4-6727d1822983
keywords:
- Сообщение WM_CAP_DRIVER_CONNECT
- макрос Капдриверконнект
- Функция Капжетдривердескриптион
- Сообщение WM_CAP_DRIVER_GET_NAME
- макрос Капдривержетнаме
- Сообщение WM_CAP_DRIVER_GET_VERSION
- макрос Капдривержетверсион
- Сообщение WM_CAP_DRIVER_DISCONNECT
- макрос Капдривердисконнект
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c189ad3ea5631e269ffbe85f20a143b074486f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775692"
---
# <a name="connecting-a-capture-window-to-a-capture-driver"></a><span data-ttu-id="23892-112">Подключение окна записи к драйверу записи</span><span class="sxs-lookup"><span data-stu-id="23892-112">Connecting a Capture Window to a Capture Driver</span></span>

<span data-ttu-id="23892-113">Вы можете динамически подключать или отключать окно записи в драйвер записи.</span><span class="sxs-lookup"><span data-stu-id="23892-113">You can dynamically connect or disconnect a capture window to a capture driver.</span></span> <span data-ttu-id="23892-114">Вы можете подключить или связать окно записи с драйвером записи с помощью сообщения [**Connect с \_ \_ драйвером \_ WM**](wm-cap-driver-connect.md) (или макроса [**капдриверконнект**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) ).</span><span class="sxs-lookup"><span data-stu-id="23892-114">You can connect or associate a capture window with a capture driver by using the [**WM\_CAP\_DRIVER\_CONNECT**](wm-cap-driver-connect.md) message (or the [**capDriverConnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverconnect) macro).</span></span> <span data-ttu-id="23892-115">После подключения окна записи и драйвера записи можно отправить сообщения, относящиеся к конкретному устройству, к драйверу записи, связанному с окном записи.</span><span class="sxs-lookup"><span data-stu-id="23892-115">After a capture window and capture driver are connected, you can send device-specific messages to the capture driver associated with a capture window.</span></span>

<span data-ttu-id="23892-116">Если в системе установлено более одного устройства записи, можно подключить окно записи к конкретному драйверу устройства записи видео, указав целое число для параметра *wParam* \_ \_ сообщения Connect драйвера WM Cap \_ .</span><span class="sxs-lookup"><span data-stu-id="23892-116">If you have more than one capture device installed on a system, you can connect a capture window to a particular video capture device driver by specifying an integer for the *wParam* parameter of the WM\_CAP\_DRIVER\_CONNECT message.</span></span> <span data-ttu-id="23892-117">Целое число — это индекс, который определяет драйвер видеозаписи, указанный в реестре или \[ в \] разделе драйверов файла SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="23892-117">The integer is an index that identifies a video capture driver listed in the registry or in the \[drivers\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="23892-118">Используйте ноль для первой записи индекса.</span><span class="sxs-lookup"><span data-stu-id="23892-118">Use zero for the first index entry.</span></span>

<span data-ttu-id="23892-119">Имя и версию установленного драйвера записи можно получить с помощью функции [**капжетдривердескриптион**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) .</span><span class="sxs-lookup"><span data-stu-id="23892-119">You can retrieve the name and version of an installed capture driver by using the [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) function.</span></span> <span data-ttu-id="23892-120">Приложение может использовать эту функцию для перечисления установленных устройств и драйверов записи, чтобы пользователь мог выбрать устройство записи для подключения к окну записи.</span><span class="sxs-lookup"><span data-stu-id="23892-120">Your application can use this function to enumerate the installed capture devices and drivers, so the user can select a capture device to connect to a capture window.</span></span>

<span data-ttu-id="23892-121">Имя драйвера устройства записи, подключенного к окну записи, можно получить с помощью сообщения [**\_ \_ \_ Get \_ Name драйвера WM Cap**](wm-cap-driver-get-name.md) (или макроса [**капдривержетнаме**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) ).</span><span class="sxs-lookup"><span data-stu-id="23892-121">You can retrieve the name of the capture device driver connected to a capture window by using the [**WM\_CAP\_DRIVER\_GET\_NAME**](wm-cap-driver-get-name.md) message (or the [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) macro).</span></span> <span data-ttu-id="23892-122">Чтобы получить версию установленного драйвера записи, используйте сообщение о [**\_ \_ \_ получении \_ версии драйвера WM Cap**](wm-cap-driver-get-version.md) (или макрос [**капдривержетверсион**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) ).</span><span class="sxs-lookup"><span data-stu-id="23892-122">To retrieve the version of an installed capture driver, use the [**WM\_CAP\_DRIVER\_GET\_VERSION**](wm-cap-driver-get-version.md) message (or the [**capDriverGetVersion**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetversion) macro).</span></span>

<span data-ttu-id="23892-123">Вы можете отключить окно записи из драйвера записи с помощью сообщения об [**\_ \_ \_ отключении драйвера WM Cap**](wm-cap-driver-disconnect.md) (или макроса [**капдривердисконнект**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) ).</span><span class="sxs-lookup"><span data-stu-id="23892-123">You can disconnect a capture window from a capture driver by using the [**WM\_CAP\_DRIVER\_DISCONNECT**](wm-cap-driver-disconnect.md) message (or the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro).</span></span>

<span data-ttu-id="23892-124">При уничтожении окна записи все подключенные драйверы устройства записи видео автоматически отключаются.</span><span class="sxs-lookup"><span data-stu-id="23892-124">When an capture window is destroyed, any connected video capture device drivers are automatically disconnected.</span></span>

 

 




