---
title: Макросы представления в виде дерева
description: Макросы представления в виде дерева
ms.assetid: ee569a0e-21f3-4d46-ac7d-e152f8b35391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63ffb8c7e643daba2cb01d188c3d111179ba6441dde76f9ab0c08b41de703a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833085"
---
# <a name="tree-view-macros"></a>Макросы представления в виде дерева

## <a name="in-this-section"></a>В этом разделе

-   [**\_Креатедрагимаже TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage)
-   [**\_Делетеаллитемс TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteallitems)
-   [**\_DeleteItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_deleteitem)
-   [**\_Едитлабел TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel)
-   [**\_Ендедитлабелнов TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow)
-   [**\_Енсуревисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible)
-   [**\_Развернуть TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_expand)
-   [**\_Жетбкколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor)
-   [**\_Жетчеккстате TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcheckstate)
-   [**Элемент управления TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getchild)
-   [**Число в TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getcount)
-   [**\_Жетдрофилигхт TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getdrophilight)
-   [**\_Жетедитконтрол TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol)
-   [**\_Жетекстендедстиле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getextendedstyle)
-   [**\_Жетфирствисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getfirstvisible)
-   [**TreeView — \_ ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist)
-   [**Отступ в TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getindent)
-   [**\_Жетинсертмаркколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor)
-   [**\_Жетисеарчстринг TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring)
-   [**\_Элемент TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem)
-   [**\_GetItemHeight TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemheight)
-   [**\_Жетитемпартрект TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitempartrect)
-   [**\_Жетитемрект TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemrect)
-   [**\_Жетитемстате TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitemstate)
-   [**\_Жетластвисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlastvisible)
-   [**\_Жетлинеколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getlinecolor)
-   [**\_Жетнекститем TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextitem)
-   [**\_Жетнекстселектед TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextselected)
-   [**\_Жетнекстсиблинг TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextsibling)
-   [**\_Жетнекствисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getnextvisible)
-   [**\_Родители TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getparent)
-   [**\_Жетпревсиблинг TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevsibling)
-   [**\_Жетпреввисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getprevvisible)
-   [**\_Корень TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getroot)
-   [**\_Жетскроллтиме TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getscrolltime)
-   [**\_Жетселектедкаунт TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselectedcount)
-   [**\_Выбор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getselection)
-   [**\_Жеттекстколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettextcolor)
-   [**\_Подсказки TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_gettooltips)
-   [**\_Жетуникодеформат TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getunicodeformat)
-   [**\_Жетвисиблекаунт TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getvisiblecount)
-   [**\_HitTest TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest)
-   [**\_InsertItem TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_insertitem)
-   [**\_МапакЦидтохтриитем TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
-   [**\_МафтриитемтоакЦид TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
-   [**\_Выбор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_select)
-   [**\_Селектдроптаржет TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectdroptarget)
-   [**\_Селектитем TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectitem)
-   [**\_Селектсетфирствисибле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_selectsetfirstvisible)
-   [**\_Сетаутоскроллинфо TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo)
-   [**\_Сетбкколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor)
-   [**\_Сетбордер TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setborder)
-   [**\_Сетчеккстате TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setcheckstate)
-   [**\_Сетекстендедстиле TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle)
-   [**\_Сесот TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
-   [**\_Сетимажелист TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist)
-   [**\_Сетиндент TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
-   [**\_Сетинсертмарк TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmark)
-   [**\_Сетинсертмаркколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setinsertmarkcolor)
-   [**\_Сетитем TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)
-   [**\_Сетитемхеигхт TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight)
-   [**\_Сетитемстате TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemstate)
-   [**\_Сетлинеколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setlinecolor)
-   [**\_Сетскроллтиме TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setscrolltime)
-   [**\_Сеттекстколор TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor)
-   [**\_Сеттултипс TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settooltips)
-   [**\_Сетуникодеформат TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat)
-   [**\_Шовинфотип TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_showinfotip)
-   [**\_Сортчилдрен TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildren)
-   [**\_Сортчилдренкб TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb)

 

 




