---
title: Предоставление для безопасности клиента RDP
description: Некоторые свойства объекта элемента управления ActiveX удаленный рабочий стол ограничены определенными зонами безопасности URL-адресов Internet Explorer.
ms.assetid: fd20ec03-a5e4-4c3e-9bf5-5fa841e869c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bbb143abd3ec09a7f1aeff67a7b6dfa224b56b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775722"
---
# <a name="providing-for-rdp-client-security"></a><span data-ttu-id="cabf1-103">Предоставление для безопасности клиента RDP</span><span class="sxs-lookup"><span data-stu-id="cabf1-103">Providing for RDP client security</span></span>

<span data-ttu-id="cabf1-104">Чтобы позволить клиентам защищать себя от потенциально ненадежных серверов, некоторые свойства объекта элемента управления ActiveX удаленный рабочий стол ограничены определенными зонами безопасности URL-адресов Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="cabf1-104">To allow clients to protect themselves from potentially untrustworthy servers, some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="cabf1-105">Это означает, что если пользователь, просматривающий веб-страницу, находится в зоне безопасности с более высоким URL-адресом, чем на компьютере, с которым осуществляется просмотр Интернета, эти свойства будут отключены.</span><span class="sxs-lookup"><span data-stu-id="cabf1-105">This means that, when a user browsing the web accesses the page and the page is in a higher URL security zone than the computer they are browsing the web with, these properties are disabled.</span></span> <span data-ttu-id="cabf1-106">Доступ к этим ограниченным свойствам осуществляется с помощью интерфейса [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md) и интерфейса [**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md) , и они доступны в следующих зонах безопасности URL-адресов Internet Explorer:</span><span class="sxs-lookup"><span data-stu-id="cabf1-106">These restricted properties are accessed using the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface and the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and are available in the following Internet Explorer URL security zones:</span></span>

-   <span data-ttu-id="cabf1-107">Мой компьютер</span><span class="sxs-lookup"><span data-stu-id="cabf1-107">My computer</span></span>
-   <span data-ttu-id="cabf1-108">Местная интрасеть</span><span class="sxs-lookup"><span data-stu-id="cabf1-108">Local intranet</span></span>
-   <span data-ttu-id="cabf1-109">Надежные сайты</span><span class="sxs-lookup"><span data-stu-id="cabf1-109">Trusted sites</span></span>

<span data-ttu-id="cabf1-110">Они отключены в этих зонах:</span><span class="sxs-lookup"><span data-stu-id="cabf1-110">They are disabled in these zones:</span></span>

-   <span data-ttu-id="cabf1-111">Интернет</span><span class="sxs-lookup"><span data-stu-id="cabf1-111">Internet</span></span>
-   <span data-ttu-id="cabf1-112">Ограниченные сайты</span><span class="sxs-lookup"><span data-stu-id="cabf1-112">Restricted sites</span></span>

<span data-ttu-id="cabf1-113">При вызове этих ограниченных свойств в веб-приложении службы удаленных рабочих столов необходимо вызвать метод [**имстскакс:: Get \_ Секуредсеттингс**](imstscax-securedsettings.md) и [**имстскакс:: Get \_ секуредсеттингсенаблед**](imstscax-securedsettingsenabled.md) для доступа к свойствам защищенных параметров.</span><span class="sxs-lookup"><span data-stu-id="cabf1-113">If you call these restricted properties within your Remote Desktop Services web application, you should call [**IMsTscAx::get\_SecuredSettings**](imstscax-securedsettings.md) and [**IMsTscAx::get\_SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) to access the Secured Settings properties.</span></span>

