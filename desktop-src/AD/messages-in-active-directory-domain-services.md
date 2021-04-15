---
title: Сообщения в домен Active Directory Services
description: Сообщения в домен Active Directory Services работают в Windows 2000 и Windows NT 4,0 с пакетом обновления 6a (SP6a) и более поздней версии с помощью DSClient.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory сообщений AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654175"
---
# <a name="messages-in-active-directory-domain-services"></a><span data-ttu-id="5ef8b-104">Сообщения в домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="5ef8b-104">Messages in Active Directory Domain Services</span></span>

<span data-ttu-id="5ef8b-105">Сообщения в домен Active Directory Services работают в Windows 2000 и Windows NT 4,0 с пакетом обновления 6a (SP6a) и более поздней версии с помощью DSClient.</span><span class="sxs-lookup"><span data-stu-id="5ef8b-105">Messages in Active Directory Domain Services are functional in Windows 2000 and Windows NT 4.0 with Service Pack 6a (SP6a) and later with DSClient.</span></span> <span data-ttu-id="5ef8b-106">Они также работают на рабочих станциях Windows 98/95 с IE 4.01 и более поздних версий и DSClient.</span><span class="sxs-lookup"><span data-stu-id="5ef8b-106">They are also functional in Windows 98/95 workstations with IE4.01 and later and DSClient.</span></span> <span data-ttu-id="5ef8b-107">Однако если в оболочке запускаются страницы свойств из многовариантного выбора, то сообщение [**\_ \_ \_ об ошибке WM адспроп notify**](wm-adsprop-notify-error.md) и соответствующие вспомогательные функции, [**адспропсендеррормессаже**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) и [**адспропшоверрордиалог**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) не работают и не будут отображаться.</span><span class="sxs-lookup"><span data-stu-id="5ef8b-107">However, if multiselect property pages are launched from the shell, then the [**WM\_ADSPROP\_NOTIFY\_ERROR**](wm-adsprop-notify-error.md) message and its corresponding helper functions, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) and [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) are not functional and will not be displayed.</span></span> <span data-ttu-id="5ef8b-108">Если в средстве администрирования запущены страницы свойств, например пользователи и компьютеры AD, то все сообщения будут работать и доступны для отображения на страницах свойств с выборкой.</span><span class="sxs-lookup"><span data-stu-id="5ef8b-108">If multiselect property pages are launched within an admin tool, for example, AD Users and Computers, then all messages are functional and available to be displayed within the multiselect property pages.</span></span>

<span data-ttu-id="5ef8b-109">Службы домен Active Directory Services используют следующие сообщения:</span><span class="sxs-lookup"><span data-stu-id="5ef8b-109">Active Directory Domain Services use the following messages:</span></span>

-   [<span data-ttu-id="5ef8b-110">**\_ \_ применение уведомления WM \_ адспроп**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-110">**WM\_ADSPROP\_NOTIFY\_APPLY**</span></span>](wm-adsprop-notify-apply.md)
-   [<span data-ttu-id="5ef8b-111">**\_ \_ изменение уведомления WM \_ адспроп**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-111">**WM\_ADSPROP\_NOTIFY\_CHANGE**</span></span>](wm-adsprop-notify-change.md)
-   [<span data-ttu-id="5ef8b-112">**\_ \_ ошибка уведомления адспроп \_ WM**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-112">**WM\_ADSPROP\_NOTIFY\_ERROR**</span></span>](wm-adsprop-notify-error.md)
-   [<span data-ttu-id="5ef8b-113">**\_ \_ выход из уведомления WM адспроп \_**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-113">**WM\_ADSPROP\_NOTIFY\_EXIT**</span></span>](wm-adsprop-notify-exit.md)
-   [<span data-ttu-id="5ef8b-114">**\_ \_ \_ передний план уведомления WM адспроп**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-114">**WM\_ADSPROP\_NOTIFY\_FOREGROUND**</span></span>](wm-adsprop-notify-foreground.md)
-   [<span data-ttu-id="5ef8b-115">**WM \_ адспроп \_ Notify \_ пажехвнд**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-115">**WM\_ADSPROP\_NOTIFY\_PAGEHWND**</span></span>](wm-adsprop-notify-pagehwnd.md)
-   [<span data-ttu-id="5ef8b-116">**WM \_ адспроп \_ Notify \_ пажеинит**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-116">**WM\_ADSPROP\_NOTIFY\_PAGEINIT**</span></span>](wm-adsprop-notify-pageinit.md)
-   [<span data-ttu-id="5ef8b-117">**WM \_ адспроп \_ уведомлять \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-117">**WM\_ADSPROP\_NOTIFY\_SETFOCUS**</span></span>](wm-adsprop-notify-setfocus.md)
-   [<span data-ttu-id="5ef8b-118">**\_ \_ Создание листа WM \_ адспроп**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-118">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
-   [<span data-ttu-id="5ef8b-119">**\_ \_ \_ уведомление о закрытии листа WM DSA \_**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-119">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
-   [<span data-ttu-id="5ef8b-120">**\_ \_ \_ уведомление о создании листа WM DSA \_**</span><span class="sxs-lookup"><span data-stu-id="5ef8b-120">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)

 

 




