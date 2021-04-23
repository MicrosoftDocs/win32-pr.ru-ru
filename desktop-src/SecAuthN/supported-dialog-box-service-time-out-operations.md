---
description: 'Winlogon реализует две операции времени ожидания: один для безопасных диалоговых окон, а другой — для активации и завершения заставки.'
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Поддерживаемые операции диалогового окна "Время использования службы"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274950cadd45cd4e7e3be890da0e4350a4d0c5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809899"
---
# <a name="supported-dialog-box-service-time-out-operations"></a><span data-ttu-id="62500-103">Поддерживаемые операции диалогового окна "Время использования службы"</span><span class="sxs-lookup"><span data-stu-id="62500-103">Supported Dialog Box Service Time-out Operations</span></span>

<span data-ttu-id="62500-104">[*Winlogon*](../secgloss/w-gly.md) реализует две операции времени ожидания: один для безопасных диалоговых окон, а другой — для активации и завершения заставки.</span><span class="sxs-lookup"><span data-stu-id="62500-104">[*Winlogon*](../secgloss/w-gly.md) implements two time-out operations, one for secure dialog boxes and the other for screen saver activation and termination.</span></span>

<span data-ttu-id="62500-105">При отображении защищенного диалогового окна, например входа в систему или разблокировки рабочей станции, Winlogon может исполнить время ожидания диалоговых окон и вернуть соответствующий код результата в процедуру диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="62500-105">While displaying a secure dialog box, such as logon or unlocking a workstation, Winlogon can time-out the dialog boxes and return an appropriate result code to the dialog box procedure.</span></span> <span data-ttu-id="62500-106">Winlogon предоставляет набор функций поддержки диалоговых окон для [*модели GINA*](../secgloss/g-gly.md).</span><span class="sxs-lookup"><span data-stu-id="62500-106">Winlogon provides a set of dialog box support functions for the [*GINA*](../secgloss/g-gly.md).</span></span> <span data-ttu-id="62500-107">В модели GINA эти функции должны использоваться вместо своих аналогов в Windows, чтобы гарантировать, что GINA и Winlogon сохраняют соответствующий контроль над диалоговыми окнами.</span><span class="sxs-lookup"><span data-stu-id="62500-107">The GINA must use these functions instead of their Windows counterparts to ensure that the GINA and Winlogon maintain appropriate control over the dialog boxes.</span></span> <span data-ttu-id="62500-108">Невозможность использования версий Winlogon этих функций может привести к тому, что неавторизованные пользователи смогут получить доступ к системе.</span><span class="sxs-lookup"><span data-stu-id="62500-108">Failure to use the Winlogon versions of these functions could result in unauthorized users gaining access to the system.</span></span>

<span data-ttu-id="62500-109">Службы диалогов диалогового окна Winlogon предоставляются следующими функциями поддержки.</span><span class="sxs-lookup"><span data-stu-id="62500-109">Winlogon dialog box services are provided by the following support functions.</span></span>



