---
description: Предоставляет доступ к контексту безопасности текущего вызова, который содержит сведения о вызывающих объектах объекта.
ms.assetid: e8ac05fb-6665-4e57-b64e-82d9799d29d4
title: Класс Секуритикаллконтекст (Комсвкс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallContext
api_type:
- COM
ms.openlocfilehash: bd15b7e0317a507a2340cc148bb927bb5d94a37b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105713339"
---
# <a name="securitycallcontext-class"></a><span data-ttu-id="05906-103">Класс Секуритикаллконтекст</span><span class="sxs-lookup"><span data-stu-id="05906-103">SecurityCallContext class</span></span>

<span data-ttu-id="05906-104">Предоставляет доступ к контексту безопасности текущего вызова, который содержит сведения о вызывающих объектах объекта.</span><span class="sxs-lookup"><span data-stu-id="05906-104">Provides access to the current call's security context, which contains information about an object's callers.</span></span> <span data-ttu-id="05906-105">С помощью этого класса можно также выяснить, является ли объект прямого вызова объекта членом определенной роли и включена ли безопасность для объекта.</span><span class="sxs-lookup"><span data-stu-id="05906-105">Using this class, you can also find out whether an object's direct caller is a member of a particular role and whether security is enabled for the object.</span></span>

<span data-ttu-id="05906-106">Только приложения COM+, использующие безопасность на основе ролей, имеют доступ к классу **секуритикаллконтекст** .</span><span class="sxs-lookup"><span data-stu-id="05906-106">Only COM+ applications that use role-based security can access the **SecurityCallContext** class.</span></span> <span data-ttu-id="05906-107">Дополнительные сведения о ролях см. в разделе [Администрирование безопасности на основе ролей](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="05906-107">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="05906-108">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="05906-108">When to implement</span></span>

<span data-ttu-id="05906-109">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="05906-109">This class is implemented by COM+.</span></span>



| <span data-ttu-id="05906-110">Требование</span><span class="sxs-lookup"><span data-stu-id="05906-110">Requirement</span></span> | <span data-ttu-id="05906-111">Значение</span><span class="sxs-lookup"><span data-stu-id="05906-111">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="05906-112">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="05906-112">Interfaces</span></span> | [<span data-ttu-id="05906-113">**исекуритикаллерсколл**</span><span class="sxs-lookup"><span data-stu-id="05906-113">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="05906-114">Назначение</span><span class="sxs-lookup"><span data-stu-id="05906-114">When to use</span></span>

<span data-ttu-id="05906-115">Используйте этот класс для доступа к методам [**исекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="05906-115">Use this class to access the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="remarks"></a><span data-ttu-id="05906-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05906-116">Remarks</span></span>

<span data-ttu-id="05906-117">Нельзя напрямую создать объект **секуритикаллконтекст** .</span><span class="sxs-lookup"><span data-stu-id="05906-117">You cannot directly create a **SecurityCallContext** object.</span></span> <span data-ttu-id="05906-118">Чтобы использовать методы [**исекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), необходимо получить ссылку на его реализацию, вызвав [**КОЖЕТКАЛЛКОНТЕКСТ**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), указав IID \_ исекуритикаллконтекст для параметра *riid* .</span><span class="sxs-lookup"><span data-stu-id="05906-118">To use the methods of [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span>

<span data-ttu-id="05906-119">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов служб COM+.</span><span class="sxs-lookup"><span data-stu-id="05906-119">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="05906-120">Объект Секуритикаллконтекст можно объявить с помощью "Комсвкслиб. Секуритикаллконтекст" в качестве имени класса; Он создается путем вызова [**жетсекуритикаллконтекст**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="05906-120">A SecurityCallContext object can be declared using "COMSVCSLib.SecurityCallContext" as the class name; it is created by calling [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="05906-121">Требования</span><span class="sxs-lookup"><span data-stu-id="05906-121">Requirements</span></span>



| <span data-ttu-id="05906-122">Требование</span><span class="sxs-lookup"><span data-stu-id="05906-122">Requirement</span></span> | <span data-ttu-id="05906-123">Значение</span><span class="sxs-lookup"><span data-stu-id="05906-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="05906-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05906-124">Minimum supported client</span></span><br/> | <span data-ttu-id="05906-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="05906-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="05906-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05906-126">Minimum supported server</span></span><br/> | <span data-ttu-id="05906-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="05906-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="05906-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="05906-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="05906-129"><dt>Комсвкс. h</dt></span><span class="sxs-lookup"><span data-stu-id="05906-129"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05906-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05906-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05906-131">**жетсекуритикаллконтекст**</span><span class="sxs-lookup"><span data-stu-id="05906-131">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="05906-132">**исекуритикаллконтекст**</span><span class="sxs-lookup"><span data-stu-id="05906-132">**ISecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="05906-133">Безопасность программных компонентов</span><span class="sxs-lookup"><span data-stu-id="05906-133">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="05906-134">Администрирование безопасности на основе ролей</span><span class="sxs-lookup"><span data-stu-id="05906-134">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="05906-135">**секуритикаллерс**</span><span class="sxs-lookup"><span data-stu-id="05906-135">**SecurityCallers**</span></span>](securitycallers.md)
</dt> <dt>

[<span data-ttu-id="05906-136">**секуритидентити**</span><span class="sxs-lookup"><span data-stu-id="05906-136">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

