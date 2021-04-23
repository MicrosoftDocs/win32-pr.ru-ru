---
title: легацисекуререференцес
description: Определяет, защищены ли вызовы AddRef/Release для приложений, которые не вызывают CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- COM-значение реестра Легацисекуререференцес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700586"
---
# <a name="legacysecurereferences"></a><span data-ttu-id="1561d-104">легацисекуререференцес</span><span class="sxs-lookup"><span data-stu-id="1561d-104">LegacySecureReferences</span></span>

<span data-ttu-id="1561d-105">Определяет  / , защищены ли вызовы **выпуска** AddRef для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="1561d-105">Determines whether **AddRef**/**Release** invocations are secured for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="1561d-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="1561d-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a><span data-ttu-id="1561d-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1561d-107">Remarks</span></span>

<span data-ttu-id="1561d-108">Это значение **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="1561d-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="1561d-109">Значение "Y" или "y" указывает, что **AddRef** и **Release** защищены.</span><span class="sxs-lookup"><span data-stu-id="1561d-109">A value of 'Y' or 'y' indicate that **AddRef** and **Release** are secured.</span></span> <span data-ttu-id="1561d-110">Если это значение реестра отсутствует или имеет значение, отличное от "Y" или "y", **AddRef** и **Release** не защищаются.</span><span class="sxs-lookup"><span data-stu-id="1561d-110">If this registry value is not present or is set to a value other than 'Y' or 'y', **AddRef** and **Release** are not secured.</span></span> <span data-ttu-id="1561d-111">Включение защиты ссылок снижает производительность удаленных вызовов.</span><span class="sxs-lookup"><span data-stu-id="1561d-111">Enabling secure references slows remote calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1561d-112">См. также</span><span class="sxs-lookup"><span data-stu-id="1561d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1561d-113">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="1561d-113">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="1561d-114">Настройка безопасности на уровне процесса</span><span class="sxs-lookup"><span data-stu-id="1561d-114">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




