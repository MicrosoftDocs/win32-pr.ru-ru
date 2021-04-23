---
title: дефаултлаунчпермиссион
description: Определяет список управления доступом (ACL) участников, которые могут запускать классы, не указывающие собственный список ACL через значение реестра Лаунчпермиссион.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- COM-значение реестра Дефаултлаунчпермиссион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700723"
---
# <a name="defaultlaunchpermission"></a><span data-ttu-id="399e2-104">дефаултлаунчпермиссион</span><span class="sxs-lookup"><span data-stu-id="399e2-104">DefaultLaunchPermission</span></span>

<span data-ttu-id="399e2-105">Определяет список управления доступом (ACL) участников, которые могут запускать классы, не указывающие собственный список ACL через значение реестра [**лаунчпермиссион**](launchpermission.md) .</span><span class="sxs-lookup"><span data-stu-id="399e2-105">Defines the Access Control List (ACL) of the principals that can launch classes that do not specify their own ACL through the [**LaunchPermission**](launchpermission.md) registry value.</span></span>

> [!Caution]  
> <span data-ttu-id="399e2-106">Не рекомендуется изменять это значение, так как это повлияет на все серверные приложения COM, не устанавливающие собственный уровень безопасности на уровне процесса, и может препятствовать их правильной работе.</span><span class="sxs-lookup"><span data-stu-id="399e2-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="399e2-107">Если вы изменяете это значение, чтобы оно влияло на параметры безопасности для конкретного приложения COM, вместо этого следует изменить параметры безопасности для этого конкретного COM-приложения.</span><span class="sxs-lookup"><span data-stu-id="399e2-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="399e2-108">Дополнительные сведения о настройке безопасности на уровне процесса см. в разделе [Настройка безопасности на уровне процесса](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="399e2-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="399e2-109">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="399e2-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="399e2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="399e2-110">Remarks</span></span>

<span data-ttu-id="399e2-111">Это **\_ двоичное значение reg** .</span><span class="sxs-lookup"><span data-stu-id="399e2-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="399e2-112">Разрешения на доступ по умолчанию приведены ниже.</span><span class="sxs-lookup"><span data-stu-id="399e2-112">The default access permissions are as follows:</span></span>

-   <span data-ttu-id="399e2-113">Администраторы: разрешить запуск</span><span class="sxs-lookup"><span data-stu-id="399e2-113">Administrators: allow launch</span></span>
-   <span data-ttu-id="399e2-114">СИСТЕМА: разрешить запуск</span><span class="sxs-lookup"><span data-stu-id="399e2-114">SYSTEM: allow launch</span></span>
-   <span data-ttu-id="399e2-115">ИНТЕРАКТИВный: разрешить запуск</span><span class="sxs-lookup"><span data-stu-id="399e2-115">INTERACTIVE: allow launch</span></span>

<span data-ttu-id="399e2-116">Если для сервера задано значение [**лаунчпермиссион**](launchpermission.md) , оно имеет приоритет над значением **дефаултлаунчпермиссион** .</span><span class="sxs-lookup"><span data-stu-id="399e2-116">If the [**LaunchPermission**](launchpermission.md) value is set for a server, it takes precedence over the **DefaultLaunchPermission** value.</span></span> <span data-ttu-id="399e2-117">После получения локального или удаленного запроса на запуск сервера, у которого ключ [**AppID**](appid-key.md) не имеет собственного значения **лаунчпермиссион** , список ACL, описываемый этим значением, проверяется при олицетворении клиента и его успешном выполнении либо разрешает, либо запрещает запуск кода класса.</span><span class="sxs-lookup"><span data-stu-id="399e2-117">Upon receiving a local or remote request to launch a server whose [**AppID**](appid-key.md) key has no **LaunchPermission** value of its own, the ACL described by this value is checked while impersonating the client and its success either allows or disallows the launching of the class code.</span></span>

<span data-ttu-id="399e2-118">Это значение обеспечивает простой уровень централизованного администрирования по умолчанию для запуска доступа к неконтролируемым другим классам на компьютере.</span><span class="sxs-lookup"><span data-stu-id="399e2-118">This value provides a simple level of centralized administration of the default launching access to otherwise unadministered classes on a computer.</span></span> <span data-ttu-id="399e2-119">Например, администратор может использовать средство DCOMCNFG, чтобы настроить систему для разрешения доступа только для чтения для опытных пользователей.</span><span class="sxs-lookup"><span data-stu-id="399e2-119">For example, an administrator might use the DCOMCNFG tool to configure the system to allow read-only access for Power Users.</span></span> <span data-ttu-id="399e2-120">Таким образом, OLE ограничит запросы на запуск кода класса для членов группы опытных пользователей.</span><span class="sxs-lookup"><span data-stu-id="399e2-120">OLE would therefore restrict requests to launch class code to members of the Power Users group.</span></span> <span data-ttu-id="399e2-121">Администратор может впоследствии настроить разрешения на запуск для отдельных классов, чтобы предоставить возможность запускать код класса для других групп или отдельных пользователей по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="399e2-121">An administrator could subsequently configure launch permissions for individual classes to grant the ability to launch class code to other groups or individual users as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="399e2-122">См. также</span><span class="sxs-lookup"><span data-stu-id="399e2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="399e2-123">**лаунчпермиссион**</span><span class="sxs-lookup"><span data-stu-id="399e2-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="399e2-124">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="399e2-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="399e2-125">Настройка безопасности на уровне процесса</span><span class="sxs-lookup"><span data-stu-id="399e2-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




