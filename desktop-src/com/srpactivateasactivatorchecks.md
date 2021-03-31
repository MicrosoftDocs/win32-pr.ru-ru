---
title: српактиватеасактиваторчеккс
description: Определяет, используются ли уровни доверия политики ограниченного использования программ (SRP) во время активации Активатеасактиватор.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- COM-значение реестра Српактиватеасактиваторчеккс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774969"
---
# <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="e235d-104">српактиватеасактиваторчеккс</span><span class="sxs-lookup"><span data-stu-id="e235d-104">SRPActivateAsActivatorChecks</span></span>

<span data-ttu-id="e235d-105">Определяет, используются ли уровни доверия политики ограниченного использования программ (SRP) во время активации Активатеасактиватор.</span><span class="sxs-lookup"><span data-stu-id="e235d-105">Determines whether software restriction policy (SRP) trust levels are used during ActivateAsActivator activations.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e235d-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="e235d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a><span data-ttu-id="e235d-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e235d-107">Remarks</span></span>

<span data-ttu-id="e235d-108">Это значение **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="e235d-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="e235d-109">Строковые значения {N, N, нет, нет, нет} указывает, что серверный объект работает с уровнем доверия SRP объекта клиента, независимо от уровня доверия SRP, с которым оно было настроено.</span><span class="sxs-lookup"><span data-stu-id="e235d-109">String values of {N, n, NO, No, no} indicate that the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which it was configured.</span></span> <span data-ttu-id="e235d-110">Если для этого параметра реестра задано любое другое значение или оно не существует, то уровень доверия SRP, настроенный для объекта сервера, сравнивается с уровнем доверия SRP объекта клиента и для запуска серверного объекта используется более строгий уровень доверия.</span><span class="sxs-lookup"><span data-stu-id="e235d-110">If this registry value is set to any other value or does not exist, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and that the more stringent trust level is used to run the server object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e235d-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e235d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e235d-112">срптрустлевел</span><span class="sxs-lookup"><span data-stu-id="e235d-112">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




