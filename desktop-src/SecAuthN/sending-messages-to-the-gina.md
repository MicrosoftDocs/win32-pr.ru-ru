---
description: Winlogon отправляет сообщения в GINA во время отображения диалоговых окон. Эти сообщения инкапсулируются в \_ \_ сообщении SAS влкс WM следующим образом.
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Отправка сообщений в GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663019"
---
# <a name="sending-messages-to-the-gina"></a><span data-ttu-id="a64e6-104">Отправка сообщений в GINA</span><span class="sxs-lookup"><span data-stu-id="a64e6-104">Sending Messages to the GINA</span></span>

<span data-ttu-id="a64e6-105">[*Winlogon*](../secgloss/w-gly.md) отправляет сообщения в [*GINA*](../secgloss/g-gly.md) во время отображения диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="a64e6-105">[*Winlogon*](../secgloss/w-gly.md) sends messages to the [*GINA*](../secgloss/g-gly.md) while dialog boxes are displayed.</span></span> <span data-ttu-id="a64e6-106">Эти сообщения инкапсулируются в \_ \_ сообщении SAS влкс WM следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a64e6-106">These messages are all encapsulated in the WLX\_WM\_SAS message as follows.</span></span>



| <span data-ttu-id="a64e6-107">Тип последовательности с защитой внимания в параметре wParam</span><span class="sxs-lookup"><span data-stu-id="a64e6-107">Secure attention sequence type in wParam parameter</span></span> | <span data-ttu-id="a64e6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a64e6-108">Description</span></span>                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a64e6-109">ВЛКС \_ SAS \_ Type \_ CTRL \_ Alt \_ Del</span><span class="sxs-lookup"><span data-stu-id="a64e6-109">WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL</span></span>                     | <span data-ttu-id="a64e6-110">Указывает, что была получена последовательность клавиш CTRL + ALT + DEL.</span><span class="sxs-lookup"><span data-stu-id="a64e6-110">Indicates that a CTRL+ALT+DEL key sequence was received.</span></span>                                                                                      |
| <span data-ttu-id="a64e6-111">ВЛКС \_ SAS \_ Type \_ SC \_ INSERT</span><span class="sxs-lookup"><span data-stu-id="a64e6-111">WLX\_SAS\_TYPE\_SC\_INSERT</span></span>                         | <span data-ttu-id="a64e6-112">Указывает, что [*смарт-карта*](../secgloss/s-gly.md) вставлена в совместимое устройство.</span><span class="sxs-lookup"><span data-stu-id="a64e6-112">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span> |
| <span data-ttu-id="a64e6-113">\_тип SAS \_ влкс \_ SC \_ Remove</span><span class="sxs-lookup"><span data-stu-id="a64e6-113">WLX\_SAS\_TYPE\_SC\_REMOVE</span></span>                         | <span data-ttu-id="a64e6-114">Указывает, что смарт-карта была удалена из совместимого устройства.</span><span class="sxs-lookup"><span data-stu-id="a64e6-114">Indicates that a smart card has been removed from a compatible device.</span></span>                                                                        |
| <span data-ttu-id="a64e6-115">\_тип SAS \_ влкс \_ \_ Выход пользователя</span><span class="sxs-lookup"><span data-stu-id="a64e6-115">WLX\_SAS\_TYPE\_USER\_LOGOFF</span></span>                       | <span data-ttu-id="a64e6-116">Указывает, что пользователь запросил выход из системы.</span><span class="sxs-lookup"><span data-stu-id="a64e6-116">Indicates that a user requested logoff.</span></span>                                                                                                       |
| <span data-ttu-id="a64e6-117">ВЛКС \_ SAS \_ типа \_ скрнсвр \_ timeout</span><span class="sxs-lookup"><span data-stu-id="a64e6-117">WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT</span></span>                   | <span data-ttu-id="a64e6-118">Указывает, что экранная заставка должна запускаться из-за отсутствия вводимых пользователем данных.</span><span class="sxs-lookup"><span data-stu-id="a64e6-118">Indicates that the screen saver should be run due to lack of user input.</span></span>                                                                      |
| <span data-ttu-id="a64e6-119">\_ \_ время ожидания типа SAS влкс \_</span><span class="sxs-lookup"><span data-stu-id="a64e6-119">WLX\_SAS\_TYPE\_TIMEOUT</span></span>                            | <span data-ttu-id="a64e6-120">Указывает, что в течение указанного периода ожидания не было получено ни одного пользовательского ввода.</span><span class="sxs-lookup"><span data-stu-id="a64e6-120">Indicates that no user input was received within the specified time-out period.</span></span>                                                               |



 

<span data-ttu-id="a64e6-121">Для времени ожидания и выхода из системы Winlogon закроет диалоговое окно после отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="a64e6-121">For time-outs and logoffs, Winlogon will close the dialog box after the message has been sent.</span></span> <span data-ttu-id="a64e6-122">Это сообщение отправляется, поэтому операция с диалоговым окном может быть полезной (например, при закрытии в случае выхода из системы).</span><span class="sxs-lookup"><span data-stu-id="a64e6-122">This message is sent so the dialog box operation can respond in a useful manner (for example, by closing itself down if a logoff has occurred).</span></span>

<span data-ttu-id="a64e6-123">Для истечения времени ожидания входное диалоговое окно закрывается с ВЛКС кода диалогового окна \_ \_ ввода \_ .</span><span class="sxs-lookup"><span data-stu-id="a64e6-123">For input time-outs, the dialog box is closed with the code WLX\_DLG\_INPUT\_TIMEOUT.</span></span>

<span data-ttu-id="a64e6-124">Для времени ожидания экранных заставок диалоговое окно закрывается с помощью кода ВЛКС \_ диалогового окна \_ Экранная \_ Заставка \_ .</span><span class="sxs-lookup"><span data-stu-id="a64e6-124">For screen saver time-outs, the dialog box is closed with the code WLX\_DLG\_SCREEN\_SAVER\_TIMEOUT.</span></span>

<span data-ttu-id="a64e6-125">Для выходов из системы диалоговое окно закрывается с кодом ВЛКС \_ диалогового окна " \_ Выход пользователя" \_ .</span><span class="sxs-lookup"><span data-stu-id="a64e6-125">For logoffs, the dialog box operation is closed with the code WLX\_DLG\_USER\_LOGOFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a64e6-126">См. также</span><span class="sxs-lookup"><span data-stu-id="a64e6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a64e6-127">Инициализация Winlogon</span><span class="sxs-lookup"><span data-stu-id="a64e6-127">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="a64e6-128">Состояния Winlogon</span><span class="sxs-lookup"><span data-stu-id="a64e6-128">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="a64e6-129">Поддерживаемые операции диалогового окна "Время использования службы"</span><span class="sxs-lookup"><span data-stu-id="a64e6-129">Supported Dialog Box Service Time-out Operations</span></span>](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[<span data-ttu-id="a64e6-130">Функции поддержки Winlogon</span><span class="sxs-lookup"><span data-stu-id="a64e6-130">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
