---
title: мачинеакцессрестриктион
description: Задает политику ограничения на уровне компьютера для доступа к компоненту.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- COM-значение реестра Мачинеакцессрестриктион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691326"
---
# <a name="machineaccessrestriction"></a><span data-ttu-id="cd578-104">мачинеакцессрестриктион</span><span class="sxs-lookup"><span data-stu-id="cd578-104">MachineAccessRestriction</span></span>

<span data-ttu-id="cd578-105">Задает политику ограничения на уровне компьютера для доступа к компоненту.</span><span class="sxs-lookup"><span data-stu-id="cd578-105">Sets the computer-wide restriction policy for component access.</span></span>

> [!Caution]  
> <span data-ttu-id="cd578-106">Изменение этого значения повлияет на все серверные приложения COM и может препятствовать их правильной работе.</span><span class="sxs-lookup"><span data-stu-id="cd578-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="cd578-107">Если существуют приложения COM-сервера с ограничениями, которые менее строгими по сравнению с ограничениями на уровне компьютера, уменьшение ограничений на уровне компьютера может предоставить этим приложениям нежелательный доступ.</span><span class="sxs-lookup"><span data-stu-id="cd578-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="cd578-108">И наоборот, при увеличении ограничений на уровне компьютера некоторые серверные приложения COM могут быть недоступны при вызове приложений.</span><span class="sxs-lookup"><span data-stu-id="cd578-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="cd578-109">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="cd578-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="cd578-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd578-110">Remarks</span></span>

<span data-ttu-id="cd578-111">Это **\_ двоичное значение reg** .</span><span class="sxs-lookup"><span data-stu-id="cd578-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="cd578-112">Участники, не имеющие разрешений здесь, не могут получить их, даже если разрешения предоставлены значением реестра [дефаултакцесспермиссион](defaultaccesspermission.md) или функцией [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="cd578-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="cd578-113">По умолчанию члены группы «все» могут получать разрешения локального и удаленного доступа, а анонимные пользователи могут получать разрешения локального доступа.</span><span class="sxs-lookup"><span data-stu-id="cd578-113">By default, members of the Everyone group can obtain local and remote access permissions, and anonymous users can obtain local access permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd578-114">См. также</span><span class="sxs-lookup"><span data-stu-id="cd578-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd578-115">Настройка безопасности для приложений COM</span><span class="sxs-lookup"><span data-stu-id="cd578-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




