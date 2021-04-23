---
description: Страница свойств Расширенная безопасность позволяет пользователю выполнять операции редактирования, недоступные на странице Основные свойства безопасности редактора управления доступом.
ms.assetid: 99911751-d4ac-4325-89f5-23d237bfd428
title: Страница свойств расширенной безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c8fe19b9336434c789d5e61a295cf7784afbf3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647727"
---
# <a name="advanced-security-property-sheet"></a><span data-ttu-id="38dab-103">Страница свойств расширенной безопасности</span><span class="sxs-lookup"><span data-stu-id="38dab-103">Advanced Security Property Sheet</span></span>

<span data-ttu-id="38dab-104">Страница свойств Расширенная безопасность позволяет пользователю выполнять операции редактирования, недоступные на [странице Основные свойства безопасности](basic-security-property-page.md) редактора управления доступом.</span><span class="sxs-lookup"><span data-stu-id="38dab-104">The advanced security property sheet enables the user to perform editing operations that are not available on the [basic security property page](basic-security-property-page.md) of an access control editor.</span></span> <span data-ttu-id="38dab-105">Страница свойств может включать следующие страницы свойств:</span><span class="sxs-lookup"><span data-stu-id="38dab-105">The property sheet can include the following property pages:</span></span>

-   <span data-ttu-id="38dab-106">Страница свойств « [разрешения](permissions-property-page.md) » для расширенного редактирования [*списка управления*](/windows/desktop/SecGloss/d-gly) доступом (DACL) объекта, например для редактирования [объектов ACE, связанных с объектами](object-specific-aces.md) , или управления [наследованием ACE](ace-inheritance.md).</span><span class="sxs-lookup"><span data-stu-id="38dab-106">A [Permissions](permissions-property-page.md) property page for advanced editing of the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), such as editing [object-specific ACEs](object-specific-aces.md) or controlling [ACE inheritance](ace-inheritance.md).</span></span>
-   <span data-ttu-id="38dab-107">Страница свойств [аудита](auditing-property-page.md) для просмотра и изменения [*системного списка управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL) объекта.</span><span class="sxs-lookup"><span data-stu-id="38dab-107">An [Auditing](auditing-property-page.md) property page for viewing and editing the object's [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span>
-   <span data-ttu-id="38dab-108">Страница свойств [владельца](owner-property-page.md) для изменения владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="38dab-108">An [Owner](owner-property-page.md) property page for changing the object's owner.</span></span>

<span data-ttu-id="38dab-109">Пользователь может отобразить страницу свойств Advanced Security (Расширенная безопасность), нажав кнопку **Дополнительно** на странице свойств базовая безопасность.</span><span class="sxs-lookup"><span data-stu-id="38dab-109">The user can display the advanced security property sheet by clicking the **Advanced** button on the basic security property page.</span></span> <span data-ttu-id="38dab-110">Чтобы отобразить кнопку " **Дополнительно** ", установите флаг "Advanced Si" \_ в структуре [**\_ \_ сведений об объекте Si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) , возвращаемой реализацией [**исекуритинформатион:: жетобжектинформатион**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="38dab-110">To display the **Advanced** button, set the SI\_ADVANCED flag in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
