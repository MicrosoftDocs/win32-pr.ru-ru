---
title: легациимперсонатионлевел
description: Задает уровень олицетворения по умолчанию для приложений, которые не вызывают CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- COM-значение реестра Легациимперсонатионлевел
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700585"
---
# <a name="legacyimpersonationlevel"></a><span data-ttu-id="0b136-104">легациимперсонатионлевел</span><span class="sxs-lookup"><span data-stu-id="0b136-104">LegacyImpersonationLevel</span></span>

<span data-ttu-id="0b136-105">Задает уровень олицетворения по умолчанию для приложений, которые не вызывают [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="0b136-105">Sets the default level of impersonation for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="0b136-106">Не рекомендуется изменять это значение, так как это повлияет на все серверные приложения COM, не устанавливающие собственный уровень безопасности на уровне процесса, и может препятствовать их правильной работе.</span><span class="sxs-lookup"><span data-stu-id="0b136-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="0b136-107">Если вы изменяете это значение, чтобы оно влияло на параметры безопасности для конкретного приложения COM, вместо этого следует изменить параметры безопасности для этого конкретного COM-приложения.</span><span class="sxs-lookup"><span data-stu-id="0b136-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="0b136-108">Дополнительные сведения о настройке безопасности на уровне процесса см. в разделе [Настройка безопасности на уровне процесса](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="0b136-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="0b136-109">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="0b136-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="0b136-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0b136-110">Remarks</span></span>

<span data-ttu-id="0b136-111">Это значение **\_ слова reg** , эквивалентное \_ \_ константам уровня "RPC C" \_ .</span><span class="sxs-lookup"><span data-stu-id="0b136-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_IMP\_LEVEL constants.</span></span>



| <span data-ttu-id="0b136-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0b136-112">Value</span></span> | <span data-ttu-id="0b136-113">Константа</span><span class="sxs-lookup"><span data-stu-id="0b136-113">Constant</span></span>                        |
|-------|---------------------------------|
| <span data-ttu-id="0b136-114">1</span><span class="sxs-lookup"><span data-stu-id="0b136-114">1</span></span>     | <span data-ttu-id="0b136-115">\_ \_ \_ Анонимный уровень RPC \_ C</span><span class="sxs-lookup"><span data-stu-id="0b136-115">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   |
| <span data-ttu-id="0b136-116">2</span><span class="sxs-lookup"><span data-stu-id="0b136-116">2</span></span>     | <span data-ttu-id="0b136-117">\_Обнаружение на \_ \_ уровне Imp RPC C \_</span><span class="sxs-lookup"><span data-stu-id="0b136-117">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    |
| <span data-ttu-id="0b136-118">3</span><span class="sxs-lookup"><span data-stu-id="0b136-118">3</span></span>     | <span data-ttu-id="0b136-119">\_ \_ \_ олицетворение на уровне \_ Imp RPC C</span><span class="sxs-lookup"><span data-stu-id="0b136-119">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> |
| <span data-ttu-id="0b136-120">4</span><span class="sxs-lookup"><span data-stu-id="0b136-120">4</span></span>     | <span data-ttu-id="0b136-121">\_ \_ \_ ДЕЛЕГАТ уровня Imp RPC \_ C</span><span class="sxs-lookup"><span data-stu-id="0b136-121">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    |



 

<span data-ttu-id="0b136-122">Если это значение реестра отсутствует, уровень олицетворения по умолчанию, установленный системой, — 2 (идентификатор RPC C, определяемый на \_ \_ \_ уровне Imp \_ ).</span><span class="sxs-lookup"><span data-stu-id="0b136-122">If this registry value is not present, the default impersonation level established by the system is 2 (RPC\_C\_IMP\_LEVEL\_IDENTIFY).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b136-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0b136-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b136-124">Регистрация серверов COM</span><span class="sxs-lookup"><span data-stu-id="0b136-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="0b136-125">Настройка безопасности на уровне процесса</span><span class="sxs-lookup"><span data-stu-id="0b136-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




