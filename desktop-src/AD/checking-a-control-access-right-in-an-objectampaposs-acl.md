---
title: Проверка прав доступа к элементу управления в ACL объекта
description: Чтобы проверить права доступа к списку управления доступом объекта, используйте функцию Акцессчеккбитипересултлист.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Проверка прав доступа к элементу управления в ACL объекта Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069811"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a><span data-ttu-id="dc5dd-104">Проверка прав доступа к элементу управления в ACL объекта</span><span class="sxs-lookup"><span data-stu-id="dc5dd-104">Checking a Control Access Right in an Object's ACL</span></span>

<span data-ttu-id="dc5dd-105">Чтобы проверить права доступа к списку управления доступом объекта, используйте функцию [**акцессчеккбитипересултлист**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) .</span><span class="sxs-lookup"><span data-stu-id="dc5dd-105">To check a control access right on an object's ACL, use the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function.</span></span> <span data-ttu-id="dc5dd-106">Для использования этой функции приложению требуется указатель на [**\_ дескриптор безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) объекта, а не интерфейса [**иадссекуритидескриптор**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) в COM-объект дескриптора безопасности ADSI.</span><span class="sxs-lookup"><span data-stu-id="dc5dd-106">To use this function, an application requires a pointer to the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) for the object instead of an [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) interface to an ADSI security descriptor COM object.</span></span>

<span data-ttu-id="dc5dd-107">Чтобы проверить доступ для управляемого права доступа к объекту, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dc5dd-107">Use the following steps to check access for an controlled access right on an object:</span></span>

1.  <span data-ttu-id="dc5dd-108">Получите указатель интерфейса [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) на объект.</span><span class="sxs-lookup"><span data-stu-id="dc5dd-108">Get an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface pointer to the object.</span></span>
2.  <span data-ttu-id="dc5dd-109">Чтобы получить дескриптор безопасности объекта, используйте метод [**идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="dc5dd-109">Use the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to get the security descriptor of the object.</span></span> <span data-ttu-id="dc5dd-110">Имя свойства, содержащего дескриптор безопасности, — [**нтсекуритидескриптор**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span><span class="sxs-lookup"><span data-stu-id="dc5dd-110">The name of the property containing the security descriptor is [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span></span> <span data-ttu-id="dc5dd-111">Свойство возвращается в виде указателя на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="dc5dd-111">The property is returned as a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span>
3.  <span data-ttu-id="dc5dd-112">Используйте структуру [**\_ дескрипторов безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) с функцией [**акцессчеккбитипересултлист**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) для проверки разрешений на доступ к указанному элементу управления для указанного клиента.</span><span class="sxs-lookup"><span data-stu-id="dc5dd-112">Use the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure with the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function to check the permissions for the specified control access right for the specified client.</span></span>

<span data-ttu-id="dc5dd-113">Пример кода в [примере кода для проверки прав доступа к элементу управления в списке ACL объекта](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) показывает, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="dc5dd-113">The example code in [Example Code for Checking a Control Access Right in an Object's ACL](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) shows, in detail, how to do this.</span></span>

 

 