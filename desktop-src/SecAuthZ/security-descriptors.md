---
description: Дескриптор безопасности содержит сведения о безопасности, связанные с защищаемым объектом.
ms.assetid: 4ab0e7b1-1b44-4368-b2bd-106c9d2c652c
title: Дескрипторы безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f864505f135b46d3e16a4e369c019444918fb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897774"
---
# <a name="security-descriptors"></a><span data-ttu-id="c0073-103">Дескрипторы безопасности</span><span class="sxs-lookup"><span data-stu-id="c0073-103">Security Descriptors</span></span>

<span data-ttu-id="c0073-104">[*Дескриптор безопасности*](/windows/desktop/SecGloss/s-gly) содержит сведения о безопасности, связанные с [защищаемым объектом](securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c0073-104">A [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains the security information associated with a [securable object](securable-objects.md).</span></span> <span data-ttu-id="c0073-105">Дескриптор безопасности состоит из структуры [**\_ дескрипторов безопасности**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) и связанных с ней сведений о безопасности.</span><span class="sxs-lookup"><span data-stu-id="c0073-105">A security descriptor consists of a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structure and its associated security information.</span></span> <span data-ttu-id="c0073-106">Дескриптор безопасности может включать следующие сведения о безопасности:</span><span class="sxs-lookup"><span data-stu-id="c0073-106">A security descriptor can include the following security information:</span></span>

-   <span data-ttu-id="c0073-107">[Идентификаторы безопасности](security-identifiers.md) (SID) для владельца и основной группы объекта.</span><span class="sxs-lookup"><span data-stu-id="c0073-107">[Security identifiers](security-identifiers.md) (SIDs) for the owner and primary group of an object.</span></span>
-   <span data-ttu-id="c0073-108">[Список DACL](access-control-lists.md) , указывающий права доступа, разрешенные или запрещенные определенным пользователям или группам.</span><span class="sxs-lookup"><span data-stu-id="c0073-108">A [DACL](access-control-lists.md) that specifies the access rights allowed or denied to particular users or groups.</span></span>
-   <span data-ttu-id="c0073-109">[Список SACL](access-control-lists.md) , указывающий типы попыток доступа, создающих записи аудита для объекта.</span><span class="sxs-lookup"><span data-stu-id="c0073-109">A [SACL](access-control-lists.md) that specifies the types of access attempts that generate audit records for the object.</span></span>
-   <span data-ttu-id="c0073-110">Набор контрольных битов, определяющих значение дескриптора безопасности или его отдельных членов.</span><span class="sxs-lookup"><span data-stu-id="c0073-110">A set of control bits that qualify the meaning of a security descriptor or its individual members.</span></span>

<span data-ttu-id="c0073-111">Приложения не должны напрямую манипулировать содержимым дескриптора безопасности.</span><span class="sxs-lookup"><span data-stu-id="c0073-111">Applications must not directly manipulate the contents of a security descriptor.</span></span> <span data-ttu-id="c0073-112">Windows API предоставляет функции для настройки и получения сведений о безопасности в дескрипторе безопасности объекта.</span><span class="sxs-lookup"><span data-stu-id="c0073-112">The Windows API provides functions for setting and retrieving the security information in an object's security descriptor.</span></span> <span data-ttu-id="c0073-113">Кроме того, существуют функции для создания и инициализации дескриптора безопасности для нового объекта.</span><span class="sxs-lookup"><span data-stu-id="c0073-113">In addition, there are functions for creating and initializing a security descriptor for a new object.</span></span>

<span data-ttu-id="c0073-114">Приложения, работающие с дескрипторами безопасности на Active Directory объектах, могут использовать функции безопасности Windows или интерфейсы безопасности, предоставляемые интерфейсами служб Active Directory (ADSI).</span><span class="sxs-lookup"><span data-stu-id="c0073-114">Applications working with security descriptors on Active Directory objects can use the Windows security functions or the security interfaces provided by the Active Directory Service Interfaces (ADSI).</span></span> <span data-ttu-id="c0073-115">Дополнительные сведения об интерфейсах безопасности ADSI см. [в разделе как работает управление доступом в Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="c0073-115">For more information about ADSI security interfaces, see [How Access Control Works in Active Directory](/windows/desktop/AD/how-access-control-works-in-active-directory-domain-services).</span></span>

 

 
