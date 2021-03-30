---
title: Завершение записи ключей
description: Завершение записи ключей
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- Сообщение WM_CAP_GET_SEQUENCE_SETUP
- макрос Капкаптурежетсетуп
- Структура КАПТУРЕПАРМС
- Сообщение WM_CAP_SET_SEQUENCE_SETUP
- макрос Капкаптуресетсетуп
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a91d6ee7d07ed36c11cce7e888c9a9710f403cf9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789985"
---
# <a name="keys-ending-capture"></a><span data-ttu-id="1529a-108">Завершение записи ключей</span><span class="sxs-lookup"><span data-stu-id="1529a-108">Keys Ending Capture</span></span>

<span data-ttu-id="1529a-109">Вы можете разрешить пользователю прервать сеанс записи, нажав клавишу или сочетание клавиш, или нажав правую или левую кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="1529a-109">You can allow the user to abort a capture session by pressing a key or keystroke combination from the keyboard, or by pressing the right or left mouse button.</span></span> <span data-ttu-id="1529a-110">Если пользователь прерывает сеанс записи в режиме реального времени, содержимое файла записи удаляется.</span><span class="sxs-lookup"><span data-stu-id="1529a-110">If the user aborts a real-time capture session, the contents of the capture file are discarded.</span></span> <span data-ttu-id="1529a-111">Если пользователь прерывает сеанс записи кадров, выполняется сохранение содержимого файла записи вплоть до точки прерывания записи.</span><span class="sxs-lookup"><span data-stu-id="1529a-111">If the user aborts a step-frame capture session, the contents of the capture file up to the point of aborting the capture are saved.</span></span>

<span data-ttu-id="1529a-112">Вы можете получить параметры для прерывания сеанса записи с помощью сообщения о [**\_ \_ \_ \_ настройке установки последовательностей WM Cap**](wm-cap-get-sequence-setup.md) (или макроса [**капкаптурежетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="1529a-112">You can retrieve the settings for aborting a capture session by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="1529a-113">Текущее нажатие клавиш сохраняется в элементе **вкэйаборт** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) . текущие параметры мыши хранятся в членах **фабортлефтмаусе** и **фабортригхтмаусе** .</span><span class="sxs-lookup"><span data-stu-id="1529a-113">The current keystroke setting is stored in the **vKeyAbort** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure; the current mouse settings are stored in the **fAbortLeftMouse** and **fAbortRightMouse** members.</span></span> <span data-ttu-id="1529a-114">Можно задать новое сочетание клавиш или сочетаний клавиш, указав сочетание keyCode или KeyCode (как в сочетаниях клавиш CTRL или SHIFT) в качестве значения **вкэйаборт** или установите левую или правую кнопку мыши в качестве ключа прерывания, указав элемент **фабортлефтмаусе** или **фабортригхтмаусе** .</span><span class="sxs-lookup"><span data-stu-id="1529a-114">You can set a new key or keystroke combination by specifying the keycode or keycode combination (as in a CTRL or SHIFT key combination) as the value of **vKeyAbort**, or set the left or right mouse button as the abort key by specifying the **fAbortLeftMouse** or **fAbortRightMouse** member.</span></span> <span data-ttu-id="1529a-115">После установки этих членов отправьте обновленную структуру **каптурепармс** в окно Capture с помощью сообщения [**\_ установки закрепления WM \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (или макроса [**капкаптуресетсетуп**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="1529a-115">After you set these members, send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="1529a-116">Значение по умолчанию **вкэйаборт** — VK \_ Escape.</span><span class="sxs-lookup"><span data-stu-id="1529a-116">The default value of **vKeyAbort** is VK\_ESCAPE.</span></span> <span data-ttu-id="1529a-117">Перед указанием нажатия клавиши, которая может прервать сеанс записи, необходимо вызвать функцию [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) .</span><span class="sxs-lookup"><span data-stu-id="1529a-117">You must call the [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) function before specifying a keystroke that can abort a capture session.</span></span> <span data-ttu-id="1529a-118">Значения **фабортлефтмаусе** и **фабортригхтмаусе** по умолчанию имеют **значение true**.</span><span class="sxs-lookup"><span data-stu-id="1529a-118">The default values of **fAbortLeftMouse** and **fAbortRightMouse** are **TRUE**.</span></span>

 

 