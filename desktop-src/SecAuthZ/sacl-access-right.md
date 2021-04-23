---
description: Право доступа \_ безопасности системы доступа \_ контролирует возможность получения или задания списка SACL в дескрипторе безопасности объектов. Система предоставляет это право доступа, если \_ \_ в маркере доступа запрашивающего потока включена привилегия предоставления имени безопасности SE.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Право доступа к SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662567"
---
# <a name="sacl-access-right"></a><span data-ttu-id="79f60-104">Право доступа к SACL</span><span class="sxs-lookup"><span data-stu-id="79f60-104">SACL Access Right</span></span>

<span data-ttu-id="79f60-105">Право доступа \_ безопасности системы доступа \_ контролирует возможность получения или задания списка SACL в [*дескрипторе безопасности*](/windows/desktop/SecGloss/s-gly)объекта.</span><span class="sxs-lookup"><span data-stu-id="79f60-105">The ACCESS\_SYSTEM\_SECURITY access right controls the ability to get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="79f60-106">Система предоставляет это право доступа только в том случае, \_ Если \_ в [*маркере доступа*](/windows/desktop/SecGloss/a-gly) запрашивающего потока включена привилегия разрешения имен безопасности SE.</span><span class="sxs-lookup"><span data-stu-id="79f60-106">The system grants this access right only if the SE\_SECURITY\_NAME privilege is enabled in the [*access token*](/windows/desktop/SecGloss/a-gly) of the requesting thread.</span></span>

<span data-ttu-id="79f60-107">**Доступ к SACL объекта**</span><span class="sxs-lookup"><span data-stu-id="79f60-107">**To access an object's SACL**</span></span>

1.  <span data-ttu-id="79f60-108">Вызовите функцию [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , чтобы включить \_ \_ привилегию имени безопасности SE.</span><span class="sxs-lookup"><span data-stu-id="79f60-108">Call the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable the SE\_SECURITY\_NAME privilege.</span></span>
2.  <span data-ttu-id="79f60-109">Запросите \_ право доступа системы \_ безопасности при открытии маркера объекта.</span><span class="sxs-lookup"><span data-stu-id="79f60-109">Request the ACCESS\_SYSTEM\_SECURITY access right when you open a handle to the object.</span></span>
3.  <span data-ttu-id="79f60-110">Возвращает или задает список SACL объекта с помощью такой функции, как [**жетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) или [**сетсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span><span class="sxs-lookup"><span data-stu-id="79f60-110">Get or set the object's SACL by using a function such as [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) or [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span></span>
4.  <span data-ttu-id="79f60-111">Вызовите [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , чтобы отключить \_ \_ привилегию имени безопасности SE.</span><span class="sxs-lookup"><span data-stu-id="79f60-111">Call [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to disable the SE\_SECURITY\_NAME privilege.</span></span>

<span data-ttu-id="79f60-112">Чтобы получить доступ к SACL с помощью функций [**жетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) или [**сетнамедсекуритинфо**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , включите \_ привилегию SE- \_ имя безопасности.</span><span class="sxs-lookup"><span data-stu-id="79f60-112">To access a SACL using the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) or [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions, enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="79f60-113">Функция внутренне запрашивает право доступа.</span><span class="sxs-lookup"><span data-stu-id="79f60-113">The function internally requests the access right.</span></span>

<span data-ttu-id="79f60-114">Право доступа \_ безопасности системы доступа недопустимо \_ в списке DACL, так как списки DACL не контролируют доступ к SACL.</span><span class="sxs-lookup"><span data-stu-id="79f60-114">The ACCESS\_SYSTEM\_SECURITY access right is not valid in a DACL because DACLs do not control access to a SACL.</span></span> <span data-ttu-id="79f60-115">Тем не менее можно использовать право доступа \_ System \_ Security в списке SACL для аудита попыток использовать право доступа.</span><span class="sxs-lookup"><span data-stu-id="79f60-115">However, you can use the ACCESS\_SYSTEM\_SECURITY access right in a SACL to audit attempts to use the access right.</span></span>

 

 