| <span data-ttu-id="62500-110">Функция поддержки</span><span class="sxs-lookup"><span data-stu-id="62500-110">Support function</span></span>                                               | <span data-ttu-id="62500-111">Описание</span><span class="sxs-lookup"><span data-stu-id="62500-111">Description</span></span>                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62500-112">**влксмессажебокс**</span><span class="sxs-lookup"><span data-stu-id="62500-112">**WlxMessageBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | <span data-ttu-id="62500-113">Аналогично функции Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) .</span><span class="sxs-lookup"><span data-stu-id="62500-113">Similar to the Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>                         |
| [<span data-ttu-id="62500-114">**влксдиалогбокс**</span><span class="sxs-lookup"><span data-stu-id="62500-114">**WlxDialogBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | <span data-ttu-id="62500-115">Аналогично функции Windows [**диалогбокс**](/windows/win32/api/winuser/nf-winuser-dialogboxa) .</span><span class="sxs-lookup"><span data-stu-id="62500-115">Similar to the Windows [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function.</span></span>                           |
| [<span data-ttu-id="62500-116">**влксдиалогбоксиндирект**</span><span class="sxs-lookup"><span data-stu-id="62500-116">**WlxDialogBoxIndirect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | <span data-ttu-id="62500-117">Аналогично функции Windows [**диалогбоксиндирект**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) .</span><span class="sxs-lookup"><span data-stu-id="62500-117">Similar to the Windows [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) function.</span></span>           |
| [<span data-ttu-id="62500-118">**влксдиалогбокспарам**</span><span class="sxs-lookup"><span data-stu-id="62500-118">**WlxDialogBoxParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | <span data-ttu-id="62500-119">Аналогично функции Windows [**диалогбокспарам**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) .</span><span class="sxs-lookup"><span data-stu-id="62500-119">Similar to the Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) function.</span></span>                 |
| [<span data-ttu-id="62500-120">**влксдиалогбоксиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="62500-120">**WlxDialogBoxIndirectParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | <span data-ttu-id="62500-121">Аналогично функции Windows [**диалогбоксиндиректпарам**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) .</span><span class="sxs-lookup"><span data-stu-id="62500-121">Similar to the Windows [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) function.</span></span> |



 

<span data-ttu-id="62500-122">Библиотеки DLL GINA также могут получить \_ \_ сообщения SAS влкс WM из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="62500-122">GINA DLLs can also receive WLX\_WM\_SAS messages from Winlogon.</span></span> <span data-ttu-id="62500-123">Эти сообщения отправляются в активные диалоговые окна при получении [*последовательности безопасности*](../secgloss/s-gly.md) (SAS).</span><span class="sxs-lookup"><span data-stu-id="62500-123">These messages are sent to active dialog boxes if an [*secure attention sequence*](../secgloss/s-gly.md) (SAS) is received.</span></span> <span data-ttu-id="62500-124">Это полезно в том случае, если GINA находится в процессе запроса на сопоставление для [*смарт-карты*](../secgloss/s-gly.md), и карта удаляется из [*считывателя*](../secgloss/r-gly.md)смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="62500-124">This is useful if the GINA is in the process of prompting for the matching PIN for a [*smart card*](../secgloss/s-gly.md), and the card is removed from the smart card [*reader*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="62500-125">Winlogon использует \_ SAS влкс DLG в \_ качестве кода результата EndDialog при возникновении события SAS во время операции диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="62500-125">Winlogon uses WLX\_DLG\_SAS as the EndDialog result code when an SAS event occurs during a dialog box operation.</span></span>

<span data-ttu-id="62500-126">Время ожидания также доставляется таким образом.</span><span class="sxs-lookup"><span data-stu-id="62500-126">Time-outs are also delivered in this manner.</span></span> <span data-ttu-id="62500-127">\_ \_ Сообщение SAS влкс WM отправляется с влкс \_ SAS \_ типа \_ скрнсвр \_ timeout или влкс \_ SAS \_ Type \_ timeout.</span><span class="sxs-lookup"><span data-stu-id="62500-127">A WLX\_WM\_SAS message is sent with WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT or WLX\_SAS\_TYPE\_TIMEOUT.</span></span> <span data-ttu-id="62500-128">Диалоговое окно завершится соответствующим кодом выхода, чтобы позволить разработчикам GINA присоединить уведомления о времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="62500-128">The dialog box will end with an appropriate exit code to allow GINA developers to hook the time-out notifications.</span></span>

<span data-ttu-id="62500-129">Диалоговые окна GINA могут быть завершены с помощью программы Winlogon с кодом ВЛКС, выполнив \_ \_ \_ Выход пользователя.</span><span class="sxs-lookup"><span data-stu-id="62500-129">GINA dialog boxes can be terminated by Winlogon by using the code WLX\_DLG\_USER\_LOGOFF.</span></span> <span data-ttu-id="62500-130">Это означает, что пользователь вышел из системы во время выполнения диалогового окна (например, путем вызова функции [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) из другого потока).</span><span class="sxs-lookup"><span data-stu-id="62500-130">This indicates that the user has logged off during the running of the dialog box (for example, by calling the [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) function from another thread).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62500-131">См. также</span><span class="sxs-lookup"><span data-stu-id="62500-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62500-132">Инициализация Winlogon</span><span class="sxs-lookup"><span data-stu-id="62500-132">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="62500-133">Состояния Winlogon</span><span class="sxs-lookup"><span data-stu-id="62500-133">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="62500-134">Отправка сообщений в GINA</span><span class="sxs-lookup"><span data-stu-id="62500-134">Sending Messages to the GINA</span></span>](sending-messages-to-the-gina.md)
</dt> <dt>

[<span data-ttu-id="62500-135">Функции поддержки Winlogon</span><span class="sxs-lookup"><span data-stu-id="62500-135">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
