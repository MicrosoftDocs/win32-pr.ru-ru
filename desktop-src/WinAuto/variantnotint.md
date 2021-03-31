---
title: Вариантнотинт (Чеккроле)
description: Вариантнотинт (Чеккроле)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330219"
---
# <a name="variantnotint-checkrole"></a><span data-ttu-id="b3095-103">Вариантнотинт (Чеккроле)</span><span class="sxs-lookup"><span data-stu-id="b3095-103">VariantNotInt (CheckRole)</span></span>

## <a name="text"></a><span data-ttu-id="b3095-104">Текст</span><span class="sxs-lookup"><span data-stu-id="b3095-104">Text</span></span>

<span data-ttu-id="b3095-105">Вариант, возвращаемый методом, {0} должен быть, {1} но является {2} .</span><span class="sxs-lookup"><span data-stu-id="b3095-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="b3095-106">Тип</span><span class="sxs-lookup"><span data-stu-id="b3095-106">Type</span></span>

<span data-ttu-id="b3095-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="b3095-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="b3095-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b3095-108">Description</span></span>

<span data-ttu-id="b3095-109">Элемент сообщает о недопустимой роли MSAA.</span><span class="sxs-lookup"><span data-stu-id="b3095-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="b3095-110">Например, метод [**Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) , используемый для получения роли MSAA элемента, должен возвращать целочисленное значение, представляющее одну из констант роли MSAA, но вместо этого возвращает другой вариант.</span><span class="sxs-lookup"><span data-stu-id="b3095-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method used to retrieve the MSAA role of an element should return an integer value that represents one of the MSAA role constants, but is returning another variant instead.</span></span>

<span data-ttu-id="b3095-111">Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку элементы могут быть неверно идентифицированы для пользователя.</span><span class="sxs-lookup"><span data-stu-id="b3095-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="b3095-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="b3095-112">Possible causes</span></span>

<span data-ttu-id="b3095-113">Элемент или его родитель имеет набор ролей MSAA.</span><span class="sxs-lookup"><span data-stu-id="b3095-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3095-114">См. также</span><span class="sxs-lookup"><span data-stu-id="b3095-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3095-115">**IAccessible:: Get \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="b3095-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="b3095-116">**Роли объектов**</span><span class="sxs-lookup"><span data-stu-id="b3095-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




