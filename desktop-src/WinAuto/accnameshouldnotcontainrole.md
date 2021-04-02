---
title: аккнамешаулднотконтаинроле
description: аккнамешаулднотконтаинроле
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779730"
---
# <a name="accnameshouldnotcontainrole"></a><span data-ttu-id="215ee-103">аккнамешаулднотконтаинроле</span><span class="sxs-lookup"><span data-stu-id="215ee-103">AccNameShouldNotContainRole</span></span>

## <a name="text"></a><span data-ttu-id="215ee-104">Текст</span><span class="sxs-lookup"><span data-stu-id="215ee-104">Text</span></span>

<span data-ttu-id="215ee-105">Имя элемента ( {0} ) не должно содержать текст роли элемента ( {1} )</span><span class="sxs-lookup"><span data-stu-id="215ee-105">Element's Name ({0}) should not contain the text of the Element's Role ({1})</span></span>

## <a name="type"></a><span data-ttu-id="215ee-106">Тип</span><span class="sxs-lookup"><span data-stu-id="215ee-106">Type</span></span>

<span data-ttu-id="215ee-107">Предупреждение</span><span class="sxs-lookup"><span data-stu-id="215ee-107">Warning</span></span>

## <a name="description"></a><span data-ttu-id="215ee-108">Описание</span><span class="sxs-lookup"><span data-stu-id="215ee-108">Description</span></span>

<span data-ttu-id="215ee-109">Имя элемента включает свою роль MSAA или тип элемента управления UIA.</span><span class="sxs-lookup"><span data-stu-id="215ee-109">The name of an element incorporates its MSAA role or UIA control type.</span></span> <span data-ttu-id="215ee-110">Например, это предупреждение может возникать, если метод [**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , используемый для получения имени MSAA элемента, Возвращает «роль \_ системы роли \_ \_ \* ».</span><span class="sxs-lookup"><span data-stu-id="215ee-110">For example, this warning can occur if the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method—which is used to retrieve the MSAA name of an element—returns "ROLE\_SYSTEM\_SCROLLBAR\_\*".</span></span>

<span data-ttu-id="215ee-111">Эта проблема вызывает проблемы для людей, которые используют средство чтения с экрана и клавиатуру для навигации, так как роль будет прочитана дважды или не может быть произношена или интуитивно понятна для пользователей.</span><span class="sxs-lookup"><span data-stu-id="215ee-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because the role will be read twice, or it may be unpronounceable or non-intuitive for users.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="215ee-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="215ee-112">Possible causes</span></span>

-   <span data-ttu-id="215ee-113">Элемент или его родитель имеет неправильно назначенное имя или подпись.</span><span class="sxs-lookup"><span data-stu-id="215ee-113">The element or its parent has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="215ee-114">Элемент или его родитель имеет имя по умолчанию, которое не было изменено на понятное имя.</span><span class="sxs-lookup"><span data-stu-id="215ee-114">The element or its parent has a default name that has not been revised to a friendly name.</span></span> <span data-ttu-id="215ee-115">Например, button1.</span><span class="sxs-lookup"><span data-stu-id="215ee-115">For example, button1.</span></span>
-   <span data-ttu-id="215ee-116">Разработчик не знает, что читатели экрана считывают имена.</span><span class="sxs-lookup"><span data-stu-id="215ee-116">A developer is not aware that screen readers read names.</span></span>

## <a name="related-topics"></a><span data-ttu-id="215ee-117">См. также</span><span class="sxs-lookup"><span data-stu-id="215ee-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="215ee-118">**IAccessible:: Get \_ аккнаме**</span><span class="sxs-lookup"><span data-stu-id="215ee-118">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="215ee-119">Свойство Name</span><span class="sxs-lookup"><span data-stu-id="215ee-119">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




