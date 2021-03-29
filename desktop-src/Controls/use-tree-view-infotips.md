---
title: Использование Tree-View Инфотипс
description: При применении стиля подсказки «ТЕЛЕВИЗОРы» \_ к элементу управления древовидного представления он создает ТВН \_ жетинфотип уведомления при наведении курсора на элемент в представлении в виде дерева. Отвечая на это уведомление, можно задать текст, отображаемый в подсказке.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0ef862d68cfd9f6ac5a97e82c80622e9c02121
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "105654265"
---
# <a name="how-to-use-tree-view-infotips"></a><span data-ttu-id="da3f6-104">Использование Tree-View Инфотипс</span><span class="sxs-lookup"><span data-stu-id="da3f6-104">How to Use Tree-View Infotips</span></span>

<span data-ttu-id="da3f6-105">При применении стиля [**\_ подсказки «телевизоры**](tree-view-control-window-styles.md) » к элементу управления древовидного представления он создает [ТВН \_ жетинфотип](tvn-getinfotip.md) уведомления при наведении курсора на элемент в представлении в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="da3f6-105">When you apply the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style to a tree-view control, it generates [TVN\_GETINFOTIP](tvn-getinfotip.md) notifications when the cursor is over an item in the tree view.</span></span> <span data-ttu-id="da3f6-106">Отвечая на это уведомление, можно задать текст, отображаемый в подсказке.</span><span class="sxs-lookup"><span data-stu-id="da3f6-106">By responding to this notification, you can set the text that appears in the infotip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="da3f6-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="da3f6-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="da3f6-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="da3f6-108">Technologies</span></span>

-   [<span data-ttu-id="da3f6-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="da3f6-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="da3f6-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="da3f6-110">Prerequisites</span></span>

-   <span data-ttu-id="da3f6-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="da3f6-111">C/C++</span></span>
-   <span data-ttu-id="da3f6-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="da3f6-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="da3f6-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="da3f6-113">Instructions</span></span>

### <a name="use-tree-view-infotips"></a><span data-ttu-id="da3f6-114">Использование Tree-View Инфотипс</span><span class="sxs-lookup"><span data-stu-id="da3f6-114">Use Tree-View Infotips</span></span>

<span data-ttu-id="da3f6-115">В следующем примере кода показано, как приложение может реагировать на уведомление.</span><span class="sxs-lookup"><span data-stu-id="da3f6-115">The following example code shows how an application might respond to the notification.</span></span> <span data-ttu-id="da3f6-116">Для простоты в примере просто копируется текст элемента в подсказка.</span><span class="sxs-lookup"><span data-stu-id="da3f6-116">For simplicity, the example just copies the text for the item to the infotip.</span></span>


```
  case WM_NOTIFY:
    switch (((LPNMHDR) lParam)->code)
    {
    case TVN_GETINFOTIP:
        {
          LPNMTVGETINFOTIP pTip = (LPNMTVGETINFOTIP)lParam;
          HWND hTree            = GetDlgItem(hDlg, IDC_TREE1);
          HTREEITEM item        = pTip->hItem;

          // Get the text for the item.
          TVITEM tvitem;
          tvitem.mask       = TVIF_TEXT;
          tvitem.hItem      = item;
          TCHAR temp[1024];
          tvitem.pszText    = infoTipBuf;
          tvitem.cchTextMax = sizeof(temp) / sizeof(TCHAR);
          TreeView_GetItem(hTree, &tvitem);

          // Copy the text to the infotip.
          wcscpy_s(pTip->pszText, pTip->cchTextMax, tvitem.pszText);
          break;
        }
      }
      return TRUE;
```



## <a name="related-topics"></a><span data-ttu-id="da3f6-117">См. также</span><span class="sxs-lookup"><span data-stu-id="da3f6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da3f6-118">Использование элементов управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="da3f6-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="da3f6-119">Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View</span><span class="sxs-lookup"><span data-stu-id="da3f6-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




