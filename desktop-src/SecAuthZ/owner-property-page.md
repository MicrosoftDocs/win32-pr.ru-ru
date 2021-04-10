---
description: Редактор управления доступом может включать страницу свойств владелец, которая позволяет пользователю изменять владельца объектов. Дополнительные сведения о владельце объектов см. в разделе Владелец нового объекта и получение владения объектом в C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Страница свойств Owner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee9d5c276071674ec274c9955a2e8c5cd5a856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156775"
---
# <a name="owner-property-page"></a><span data-ttu-id="4855b-104">Страница свойств Owner</span><span class="sxs-lookup"><span data-stu-id="4855b-104">Owner Property Page</span></span>

<span data-ttu-id="4855b-105">Редактор управления доступом может включать страницу свойств владелец, которая позволяет пользователю изменять владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="4855b-105">The access control editor can include an Owner property page that enables the user to change an object's owner.</span></span> <span data-ttu-id="4855b-106">Дополнительные сведения о владельце объекта см. в разделе [владелец нового объекта](owner-of-a-new-object.md) и [получение владения объектом в C++](taking-object-ownership-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="4855b-106">For more information about an object's owner, see [Owner of a New Object](owner-of-a-new-object.md) and [Taking Object Ownership in C++](taking-object-ownership-in-c--.md).</span></span>

<span data-ttu-id="4855b-107">Страница свойств **владелец** находится на странице [свойств Расширенная безопасность](advanced-security-property-sheet.md) , которая отображается, когда пользователь нажимает кнопку **Дополнительно** на [странице свойств основные параметры безопасности](basic-security-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="4855b-107">The **Owner** property page is in the [advanced security property sheet](advanced-security-property-sheet.md) displayed when the user clicks the **Advanced** button on the [basic security property page](basic-security-property-page.md).</span></span> <span data-ttu-id="4855b-108">Чтобы включить страницу свойств **владелец** , задайте \_ Флаги "Расширенный" и "изменение владельца Si" \_ \_ в структуре [**\_ \_ сведений об объекте Si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) , возвращаемой реализацией [**исекуритинформатион:: жетобжектинформатион**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .</span><span class="sxs-lookup"><span data-stu-id="4855b-108">To include the **Owner** property page, set the SI\_ADVANCED and SI\_EDIT\_OWNER flags in the [**SI\_OBJECT\_INFO**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) structure returned by your [**ISecurityInformation::GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) implementation.</span></span>

 

 
