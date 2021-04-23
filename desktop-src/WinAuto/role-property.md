---
title: Свойство Role
description: Свойство Role описывает элемент пользовательского интерфейса объекта. Все объекты поддерживают свойство Role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700494"
---
# <a name="role-property"></a><span data-ttu-id="56c7f-104">Свойство Role</span><span class="sxs-lookup"><span data-stu-id="56c7f-104">Role Property</span></span>

<span data-ttu-id="56c7f-105">Свойство **Role** описывает элемент пользовательского интерфейса объекта.</span><span class="sxs-lookup"><span data-stu-id="56c7f-105">The **Role** property describes an object's user interface element.</span></span> <span data-ttu-id="56c7f-106">Все объекты поддерживают свойство **Role** .</span><span class="sxs-lookup"><span data-stu-id="56c7f-106">All objects support the **Role** property.</span></span>

<span data-ttu-id="56c7f-107">Во многих случаях роль объекта очевидна.</span><span class="sxs-lookup"><span data-stu-id="56c7f-107">In many cases, the object's role is obvious.</span></span> <span data-ttu-id="56c7f-108">Например, у Windows есть роль [**системного \_ \_ окна роли**](object-roles.md) и кнопки с кнопками « [**роль \_ системы \_**](object-roles.md) ».</span><span class="sxs-lookup"><span data-stu-id="56c7f-108">For example, windows have the [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) role and push buttons have the [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md) role.</span></span>

<span data-ttu-id="56c7f-109">Свойство **Role** извлекается путем вызова метода [**IAccessible:: Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span><span class="sxs-lookup"><span data-stu-id="56c7f-109">The **Role** property is retrieved by calling [**IAccessible::get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).</span></span>

## <a name="identifying-an-objects-role"></a><span data-ttu-id="56c7f-110">Определение роли объекта</span><span class="sxs-lookup"><span data-stu-id="56c7f-110">Identifying an Object's Role</span></span>

<span data-ttu-id="56c7f-111">Microsoft Active Accessibility предоставляет [константы ролей](object-roles.md), определенные в олеакк. h, которые определяют общие роли объектов.</span><span class="sxs-lookup"><span data-stu-id="56c7f-111">Microsoft Active Accessibility provides [role constants](object-roles.md), defined in oleacc.h, that identify common object roles.</span></span> <span data-ttu-id="56c7f-112">Рекомендуется, чтобы разработчики сервера использовали эти стандартные значения ролей.</span><span class="sxs-lookup"><span data-stu-id="56c7f-112">It is recommended that server developers use these predefined role values.</span></span> <span data-ttu-id="56c7f-113">Если возвращается предопределенная константа роли, клиенты используют функцию [**жетролетекст**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) для получения локализованной строки, описывающей роль.</span><span class="sxs-lookup"><span data-stu-id="56c7f-113">If a predefined role constant is returned, clients use the [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) function to retrieve a localized string that describes the role.</span></span>

<span data-ttu-id="56c7f-114">Для элементов управления "анимация", таких как элемент управления анимацией, отображаемый при копировании файлов, используйте [**\_ \_ анимацию системы роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="56c7f-114">For animation controls, such as the animation control displayed when copying files, use [**ROLE\_SYSTEM\_ANIMATION**](object-roles.md).</span></span> <span data-ttu-id="56c7f-115">Графика, которые иногда анимированы, описаны [**как \_ \_ график системы роли**](object-roles.md) , свойство [**State**](state-property.md) которого имеет [**значение \_ \_ анимация системы состояний**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="56c7f-115">Graphics that are occasionally animated are described as [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md) with the [**State**](state-property.md) property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md).</span></span>

<span data-ttu-id="56c7f-116">Обратите внимание, что некоторые роли не просто описать.</span><span class="sxs-lookup"><span data-stu-id="56c7f-116">Note that some roles are not easy to describe.</span></span> <span data-ttu-id="56c7f-117">Например, представление с большим значком папки позволяет произвольно упорядочивать значки, поэтому его роль можно описать как [**\_ \_ группирование системы ролей**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="56c7f-117">For example, a folder's large-icon view allows arbitrary arrangement of icons, so its role could be described as [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span> <span data-ttu-id="56c7f-118">Или элемент управления, предоставляющий элементы в фиксированных строках и столбцах, может иметь роль [**\_ системной \_ таблицы Role**](object-roles.md) .</span><span class="sxs-lookup"><span data-stu-id="56c7f-118">Or, a control that provides items in fixed rows and columns could have the [**ROLE\_SYSTEM\_TABLE**](object-roles.md) role.</span></span> <span data-ttu-id="56c7f-119">Поскольку роль используется для передачи модели использования конечному пользователю, важно использовать соответствующую роль.</span><span class="sxs-lookup"><span data-stu-id="56c7f-119">Since a role is used to communicate the use model to an end user, it is important to use the appropriate role.</span></span> <span data-ttu-id="56c7f-120">Например, если элемент управления действует как кнопка, используйте кнопку [**\_ системы \_ роли**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="56c7f-120">For example, if your control acts like a button, then use [**ROLE\_SYSTEM\_PUSHBUTTON**](object-roles.md).</span></span>

 

 




