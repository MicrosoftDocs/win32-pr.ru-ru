---
title: тримигхтбециклик
description: тримигхтбециклик
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337668"
---
# <a name="treemightbecyclic"></a><span data-ttu-id="df868-103">тримигхтбециклик</span><span class="sxs-lookup"><span data-stu-id="df868-103">TreeMightBeCyclic</span></span>

## <a name="text"></a><span data-ttu-id="df868-104">Текст</span><span class="sxs-lookup"><span data-stu-id="df868-104">Text</span></span>

<span data-ttu-id="df868-105">Дерево имеет {0} уровень вложенности.</span><span class="sxs-lookup"><span data-stu-id="df868-105">Tree is {0} levels deep.</span></span> <span data-ttu-id="df868-106">Это может означать, что дерево специальных возможностей является циклическим, и поэтому оно кажется бесконечным.</span><span class="sxs-lookup"><span data-stu-id="df868-106">This might indicate that the accessibility tree is cyclic, and thus it would appear to be infinite.</span></span>

## <a name="type"></a><span data-ttu-id="df868-107">Тип</span><span class="sxs-lookup"><span data-stu-id="df868-107">Type</span></span>

<span data-ttu-id="df868-108">Ошибка</span><span class="sxs-lookup"><span data-stu-id="df868-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="df868-109">Описание</span><span class="sxs-lookup"><span data-stu-id="df868-109">Description</span></span>

<span data-ttu-id="df868-110">Дерево элементов является циклическим, а глубина дерева может быть бесконечной.</span><span class="sxs-lookup"><span data-stu-id="df868-110">The element tree is cyclic and the tree depth might be infinite.</span></span>

<span data-ttu-id="df868-111">Эта проблема вызывает проблемы для людей, которые используют средство чтения с экрана и клавиатуру для навигации, так как в целевом приложении не будет заметного ограничения для обхода элементов.</span><span class="sxs-lookup"><span data-stu-id="df868-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there will be no apparent limit to the traversal of elements in the target application.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="df868-112">Возможные причины</span><span class="sxs-lookup"><span data-stu-id="df868-112">Possible causes</span></span>

<span data-ttu-id="df868-113">Несколько элементов или их родителей являются пользовательскими элементами управления, которые не реализуют правильную работу с вкладками.</span><span class="sxs-lookup"><span data-stu-id="df868-113">Multiple elements, or their parents, are custom controls that do not implement tabbing correctly.</span></span> <span data-ttu-id="df868-114">Например, свойство [состояния](state-property.md) MSAA неправильно обновляется.</span><span class="sxs-lookup"><span data-stu-id="df868-114">For example, the MSAA [State](state-property.md) property is not updated correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df868-115">См. также</span><span class="sxs-lookup"><span data-stu-id="df868-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df868-116">Рекомендации по проектированию пользовательского интерфейса клавиатуры</span><span class="sxs-lookup"><span data-stu-id="df868-116">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[<span data-ttu-id="df868-117">Рекомендации по взаимодействию с пользователем Windows — клавиатура</span><span class="sxs-lookup"><span data-stu-id="df868-117">Windows User Experience Interaction Guidelines - Keyboard</span></span>](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 