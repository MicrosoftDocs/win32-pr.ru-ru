---
title: српруннингобжектчеккс
description: Определяет, будут ли попытки подключения к выполняемым объектам выводятся на экран совместимые уровни доверия политики ограниченного использования программ (SRP).
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- COM-значение реестра Српруннингобжектчеккс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774966"
---
# <a name="srprunningobjectchecks"></a><span data-ttu-id="6dd6e-104">српруннингобжектчеккс</span><span class="sxs-lookup"><span data-stu-id="6dd6e-104">SRPRunningObjectChecks</span></span>

<span data-ttu-id="6dd6e-105">Определяет, будут ли попытки подключения к выполняемым объектам выводятся на экран совместимые уровни доверия политики ограниченного использования программ (SRP).</span><span class="sxs-lookup"><span data-stu-id="6dd6e-105">Determines whether attempts to connect to running objects are screened for compatible software restriction policy (SRP) trust levels.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6dd6e-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="6dd6e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a><span data-ttu-id="6dd6e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6dd6e-107">Remarks</span></span>

<span data-ttu-id="6dd6e-108">Это значение **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="6dd6e-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="6dd6e-109">Строковые значения {N, N, нет, нет, нет} указывает, что попытки подключения к работающим объектам не отображаются на экране для совместимых уровней безопасности SRP.</span><span class="sxs-lookup"><span data-stu-id="6dd6e-109">String values of {N, n, NO, No, no} indicate that attempts to connect to running objects are not screened for compatible SRP trust levels.</span></span> <span data-ttu-id="6dd6e-110">Если для этого параметра реестра задано любое другое значение или оно не существует, то выполняющийся объект не может иметь менее строгий уровень доверия SRP, чем объект клиента.</span><span class="sxs-lookup"><span data-stu-id="6dd6e-110">If this registry value is set to any other value or does not exist, the running object cannot have a less stringent SRP trust level than the client object.</span></span> <span data-ttu-id="6dd6e-111">Например, выполняющийся объект не может иметь неразрешенный уровень доверия, если у клиентского объекта есть неограниченный уровень доверия.</span><span class="sxs-lookup"><span data-stu-id="6dd6e-111">For example, the running object cannot have a Disallowed trust level if the client object has an Unrestricted trust level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dd6e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="6dd6e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dd6e-113">срптрустлевел</span><span class="sxs-lookup"><span data-stu-id="6dd6e-113">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




