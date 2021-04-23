---
title: Работа с индексами изображений состояний
description: Часто возникает путаница с тем, как задать и извлечь индекс изображения состояния в элементе управления "дерево-представление".
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be84035907b69ba98ed60a33046f1a58fd2b47b2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "103788904"
---
# <a name="how-to-work-with-state-image-indexes"></a><span data-ttu-id="f0c76-103">Работа с индексами изображений состояний</span><span class="sxs-lookup"><span data-stu-id="f0c76-103">How to Work With State Image Indexes</span></span>

<span data-ttu-id="f0c76-104">Часто возникает путаница с тем, как задать и извлечь индекс изображения состояния в элементе управления "дерево-представление".</span><span class="sxs-lookup"><span data-stu-id="f0c76-104">There is often confusion about how to set and retrieve the state image index in a tree-view control.</span></span> <span data-ttu-id="f0c76-105">В следующих примерах демонстрируется правильный метод установки и получения индекса изображения состояния.</span><span class="sxs-lookup"><span data-stu-id="f0c76-105">The following examples demonstrate the proper method for setting and retrieving the state image index.</span></span> <span data-ttu-id="f0c76-106">В примерах предполагается, что в элементе управления "дерево" установлены только два индекса состояния: "снят" и "Проверено".</span><span class="sxs-lookup"><span data-stu-id="f0c76-106">The examples assume that there are only two state image indexes in the tree-view control, unchecked and checked.</span></span> <span data-ttu-id="f0c76-107">Если приложение содержит более двух, эти функции необходимо изменить, чтобы обрабатывать этот случай.</span><span class="sxs-lookup"><span data-stu-id="f0c76-107">If your application contains more than two, these functions will need to be modified to handle that case.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f0c76-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="f0c76-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f0c76-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="f0c76-109">Technologies</span></span>

-   [<span data-ttu-id="f0c76-110">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="f0c76-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f0c76-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="f0c76-111">Prerequisites</span></span>

-   <span data-ttu-id="f0c76-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="f0c76-112">C/C++</span></span>
-   <span data-ttu-id="f0c76-113">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="f0c76-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f0c76-114">Инструкции</span><span class="sxs-lookup"><span data-stu-id="f0c76-114">Instructions</span></span>

### <a name="set-a-tree-view-items-check-state"></a><span data-ttu-id="f0c76-115">Задание состояния проверки Tree-View элемента</span><span class="sxs-lookup"><span data-stu-id="f0c76-115">Set a Tree-View Item's Check State</span></span>

<span data-ttu-id="f0c76-116">В следующем примере показано, как задать состояние флажка для элемента представления в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="f0c76-116">The following example demonstrates how to set a tree-view item's check state.</span></span>


```C++
  BOOL TreeView_SetCheckState(HWND hwndTreeView, HTREEITEM hItem, BOOL fCheck)
  {
      TVITEM tvItem;

      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Image 1 in the tree-view check box image list is the unchecked box. 
      // Image 2 is the checked box.

      tvItem.state = INDEXTOSTATEIMAGEMASK((fCheck ? 2 : 1));

      return TreeView_SetItem(hwndTreeView, &tvItem);
  }
```



### <a name="retrieve-a-tree-view-items-check-state"></a><span data-ttu-id="f0c76-117">Получение состояния проверки Tree-View элемента</span><span class="sxs-lookup"><span data-stu-id="f0c76-117">Retrieve a Tree-View Item's Check State</span></span>

<span data-ttu-id="f0c76-118">В следующем примере показано, как получить состояние проверки элемента древовидного представления.</span><span class="sxs-lookup"><span data-stu-id="f0c76-118">The following example demonstrates how to retrieve a tree-view item's check state.</span></span>


```C++
  BOOL TreeView_GetCheckState(HWND hwndTreeView, HTREEITEM hItem)
  {
      TVITEM tvItem;

      // Prepare to receive the desired information.
      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Request the information.
      TreeView_GetItem(hwndTreeView, &tvItem);

      // Return zero if it's not checked, or nonzero otherwise.
      return ((BOOL)(tvItem.state >> 12) - 1);
  }
```



## <a name="related-topics"></a><span data-ttu-id="f0c76-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f0c76-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0c76-120">Использование элементов управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="f0c76-120">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="f0c76-121">Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="f0c76-121">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




