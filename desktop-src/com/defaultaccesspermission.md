---
title: дефаултакцесспермиссион
description: Задает список управления доступом (ACL) для участников, которые могут обращаться к классам, для которых не задан параметр Акцесспермиссион.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- COM-значение реестра Дефаултакцесспермиссион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700477"
---
# <a name="defaultaccesspermission"></a><span data-ttu-id="c5f3b-104">дефаултакцесспермиссион</span><span class="sxs-lookup"><span data-stu-id="c5f3b-104">DefaultAccessPermission</span></span>

<span data-ttu-id="c5f3b-105">Задает список управления доступом (ACL) для участников, которые могут обращаться к классам, для которых не задан параметр [**акцесспермиссион**](accesspermission.md) .</span><span class="sxs-lookup"><span data-stu-id="c5f3b-105">Sets the Access Control List (ACL) of the principals that can access classes for which there is no [**AccessPermission**](accesspermission.md) setting.</span></span> <span data-ttu-id="c5f3b-106">Этот список ACL используется только приложениями, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) и не имеют значения **акцесспермиссион** под своим ключом [**AppID**](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="c5f3b-106">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and do not have an **AccessPermission** value under their [**AppID**](appid-key.md) key.</span></span>

> [!Caution]  
> <span data-ttu-id="c5f3b-107">Не рекомендуется изменять это значение, так как это повлияет на все серверные приложения COM, не устанавливающие собственный уровень безопасности на уровне процесса, и может препятствовать их правильной работе.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-107">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="c5f3b-108">Если вы изменяете это значение, чтобы оно влияло на параметры безопасности для конкретного приложения COM, вместо этого следует изменить параметры безопасности для этого конкретного COM-приложения.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-108">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="c5f3b-109">Дополнительные сведения о настройке безопасности на уровне процесса см. в разделе [Настройка безопасности на уровне процесса](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="c5f3b-109">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="c5f3b-110">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="c5f3b-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="c5f3b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c5f3b-111">Remarks</span></span>

<span data-ttu-id="c5f3b-112">Это **\_ двоичное значение reg** .</span><span class="sxs-lookup"><span data-stu-id="c5f3b-112">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="c5f3b-113">Среда выполнения COM на сервере проверяет список управления доступом, описываемый этим значением, при олицетворении вызывающего объекта, пытающегося подключиться к объекту, и его успешное определение того, разрешен или запрещен доступ.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-113">The COM runtime in the server checks the ACL described by this value while impersonating the caller that is attempting to connect to the object, and its success determines whether the access is allowed or disallowed.</span></span> <span data-ttu-id="c5f3b-114">Если проверка доступа завершается неудачно, соединение с объектом запрещено.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-114">If the access-check fails, the connection to the object is disallowed.</span></span> <span data-ttu-id="c5f3b-115">Если это именованное значение не существует, вызов сервера разрешен только участнику сервера и локальной системе.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-115">If this named value does not exist, only the server principal and local system are allowed to call the server.</span></span>

<span data-ttu-id="c5f3b-116">По умолчанию это значение не содержит записей.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-116">By default, this value has no entries in it.</span></span> <span data-ttu-id="c5f3b-117">Только сервер-участник и система могут вызывать сервер.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-117">Only the server principal and system are allowed to call the server.</span></span>

<span data-ttu-id="c5f3b-118">Это значение обеспечивает простой уровень централизованного администрирования доступа к соединению по умолчанию для запуска объектов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c5f3b-118">This value provides a simple level of centralized administration of the default connection access to running objects on a computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5f3b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c5f3b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5f3b-120">**акцесспермиссион**</span><span class="sxs-lookup"><span data-stu-id="c5f3b-120">**AccessPermission**</span></span>](accesspermission.md)
</dt> <dt>

[<span data-ttu-id="c5f3b-121">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="c5f3b-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="c5f3b-122">Настройка безопасности на уровне процесса</span><span class="sxs-lookup"><span data-stu-id="c5f3b-122">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




