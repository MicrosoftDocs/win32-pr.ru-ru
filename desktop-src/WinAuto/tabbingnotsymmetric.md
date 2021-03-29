---
title: таббингнотсимметрик
description: таббингнотсимметрик
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134110"
---
# <a name="tabbingnotsymmetric"></a><span data-ttu-id="a16a2-103">таббингнотсимметрик</span><span class="sxs-lookup"><span data-stu-id="a16a2-103">TabbingNotSymmetric</span></span>

## <a name="text"></a><span data-ttu-id="a16a2-104">Текст</span><span class="sxs-lookup"><span data-stu-id="a16a2-104">Text</span></span>

<span data-ttu-id="a16a2-105">Переходы назад и вперед не дают того же самого элемента.</span><span class="sxs-lookup"><span data-stu-id="a16a2-105">Tabbing backwards and forwards does not yield the same element.</span></span> <span data-ttu-id="a16a2-106">Ожидалось, {0} но получено {1}</span><span class="sxs-lookup"><span data-stu-id="a16a2-106">Expected {0} but received {1}</span></span>

## <a name="type"></a><span data-ttu-id="a16a2-107">Тип</span><span class="sxs-lookup"><span data-stu-id="a16a2-107">Type</span></span>

<span data-ttu-id="a16a2-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="a16a2-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="a16a2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a16a2-109">Description</span></span>

<span data-ttu-id="a16a2-110">При использовании стандартной навигации с помощью клавиатуры (TAB или SHIFT + TAB) невозможно повторить путь обхода по дереву элементов целевого объекта проверки, если направление обхода отменено.</span><span class="sxs-lookup"><span data-stu-id="a16a2-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to repeat the path of traversal through the element tree of the verification target if the direction of traversal is reversed.</span></span> <span data-ttu-id="a16a2-111">Например, переход вперед (TAB) x раз от элемента A (0) к элементу A (x), а затем по нажатию клавиши TAB (Shift + Tab) x раз приводит к возврату фокуса с помощью другого набора промежуточных элементов.</span><span class="sxs-lookup"><span data-stu-id="a16a2-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times results in element A(0) regaining focus through a different set of intermediate elements.</span></span>

<span data-ttu-id="a16a2-112">Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, так как обход элементов выглядит неустойчивым и непредсказуемым.</span><span class="sxs-lookup"><span data-stu-id="a16a2-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because traversing elements appears erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a16a2-113">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="a16a2-113">Possible causes</span></span>

-   <span data-ttu-id="a16a2-114">Несколько элементов или их родителей являются пользовательскими элементами управления, которые не реализуют правильную работу с вкладками.</span><span class="sxs-lookup"><span data-stu-id="a16a2-114">Multiple elements or their parents are custom controls that don't implement tabbing correctly.</span></span> <span data-ttu-id="a16a2-115">Например, свойство состояния MSAA задано неправильно.</span><span class="sxs-lookup"><span data-stu-id="a16a2-115">For example, the MSAA State property is not set correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a16a2-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a16a2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a16a2-117">Рекомендации по проектированию пользовательского интерфейса клавиатуры</span><span class="sxs-lookup"><span data-stu-id="a16a2-117">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 