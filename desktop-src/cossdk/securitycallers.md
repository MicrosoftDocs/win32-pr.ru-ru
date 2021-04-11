---
description: Предоставляет доступ к сведениям об отдельных вызывающих методах в коллекции вызывающих объектов. Коллекция представляет цепь вызовов, завершающихся текущим вызовом, и каждый вызывающий объект в коллекции представляет удостоверение одного вызывающего.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: Класс Секуритикаллерс (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: c757b11bba6a30e8951915e1eace0811b6b6f732
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342192"
---
# <a name="securitycallers-class"></a><span data-ttu-id="43d91-104">Класс Секуритикаллерс</span><span class="sxs-lookup"><span data-stu-id="43d91-104">SecurityCallers class</span></span>

<span data-ttu-id="43d91-105">Предоставляет доступ к сведениям об отдельных вызывающих методах в коллекции вызывающих объектов.</span><span class="sxs-lookup"><span data-stu-id="43d91-105">Provides access to information about individual callers in a collection of callers.</span></span> <span data-ttu-id="43d91-106">Коллекция представляет цепь вызовов, завершающихся текущим вызовом, и каждый вызывающий объект в коллекции представляет удостоверение одного вызывающего.</span><span class="sxs-lookup"><span data-stu-id="43d91-106">The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller.</span></span> <span data-ttu-id="43d91-107">В цепочку вызывающих объектов включаются только те, которые пересекают границу, в которой проверяется безопасность.</span><span class="sxs-lookup"><span data-stu-id="43d91-107">Only callers who cross a boundary where security is checked are included in the chain of callers.</span></span> <span data-ttu-id="43d91-108">(В среде COM+ безопасность проверяется на границах приложений.) Доступ к сведениям об удостоверении конкретного вызывающего объекта предоставляется с помощью класса [**секуритидентити**](securityidentity.md) , коллекции удостоверений.</span><span class="sxs-lookup"><span data-stu-id="43d91-108">(In the COM+ environment, security is checked at application boundaries.) Access to information about a particular caller's identity is provided through the [**SecurityIdentity**](securityidentity.md) class, an identity collection.</span></span>

<span data-ttu-id="43d91-109">Только приложения COM+, использующие безопасность на основе ролей, имеют доступ к классу **секуритикаллерс** .</span><span class="sxs-lookup"><span data-stu-id="43d91-109">Only COM+ applications that use role-based security can access the **SecurityCallers** class.</span></span> <span data-ttu-id="43d91-110">Дополнительные сведения о ролях см. в разделе [Администрирование безопасности на основе ролей](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="43d91-110">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="43d91-111">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="43d91-111">When to implement</span></span>

<span data-ttu-id="43d91-112">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="43d91-112">This class is implemented by COM+.</span></span>



| <span data-ttu-id="43d91-113">Требование</span><span class="sxs-lookup"><span data-stu-id="43d91-113">Requirement</span></span> | <span data-ttu-id="43d91-114">Значение</span><span class="sxs-lookup"><span data-stu-id="43d91-114">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="43d91-115">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="43d91-115">Interfaces</span></span> | [<span data-ttu-id="43d91-116">**исекуритикаллерсколл**</span><span class="sxs-lookup"><span data-stu-id="43d91-116">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="43d91-117">Назначение</span><span class="sxs-lookup"><span data-stu-id="43d91-117">When to use</span></span>

<span data-ttu-id="43d91-118">Используйте этот класс для доступа к методам [**исекуритикаллерсколл**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span><span class="sxs-lookup"><span data-stu-id="43d91-118">Use this class to access the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="43d91-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43d91-119">Remarks</span></span>

<span data-ttu-id="43d91-120">Нельзя напрямую создать объект **секуритикаллерс** .</span><span class="sxs-lookup"><span data-stu-id="43d91-120">You cannot directly create a **SecurityCallers** object.</span></span> <span data-ttu-id="43d91-121">Чтобы использовать методы [**исекуритикаллерсколл**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), необходимо получить ссылку на его реализацию, вызвав [**КОЖЕТКАЛЛКОНТЕКСТ**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), указав IID \_ исекуритикаллконтекст для параметра *riid* .</span><span class="sxs-lookup"><span data-stu-id="43d91-121">To use the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="43d91-122">Затем вызовите метод [**исекуритикаллконтекст:: Get \_ Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) , запрашивающий элемент контекста безопасности вызова, который является коллекцией удостоверений безопасности (например, "директкаллер" или "оригиналкаллер").</span><span class="sxs-lookup"><span data-stu-id="43d91-122">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

<span data-ttu-id="43d91-123">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="43d91-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="43d91-124">Нельзя напрямую создать объект Секуритикаллерс.</span><span class="sxs-lookup"><span data-stu-id="43d91-124">You cannot directly create a SecurityCallers object.</span></span> <span data-ttu-id="43d91-125">Чтобы использовать его свойства, необходимо получить рефернеце для своей реализации с помощью [**жетсекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="43d91-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="43d91-126">Затем получите свойство Item объекта, запрашивая элемент контекста безопасности вызова, который является коллекцией удостоверений безопасности (например, "Директкаллер" или "Оригиналкаллер").</span><span class="sxs-lookup"><span data-stu-id="43d91-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

## <a name="requirements"></a><span data-ttu-id="43d91-127">Требования</span><span class="sxs-lookup"><span data-stu-id="43d91-127">Requirements</span></span>



| <span data-ttu-id="43d91-128">Требование</span><span class="sxs-lookup"><span data-stu-id="43d91-128">Requirement</span></span> | <span data-ttu-id="43d91-129">Значение</span><span class="sxs-lookup"><span data-stu-id="43d91-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="43d91-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43d91-130">Minimum supported client</span></span><br/> | <span data-ttu-id="43d91-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43d91-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="43d91-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43d91-132">Minimum supported server</span></span><br/> | <span data-ttu-id="43d91-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="43d91-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="43d91-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="43d91-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="43d91-135"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="43d91-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43d91-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43d91-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43d91-137">**жетсекуритикаллконтекст**</span><span class="sxs-lookup"><span data-stu-id="43d91-137">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="43d91-138">**исекуритикаллерсколл**</span><span class="sxs-lookup"><span data-stu-id="43d91-138">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="43d91-139">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="43d91-139">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="43d91-140">Администрирование безопасности на основе ролей</span><span class="sxs-lookup"><span data-stu-id="43d91-140">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="43d91-141">**секуритикаллконтекст**</span><span class="sxs-lookup"><span data-stu-id="43d91-141">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="43d91-142">**секуритидентити**</span><span class="sxs-lookup"><span data-stu-id="43d91-142">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

