---
title: елементисорфанед
description: елементисорфанед
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700711"
---
# <a name="elementisorphaned"></a><span data-ttu-id="85863-103">елементисорфанед</span><span class="sxs-lookup"><span data-stu-id="85863-103">ElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="85863-104">Текст</span><span class="sxs-lookup"><span data-stu-id="85863-104">Text</span></span>

<span data-ttu-id="85863-105">Элемент является потерянным IAccessible в дереве</span><span class="sxs-lookup"><span data-stu-id="85863-105">Element is an orphaned IAccessible in the tree</span></span>

## <a name="type"></a><span data-ttu-id="85863-106">Тип</span><span class="sxs-lookup"><span data-stu-id="85863-106">Type</span></span>

<span data-ttu-id="85863-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="85863-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="85863-108">Описание</span><span class="sxs-lookup"><span data-stu-id="85863-108">Description</span></span>

<span data-ttu-id="85863-109">Адресом интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) объекта, полученного для заданных координат, является ссылка на потерянный элемент в дереве элементов.</span><span class="sxs-lookup"><span data-stu-id="85863-109">The address of the object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="85863-110">Эта проблема возникает для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, поскольку элементы будут рассматриваться как невидимые и не будут объявлены пользователю.</span><span class="sxs-lookup"><span data-stu-id="85863-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="85863-111">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="85863-111">Possible causes</span></span>

-   <span data-ttu-id="85863-112">Взаимодействие с пользователем во время проверки, например перемещение фокуса на нецелевой HWND, мешает процессу проверки.</span><span class="sxs-lookup"><span data-stu-id="85863-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="85863-113">Неправильная или недопустимая реализация MSAA.</span><span class="sxs-lookup"><span data-stu-id="85863-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85863-114">См. также</span><span class="sxs-lookup"><span data-stu-id="85863-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85863-115">Навигация с помощью проверки попадания и расположения на экране</span><span class="sxs-lookup"><span data-stu-id="85863-115">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[<span data-ttu-id="85863-116">**акцессиблеобжектфромпоинт**</span><span class="sxs-lookup"><span data-stu-id="85863-116">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




