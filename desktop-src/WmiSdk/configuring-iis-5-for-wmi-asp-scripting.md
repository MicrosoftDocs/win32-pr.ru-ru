---
description: Все параметры проверки подлинности выполняются с помощью диспетчер служб Интернета.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Настройка IIS 5,0 и более поздних версий для сценариев ASP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711757"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a><span data-ttu-id="b7d05-103">Настройка IIS 5,0 и более поздних версий для сценариев ASP WMI</span><span class="sxs-lookup"><span data-stu-id="b7d05-103">Configuring IIS 5.0 and Later for WMI ASP Scripting</span></span>

<span data-ttu-id="b7d05-104">Все параметры проверки подлинности выполняются с помощью диспетчер служб Интернета.</span><span class="sxs-lookup"><span data-stu-id="b7d05-104">All authentication settings are made through the Internet Services Manager.</span></span>

<span data-ttu-id="b7d05-105">При настройке безопасности Internet Information Server (IIS) 5,0 и IIS 6,0 для сценариев ASP WMI необходимо учитывать следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="b7d05-105">When configuring Internet Information Server (IIS) 5.0 and IIS 6.0 security for WMI ASP scripts, consider the following issues:</span></span>

-   [<span data-ttu-id="b7d05-106">Уровень проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b7d05-106">Authentication level</span></span>](#authentication-level)

    <span data-ttu-id="b7d05-107">Можно настроить на уровне сервера, каталога или файла.</span><span class="sxs-lookup"><span data-stu-id="b7d05-107">You can configure at the server, directory, or file level.</span></span>

-   [<span data-ttu-id="b7d05-108">Настройка проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b7d05-108">Authentication setting</span></span>](#authentication-setting)

    <span data-ttu-id="b7d05-109">Для проверки подлинности можно задать значение анонимно, интегрированные окна или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="b7d05-109">You can set authentication to Anonymous, Integrated Windows, or both.</span></span>

-   [<span data-ttu-id="b7d05-110">Защита</span><span class="sxs-lookup"><span data-stu-id="b7d05-110">Protection</span></span>](#protection)

    <span data-ttu-id="b7d05-111">Можно настроить выполнение ASP в процессе (низкий уровень защиты) или вне процесса с помощью Dllhost.exe (среднего или высокого уровня защиты).</span><span class="sxs-lookup"><span data-stu-id="b7d05-111">You can set the ASP to run in-process (low protection), or out-of-process by using Dllhost.exe (medium or high protection).</span></span>

## <a name="authentication-level"></a><span data-ttu-id="b7d05-112">Уровень проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b7d05-112">Authentication Level</span></span>

<span data-ttu-id="b7d05-113">Для повышения безопасности можно настроить проверку подлинности на уровне каталога или файла.</span><span class="sxs-lookup"><span data-stu-id="b7d05-113">For added security, you can configure the authentication at the directory or file level.</span></span>

<span data-ttu-id="b7d05-114">Если проверка подлинности установлена на уровне сервера, все последующие каталоги и файлы соответствуют проверке подлинности сервера, если только на уровне каталога или файла не было явно изменено.</span><span class="sxs-lookup"><span data-stu-id="b7d05-114">If authentication is set at the server level, all subsequent directories and files adhere to the server authentication unless explicitly altered at the directory or file level.</span></span> <span data-ttu-id="b7d05-115">Можно создать структуру каталогов, которая будет содержать все сценарии ASP WMI, в которых страницы HTML и планах ASP, относящиеся к WMI, можно настроить независимо от остальной части сервера.</span><span class="sxs-lookup"><span data-stu-id="b7d05-115">You can create a directory structure to contain all WMI ASP scripts where HTML pages and ASPs specific to WMI can be configured independently from the rest of the server.</span></span> <span data-ttu-id="b7d05-116">Чтобы изменить уровень проверки подлинности сервера, каталога или файла, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b7d05-116">Perform the following procedure to change the authentication level of a server, directory, or file.</span></span>

<span data-ttu-id="b7d05-117">**Настройка проверки подлинности на любом уровне**</span><span class="sxs-lookup"><span data-stu-id="b7d05-117">**To set the authentication at any level**</span></span>

1.  <span data-ttu-id="b7d05-118">На панели управления дважды щелкните **Администрирование**, а затем дважды щелкните оснастку IIS.</span><span class="sxs-lookup"><span data-stu-id="b7d05-118">In Control Panel, double-click **Administrative Tools**, and then double-click the IIS snap-in.</span></span>

2.  <span data-ttu-id="b7d05-119">Найдите значок страницы ASP, а затем откройте свойства заданного уровня, который может быть сервером, каталогом или файлом.</span><span class="sxs-lookup"><span data-stu-id="b7d05-119">Locate the ASP page icon, and then open the properties for the level to set, which can be server, directory, or file.</span></span>

    > [!Note]  
    > <span data-ttu-id="b7d05-120">Параметры проверки подлинности расположены на вкладке **Безопасность каталога** или **Безопасность файла** страницы **свойств**.</span><span class="sxs-lookup"><span data-stu-id="b7d05-120">Authentication settings are located on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

     

## <a name="authentication-setting"></a><span data-ttu-id="b7d05-121">Настройка проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b7d05-121">Authentication Setting</span></span>

<span data-ttu-id="b7d05-122">Для сценариев ASP WMI сочетание отключенной анонимной проверки подлинности (снято) и встроенной проверки подлинности Windows (установлен) обеспечивает большую возможность настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="b7d05-122">For WMI ASP scripts, the combination of Anonymous authentication turned off (unchecked), and Integrated Windows authentication turned on (checked) provides greater opportunity to set security.</span></span> <span data-ttu-id="b7d05-123">Чтобы использовать параметры проверки подлинности с помощью NT LAN Manager (NTLM), Passport или Digest IIS, необходимо включить разрешения на удаленное включение, так как пользователь обрабатывается как сетевое удостоверение и регистрируется удаленно.</span><span class="sxs-lookup"><span data-stu-id="b7d05-123">To use NT LAN Manager (NTLM), Passport, or Digest IIS authentication settings, you must turn on the remote enable privileges, because the user is treated as a network identity and logged remotely.</span></span> <span data-ttu-id="b7d05-124">Параметр Remote Enable не требуется для анонимной и обычной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b7d05-124">The remote enable setting is not required for Anonymous and Basic authentication.</span></span> <span data-ttu-id="b7d05-125">Однако при использовании анонимной и обычной проверки подлинности система гораздо менее безопасна.</span><span class="sxs-lookup"><span data-stu-id="b7d05-125">However, the system is much less secure when you are using Anonymous and Basic authentication.</span></span>

<span data-ttu-id="b7d05-126">Если анонимная проверка подлинности используется с встроенной проверкой подлинности Windows или без нее, самый безопасный подход заключается в использовании входа, требующего ввода имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="b7d05-126">If Anonymous authentication is used with or without Integrated Windows authentication, the most secure approach is to use a logon that requires a user to enter a username and password.</span></span> <span data-ttu-id="b7d05-127">При входе по умолчанию используется удостоверение IIS, но можно создать вход с помощью специальных разрешений, предназначенных для сценариев ASP WMI, которые можно использовать в качестве учетной записи для анонимных или гостевых подключений.</span><span class="sxs-lookup"><span data-stu-id="b7d05-127">The default logon is the IIS identity, but a logon can be created by using specific permissions suited for the WMI ASP Scripts that can be used as the account for the anonymous or guest connections.</span></span>

<span data-ttu-id="b7d05-128">Если выбран идентификатор входа, не являющийся удостоверением IIS, снимите флажок **Разрешить управление паролем в IIS** и введите правильный пароль.</span><span class="sxs-lookup"><span data-stu-id="b7d05-128">If you choose a logon identifier that is not an IIS identity, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="b7d05-129">Это заставляет все анонимные или гостевые подключения использовать идентификатор входа.</span><span class="sxs-lookup"><span data-stu-id="b7d05-129">This forces all anonymous or guest connections to use the logon identifier.</span></span> <span data-ttu-id="b7d05-130">Создавая имя входа отдельно от удостоверения IIS, привилегии учетной записи, обращающейся к WMI, можно контролировать, не затрагивая другие каталоги или файлы на сервере IIS — если только проверка подлинности не установлена на уровне сервера.</span><span class="sxs-lookup"><span data-stu-id="b7d05-130">By creating a logon separate from the IIS identity, the privileges of an account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="b7d05-131">Выполните следующую процедуру, чтобы задать требования к проверке подлинности для страницы ASP с помощью оснастки IIS на панели управления.</span><span class="sxs-lookup"><span data-stu-id="b7d05-131">Perform the following procedure to set the authentication requirements for the ASP page using the IIS snap-in in the Control Panel.</span></span>

<span data-ttu-id="b7d05-132">**Чтобы перейти к параметру учетной записи**</span><span class="sxs-lookup"><span data-stu-id="b7d05-132">**To get to the account setting**</span></span>

1.  <span data-ttu-id="b7d05-133">На панели управления дважды щелкните значок " **Администрирование** ", откройте оснастку "службы IIS", перейдите на страницу ASP и откройте свойства заданного уровня, который может быть сервером, каталогом или файлом.</span><span class="sxs-lookup"><span data-stu-id="b7d05-133">In Control Panel, double-click the **Administrative Tools** icon, open the IIS snap-in, locate your ASP page, and open the properties of the level to set, which can be server, directory, or file.</span></span>

    <span data-ttu-id="b7d05-134">Параметры проверки подлинности можно найти на вкладке **Безопасность каталога** или **Безопасность файла** на странице **свойств** .</span><span class="sxs-lookup"><span data-stu-id="b7d05-134">Authentication settings can be found on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

2.  <span data-ttu-id="b7d05-135">В области анонимная проверка подлинности нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="b7d05-135">In the Anonymous authentication area, click **Edit**.</span></span>

3.  <span data-ttu-id="b7d05-136">Если выбран идентификатор входа, отличный от удостоверения IIS, снимите флажок **разрешить службе IIS управлять паролем** и введите правильный пароль.</span><span class="sxs-lookup"><span data-stu-id="b7d05-136">If a logon identifier other than the IIS identity is selected, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="b7d05-137">Это заставляет все анонимные или гостевые подключения использовать идентификатор входа.</span><span class="sxs-lookup"><span data-stu-id="b7d05-137">This forces all anonymous or guest connections to use the logon identifier.</span></span>

<span data-ttu-id="b7d05-138">При использовании имени входа, отличного от удостоверения IIS, привилегии учетной записи, обращающейся к WMI, можно контролировать, не затрагивая другие каталоги или файлы на сервере IIS, если только проверка подлинности не установлена на уровне сервера.</span><span class="sxs-lookup"><span data-stu-id="b7d05-138">By using a logon different from the IIS identity, the privileges of the account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="b7d05-139">Предыдущая конфигурация позволяет серверу IIS использовать анонимную проверку подлинности в некоторых областях, а также интегрированную аутентификацию Windows или смешанную проверку подлинности в других.</span><span class="sxs-lookup"><span data-stu-id="b7d05-139">The previous configuration allows the IIS server to use Anonymous authentication in some areas, and Integrated Windows or mixed authentication in others.</span></span>

## <a name="protection"></a><span data-ttu-id="b7d05-140">Защита</span><span class="sxs-lookup"><span data-stu-id="b7d05-140">Protection</span></span>

<span data-ttu-id="b7d05-141">Последнее замечание при настройке сервера IIS — какую защиту использовать при выполнении ASP.</span><span class="sxs-lookup"><span data-stu-id="b7d05-141">The last consideration when configuring the IIS server is which protection to use when executing an ASP.</span></span>

<span data-ttu-id="b7d05-142">Вы можете настроить ASP для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="b7d05-142">You can set an ASP to run the following:</span></span>

-   <span data-ttu-id="b7d05-143">Внутрипроцессный в IIS (низкая защита).</span><span class="sxs-lookup"><span data-stu-id="b7d05-143">In-process to IIS (low protection).</span></span>

-   <span data-ttu-id="b7d05-144">Внешние к службам IIS с Dllhost.exe как в пуле, так и вне процесса (в составе пула со средним уровнем защиты).</span><span class="sxs-lookup"><span data-stu-id="b7d05-144">External to IIS with Dllhost.exe as pooled or out-of-process (pooled medium protection).</span></span>

-   <span data-ttu-id="b7d05-145">Вне процесса (высокая защита).</span><span class="sxs-lookup"><span data-stu-id="b7d05-145">Out-of-process self-host (high protection).</span></span>

> [!Note]  
> <span data-ttu-id="b7d05-146">Для лучшего баланса безопасности и производительности используйте узел в составе пула.</span><span class="sxs-lookup"><span data-stu-id="b7d05-146">For the best balance of security and performance, use pooled host.</span></span>

 

 

 



