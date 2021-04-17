---
title: инвалидроле
description: инвалидроле
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710041"
---
# <a name="invalidrole"></a><span data-ttu-id="bda2a-103">инвалидроле</span><span class="sxs-lookup"><span data-stu-id="bda2a-103">InvalidRole</span></span>

## <a name="text"></a><span data-ttu-id="bda2a-104">Текст</span><span class="sxs-lookup"><span data-stu-id="bda2a-104">Text</span></span>

<span data-ttu-id="bda2a-105">Целочисленное значение, возвращенное из Get \_ аккроле, не является допустимой константой роли, системой роли IE \_\_\*</span><span class="sxs-lookup"><span data-stu-id="bda2a-105">The int returned from get\_accRole is not a valid role constant, ie ROLE\_SYSTEM\_\*</span></span>

## <a name="type"></a><span data-ttu-id="bda2a-106">Тип</span><span class="sxs-lookup"><span data-stu-id="bda2a-106">Type</span></span>

<span data-ttu-id="bda2a-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="bda2a-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="bda2a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="bda2a-108">Description</span></span>

<span data-ttu-id="bda2a-109">Элемент сообщает о недопустимой роли MSAA.</span><span class="sxs-lookup"><span data-stu-id="bda2a-109">An element is reporting an invalid MSAA role.</span></span> <span data-ttu-id="bda2a-110">Например, метод [**Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) возвращает целочисленное значение, которое не соответствует допустимой константе роли объекта (например, \_ системе роли \_ ).</span><span class="sxs-lookup"><span data-stu-id="bda2a-110">For example, the [**get\_accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) method returns an integer value that does not map to a valid object role constant (such as ROLE\_SYSTEM\_LISTITEM).</span></span>

<span data-ttu-id="bda2a-111">Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку элементы могут быть неверно идентифицированы для пользователя.</span><span class="sxs-lookup"><span data-stu-id="bda2a-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because elements may be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="bda2a-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="bda2a-112">Possible causes</span></span>

<span data-ttu-id="bda2a-113">Элемент или его родитель имеет набор ролей MSAA.</span><span class="sxs-lookup"><span data-stu-id="bda2a-113">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bda2a-114">См. также</span><span class="sxs-lookup"><span data-stu-id="bda2a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bda2a-115">**IAccessible:: Get \_ аккроле**</span><span class="sxs-lookup"><span data-stu-id="bda2a-115">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="bda2a-116">**Роли объектов**</span><span class="sxs-lookup"><span data-stu-id="bda2a-116">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




