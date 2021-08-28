---
title: Использование пользовательского рисования
description: В этом разделе содержатся примеры, демонстрирующие реализацию пользовательского рисования.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90cff5fd4d692d31b69c85980f872f3aca4504cad81a3439d0c4d31a4c73d90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655874"
---
# <a name="using-custom-draw"></a>Использование пользовательского рисования

В этом разделе содержатся примеры, демонстрирующие реализацию пользовательского рисования.

Следующий фрагмент кода является частью обработчика [**\_ уведомлений WM**](wm-notify.md) , который показывает, как управлять пользовательскими уведомлениями рисования, отправленными в элемент управления "представление списка".


```C++
        
LPNMLISTVIEW  pnm  = (LPNMLISTVIEW)lParam;

switch (pnm->hdr.code){
...
case NM_CUSTOMDRAW:

    LPNMLVCUSTOMDRAW  lplvcd = (LPNMLVCUSTOMDRAW)lParam;

    switch(lplvcd->nmcd.dwDrawStage) {

    case CDDS_PREPAINT :
        return CDRF_NOTIFYITEMDRAW;

    case CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForItem(lplvcd->nmcd.dwItemSpec,
                                    lplvcd->nmcd.lItemlParam) );
        lplvcd->clrText = GetColorForItem(lplvcd->nmcd.dwItemSpec,
                                          lplvcd->nmcd.lItemlParam);
        lplvcd->clrTextBk = GetBkColorForItem(lplvcd->nmcd.dwItemSpec,
                                              lplvcd->nmcd.lItemlParam);

/* At this point, you can change the background colors for the item
and any subitems and return CDRF_NEWFONT. If the list-view control
is in report mode, you can simply return CDRF_NOTIFYSUBITEMDRAW
to customize the item's subitems individually */
        ...

        return CDRF_NEWFONT;
    //  or return CDRF_NOTIFYSUBITEMDRAW;

    case CDDS_SUBITEM | CDDS_ITEMPREPAINT:
        SelectObject(lplvcd->nmcd.hdc,
                     GetFontForSubItem(lplvcd->nmcd.dwItemSpec,
                                       lplvcd->nmcd.lItemlParam,
                                       lplvcd->iSubItem));
        lplvcd->clrText = GetColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                             lplvcd->nmcd.lItemlParam,
                                             lplvcd->iSubItem));
        lplvcd->clrTextBk = GetBkColorForSubItem(lplvcd->nmcd.dwItemSpec,
                                                 lplvcd->nmcd.lItemlParam,
                                                 lplvcd->iSubItem));

/* This notification is received only if you are in report mode and
returned CDRF_NOTIFYSUBITEMDRAW in the previous step. At
this point, you can change the background colors for the
subitem and return CDRF_NEWFONT.*/
        ...
        return CDRF_NEWFONT;    
    }
...
}
        
```



В первом уведомлении [ \_ кустомдрав](nm-customdraw.md) в качестве элемента **двдравстаже** структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) задано значение **кддс \_**. Обработчик возвращает [**кдрф \_ нотифитемдрав**](cdrf-constants.md) , чтобы указать, что он хочет изменить один или несколько элементов по отдельности.

Если на предыдущем шаге был возвращен [**кдрф \_ нотифитемдрав**](cdrf-constants.md) , то в следующем уведомлении [ \_ кустомдрав](nm-customdraw.md) для **двдравстаже** задано значение **кддс \_ итемпрепаинт**. Обработчик получает текущие значения цвета и шрифта. На этом этапе можно указать новые значения для мелких значков, крупных значков и режимов списка. Если элемент управления находится в режиме отчета, можно также указать новые значения, которые будут применяться ко всем подэлементам элемента. Если ничего не изменилось, возвратите [**кдрф \_ невфонт**](cdrf-constants.md). Если элемент управления находится в режиме отчета и необходимо обменять подэлементы по отдельности, возвращается **кдрф \_ нотифисубитемдрав**.

Окончательное уведомление отправляется только в том случае, если элемент управления находится в режиме отчета и вы вернули **кдрф \_ нотифисубитемдрав** на предыдущем шаге. Процедура изменения шрифтов и цветов такая же, как и на этом шаге, но применяется только к одному подэлементу. Возвращает [**кдрф \_ невфонт**](cdrf-constants.md) , чтобы уведомить элемент управления об изменении цвета или шрифта.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[О пользовательской прорисовке](about-custom-draw.md)
</dt> <dt>

[Пользовательская ссылка для рисования](custom-draw-reference.md)
</dt> <dt>

**Другие ресурсы**
</dt> <dt>

[Пример: Кустдтв демонстрирует пользовательское рисование в TreeView (Q248496)](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




