---
title: Установка в качестве приложения службы
description: Установка в качестве приложения службы
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed5c474d73c74b3be40bae773c3d51eadf6c69a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070668"
---
# <a name="installing-as-a-service-application"></a><span data-ttu-id="c1894-103">Установка в качестве приложения службы</span><span class="sxs-lookup"><span data-stu-id="c1894-103">Installing as a Service Application</span></span>

<span data-ttu-id="c1894-104">Помимо запуска в качестве исполняемого файла локального сервера (EXE), COM-объект также может быть упакован для запуска в качестве приложения службы при активации с помощью локального или удаленного клиента.</span><span class="sxs-lookup"><span data-stu-id="c1894-104">In addition to running as a local server executable (EXE), a COM object may also package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="c1894-105">Службы поддерживают многочисленные полезные и пользовательские функции интерфацеâ, включая запуск, остановку, приостановку и перезапуск, а также возможность установить сервер для работы под определенной [учетной записью пользователя](/windows/desktop/Services/service-user-accounts) и с помощью [оконной станции](/windows/desktop/winstation/window-stations).</span><span class="sxs-lookup"><span data-stu-id="c1894-105">Services support numerous useful and user interfaceâ€“integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific [user account](/windows/desktop/Services/service-user-accounts) and [window station](/windows/desktop/winstation/window-stations).</span></span>

<span data-ttu-id="c1894-106">Объект, написанный как служба, устанавливается для использования в COM путем установки значения [LocalService](localservice.md) в качестве ключа [AppID](appid-key.md) и выполнения стандартной установки службы.</span><span class="sxs-lookup"><span data-stu-id="c1894-106">An object written as a service is installed for use by COM by establishing a [LocalService](localservice.md) value under its [AppID](appid-key.md) key and performing a standard service installation.</span></span>

<span data-ttu-id="c1894-107">Классы также могут быть настроены для запуска от имени определенной учетной записи пользователя при активации удаленным клиентом без записи в качестве приложения службы.</span><span class="sxs-lookup"><span data-stu-id="c1894-107">Classes may also be configured to run under a specific user account when activated by a remote client without being written as a service application.</span></span> <span data-ttu-id="c1894-108">Для этого класс устанавливает имя пользователя и пароль, которые будут использоваться, когда SCM запускает свой локальный серверный процесс.</span><span class="sxs-lookup"><span data-stu-id="c1894-108">To do this, the class installs a user name and a password to be used when the SCM launches its local server process.</span></span>

<span data-ttu-id="c1894-109">Если класс настроен таким образом, вызовы [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) с этим CLSID завершатся ошибкой, если процесс не был запущен com от имени фактического запроса на активацию.</span><span class="sxs-lookup"><span data-stu-id="c1894-109">When a class is configured in this fashion, calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID will fail unless the process was launched by COM on behalf of an actual activation request.</span></span> <span data-ttu-id="c1894-110">Иными словами, классы, настроенные для запуска от имени конкретного пользователя, могут не регистрироваться под другим удостоверением.</span><span class="sxs-lookup"><span data-stu-id="c1894-110">In other words, classes configured to run as a particular user may not be registered under any other identity.</span></span>

<span data-ttu-id="c1894-111">Имя пользователя берется из ключевого значения [запуска от имени](runas.md) в ключе AppID класса.</span><span class="sxs-lookup"><span data-stu-id="c1894-111">The user name is taken from the [RunAs](runas.md) named-value under the class's APPID key.</span></span> <span data-ttu-id="c1894-112">Если имя пользователя — "Интерактивный пользователь", код класса выполняется в контексте безопасности вошедшего в систему пользователя и подключается к интерактивной рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="c1894-112">If the user name is "Interactive User", the class code is run in the security context of the currently logged on user and is connected to the interactive window station.</span></span>

<span data-ttu-id="c1894-113">В противном случае пароль будет извлечен из скрытой части реестра, доступной только администраторам компьютера и системы.</span><span class="sxs-lookup"><span data-stu-id="c1894-113">Otherwise, the password is retrieved from a hidden portion of the registry available only to administrators of the machine and to the system.</span></span> <span data-ttu-id="c1894-114">Затем имя пользователя и пароль используются для создания сеанса входа в систему, в котором выполняется код класса.</span><span class="sxs-lookup"><span data-stu-id="c1894-114">The user name and password are then used to create a logon session in which the class code is run.</span></span> <span data-ttu-id="c1894-115">При запуске таким образом код класса выполняется с помощью собственного рабочего стола и станции окна и не использует дескрипторы окон, буфер обмена или другие элементы пользовательского интерфейса с интерактивным пользователем или другими классами, запущенными в других учетных записях пользователя.</span><span class="sxs-lookup"><span data-stu-id="c1894-115">When launched in this way, the class code runs with its own desktop and window-station and does not share window handles, the clipboard, or other user interface elements with the interactive user or other classes running in other user accounts.</span></span>

<span data-ttu-id="c1894-116">Сервер, зарегистрированный с помощью **LocalService** или **runas** , может зарегистрировать объект в таблице выполняющегося объекта, чтобы разрешить любому клиенту подключаться к нему.</span><span class="sxs-lookup"><span data-stu-id="c1894-116">A server registered either with **LocalService** or **RunAs** can register an object in the running object table to allow any client to connect to it.</span></span> <span data-ttu-id="c1894-117">Для этого в вызове [**ируннингобжекттабле:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) на сервере должен быть установлен \_ флаг ротфлагс аллованиклиент.</span><span class="sxs-lookup"><span data-stu-id="c1894-117">To do so, the server's call to [**IRunningObjectTable::Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) must set the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="c1894-118">Параметр сервера этот бит должен иметь имя исполняемого файла в разделе AppID реестра, который ссылается на AppID для исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="c1894-118">A server setting this bit must have its executable name in the AppID section of the registry that refers to the AppID for the executable.</span></span> <span data-ttu-id="c1894-119">Сервер, не зарегистрированный как **LocalService** или **runas**, может не зарегистрировать объект с этим флагом.</span><span class="sxs-lookup"><span data-stu-id="c1894-119">An "activate as activator" server (not registered as either **LocalService** or **RunAs**) may not register an object with this flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1894-120">См. также</span><span class="sxs-lookup"><span data-stu-id="c1894-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1894-121">Регистрация класса при установке</span><span class="sxs-lookup"><span data-stu-id="c1894-121">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="c1894-122">Регистрация работающего сервера EXE</span><span class="sxs-lookup"><span data-stu-id="c1894-122">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="c1894-123">Регистрация объектов в таблице ROT</span><span class="sxs-lookup"><span data-stu-id="c1894-123">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="c1894-124">Самостоятельная регистрация</span><span class="sxs-lookup"><span data-stu-id="c1894-124">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 