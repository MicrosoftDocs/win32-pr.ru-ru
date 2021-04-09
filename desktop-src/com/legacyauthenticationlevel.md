---
title: легациаусентикатионлевел
description: Задает уровень проверки подлинности по умолчанию для приложений, которые не вызывают CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- COM-значение реестра Легациаусентикатионлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068624"
---
# <a name="legacyauthenticationlevel"></a><span data-ttu-id="370d7-104">легациаусентикатионлевел</span><span class="sxs-lookup"><span data-stu-id="370d7-104">LegacyAuthenticationLevel</span></span>

<span data-ttu-id="370d7-105">Задает уровень проверки подлинности по умолчанию для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="370d7-105">Sets the default authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="370d7-106">Не рекомендуется изменять это значение, так как это повлияет на все серверные приложения COM, не устанавливающие собственный уровень безопасности на уровне процесса, и может препятствовать их правильной работе.</span><span class="sxs-lookup"><span data-stu-id="370d7-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="370d7-107">Если вы изменяете это значение, чтобы оно влияло на параметры безопасности для конкретного приложения COM, вместо этого следует изменить параметры безопасности для этого конкретного COM-приложения.</span><span class="sxs-lookup"><span data-stu-id="370d7-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="370d7-108">Дополнительные сведения о настройке безопасности на уровне процесса см. в разделе [Настройка безопасности на уровне процесса](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="370d7-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="370d7-109">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="370d7-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="370d7-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="370d7-110">Remarks</span></span>

<span data-ttu-id="370d7-111">Это значение **\_ слова reg** , эквивалентное \_ \_ \_ константам уровня RPC C AUTHN.</span><span class="sxs-lookup"><span data-stu-id="370d7-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="370d7-112">Значение</span><span class="sxs-lookup"><span data-stu-id="370d7-112">Value</span></span> | <span data-ttu-id="370d7-113">Константа</span><span class="sxs-lookup"><span data-stu-id="370d7-113">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="370d7-114">1</span><span class="sxs-lookup"><span data-stu-id="370d7-114">1</span></span>     | <span data-ttu-id="370d7-115">\_уровень RPC \_ C \_ AUTHN \_ None</span><span class="sxs-lookup"><span data-stu-id="370d7-115">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="370d7-116">2</span><span class="sxs-lookup"><span data-stu-id="370d7-116">2</span></span>     | <span data-ttu-id="370d7-117">\_подключение на уровне RPC C \_ AUTHN \_ \_</span><span class="sxs-lookup"><span data-stu-id="370d7-117">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="370d7-118">3</span><span class="sxs-lookup"><span data-stu-id="370d7-118">3</span></span>     | <span data-ttu-id="370d7-119">\_ \_ \_ вызов уровня RPC C \_ AUTHN</span><span class="sxs-lookup"><span data-stu-id="370d7-119">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="370d7-120">4</span><span class="sxs-lookup"><span data-stu-id="370d7-120">4</span></span>     | <span data-ttu-id="370d7-121">\_PKT на уровне RPC C \_ AUTHN \_ \_</span><span class="sxs-lookup"><span data-stu-id="370d7-121">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="370d7-122">5</span><span class="sxs-lookup"><span data-stu-id="370d7-122">5</span></span>     | <span data-ttu-id="370d7-123">\_ \_ \_ \_ целостность PKT RPC C AUTHN Level \_</span><span class="sxs-lookup"><span data-stu-id="370d7-123">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="370d7-124">6</span><span class="sxs-lookup"><span data-stu-id="370d7-124">6</span></span>     | <span data-ttu-id="370d7-125">\_Конфиденциальность RPC C \_ AUTHN \_ Level \_ PKT \_</span><span class="sxs-lookup"><span data-stu-id="370d7-125">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="370d7-126">Если это значение реестра отсутствует, уровень проверки подлинности по умолчанию, установленный системой, — 2 (RPC \_ C \_ AUTHN \_ Connect).</span><span class="sxs-lookup"><span data-stu-id="370d7-126">If this registry value is not present, the default authentication level established by the system is 2 (RPC\_C\_AUTHN\_CONNECT).</span></span>

## <a name="related-topics"></a><span data-ttu-id="370d7-127">См. также</span><span class="sxs-lookup"><span data-stu-id="370d7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="370d7-128">**аусентикатионлевел**</span><span class="sxs-lookup"><span data-stu-id="370d7-128">**AuthenticationLevel**</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="370d7-129">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="370d7-129">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="370d7-130">Настройка безопасности на уровне процесса</span><span class="sxs-lookup"><span data-stu-id="370d7-130">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




