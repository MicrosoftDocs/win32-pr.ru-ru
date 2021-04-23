---
title: локальная служба.
description: Устанавливает объект как приложение службы.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Значение реестра LocalService — COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103891145"
---
# <a name="localservice"></a><span data-ttu-id="c2e2e-104">локальная служба.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-104">LocalService</span></span>

<span data-ttu-id="c2e2e-105">Устанавливает объект как приложение службы.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-105">Installs an object as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c2e2e-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="c2e2e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a><span data-ttu-id="c2e2e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2e2e-107">Remarks</span></span>

<span data-ttu-id="c2e2e-108">Помимо запуска в качестве исполняемого файла локального сервера (EXE), COM-объект может также выбрать сам пакет для запуска в качестве приложения службы при активации с помощью локального или удаленного клиента.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-108">In addition to running as a local server executable (EXE), a COM object may also choose to package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="c2e2e-109">Службы поддерживают многочисленные полезные функции администрирования, интегрированные с интерфейсом пользователя, включая локальные и удаленные запуски, остановку, приостановку и перезапуск, а также возможность установить сервер для работы под определенной учетной записью пользователя и с помощью оконной станции.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-109">Services support numerous useful and UI-integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific user account and window station.</span></span>

<span data-ttu-id="c2e2e-110">Объект, написанный как служба, устанавливается для использования в COM путем установки значения **LocalService** и выполнения стандартной установки службы.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-110">An object written as a service is installed for use by COM by establishing a **LocalService** value and performing a standard service installation.</span></span> <span data-ttu-id="c2e2e-111">Для параметра **LocalService** должно быть задано имя службы, настроенное в **\_ \_ \\ \\ CurrentControlSet \\ Services System локального компьютера**, в качестве значения **reg \_ SZ** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-111">The **LocalService** value must be set to the service name, as configured in **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services**, as the default **REG\_SZ** value.</span></span>

<span data-ttu-id="c2e2e-112">Если задана **Локальная** служба, любая строка, назначенная [**сервицепараметерс**](serviceparameters.md) , передается в качестве аргумента командной строки в службу при запуске.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-112">When **LocalService** is set, any string assigned to [**ServiceParameters**](serviceparameters.md) is passed as a command-line argument to the service as it is being launched.</span></span>

<span data-ttu-id="c2e2e-113">Конфигурация службы является предпочтительной во многих ситуациях, когда возможности локальных и удаленных интерфейсов API управления службами и пользовательского интерфейса могут быть полезны для служб, предоставляемых объектом.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-113">The service configuration is preferred in many situations where the capabilities of the local and remote service management APIs and user interface might be useful for the services that the object provides.</span></span> <span data-ttu-id="c2e2e-114">Например, использование существующей административной структуры архитектуры службы должна быть очевидным выбором, если объект является длительным или полностью поддерживает такие концепции, как запуск, остановка, сброс или приостановка.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-114">For example, leveraging the existing administrative framework of the service architecture should be an obvious choice if the object is long-lived or readily supports concepts such as starting, stopping, resetting, or pausing.</span></span>

<span data-ttu-id="c2e2e-115">Службы могут быть настроены динамически и могут быть настроены для автоматического запуска при загрузке компьютера или запуска по запросу клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-115">Services can be dynamically configured and can be configured to run automatically when the machine boots, or to be launched when requested by a client application.</span></span>

<span data-ttu-id="c2e2e-116">При реализации классов в качестве служб следует учитывать следующие моменты.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-116">If you are implementing classes as services, you should be aware of the following points:</span></span>

-   <span data-ttu-id="c2e2e-117">Это значение используется в качестве параметра для ключа [**LocalServer32**](localserver32.md) для локальной и удаленной активации рекуестсâ € **' если существует** и ссылается на допустимую службу, ключ **LocalServer32** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-117">This value is used in preference to the [**LocalServer32**](localserver32.md) key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>
-   <span data-ttu-id="c2e2e-118">В настоящее время на компьютере может выполняться только один экземпляр приложения службы.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-118">Currently, only a single instance of a service application may be running at a given time on a computer.</span></span> <span data-ttu-id="c2e2e-119">Поэтому службы COM должны зарегистрировать объекты класса при запуске с помощью РЕГКЛС \_ мултиплеусе для поддержки нескольких клиентов.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-119">COM services must therefore register their class objects on launch using REGCLS\_MULTIPLEUSE to support multiple clients.</span></span>
-   <span data-ttu-id="c2e2e-120">Для правильного запуска и инициализации службы COM, настроенные для автоматического запуска при загрузке компьютера, должны содержать службы RPCSS в списке зависимых служб.</span><span class="sxs-lookup"><span data-stu-id="c2e2e-120">To launch and initialize properly, COM services configured to run automatically when a machine boots must include RPCSS in their list of dependent services.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2e2e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c2e2e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2e2e-122">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="c2e2e-122">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="c2e2e-123">**сервицепараметерс**</span><span class="sxs-lookup"><span data-stu-id="c2e2e-123">**ServiceParameters**</span></span>](serviceparameters.md)
</dt> <dt>

[<span data-ttu-id="c2e2e-124">Службы</span><span class="sxs-lookup"><span data-stu-id="c2e2e-124">Services</span></span>](/windows/desktop/Services/services)
</dt> </dl>

 

 