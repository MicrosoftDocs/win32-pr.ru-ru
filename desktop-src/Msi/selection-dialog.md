---
description: Это модальное диалоговое окно позволяет пользователям выбирать определенные элементы.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Диалоговое окно выбора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651195"
---
# <a name="selection-dialog"></a><span data-ttu-id="17e0c-103">Диалоговое окно выбора</span><span class="sxs-lookup"><span data-stu-id="17e0c-103">Selection Dialog</span></span>

<span data-ttu-id="17e0c-104">Это модальное диалоговое окно позволяет пользователям выбирать определенные элементы.</span><span class="sxs-lookup"><span data-stu-id="17e0c-104">This modal dialog box enables users to select particular items.</span></span>

<span data-ttu-id="17e0c-105">Диалоговое окно выбора содержит [элемент управления селектионтри](selectiontree-control.md) , который публикует несколько контролевентс.</span><span class="sxs-lookup"><span data-stu-id="17e0c-105">A Selection Dialog box contains a [SelectionTree control](selectiontree-control.md) that publishes several ControlEvents.</span></span> <span data-ttu-id="17e0c-106">Обычно эти Контролевентс подписываются в виде [текста](text-control.md), [значков](icon-control.md)или [растровых](bitmap-control.md) элементов управления, отображающих описание, размер, путь и значок выделенного элемента.</span><span class="sxs-lookup"><span data-stu-id="17e0c-106">Commonly these ControlEvents are subscribed to by [Text](text-control.md), [Icon](icon-control.md), or [Bitmap](bitmap-control.md) controls that display a description, the size, the path, and the icon of the highlighted item.</span></span>

<span data-ttu-id="17e0c-107">В диалоговом окне имеется [элемент управления "кнопка](pushbutton-control.md) ", который публикует [селектионбровсе таблице ControlEvent событие](selectionbrowse-controlevent.md) и порождает [диалоговое окно обзора](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="17e0c-107">There is a [PushButton control](pushbutton-control.md) on the dialog box that publishes the [SelectionBrowse ControlEvent](selectionbrowse-controlevent.md) and spawns a [Browse Dialog](browse-dialog.md).</span></span> <span data-ttu-id="17e0c-108">Элемент управления Обзор позволяет пользователю выбрать каталог.</span><span class="sxs-lookup"><span data-stu-id="17e0c-108">The Browse control enables the user to select a directory.</span></span>

<span data-ttu-id="17e0c-109">Дерево выбора заполняется только после вызова действия [костинитиализе](costinitialize-action.md) и [костфинализе](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="17e0c-109">The selection tree is populated only after the [CostInitialize action](costinitialize-action.md) and [CostFinalize action](costfinalize-action.md) are called.</span></span>

<span data-ttu-id="17e0c-110">Диалоговое окно выбора обычно используется для выбора компонентов.</span><span class="sxs-lookup"><span data-stu-id="17e0c-110">A Selection dialog box is commonly used to select features.</span></span> <span data-ttu-id="17e0c-111">Функции перечислены как элементы в элементе управления Селектионтри и помечаются короткой строкой текста, отображаемой в столбце Title [таблицы Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="17e0c-111">The features are listed as items in a SelectionTree control and labeled with the short string of text appearing in the Title column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="17e0c-112">Текстовая строка в столбце Description таблицы Feature публикуется в виде [Селектиондескриптион таблице ControlEvent событие](selectiondescription-controlevent.md) и отображается в [элементе управления "текст](text-control.md) " в диалоговом окне выбора.</span><span class="sxs-lookup"><span data-stu-id="17e0c-112">The text string in the Description column of the Feature table is published as a [SelectionDescription ControlEvent](selectiondescription-controlevent.md) and displayed by a [Text control](text-control.md) in the Selection Dialog box.</span></span> <span data-ttu-id="17e0c-113">Элемент управления "дерево выбора" также публикует маркер для значка выделенного элемента.</span><span class="sxs-lookup"><span data-stu-id="17e0c-113">The Selection tree control also publishes the handle to the icon of the highlighted item.</span></span>

 

 



