---
title: Использование Tree-View Инфотипс
description: При применении стиля подсказки «ТЕЛЕВИЗОРы» \_ к элементу управления древовидного представления он создает ТВН \_ жетинфотип уведомления при наведении курсора на элемент в представлении в виде дерева. Отвечая на это уведомление, можно задать текст, отображаемый в подсказке.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff9273b28b614e7935f6ac507288a5733271fb455a6be1e85b52c5b0ba8bbb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132034"
---
# <a name="how-to-use-tree-view-infotips"></a>Использование Tree-View Инфотипс

При применении стиля [**\_ подсказки «телевизоры**](tree-view-control-window-styles.md) » к элементу управления древовидного представления он создает [ТВН \_ жетинфотип](tvn-getinfotip.md) уведомления при наведении курсора на элемент в представлении в виде дерева. Отвечая на это уведомление, можно задать текст, отображаемый в подсказке.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Windows Программирование пользовательского интерфейса

## <a name="instructions"></a>Инструкции

### <a name="use-tree-view-infotips"></a>Использование Tree-View Инфотипс

В следующем примере кода показано, как приложение может реагировать на уведомление. Для простоты в примере просто копируется текст элемента в подсказка.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование элементов управления Tree-View](using-treeview.md)
</dt> <dt>

[Пример Кустдтв иллюстрирует пользовательский вывод в элементе управления Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




