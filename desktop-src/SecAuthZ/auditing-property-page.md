---
description: Редактор управления доступом может включать страницу свойств аудита, позволяющую пользователю просматривать и изменять записи контроля доступа (ACE) в списке объектов системы управления доступом (SACL). Дополнительные сведения о списках SACL см. в разделе списки управления доступом (ACL).
ms.assetid: 2a9152b7-c72d-4f03-bc3f-b75927fb4b6c
title: Страница свойств «аудит»
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7fc85691c93994a764199f0b77d52a7a8a71e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265398"
---
# <a name="auditing-property-page"></a><span data-ttu-id="1efe4-104">Страница свойств «аудит»</span><span class="sxs-lookup"><span data-stu-id="1efe4-104">Auditing Property Page</span></span>

<span data-ttu-id="1efe4-105">Редактор управления доступом может включать страницу свойств **аудита** , которая позволяет пользователю просматривать и изменять [*записи управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE) в [*системном списке управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL) объекта.</span><span class="sxs-lookup"><span data-stu-id="1efe4-105">The access control editor can include an **Auditing** property page that enables the user to view and edit the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) in an object's [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="1efe4-106">Дополнительные сведения о списках SACL см. в разделе [списки управления доступом](access-control-lists.md) (ACL).</span><span class="sxs-lookup"><span data-stu-id="1efe4-106">For more information about SACLs, see [Access Control Lists](access-control-lists.md) (ACLs).</span></span>

<span data-ttu-id="1efe4-107">**Просмотр страницы свойств «аудит»**</span><span class="sxs-lookup"><span data-stu-id="1efe4-107">**To view the Auditing property page**</span></span>

-   <span data-ttu-id="1efe4-108">На [странице свойств базовая безопасность](basic-security-property-page.md)нажмите кнопку **Дополнительно**.</span><span class="sxs-lookup"><span data-stu-id="1efe4-108">On the [basic security property page](basic-security-property-page.md), click **Advanced**.</span></span> <span data-ttu-id="1efe4-109">Страница свойств **Аудит** находится на странице [свойств Расширенная безопасность](advanced-security-property-sheet.md).</span><span class="sxs-lookup"><span data-stu-id="1efe4-109">The **Auditing** property page is in the [advanced security property sheet](advanced-security-property-sheet.md).</span></span>

<span data-ttu-id="1efe4-110">Чтобы включить страницу свойств « **Аудит** », установите флаги **\_ расширенной** **\_ \_ проверки и изменения** состояния системы SI в структуре [**\_ \_ сведений об объекте Si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) , возвращаемой реализацией [**исекуритинформатион:: жетобжектинформатион**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="1efe4-110">To include the **Auditing** property page, set the **SI\_ADVANCED** and **SI\_EDIT\_AUDITS** flags in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
