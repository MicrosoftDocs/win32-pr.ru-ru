---
title: Дочерние сеансы
description: Начиная с Windows Server 2012 и Windows 8, удаленный рабочий стол поддерживает концепцию дочернего сеанса, которая является специальным удаленный рабочий столным сеансом замыкания на себя, привязанным к существующему сеансу пользователя.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252809"
---
# <a name="child-sessions"></a><span data-ttu-id="9f05e-103">Дочерние сеансы</span><span class="sxs-lookup"><span data-stu-id="9f05e-103">Child Sessions</span></span>

<span data-ttu-id="9f05e-104">Начиная с Windows Server 2012 и Windows 8, удаленный рабочий стол поддерживает концепцию *дочернего сеанса*, которая является специальным удаленный рабочий столным сеансом замыкания на себя, привязанным к существующему сеансу пользователя.</span><span class="sxs-lookup"><span data-stu-id="9f05e-104">Beginning with Windows Server 2012 and Windows 8, Remote Desktop supports the concept of a *child session*, which is a special loopback Remote Desktop session that is tied to a user's existing session.</span></span>

<span data-ttu-id="9f05e-105">Дочерние сеансы не поддерживаются в следующих операционных системах:</span><span class="sxs-lookup"><span data-stu-id="9f05e-105">Child sessions are not supported on the following operating systems:</span></span>

<dl> <span data-ttu-id="9f05e-106">Windows RT</span><span class="sxs-lookup"><span data-stu-id="9f05e-106">Windows RT</span></span>  
<span data-ttu-id="9f05e-107">Вариант установки Windows Server 2012 Server Core</span><span class="sxs-lookup"><span data-stu-id="9f05e-107">Windows Server 2012 Server Core installation option</span></span>  
<span data-ttu-id="9f05e-108">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="9f05e-108">Microsoft Hyper-V Server 2012</span></span>  
</dl>

<span data-ttu-id="9f05e-109">В любой момент времени в системе может быть только один активный и подключенный дочерний сеанс.</span><span class="sxs-lookup"><span data-stu-id="9f05e-109">A system can only have one active and connected child session at any given time.</span></span>

<span data-ttu-id="9f05e-110">Дочерний сеанс можно завершить, выполнив выход непосредственно из него, или же он завершится после завершения его родительского сеанса.</span><span class="sxs-lookup"><span data-stu-id="9f05e-110">The child session can be terminated by logging off directly from it, or it will be terminated when its parent session terminates.</span></span>

<span data-ttu-id="9f05e-111">Прежде чем дочерние сеансы можно будет использовать в системе, необходимо включить функциональность дочернего сеанса, вызвав функцию [**втсенаблечилдсессионс**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) .</span><span class="sxs-lookup"><span data-stu-id="9f05e-111">Before child sessions can be used on a system, you must enable the child session functionality by calling the [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) function.</span></span> <span data-ttu-id="9f05e-112">Можно также определить, включены ли дочерние сеансы с помощью функции [**втсисчилдсессионсенаблед**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) .</span><span class="sxs-lookup"><span data-stu-id="9f05e-112">You can also determine if child sessions have been enabled by using the [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) function.</span></span>

<span data-ttu-id="9f05e-113">Дочерний сеанс можно создать только из сеанса существующего пользователя, используя [Удаленный рабочий стол элемент управления ActiveX](remote-desktop-activex-control.md) и установив свойство "коннектточилдсессион" с [**имсрдпекстендедсеттингс. Property**](imsrdpextendedsettings-property.md) перед соединением.</span><span class="sxs-lookup"><span data-stu-id="9f05e-113">A child session can only be created from within an existing user's session by using the [Remote Desktop ActiveX control](remote-desktop-activex-control.md) and setting the "ConnectToChildSession" property with [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) prior to connecting.</span></span> <span data-ttu-id="9f05e-114">При удаленный рабочий стол вызове метода [**имстскакс. Connect**](imstscax-connect.md) элемент управления ActiveX автоматически подключается к дочернему сеансу без запроса учетных данных, за исключением случаев, когда пользователь вошел в родительский сеанс с помощью смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="9f05e-114">When the [**IMsTscAx.Connect**](imstscax-connect.md) method is called, the Remote Desktop ActiveX control will automatically log on to the child session without prompting for credentials, except when the user is logged into the parent session using a smart card.</span></span> <span data-ttu-id="9f05e-115">В отличие от обычного сеанса удаленный рабочий стол, пользователю не требуется удаленное интерактивное право на вход в дочерний сеанс, так как это сеанс замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="9f05e-115">Unlike a regular Remote Desktop session, a user does not need the Remote Interactive right to log on to the child session because this is a loopback session.</span></span>

<span data-ttu-id="9f05e-116">Не удается заблокировать дочерний сеанс.</span><span class="sxs-lookup"><span data-stu-id="9f05e-116">A child session cannot be locked.</span></span> <span data-ttu-id="9f05e-117">Экран не заставка и экран входа не отображаются.</span><span class="sxs-lookup"><span data-stu-id="9f05e-117">It will have no screen saver and no logon screen.</span></span> <span data-ttu-id="9f05e-118">Кроме того, в отличие от обычного сеанса, если задана политика текстового входа WinLogon, текст для входа не будет отображаться в этом дочернем сеансе.</span><span class="sxs-lookup"><span data-stu-id="9f05e-118">Also, unlike a regular session, if the WinLogon logon text policy is set, the logon text will not be displayed in this child session.</span></span> <span data-ttu-id="9f05e-119">Кроме того, при установке этих политик не будет действовать подключение к удаленному рабочему столу групповых политик времени ожидания в дочернем сеансе.</span><span class="sxs-lookup"><span data-stu-id="9f05e-119">Also, there will be no effect of Remote Desktop Connection Timeout Group policies on the child session if these policies are set.</span></span>

<span data-ttu-id="9f05e-120">В сочетании с дочерними сеансами используются следующие API:</span><span class="sxs-lookup"><span data-stu-id="9f05e-120">The following APIs are used in conjunction with child sessions:</span></span>

-   [<span data-ttu-id="9f05e-121">**втсенаблечилдсессионс**</span><span class="sxs-lookup"><span data-stu-id="9f05e-121">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [<span data-ttu-id="9f05e-122">**втсисчилдсессионсенаблед**</span><span class="sxs-lookup"><span data-stu-id="9f05e-122">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [<span data-ttu-id="9f05e-123">**втсжетчилдсессионид**</span><span class="sxs-lookup"><span data-stu-id="9f05e-123">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   <span data-ttu-id="9f05e-124">Свойство "Коннектточилдсессион" в [ **Имсрдпекстендедсеттингс. Property**](imsrdpextendedsettings-property.md)</span><span class="sxs-lookup"><span data-stu-id="9f05e-124">"ConnectToChildSession" property in [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)</span></span>

 

 