<span data-ttu-id="cabf1-114">Ниже перечислены ограниченные свойства, к которым обращается интерфейс **имстсксекуредсеттингс** .</span><span class="sxs-lookup"><span data-stu-id="cabf1-114">The restricted properties that the **IMsTscSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="cabf1-115">[**Стартпрограм**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="cabf1-115">[**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span> <span data-ttu-id="cabf1-116">Это свойство указывает программу, которая будет запускаться при подключении.</span><span class="sxs-lookup"><span data-stu-id="cabf1-116">This property specifies the program that will be started upon connection.</span></span>
-   <span data-ttu-id="cabf1-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span><span class="sxs-lookup"><span data-stu-id="cabf1-117">[**WorkDir**](imstscsecuredsettings-workdir.md).</span></span> <span data-ttu-id="cabf1-118">Это свойство указывает рабочий каталог программы, указанной в [**стартпрограм**](imstscsecuredsettings-startprogram.md).</span><span class="sxs-lookup"><span data-stu-id="cabf1-118">This property specifies the working directory of the program specified in [**StartProgram**](imstscsecuredsettings-startprogram.md).</span></span>
-   <span data-ttu-id="cabf1-119">Во [**весь экран**](imstscsecuredsettings-fullscreen.md).</span><span class="sxs-lookup"><span data-stu-id="cabf1-119">[**FullScreen**](imstscsecuredsettings-fullscreen.md).</span></span> <span data-ttu-id="cabf1-120">Это свойство указывает, будет ли состояние элемента управления при соединении находиться в полноэкранном режиме или в режимах окна.</span><span class="sxs-lookup"><span data-stu-id="cabf1-120">This property specifies whether the state of the control upon connection will be in full-screen or window mode.</span></span> <span data-ttu-id="cabf1-121">Если значение этого свойства равно **true**, соединение будет открыто в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="cabf1-121">If the value of this property is **TRUE**, the connection will be opened in full-screen mode.</span></span> <span data-ttu-id="cabf1-122">Хотя использование свойства " **полноэкранное** " ограничено в перечисленных выше зонах безопасности URL-адресов Internet Explorer, пользователь всегда может перейти в полноэкранный режим после подключения, нажав [сочетание клавиш в полноэкранном режиме (](terminal-services-shortcut-keys.md) Ctrl + Alt + Break).</span><span class="sxs-lookup"><span data-stu-id="cabf1-122">Although the use of the **FullScreen** property is restricted to the Internet Explorer URL security zones listed earlier, a user can always change to full-screen mode after connection by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="cabf1-123">Ниже перечислены свойства, к которым обращается интерфейс **имсрдпклиентсекуредсеттингс** .</span><span class="sxs-lookup"><span data-stu-id="cabf1-123">The properties that the **IMsRdpClientSecuredSettings** interface accesses are the following:</span></span>

-   <span data-ttu-id="cabf1-124">[**Аудиоредиректионмоде**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span><span class="sxs-lookup"><span data-stu-id="cabf1-124">[**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md).</span></span> <span data-ttu-id="cabf1-125">Это свойство указывает, следует ли перенаправлять звуки или воспроизводить звуки на сервере узла сеансов удаленный рабочий стол (на узле сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="cabf1-125">This property specifies whether to redirect sounds, or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>
-   <span data-ttu-id="cabf1-126">[**Кэйбоардхукмоде**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span><span class="sxs-lookup"><span data-stu-id="cabf1-126">[**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md).</span></span> <span data-ttu-id="cabf1-127">Это свойство указывает, как и когда следует применять сочетания клавиш Windows. Например, ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="cabf1-127">This property specifies how and when to apply Windows key combinations; for example, ALT+TAB.</span></span>

<span data-ttu-id="cabf1-128">Следующий скрипт запускает Notepad.exe Майкрософт при подключении.</span><span class="sxs-lookup"><span data-stu-id="cabf1-128">The following script launches Microsoft Notepad.exe upon connection.</span></span> <span data-ttu-id="cabf1-129">Запустите этот скрипт перед вызовом метода [**имстскакс:: Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="cabf1-129">Run this script before calling the [**IMsTscAx::Connect**](imstscax-connect.md) method.</span></span>

``` syntax
if MsRdpClient.SecuredSettingsEnabled then
    MsRdpClient.SecuredSettings.StartProgram = "notepad.exe"
else
    msgbox "Cannot access secured setting (startprogram) in the current browser zone"
end if
```

 

 




