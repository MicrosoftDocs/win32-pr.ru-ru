---
title: енабледком
description: Управляет глобальной политикой активации и вызова компьютера. Только администраторы и система имеют полный доступ к этой части реестра. Все остальные пользователи имеют доступ только для чтения.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- COM-значение реестра Енабледком
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410794"
---
# <a name="enabledcom"></a><span data-ttu-id="cef39-106">енабледком</span><span class="sxs-lookup"><span data-stu-id="cef39-106">EnableDCOM</span></span>

<span data-ttu-id="cef39-107">Управляет глобальной политикой активации и вызова компьютера.</span><span class="sxs-lookup"><span data-stu-id="cef39-107">Controls the global activation and call policies of the machine.</span></span> <span data-ttu-id="cef39-108">Только администраторы и система имеют полный доступ к этой части реестра.</span><span class="sxs-lookup"><span data-stu-id="cef39-108">Only administrators and the system have full access to this portion of the registry.</span></span> <span data-ttu-id="cef39-109">Все остальные пользователи имеют доступ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cef39-109">All other users have read-only access.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="cef39-110">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="cef39-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a><span data-ttu-id="cef39-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cef39-111">Remarks</span></span>

<span data-ttu-id="cef39-112">Это значение **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="cef39-112">This is a **REG\_SZ** value.</span></span>



| <span data-ttu-id="cef39-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cef39-113">Value</span></span>    | <span data-ttu-id="cef39-114">Описание</span><span class="sxs-lookup"><span data-stu-id="cef39-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cef39-115">N (или n)</span><span class="sxs-lookup"><span data-stu-id="cef39-115">N (or n)</span></span> | <span data-ttu-id="cef39-116">Удаленные клиенты не могут запускать серверы или подключаться к объектам на этом компьютере.</span><span class="sxs-lookup"><span data-stu-id="cef39-116">No remote clients may launch servers or connect to objects on this computer.</span></span> <span data-ttu-id="cef39-117">Локальные клиенты не могут получить доступ к удаленным серверам DCOM; весь трафик DCOM блокируется.</span><span class="sxs-lookup"><span data-stu-id="cef39-117">Local clients cannot access remote DCOM servers; all DCOM traffic is blocked.</span></span> <span data-ttu-id="cef39-118">Локальный запуск кода класса и подключение к объектам разрешены для каждого класса в соответствии со значением и разрешениями на доступ к значению реестра [**лаунчпермиссион**](launchpermission.md) класса и глобальному значению реестра [**дефаултлаунчпермиссион**](defaultlaunchpermission.md) .</span><span class="sxs-lookup"><span data-stu-id="cef39-118">Local launching of class code and connecting to objects are allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span> |
| <span data-ttu-id="cef39-119">Y (или y)</span><span class="sxs-lookup"><span data-stu-id="cef39-119">Y (or y)</span></span> | <span data-ttu-id="cef39-120">Запуск серверов и подключение к объектам с помощью удаленных клиентов разрешено для каждого класса в соответствии со значением и разрешениями на доступ к значению реестра [**лаунчпермиссион**](launchpermission.md) класса и глобальному значению реестра [**дефаултлаунчпермиссион**](defaultlaunchpermission.md) .</span><span class="sxs-lookup"><span data-stu-id="cef39-120">Launching of servers and connecting to objects by remote clients is allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span>                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="cef39-121">См. также</span><span class="sxs-lookup"><span data-stu-id="cef39-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cef39-122">**дефаултлаунчпермиссион**</span><span class="sxs-lookup"><span data-stu-id="cef39-122">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="cef39-123">**лаунчпермиссион**</span><span class="sxs-lookup"><span data-stu-id="cef39-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="cef39-124">Безопасность в COM</span><span class="sxs-lookup"><span data-stu-id="cef39-124">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




