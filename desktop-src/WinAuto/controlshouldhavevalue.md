---
title: контролшаулдхавевалуе
description: контролшаулдхавевалуе
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258578"
---
# <a name="controlshouldhavevalue"></a><span data-ttu-id="0ca87-103">контролшаулдхавевалуе</span><span class="sxs-lookup"><span data-stu-id="0ca87-103">ControlShouldHaveValue</span></span>

## <a name="text"></a><span data-ttu-id="0ca87-104">Текст</span><span class="sxs-lookup"><span data-stu-id="0ca87-104">Text</span></span>

<span data-ttu-id="0ca87-105">Элемент управления с ролью {0} должен иметь значение, но Get \_ акквалуе не реализован</span><span class="sxs-lookup"><span data-stu-id="0ca87-105">A control with role of {0} should have a value but get\_accValue is not implemented</span></span>

## <a name="type"></a><span data-ttu-id="0ca87-106">Тип</span><span class="sxs-lookup"><span data-stu-id="0ca87-106">Type</span></span>

<span data-ttu-id="0ca87-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="0ca87-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="0ca87-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0ca87-108">Description</span></span>

<span data-ttu-id="0ca87-109">Элемент не предоставляет ожидаемое значение на основе назначенной роли MSAA, подразумевая, что у элемента отсутствует реализованный метод [**Get \_ акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) .</span><span class="sxs-lookup"><span data-stu-id="0ca87-109">An element does not supply a value as expected based on the assigned MSAA role, implying that the element does not have the [**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) method implemented.</span></span> <span data-ttu-id="0ca87-110">Например, следующие роли MSAA должны предоставлять значение.</span><span class="sxs-lookup"><span data-stu-id="0ca87-110">For example, the following MSAA roles should all supply a value.</span></span>

-   <span data-ttu-id="0ca87-111">\_ \_ поле со списком для системы роли</span><span class="sxs-lookup"><span data-stu-id="0ca87-111">ROLE\_SYSTEM\_COMBOBOX</span></span>
-   <span data-ttu-id="0ca87-112">\_IP- \_ адрес системы роли</span><span class="sxs-lookup"><span data-stu-id="0ca87-112">ROLE\_SYSTEM\_IPADDRESS</span></span>
-   <span data-ttu-id="0ca87-113">\_ссылка на систему роли \_</span><span class="sxs-lookup"><span data-stu-id="0ca87-113">ROLE\_SYSTEM\_LINK</span></span>
-   <span data-ttu-id="0ca87-114">\_аутлинеитем системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="0ca87-114">ROLE\_SYSTEM\_OUTLINEITEM</span></span>
-   <span data-ttu-id="0ca87-115">компонент \_ PROGRESSBAR системы ролей \_</span><span class="sxs-lookup"><span data-stu-id="0ca87-115">ROLE\_SYSTEM\_PROGRESSBAR</span></span>
-   <span data-ttu-id="0ca87-116">\_ \_ ползунок системы роли</span><span class="sxs-lookup"><span data-stu-id="0ca87-116">ROLE\_SYSTEM\_SLIDER</span></span>
-   <span data-ttu-id="0ca87-117">\_спинбуттон системы \_ ролей</span><span class="sxs-lookup"><span data-stu-id="0ca87-117">ROLE\_SYSTEM\_SPINBUTTON</span></span>
-   <span data-ttu-id="0ca87-118">\_ \_ полоса прокрутки системы роли</span><span class="sxs-lookup"><span data-stu-id="0ca87-118">ROLE\_SYSTEM\_SCROLLBAR</span></span>
-   <span data-ttu-id="0ca87-119">\_системный \_ текст роли</span><span class="sxs-lookup"><span data-stu-id="0ca87-119">ROLE\_SYSTEM\_TEXT</span></span>

<span data-ttu-id="0ca87-120">Эта проблема связана с тем, что люди, которые используют средство чтения с экрана и клавиатуру для навигации, потому что элемент с внутренним значением должен иметь возможность сообщить это значение пользователю.</span><span class="sxs-lookup"><span data-stu-id="0ca87-120">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because an element that has an intrinsic value must be able to report that value to a user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="0ca87-121">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="0ca87-121">Possible causes</span></span>

<span data-ttu-id="0ca87-122">Элемент или его родитель имеет набор ролей MSAA.</span><span class="sxs-lookup"><span data-stu-id="0ca87-122">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ca87-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0ca87-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ca87-124">**IAccessible:: Get \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="0ca87-124">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="0ca87-125">**Роли объектов**</span><span class="sxs-lookup"><span data-stu-id="0ca87-125">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




