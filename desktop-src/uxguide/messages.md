---
title: Сообщения (основы разработки)
description: Сообщения — это любые виды сообщений, которые требуются пользователям или хотят видеть, когда они используют ваше приложение. Узнайте, как представлять ошибки, предупреждения, подтверждения и уведомления в приложении.
ms.assetid: 700F1F1F-B41D-4C0A-B2EC-91C84E46E526
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dba3296c9824b2153184c45b6a021ea823b4d151
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105693812"
---
# <a name="messages-design-basics"></a><span data-ttu-id="33795-104">Сообщения (основы разработки)</span><span class="sxs-lookup"><span data-stu-id="33795-104">Messages (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="33795-105">Это руководство по проектированию было создано для Windows 7 и не Обновлено для более новых версий Windows.</span><span class="sxs-lookup"><span data-stu-id="33795-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="33795-106">Многие рекомендации по-прежнему применяются в принципе, но презентация и примеры не соответствуют нашим [текущим руководствам по проектированию](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="33795-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="33795-107">Сообщения — это любые виды сообщений, которые требуются пользователям или хотят видеть, когда они используют ваше приложение.</span><span class="sxs-lookup"><span data-stu-id="33795-107">Messages are any kind of message users need or want to see as they use your app.</span></span> <span data-ttu-id="33795-108">Узнайте, как представлять ошибки, предупреждения, подтверждения и уведомления в приложении.</span><span class="sxs-lookup"><span data-stu-id="33795-108">Learn how to present errors, warning, confirmations, and notifications in your app.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="33795-109">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="33795-109">In this section</span></span>



| <span data-ttu-id="33795-110">Раздел</span><span class="sxs-lookup"><span data-stu-id="33795-110">Topic</span></span>                                        | <span data-ttu-id="33795-111">Описание</span><span class="sxs-lookup"><span data-stu-id="33795-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33795-112">сообщения об ошибках</span><span class="sxs-lookup"><span data-stu-id="33795-112">Error Messages</span></span>](mess-error.md)<br/>  | <span data-ttu-id="33795-113">Сообщение об ошибке, которое предупреждает пользователей о проблеме, которая уже произошла.</span><span class="sxs-lookup"><span data-stu-id="33795-113">An error message alerts users of a problem that has already occurred.</span></span> <span data-ttu-id="33795-114">В отличие от этого, предупреждающее сообщение предупреждает пользователей о том, что условие может привести к возникновению проблемы в будущем.</span><span class="sxs-lookup"><span data-stu-id="33795-114">By contrast, a warning message alerts users of a condition that might cause a problem in the future.</span></span> <span data-ttu-id="33795-115">Сообщения об ошибках можно представить с помощью модальных диалоговых окон, сообщений на месте, уведомлений или выносок.</span><span class="sxs-lookup"><span data-stu-id="33795-115">Error messages can be presented using modal dialog boxes, in-place messages, notifications, or balloons.</span></span><br/>                                                  |
| [<span data-ttu-id="33795-116">Предупреждающие сообщения</span><span class="sxs-lookup"><span data-stu-id="33795-116">Warning Messages</span></span>](mess-warn.md)<br/> | <span data-ttu-id="33795-117">Предупреждающее сообщение — это модальное диалоговое окно, сообщение на месте, уведомление или всплывающее оповещение, которое предупреждает пользователя о том, что условие может привести к возникновению проблемы в будущем.</span><span class="sxs-lookup"><span data-stu-id="33795-117">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="33795-118">Подтверждения</span><span class="sxs-lookup"><span data-stu-id="33795-118">Confirmations</span></span>](mess-confirm.md)<br/> | <span data-ttu-id="33795-119">Подтверждение — это модальное диалоговое окно с запросом о том, что пользователь хочет продолжить работу с действием.</span><span class="sxs-lookup"><span data-stu-id="33795-119">A confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span><br/>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="33795-120">Уведомления</span><span class="sxs-lookup"><span data-stu-id="33795-120">Notifications</span></span>](mess-notif.md)<br/>   | <span data-ttu-id="33795-121">Уведомление информирует пользователей о событиях, которые не связаны с текущими действиями пользователя, путем краткого отображения всплывающей подсказки из значка в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="33795-121">A notification informs users of events that are unrelated to the current user activity, by briefly displaying a balloon from an icon in the notification area.</span></span> <span data-ttu-id="33795-122">Уведомление может быть вызвано пользовательским действием или значительным системным событием или может предложить потенциально полезную информацию из Microsoft Windows или приложения.</span><span class="sxs-lookup"><span data-stu-id="33795-122">The notification could result from a user action or significant system event, or could offer potentially useful information from Microsoft Windows or an application.</span></span><br/> |



 

 

