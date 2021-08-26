---
title: Работа с индексами изображений состояний
description: Часто возникает путаница с тем, как задать и извлечь индекс изображения состояния в элементе управления "дерево-представление".
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04504019f79a388b6c21f940724de884d8516263daf6d410a841a96fc2e557b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059304"
---
# <a name="how-to-work-with-state-image-indexes"></a>Работа с индексами изображений состояний

Часто возникает путаница с тем, как задать и извлечь индекс изображения состояния в элементе управления "дерево-представление". В следующих примерах демонстрируется правильный метод установки и получения индекса изображения состояния. В примерах предполагается, что в элементе управления "дерево" установлены только два индекса состояния: "снят" и "Проверено". Если приложение содержит более двух, эти функции необходимо изменить, чтобы обрабатывать этот случай.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="set-a-tree-view-items-check-state"></a>Задание состояния проверки Tree-View элемента

В следующем примере показано, как задать состояние флажка для элемента представления в виде дерева.


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



### <a name="retrieve-a-tree-view-items-check-state"></a>Получение состояния проверки Tree-View элемента

В следующем примере показано, как получить состояние проверки элемента древовидного представления.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления Tree-View](using-treeview.md)
</dt> <dt>

[Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




