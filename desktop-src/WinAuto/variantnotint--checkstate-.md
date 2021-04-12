---
title: Вариантнотинт (свойство CheckState)
description: Вариантнотинт (свойство CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253284"
---
# <a name="variantnotint-checkstate"></a><span data-ttu-id="f37da-103">Вариантнотинт (свойство CheckState)</span><span class="sxs-lookup"><span data-stu-id="f37da-103">VariantNotInt (CheckState)</span></span>

## <a name="text"></a><span data-ttu-id="f37da-104">Текст</span><span class="sxs-lookup"><span data-stu-id="f37da-104">Text</span></span>

<span data-ttu-id="f37da-105">Вариант, возвращаемый методом, {0} должен быть, {1} но является {2} .</span><span class="sxs-lookup"><span data-stu-id="f37da-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="f37da-106">Тип</span><span class="sxs-lookup"><span data-stu-id="f37da-106">Type</span></span>

<span data-ttu-id="f37da-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="f37da-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="f37da-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f37da-108">Description</span></span>

<span data-ttu-id="f37da-109">Элемент сообщает о недопустимом состоянии MSAA.</span><span class="sxs-lookup"><span data-stu-id="f37da-109">An element is reporting an invalid MSAA state.</span></span> <span data-ttu-id="f37da-110">Например, метод [**Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) , используемый для получения состояния MSAA элемента, должен возвращать целочисленное значение, представляющее одну из констант состояния MSAA, но вместо этого возвращает другой вариант.</span><span class="sxs-lookup"><span data-stu-id="f37da-110">For example, the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method used to retrieve the MSAA state of an element should return an integer value that represents one of the MSAA state constants, but is returning another variant instead.</span></span>

<span data-ttu-id="f37da-111">Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку пользователь может сообщить о неправильном состоянии элемента.</span><span class="sxs-lookup"><span data-stu-id="f37da-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="f37da-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="f37da-112">Possible causes</span></span>

<span data-ttu-id="f37da-113">Для элемента или его родителя задано неправильное состояние MSAA.</span><span class="sxs-lookup"><span data-stu-id="f37da-113">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f37da-114">См. также</span><span class="sxs-lookup"><span data-stu-id="f37da-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f37da-115">**IAccessible:: Get \_ аккстате**</span><span class="sxs-lookup"><span data-stu-id="f37da-115">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="f37da-116">**Константы состояния объектов**</span><span class="sxs-lookup"><span data-stu-id="f37da-116">**Object State Constants**</span></span>](object-state-constants.md)
</dt> </dl>

 

 




