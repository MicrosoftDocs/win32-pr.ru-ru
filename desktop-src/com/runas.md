---
title: RunAs
description: Настраивает класс для запуска от имени определенной учетной записи пользователя при активации удаленным клиентом без записи в качестве приложения службы.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Значение реестра RunAs COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700939"
---
# <a name="runas"></a><span data-ttu-id="418b4-104">RunAs</span><span class="sxs-lookup"><span data-stu-id="418b4-104">RunAs</span></span>

<span data-ttu-id="418b4-105">Настраивает класс для запуска от имени определенной учетной записи пользователя при активации удаленным клиентом без записи в качестве приложения службы.</span><span class="sxs-lookup"><span data-stu-id="418b4-105">Configures a class to run under a specific user account when activated by a remote client without being written as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="418b4-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="418b4-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a><span data-ttu-id="418b4-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="418b4-107">Remarks</span></span>

<span data-ttu-id="418b4-108">Значение указывает имя пользователя и должно быть либо в формате *username*, либо в *доменном ***\\*** имени* , либо в строке "Интерактивный пользователь".</span><span class="sxs-lookup"><span data-stu-id="418b4-108">The value specifies the user name and must be either of the form *UserName*, *Domain ***\\*** UserName* or of the string "Interactive User".</span></span> <span data-ttu-id="418b4-109">Можно также указать строки «NT Authority \\ LocalService» (для локальной службы) и «NT Authority \\ NetworkService» (для сетевой службы).</span><span class="sxs-lookup"><span data-stu-id="418b4-109">You can also specify the strings "nt authority\\localservice" (for Local Service) and "nt authority\\networkservice" (for Network Service).</span></span> <span data-ttu-id="418b4-110">\\Если {*AppID \_ GUID*} указывает на сервер COM, который уже запущен или имеет запись в таблице классов, можно также указать строку "NT Authority System".</span><span class="sxs-lookup"><span data-stu-id="418b4-110">You can also specify the string "nt authority\\system" when {*AppID\_GUID*} refers to a COM server that is already started or that has an entry in the class table.</span></span> <span data-ttu-id="418b4-111">Тем не менее нельзя использовать «систему NT Authority \\ » с сервером COM, который еще не запущен.</span><span class="sxs-lookup"><span data-stu-id="418b4-111">However, you cannot use "nt authority\\system" with a COM server that is not already started.</span></span> <span data-ttu-id="418b4-112">Пароль по умолчанию для "NT Authority \\ LocalService", "NT Authority \\ NetworkService" и "система NT Authority \\ " — "" (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="418b4-112">The default password for "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system" is "" (empty string).</span></span>

> [!Note]  
> <span data-ttu-id="418b4-113">Начиная с Windows Vista, для настройки параметров запуска от имени «служба NT Authority» \\ , «NT Authority \\ NetworkService» и «система NT Authority» больше не \\  требуется пустой пароль.</span><span class="sxs-lookup"><span data-stu-id="418b4-113">As of Windows Vista, an empty password is no longer required to configure the "nt authority\\localservice", "nt authority\\networkservice" and "nt authority\\system" **RunAs** settings.</span></span>

 

<span data-ttu-id="418b4-114">Классы, настроенные для запуска от имени конкретного пользователя, могут не регистрироваться под другим удостоверением, поэтому вызовы [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) с этим CLSID завершаются неудачей, если процесс не был запущен com от имени фактического запроса на активацию.</span><span class="sxs-lookup"><span data-stu-id="418b4-114">Classes configured to run as a particular user may not be registered under any other identity, so calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID fail unless the process was launched by COM on behalf of an actual activation request.</span></span>

<span data-ttu-id="418b4-115">Имя пользователя берется из значения **runas** в ключе **AppID** класса.</span><span class="sxs-lookup"><span data-stu-id="418b4-115">The user-name is taken from the **RunAs** value under the class's **AppID** key.</span></span> <span data-ttu-id="418b4-116">Если имя пользователя — "Интерактивный пользователь", сервер выполняется с удостоверением пользователя, который в данный момент вошел в систему и подключен к интерактивному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="418b4-116">If the user name is "Interactive User", the server is run in the identity of the user currently logged on and is connected to the interactive desktop.</span></span>

<span data-ttu-id="418b4-117">В противном случае пароль будет извлечен из части реестра, доступной только администраторам компьютера и системы.</span><span class="sxs-lookup"><span data-stu-id="418b4-117">Otherwise, the password is retrieved from a portion of the registry that is available only to administrators of the computer and to the system.</span></span> <span data-ttu-id="418b4-118">Затем имя пользователя и пароль используются для создания сеанса входа в систему, в котором выполняется сервер.</span><span class="sxs-lookup"><span data-stu-id="418b4-118">The user-name and password are then used to create a logon session in which the server is run.</span></span> <span data-ttu-id="418b4-119">При запуске таким образом пользователь работает с собственным рабочим столом и оконной станцией и не использует дескрипторы окон, буфер обмена или другие элементы пользовательского интерфейса с интерактивным пользователем или другим пользователем, запущенным в других учетных записях пользователей.</span><span class="sxs-lookup"><span data-stu-id="418b4-119">When launched in this way, the user runs with its own desktop and window station and does not share window-handles, the clipboard, or other UI elements with the interactive user or other user running in other user accounts.</span></span>

<span data-ttu-id="418b4-120">Чтобы установить пароль для класса **запуска от имени** , необходимо использовать административное средство DCOMCNFG, установленное в системном каталоге.</span><span class="sxs-lookup"><span data-stu-id="418b4-120">To establish a password for a **RunAs** class, you must use the DCOMCNFG administrative tool installed in the system directory.</span></span>

<span data-ttu-id="418b4-121">Для удостоверений **запуска от имени** , используемых серверами DCOM, учетная запись пользователя, указанная в значении, должна иметь права на вход в качестве пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="418b4-121">For **RunAs** identities used by DCOM servers, the user account specified in the value must have the rights to log on as a batch job.</span></span> <span data-ttu-id="418b4-122">Это право можно добавить с помощью средства администрирования локальной политики безопасности.</span><span class="sxs-lookup"><span data-stu-id="418b4-122">This right can be added using Local Security Policy administrative tool.</span></span> <span data-ttu-id="418b4-123">Перейдите в раздел **Локальные политики** и откройте **Назначение прав пользователя**.</span><span class="sxs-lookup"><span data-stu-id="418b4-123">Go to **Local Policies** and open **User Rights Assignment**.</span></span> <span data-ttu-id="418b4-124">Выберите **Вход в качестве пакетного задания** и добавьте учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="418b4-124">Select **Log on as a batch job**, and add the user account.</span></span>

<span data-ttu-id="418b4-125">Значение **runas** не используется для серверов, настроенных для запуска в качестве служб.</span><span class="sxs-lookup"><span data-stu-id="418b4-125">The **RunAs** value is not used for servers configured to be run as services.</span></span> <span data-ttu-id="418b4-126">Службы COM, которые должны выполняться под удостоверением, отличным от LocalSystem, должны устанавливать соответствующие имя пользователя и пароль с помощью приложения панели управления "службы" или функций контроллера служб.</span><span class="sxs-lookup"><span data-stu-id="418b4-126">COM services that need to run under an identity other than LocalSystem should set the appropriate user name and password using the services control panel applet or the service controller functions.</span></span> <span data-ttu-id="418b4-127">(Дополнительные сведения об этих функциях см. в разделе [службы](/windows/desktop/Services/services).)</span><span class="sxs-lookup"><span data-stu-id="418b4-127">(For more information about these functions, see [Services](/windows/desktop/Services/services).)</span></span>

> [!Note]  
> <span data-ttu-id="418b4-128">Начиная с Microsoft Windows Server 2003, класс AppID явно читается из **\_ \_ \\ классов программного обеспечения локального компьютера \\ hKey \\ AppID**, что, в отличие от большинства разделов реестра, не является взаимозаменяемым **с \_ \_ корневым \\ идентификатором классов hKey**.</span><span class="sxs-lookup"><span data-stu-id="418b4-128">As of Microsoft Windows Server 2003, the class AppID is explicitly read from **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\AppID**, which, unlike most registry keys, is not interchangeable with **HKEY\_CLASSES\_ROOT\\AppID**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="418b4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="418b4-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="418b4-130">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="418b4-130">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 