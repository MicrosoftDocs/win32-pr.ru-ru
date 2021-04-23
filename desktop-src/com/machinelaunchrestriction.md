---
title: мачинелаунчрестриктион
description: Задает политику ограничения на уровне компьютера для запуска и активации компонента.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- COM-значение реестра Мачинелаунчрестриктион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14dfcfe5535871c6b5b0fe310c94b920c522f05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258919"
---
# <a name="machinelaunchrestriction"></a><span data-ttu-id="bc09e-104">мачинелаунчрестриктион</span><span class="sxs-lookup"><span data-stu-id="bc09e-104">MachineLaunchRestriction</span></span>

<span data-ttu-id="bc09e-105">Задает политику ограничения на уровне компьютера для запуска и активации компонента.</span><span class="sxs-lookup"><span data-stu-id="bc09e-105">Sets the computer-wide restriction policy for component launch and activation.</span></span>

> [!Caution]  
> <span data-ttu-id="bc09e-106">Изменение этого значения повлияет на все серверные приложения COM и может препятствовать их правильной работе.</span><span class="sxs-lookup"><span data-stu-id="bc09e-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="bc09e-107">Если существуют приложения COM-сервера с ограничениями, которые менее строгими по сравнению с ограничениями на уровне компьютера, уменьшение ограничений на уровне компьютера может предоставить этим приложениям нежелательный доступ.</span><span class="sxs-lookup"><span data-stu-id="bc09e-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="bc09e-108">И наоборот, при увеличении ограничений на уровне компьютера некоторые серверные приложения COM могут быть недоступны при вызове приложений.</span><span class="sxs-lookup"><span data-stu-id="bc09e-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="bc09e-109">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="bc09e-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="bc09e-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc09e-110">Remarks</span></span>

<span data-ttu-id="bc09e-111">Это **\_ двоичное значение reg** .</span><span class="sxs-lookup"><span data-stu-id="bc09e-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="bc09e-112">Участники, не имеющие разрешений здесь, не могут получить их, даже если разрешения предоставлены значением реестра [дефаултакцесспермиссион](defaultaccesspermission.md) или функцией [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="bc09e-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="bc09e-113">По умолчанию администраторы могут получать разрешения локального и удаленного запуска и активации, а члены группы «все» могут получить разрешения локальной активации и запуска.</span><span class="sxs-lookup"><span data-stu-id="bc09e-113">By default, administrators may obtain local and remote launch and activation permissions, and members of the Everyone group may obtain local activation and launch permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc09e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="bc09e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc09e-115">Настройка безопасности для приложений COM</span><span class="sxs-lookup"><span data-stu-id="bc09e-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




