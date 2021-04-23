---
title: Создание оконной станции и рабочего стола
description: Система автоматически создает интерактивную станцию.
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aff24a29432e3e394a199bf881aa386bf17e71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337484"
---
# <a name="window-station-and-desktop-creation"></a><span data-ttu-id="60603-103">Создание оконной станции и рабочего стола</span><span class="sxs-lookup"><span data-stu-id="60603-103">Window Station and Desktop Creation</span></span>

<span data-ttu-id="60603-104">Система автоматически создает интерактивную станцию.</span><span class="sxs-lookup"><span data-stu-id="60603-104">The system automatically creates the interactive window station.</span></span> <span data-ttu-id="60603-105">Когда интерактивный пользователь входит в систему, система связывается с интерактивной рабочей станцией с сеансом входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="60603-105">When an interactive user logs on, the system associates the interactive window station with the user logon session.</span></span> <span data-ttu-id="60603-106">Система также создает входной Рабочий стол по умолчанию для интерактивной рабочей станции (Winsta0 \\ по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="60603-106">The system also creates the default input desktop for the interactive window station (Winsta0\\default).</span></span> <span data-ttu-id="60603-107">Процессы, запущенные вошедшим в систему пользователем, связаны с \\ рабочим столом Winsta0 Default.</span><span class="sxs-lookup"><span data-stu-id="60603-107">Processes started by the logged-on user are associated with the Winsta0\\default desktop.</span></span>

<span data-ttu-id="60603-108">Процесс может использовать функцию [**креатевиндовстатион**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) для создания новой станции Windows, а также функцию **креатедесктоп** или [**креатедесктопекс**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) для создания нового рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="60603-108">A process can use the [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) function to create a new window station, and the **CreateDesktop** or [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) function to create a new desktop.</span></span> <span data-ttu-id="60603-109">Число создаваемых рабочих столов ограничивается размером кучи системных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="60603-109">The number of desktops that can be created is limited by the size of the system desktop heap.</span></span> <span data-ttu-id="60603-110">Дополнительные сведения см. в разделе [**креатедесктоп**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span><span class="sxs-lookup"><span data-stu-id="60603-110">For more information, see [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span>

<span data-ttu-id="60603-111">Когда Неинтерактивный процесс, например приложение службы, пытается подключиться к рабочей станции, и для сеанса входа в систему не существует станции Windows, система пытается создать оконную станцию и Рабочий стол для сеанса.</span><span class="sxs-lookup"><span data-stu-id="60603-111">When a noninteractive process such as a service application attempts to connect to a window station and no window station exists for the process logon session, the system attempts to create a window station and desktop for the session.</span></span> <span data-ttu-id="60603-112">Имя созданной станции Windows основано на идентификаторе сеанса входа в систему, а рабочий стол имеет имя по умолчанию, как описано здесь:</span><span class="sxs-lookup"><span data-stu-id="60603-112">The name of the created window station is based on the logon session identifier, and the desktop is named default, as described here:</span></span>

-   <span data-ttu-id="60603-113">Если служба выполняется в контексте безопасности учетной записи LocalSystem, но не содержит \_ атрибут "интерактивный процесс службы" \_ , то он использует следующую оконную станцию и Рабочий стол: Service-0x0-3E7 $ \\ Default.</span><span class="sxs-lookup"><span data-stu-id="60603-113">If a service is running in the security context of the LocalSystem account but does not include the SERVICE\_INTERACTIVE\_PROCESS attribute, it uses the following window station and desktop: Service-0x0-3e7$\\default.</span></span> <span data-ttu-id="60603-114">Эта Оконная станция не является интерактивной, поэтому служба не может отобразить пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="60603-114">This window station is not interactive, so the service cannot display a user interface.</span></span> <span data-ttu-id="60603-115">Кроме того, процессы, созданные службой, не могут отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="60603-115">In addition, processes created by the service cannot display a user interface.</span></span>
-   <span data-ttu-id="60603-116">Если служба выполняется в контексте безопасности учетной записи пользователя, имя рабочей станции основано на службе SID пользователя — 0x *Z1* - *Z2*$, где *Z1* — это старшая часть идентификатора безопасности входа, а *Z2* — младшие части идентификатора безопасности входа.</span><span class="sxs-lookup"><span data-stu-id="60603-116">If the service is running in the security context of a user account, the name of the window station is based on the user SID Service-0x *Z1*-*Z2*$, where *Z1* is the high part of the logon SID and *Z2* is the low part of the logon SID.</span></span> <span data-ttu-id="60603-117">Поскольку идентификатор безопасности уникален для сеанса входа в систему, две службы, работающие в одном контексте безопасности, получают отдельные станции Window.</span><span class="sxs-lookup"><span data-stu-id="60603-117">Because a SID is unique to the logon session, two services running in the same security context receive unique window stations.</span></span> <span data-ttu-id="60603-118">Эти оконные станции не являются интерактивными.</span><span class="sxs-lookup"><span data-stu-id="60603-118">These window stations are not interactive.</span></span>

<span data-ttu-id="60603-119">Список управления доступом на уровне пользователей (DACL) для рабочей станции и рабочего стола включает следующие права доступа для учетной записи пользователя службы:</span><span class="sxs-lookup"><span data-stu-id="60603-119">The discretionary access control list (DACL) for the window station and desktop includes the following access rights for the service's user account:</span></span>

<span data-ttu-id="60603-120">Оконная станция:</span><span class="sxs-lookup"><span data-stu-id="60603-120">Window Station:</span></span>

<dl> <span data-ttu-id="60603-121">ВИНСТА \_ акцессклипбоард</span><span class="sxs-lookup"><span data-stu-id="60603-121">WINSTA\_ACCESSCLIPBOARD</span></span>  
<span data-ttu-id="60603-122">ВИНСТА \_ акцессглобалатомс</span><span class="sxs-lookup"><span data-stu-id="60603-122">WINSTA\_ACCESSGLOBALATOMS</span></span>  
<span data-ttu-id="60603-123">ВИНСТА \_ креатедесктоп</span><span class="sxs-lookup"><span data-stu-id="60603-123">WINSTA\_CREATEDESKTOP</span></span>  
<span data-ttu-id="60603-124">ВИНСТА \_ екситвиндовс</span><span class="sxs-lookup"><span data-stu-id="60603-124">WINSTA\_EXITWINDOWS</span></span>  
<span data-ttu-id="60603-125">ВИНСТА \_ реадаттрибутес</span><span class="sxs-lookup"><span data-stu-id="60603-125">WINSTA\_READATTRIBUTES</span></span>  
<span data-ttu-id="60603-126">\_требуются стандартные права \_</span><span class="sxs-lookup"><span data-stu-id="60603-126">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

<span data-ttu-id="60603-127">Настольные ПК:</span><span class="sxs-lookup"><span data-stu-id="60603-127">Desktop:</span></span>

<dl> <span data-ttu-id="60603-128">DESKTOP \_ креатемену</span><span class="sxs-lookup"><span data-stu-id="60603-128">DESKTOP\_CREATEMENU</span></span>  
<span data-ttu-id="60603-129">DESKTOP \_ CREATEWINDOW</span><span class="sxs-lookup"><span data-stu-id="60603-129">DESKTOP\_CREATEWINDOW</span></span>  
<span data-ttu-id="60603-130">\_перечисление Desktop</span><span class="sxs-lookup"><span data-stu-id="60603-130">DESKTOP\_ENUMERATE</span></span>  
<span data-ttu-id="60603-131">DESKTOP \_ хукконтрол</span><span class="sxs-lookup"><span data-stu-id="60603-131">DESKTOP\_HOOKCONTROL</span></span>  
<span data-ttu-id="60603-132">DESKTOP \_ READOBJECTS</span><span class="sxs-lookup"><span data-stu-id="60603-132">DESKTOP\_READOBJECTS</span></span>  
<span data-ttu-id="60603-133">DESKTOP \_ вритеобжектс</span><span class="sxs-lookup"><span data-stu-id="60603-133">DESKTOP\_WRITEOBJECTS</span></span>  
<span data-ttu-id="60603-134">\_требуются стандартные права \_</span><span class="sxs-lookup"><span data-stu-id="60603-134">STANDARD\_RIGHTS\_REQUIRED</span></span>  
</dl>

 

 