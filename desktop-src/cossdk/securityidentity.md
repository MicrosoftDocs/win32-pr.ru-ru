---
description: Предоставляет доступ к коллекции сведений о безопасности, представляющих удостоверение вызывающего объекта. С помощью этого класса можно узнать об определенном вызывающем объекте в цепочке вызывающих объектов, которая является частью контекста вызова безопасности.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: Класс Секуритидентити (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "103820429"
---
# <a name="securityidentity-class"></a><span data-ttu-id="f1b74-104">Класс Секуритидентити</span><span class="sxs-lookup"><span data-stu-id="f1b74-104">SecurityIdentity class</span></span>

<span data-ttu-id="f1b74-105">Предоставляет доступ к коллекции сведений о безопасности, представляющих удостоверение вызывающего объекта.</span><span class="sxs-lookup"><span data-stu-id="f1b74-105">Provides access to a collection of security information representing a caller's identity.</span></span> <span data-ttu-id="f1b74-106">С помощью этого класса можно узнать об определенном вызывающем объекте в цепочке вызывающих объектов, которая является частью контекста вызова безопасности.</span><span class="sxs-lookup"><span data-stu-id="f1b74-106">Using this class, you can find out about a particular caller in a chain of callers that is part of the security call context.</span></span> <span data-ttu-id="f1b74-107">Дополнительные сведения о том, как осуществляется доступ к сведениям о контексте вызова безопасности, см. в разделе Программная безопасность компонентов.</span><span class="sxs-lookup"><span data-stu-id="f1b74-107">For more information about how security call context information is accessed, see Programmatic Component Security.</span></span>

<span data-ttu-id="f1b74-108">Только приложения COM+, использующие безопасность на основе ролей, имеют доступ к классу **секуритидентити** .</span><span class="sxs-lookup"><span data-stu-id="f1b74-108">Only COM+ applications that use role-based security can access the **SecurityIdentity** class.</span></span> <span data-ttu-id="f1b74-109">Дополнительные сведения о ролях см. в разделе [Администрирование безопасности на основе ролей](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="f1b74-109">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="f1b74-110">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="f1b74-110">When to implement</span></span>

<span data-ttu-id="f1b74-111">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="f1b74-111">This class is implemented by COM+.</span></span>



| <span data-ttu-id="f1b74-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f1b74-112">Requirement</span></span> | <span data-ttu-id="f1b74-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f1b74-113">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="f1b74-114">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="f1b74-114">Interfaces</span></span> | [<span data-ttu-id="f1b74-115">**исекуритидентитиколл**</span><span class="sxs-lookup"><span data-stu-id="f1b74-115">**ISecurityIdentityColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="f1b74-116">Назначение</span><span class="sxs-lookup"><span data-stu-id="f1b74-116">When to use</span></span>

<span data-ttu-id="f1b74-117">Используйте этот класс для доступа к методам [**исекуритидентитиколл**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span><span class="sxs-lookup"><span data-stu-id="f1b74-117">Use this class to access the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b74-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1b74-118">Remarks</span></span>

<span data-ttu-id="f1b74-119">Нельзя напрямую создать объект **секуритидентити** .</span><span class="sxs-lookup"><span data-stu-id="f1b74-119">You cannot directly create a **SecurityIdentity** object.</span></span> <span data-ttu-id="f1b74-120">Чтобы использовать методы [**исекуритидентитиколл**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), необходимо получить ссылку на его реализацию, вызвав [**КОЖЕТКАЛЛКОНТЕКСТ**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), указав IID \_ исекуритикаллконтекст для параметра *riid* .</span><span class="sxs-lookup"><span data-stu-id="f1b74-120">To use the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="f1b74-121">Затем вызовите метод [**исекуритикаллконтекст:: Get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) , запрашивающий элемент контекста безопасности вызова, который является коллекцией удостоверений безопасности (например, "директкаллер" или "оригиналкаллер").</span><span class="sxs-lookup"><span data-stu-id="f1b74-121">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="f1b74-122">Затем вызовите [**исекуритидентитиколл:: Get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) , чтобы получить элемент идентификатора безопасности (например, "Name" или "AuthenticationService").</span><span class="sxs-lookup"><span data-stu-id="f1b74-122">Then call [**ISecurityIdentityColl::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

<span data-ttu-id="f1b74-123">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="f1b74-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="f1b74-124">Нельзя напрямую создать объект Секуритидентити.</span><span class="sxs-lookup"><span data-stu-id="f1b74-124">You cannot directly create a SecurityIdentity object.</span></span> <span data-ttu-id="f1b74-125">Чтобы использовать его свойства, необходимо получить рефернеце для своей реализации с помощью [**жетсекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="f1b74-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="f1b74-126">Затем получите свойство Item объекта, запрашивая элемент контекста безопасности вызова, который является коллекцией удостоверений безопасности (например, "Директкаллер" или "Оригиналкаллер").</span><span class="sxs-lookup"><span data-stu-id="f1b74-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="f1b74-127">Затем используйте свойство Item объекта Секуритидентити для получения элемента удостоверения безопасности (например, "Name" или "AuthenticationService").</span><span class="sxs-lookup"><span data-stu-id="f1b74-127">Then, use the Item property of the SecurityIdentity object to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b74-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f1b74-128">Requirements</span></span>



| <span data-ttu-id="f1b74-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f1b74-129">Requirement</span></span> | <span data-ttu-id="f1b74-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f1b74-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b74-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1b74-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b74-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f1b74-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f1b74-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1b74-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b74-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f1b74-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f1b74-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f1b74-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1b74-136"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1b74-136"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b74-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1b74-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b74-138">**жетсекуритикаллконтекст**</span><span class="sxs-lookup"><span data-stu-id="f1b74-138">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="f1b74-139">**исекуритикаллерсколл**</span><span class="sxs-lookup"><span data-stu-id="f1b74-139">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="f1b74-140">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="f1b74-140">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="f1b74-141">Администрирование безопасности на основе ролей</span><span class="sxs-lookup"><span data-stu-id="f1b74-141">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="f1b74-142">**секуритикаллконтекст**</span><span class="sxs-lookup"><span data-stu-id="f1b74-142">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="f1b74-143">**секуритикаллерс**</span><span class="sxs-lookup"><span data-stu-id="f1b74-143">**SecurityCallers**</span></span>](securitycallers.md)
</dt> </dl>

 

