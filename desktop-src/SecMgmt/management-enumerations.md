---
description: Перечисляет перечисления, используемые функциями управления политиками LSA.
ms.assetid: f4fd2a61-61bc-44d2-b01f-3ca07699bcb8
title: Перечисления управления безопасностью
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bec2cdd731e2a3befe75e543f692d93bc5d9ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264672"
---
# <a name="security-management-enumerations"></a><span data-ttu-id="8cabf-103">Перечисления управления безопасностью</span><span class="sxs-lookup"><span data-stu-id="8cabf-103">Security Management Enumerations</span></span>

<span data-ttu-id="8cabf-104">В число перечислений управления безопасностью входят следующие.</span><span class="sxs-lookup"><span data-stu-id="8cabf-104">The security management enumerations include the following:</span></span>

-   [<span data-ttu-id="8cabf-105">Перечисления политики LSA</span><span class="sxs-lookup"><span data-stu-id="8cabf-105">LSA Policy Enumerations</span></span>](#lsa-policy-enumerations)
-   [<span data-ttu-id="8cabf-106">Более безопасные перечисления</span><span class="sxs-lookup"><span data-stu-id="8cabf-106">Safer Enumerations</span></span>](#safer-enumerations)

## <a name="lsa-policy-enumerations"></a><span data-ttu-id="8cabf-107">Перечисления политики LSA</span><span class="sxs-lookup"><span data-stu-id="8cabf-107">LSA Policy Enumerations</span></span>

<span data-ttu-id="8cabf-108">Функции управления политиками LSA используют следующие типы перечислений.</span><span class="sxs-lookup"><span data-stu-id="8cabf-108">The following enumeration types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="8cabf-109">Перечисление</span><span class="sxs-lookup"><span data-stu-id="8cabf-109">Enumeration</span></span>                                                                               | <span data-ttu-id="8cabf-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8cabf-110">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cabf-111">**\_ \_ Тип события аудита \_ политики**</span><span class="sxs-lookup"><span data-stu-id="8cabf-111">**POLICY\_AUDIT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_audit_event_type)                             | <span data-ttu-id="8cabf-112">Определяет типы событий, которые может отслеживать система.</span><span class="sxs-lookup"><span data-stu-id="8cabf-112">Defines the types of events the system can audit.</span></span>                                                                                     |
| [<span data-ttu-id="8cabf-113">**\_класс сведений о политике \_**</span><span class="sxs-lookup"><span data-stu-id="8cabf-113">**POLICY\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_information_class)                            | <span data-ttu-id="8cabf-114">Определяет типы данных, которые могут быть заданы или запрошены для объекта [**политики**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="8cabf-114">Defines the types of information that can be set or queried for a [**Policy**](policy-object.md) object.</span></span>                             |
| [<span data-ttu-id="8cabf-115">**\_ \_ роль сервера политики \_ LSA**</span><span class="sxs-lookup"><span data-stu-id="8cabf-115">**POLICY\_LSA\_SERVER\_ROLE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_lsa_server_role)                               | <span data-ttu-id="8cabf-116">Укажите роль сервера LSA.</span><span class="sxs-lookup"><span data-stu-id="8cabf-116">Indicate the role of an LSA server.</span></span>                                                                                                   |
| [<span data-ttu-id="8cabf-117">**\_класс сведений об уведомлении политики \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8cabf-117">**POLICY\_NOTIFICATION\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_notification_information_class) | <span data-ttu-id="8cabf-118">Определяет типы сведений о политике и сведения о домене политики, для которых приложение может запрашивать уведомления об изменениях.</span><span class="sxs-lookup"><span data-stu-id="8cabf-118">Defines the types of policy information and policy domain information for which your application can request notification of changes.</span></span> |
| [<span data-ttu-id="8cabf-119">**\_ \_ состояние включения сервера \_ политики**</span><span class="sxs-lookup"><span data-stu-id="8cabf-119">**POLICY\_SERVER\_ENABLE\_STATE**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_server_enable_state)                       | <span data-ttu-id="8cabf-120">Представляет состояние сервера LSA, то есть включен ли он или отключен.</span><span class="sxs-lookup"><span data-stu-id="8cabf-120">Represents the state of the LSA server, that is, whether it is enabled or disabled.</span></span>                                                   |
| [<span data-ttu-id="8cabf-121">**класс ДОВЕРЕНной \_ информации \_**</span><span class="sxs-lookup"><span data-stu-id="8cabf-121">**TRUSTED\_INFORMATION\_CLASS**</span></span>](/windows/desktop/api/Ntsecapi/ne-ntsecapi-trusted_information_class)                          | <span data-ttu-id="8cabf-122">Определяет типы данных, которые могут быть заданы или запрошены для доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="8cabf-122">Defines the types of information that can be set or queried for a trusted domain.</span></span>                                                     |



 

## <a name="safer-enumerations"></a><span data-ttu-id="8cabf-123">Более безопасные перечисления</span><span class="sxs-lookup"><span data-stu-id="8cabf-123">Safer Enumerations</span></span>

<span data-ttu-id="8cabf-124">В [более безопасном](safer.md) использовании используются следующие перечислимые типы.</span><span class="sxs-lookup"><span data-stu-id="8cabf-124">[Safer](safer.md) uses the following enumerated types.</span></span>



| <span data-ttu-id="8cabf-125">Имя</span><span class="sxs-lookup"><span data-stu-id="8cabf-125">Name</span></span>                                                               | <span data-ttu-id="8cabf-126">Описание</span><span class="sxs-lookup"><span data-stu-id="8cabf-126">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8cabf-127">**БОЛЕЕ \_ безопасные \_ типы идентификации**</span><span class="sxs-lookup"><span data-stu-id="8cabf-127">**SAFER\_IDENTIFICATION\_TYPES**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_identification_types) | <span data-ttu-id="8cabf-128">Тип перечисления, определяющий возможные типы структур правил идентификации, которые можно определить с помощью структуры [**\_ \_ заголовков безопасной идентификации**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) .</span><span class="sxs-lookup"><span data-stu-id="8cabf-128">Enumeration type that defines the possible types of identification rule structures that can be identified by the [**SAFER\_IDENTIFICATION\_HEADER**](/windows/desktop/api/WinSafer/ns-winsafer-safer_identification_header) structure.</span></span> |
| [<span data-ttu-id="8cabf-129">**БОЛЕЕ \_ безопасный \_ класс сведений об объекте \_**</span><span class="sxs-lookup"><span data-stu-id="8cabf-129">**SAFER\_OBJECT\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_object_info_class)      | <span data-ttu-id="8cabf-130">Тип перечисления, который определяет тип запрашиваемой информации о более безопасном объекте.</span><span class="sxs-lookup"><span data-stu-id="8cabf-130">Enumeration type that defines the type of information requested about a Safer object.</span></span>                                                                                                            |
| [<span data-ttu-id="8cabf-131">**\_ \_ класс сведений об безопасной политике \_**</span><span class="sxs-lookup"><span data-stu-id="8cabf-131">**SAFER\_POLICY\_INFO\_CLASS**</span></span>](/windows/desktop/api/WinSafer/ne-winsafer-safer_policy_info_class)      | <span data-ttu-id="8cabf-132">Тип перечисления, определяющий способы, с помощью которых можно запрашивать политику.</span><span class="sxs-lookup"><span data-stu-id="8cabf-132">Enumeration type that defines the ways in which a policy may be queried.</span></span>                                                                                                                         |



 

 

 



