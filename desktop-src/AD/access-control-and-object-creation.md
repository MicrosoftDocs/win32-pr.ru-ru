---
title: Управление доступом и создание объектов
description: Сервер Active Directory не сможет создать дочерний объект, если у вызывающего объекта нет общедоступной \_ \_ службы AD DS \_ Create \_ дочернего элемента для этого типа объектов в родительском контейнере.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- Управление доступом и создание объектов AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ac54c1fe71a1821d3a02db383ca95606ae360d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104133634"
---
# <a name="access-control-and-object-creation"></a><span data-ttu-id="505f2-104">Управление доступом и создание объектов</span><span class="sxs-lookup"><span data-stu-id="505f2-104">Access Control and Object Creation</span></span>

<span data-ttu-id="505f2-105">Сервер Active Directory не сможет создать дочерний объект, если у вызывающего объекта нет общедоступной **\_ \_ службы AD DS \_ Create \_ дочернего элемента** для этого типа объектов в родительском контейнере.</span><span class="sxs-lookup"><span data-stu-id="505f2-105">The Active Directory server will fail to create a child object if the caller does not have the **ADS\_RIGHT\_DS\_CREATE\_CHILD** for that object type on the parent container.</span></span> <span data-ttu-id="505f2-106">Чтобы определить типы дочерних объектов, которые вызывающий объект может создать в объекте каталога, прочтите атрибут **алловедчилдклассесеффективе** объекта.</span><span class="sxs-lookup"><span data-stu-id="505f2-106">To determine the types of child objects that the caller can create in a directory object, read the object's **allowedChildClassesEffective** attribute.</span></span>

<span data-ttu-id="505f2-107">При использовании метода [**иадсконтаинер:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) для создания дочернего объекта объект не становится постоянным до тех пор, пока для нового объекта не будет вызван метод [**iAds:: сетинфо**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="505f2-107">When you use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) method to create a child object, the object is not made persistent until [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) is called on the new object.</span></span> <span data-ttu-id="505f2-108">Между вызовами **CREATE** и **сетинфо** , создающий поток, может поместить значения в любые свойства нового объекта.</span><span class="sxs-lookup"><span data-stu-id="505f2-108">Between the **Create** and **SetInfo** calls, the creating thread can put values into any of the new object's properties.</span></span> <span data-ttu-id="505f2-109">После вызова **сетинфо** создание потока не обязательно будет иметь права доступа для задания свойств нового объекта.</span><span class="sxs-lookup"><span data-stu-id="505f2-109">After the **SetInfo** call, the creating thread does not necessarily have the access rights to set the new object's properties.</span></span> <span data-ttu-id="505f2-110">Чтобы убедиться, что вызывающая сторона имеет эти права, укажите явный дескриптор безопасности во время создания.</span><span class="sxs-lookup"><span data-stu-id="505f2-110">To ensure that the caller has these rights, specify an explicit security descriptor during creation.</span></span> <span data-ttu-id="505f2-111">Список DACL должен иметь запись ACE, которая предоставляет вызывающей стороне необходимые права доступа к объекту.</span><span class="sxs-lookup"><span data-stu-id="505f2-111">The DACL should have an ACE that gives the caller the necessary access rights on the object.</span></span>

<span data-ttu-id="505f2-112">Дополнительные сведения об управлении доступом и создании объектов см. [в разделе как устанавливаются дескрипторы безопасности для новых объектов каталога](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="505f2-112">For more information about access control and object creation, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span>

 

 