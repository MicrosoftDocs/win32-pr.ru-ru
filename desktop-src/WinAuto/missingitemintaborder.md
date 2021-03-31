---
title: миссингитеминтабордер
description: миссингитеминтабордер
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791790"
---
# <a name="missingitemintaborder"></a><span data-ttu-id="a24ba-103">миссингитеминтабордер</span><span class="sxs-lookup"><span data-stu-id="a24ba-103">MissingItemInTabOrder</span></span>

## <a name="text"></a><span data-ttu-id="a24ba-104">Текст</span><span class="sxs-lookup"><span data-stu-id="a24ba-104">Text</span></span>

<span data-ttu-id="a24ba-105">Этот элемент по-видимому доступен для перехода, но не находится в последовательности табуляции.</span><span class="sxs-lookup"><span data-stu-id="a24ba-105">This element appears to be tabbable but is not in the tab order.</span></span>

## <a name="type"></a><span data-ttu-id="a24ba-106">Тип</span><span class="sxs-lookup"><span data-stu-id="a24ba-106">Type</span></span>

<span data-ttu-id="a24ba-107">Ошибка</span><span class="sxs-lookup"><span data-stu-id="a24ba-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="a24ba-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a24ba-108">Description</span></span>

<span data-ttu-id="a24ba-109">Элемент, на который осуществляется фокус, недоступен при использовании стандартной навигации с помощью клавиатуры (TAB или SHIFT + TAB).</span><span class="sxs-lookup"><span data-stu-id="a24ba-109">A focusable element is not accessible using standard keyboard navigation (Tab or Shift+Tab).</span></span> <span data-ttu-id="a24ba-110">Например, элемент не был помечен как позиция табуляции или присвоен индекс табуляции.</span><span class="sxs-lookup"><span data-stu-id="a24ba-110">For example, the element has not been marked as a tab stop or assigned a tab index.</span></span> <span data-ttu-id="a24ba-111">Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="a24ba-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because:</span></span>

-   <span data-ttu-id="a24ba-112">Элемент не может быть обнаружен.</span><span class="sxs-lookup"><span data-stu-id="a24ba-112">The element is not discoverable.</span></span>
-   <span data-ttu-id="a24ba-113">Если элемент является дочерним для пользовательского элемента управления "список", подсказки, указывающие на возможность перехода к дочернему элементу с помощью стрелки или клавиш страницы, могут отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="a24ba-113">If the element is a child of a custom list control, cues indicating the child element can be navigated using the Arrow or Page keys may be missing.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a24ba-114">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="a24ba-114">Possible causes</span></span>

-   <span data-ttu-id="a24ba-115">Роль MSAA элемента или его родителя задана неправильно.</span><span class="sxs-lookup"><span data-stu-id="a24ba-115">The MSAA role of the element or its parent is not set correctly.</span></span> <span data-ttu-id="a24ba-116">Например, если все элементы списка в элементе управления "список" не представлены с помощью MSAA в качестве элемента \_ ListItem системы роли \_ , проверка завершается сбоем, так как элементы списка недоступны с помощью клавиши TAB.</span><span class="sxs-lookup"><span data-stu-id="a24ba-116">For example, if all list items in a list view control are not exposed through MSAA as a ROLE\_SYSTEM\_LISTITEM, the verification fails because the list items are not accessible using the Tab key.</span></span>
-   <span data-ttu-id="a24ba-117">Элемент или его родитель является пользовательским элементом управления, который не реализует корректное выполнение вкладок.</span><span class="sxs-lookup"><span data-stu-id="a24ba-117">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="a24ba-118">Например, свойство состояния MSAA никогда не принимает \_ фокус системы состояния \_ .</span><span class="sxs-lookup"><span data-stu-id="a24ba-118">For example, the MSAA State property is never set to STATE\_SYSTEM\_FOCUSABLE.</span></span>
-   <span data-ttu-id="a24ba-119">Элемент, который выступает в качестве контейнера для других элементов, был выбран для проверки, но не поддерживает саму навигацию по клавишам.</span><span class="sxs-lookup"><span data-stu-id="a24ba-119">An element that acts as a container for other elements was selected for verification but does not support keyboard navigation itself.</span></span> <span data-ttu-id="a24ba-120">Например, панель инструментов и ее дочерние элементы недоступны при помощи клавиши TAB.</span><span class="sxs-lookup"><span data-stu-id="a24ba-120">For example, a toolbar and its child elements are not accessible using the TAB key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a24ba-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a24ba-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a24ba-122">Рекомендации по проектированию пользовательского интерфейса клавиатуры</span><span class="sxs-lookup"><span data-stu-id="a24ba-122">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 