---
title: Использование пользовательского рисования
description: В этом разделе содержатся примеры, демонстрирующие реализацию пользовательского рисования.
ms.assetid: ab2a8930-1ee1-4b9f-bd3e-4b34df84957b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f0b8a2585103aa27a27f0138a49885cc726d3b1
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104069626"
---
# <a name="using-custom-draw"></a><span data-ttu-id="26aa3-103">Использование пользовательского рисования</span><span class="sxs-lookup"><span data-stu-id="26aa3-103">Using Custom Draw</span></span>

<span data-ttu-id="26aa3-104">В этом разделе содержатся примеры, демонстрирующие реализацию пользовательского рисования.</span><span class="sxs-lookup"><span data-stu-id="26aa3-104">This section contains examples that demonstrate how to implement custom draw.</span></span>

<span data-ttu-id="26aa3-105">Следующий фрагмент кода является частью обработчика [**\_ уведомлений WM**](wm-notify.md) , который показывает, как управлять пользовательскими уведомлениями рисования, отправленными в элемент управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="26aa3-105">The following code fragment is a portion of a [**WM\_NOTIFY**](wm-notify.md) handler that illustrates how to handle custom draw notifications sent to a list-view control.</span></span>


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



<span data-ttu-id="26aa3-106">В первом уведомлении [ \_ кустомдрав](nm-customdraw.md) в качестве элемента **двдравстаже** структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) задано значение **кддс \_**.</span><span class="sxs-lookup"><span data-stu-id="26aa3-106">The first [NM\_CUSTOMDRAW](nm-customdraw.md) notification has the **dwDrawStage** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure set to **CDDS\_PREPAINT**.</span></span> <span data-ttu-id="26aa3-107">Обработчик возвращает [**кдрф \_ нотифитемдрав**](cdrf-constants.md) , чтобы указать, что он хочет изменить один или несколько элементов по отдельности.</span><span class="sxs-lookup"><span data-stu-id="26aa3-107">The handler returns [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) to indicate that it wishes to modify one or more items individually.</span></span>

<span data-ttu-id="26aa3-108">Если на предыдущем шаге был возвращен [**кдрф \_ нотифитемдрав**](cdrf-constants.md) , то в следующем уведомлении [ \_ кустомдрав](nm-customdraw.md) для **двдравстаже** задано значение **кддс \_ итемпрепаинт**.</span><span class="sxs-lookup"><span data-stu-id="26aa3-108">If [**CDRF\_NOTIFYITEMDRAW**](cdrf-constants.md) was returned in the previous step, the next [NM\_CUSTOMDRAW](nm-customdraw.md) notification has **dwDrawStage** set to **CDDS\_ITEMPREPAINT**.</span></span> <span data-ttu-id="26aa3-109">Обработчик получает текущие значения цвета и шрифта.</span><span class="sxs-lookup"><span data-stu-id="26aa3-109">The handler retrieves the current color and font values.</span></span> <span data-ttu-id="26aa3-110">На этом этапе можно указать новые значения для мелких значков, крупных значков и режимов списка.</span><span class="sxs-lookup"><span data-stu-id="26aa3-110">At this point, you can specify new values for small icon, large icon, and list modes.</span></span> <span data-ttu-id="26aa3-111">Если элемент управления находится в режиме отчета, можно также указать новые значения, которые будут применяться ко всем подэлементам элемента.</span><span class="sxs-lookup"><span data-stu-id="26aa3-111">If the control is in report mode, you can also specify new values that will apply to all subitems of the item.</span></span> <span data-ttu-id="26aa3-112">Если ничего не изменилось, возвратите [**кдрф \_ невфонт**](cdrf-constants.md).</span><span class="sxs-lookup"><span data-stu-id="26aa3-112">If you have changed anything, return [**CDRF\_NEWFONT**](cdrf-constants.md).</span></span> <span data-ttu-id="26aa3-113">Если элемент управления находится в режиме отчета и необходимо обменять подэлементы по отдельности, возвращается **кдрф \_ нотифисубитемдрав**.</span><span class="sxs-lookup"><span data-stu-id="26aa3-113">If the control is in report mode and you want to handle the subitems individually, return **CDRF\_NOTIFYSUBITEMDRAW**.</span></span>

<span data-ttu-id="26aa3-114">Окончательное уведомление отправляется только в том случае, если элемент управления находится в режиме отчета и вы вернули **кдрф \_ нотифисубитемдрав** на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="26aa3-114">The final notification is only sent if the control is in report mode and you returned **CDRF\_NOTIFYSUBITEMDRAW** in the previous step.</span></span> <span data-ttu-id="26aa3-115">Процедура изменения шрифтов и цветов такая же, как и на этом шаге, но применяется только к одному подэлементу.</span><span class="sxs-lookup"><span data-stu-id="26aa3-115">The procedure for changing fonts and colors is the same as that step, but it only applies to a single subitem.</span></span> <span data-ttu-id="26aa3-116">Возвращает [**кдрф \_ невфонт**](cdrf-constants.md) , чтобы уведомить элемент управления об изменении цвета или шрифта.</span><span class="sxs-lookup"><span data-stu-id="26aa3-116">Return [**CDRF\_NEWFONT**](cdrf-constants.md) to notify the control if the color or font was changed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26aa3-117">См. также</span><span class="sxs-lookup"><span data-stu-id="26aa3-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="26aa3-118">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="26aa3-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="26aa3-119">О пользовательской прорисовке</span><span class="sxs-lookup"><span data-stu-id="26aa3-119">About Custom Draw</span></span>](about-custom-draw.md)
</dt> <dt>

[<span data-ttu-id="26aa3-120">Пользовательская ссылка для рисования</span><span class="sxs-lookup"><span data-stu-id="26aa3-120">Custom Draw Reference</span></span>](custom-draw-reference.md)
</dt> <dt>

<span data-ttu-id="26aa3-121">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="26aa3-121">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="26aa3-122">Пример: Кустдтв демонстрирует пользовательское рисование в TreeView (Q248496)</span><span class="sxs-lookup"><span data-stu-id="26aa3-122">SAMPLE: CustDTv Illustrates Custom Draw in a TreeView (Q248496)</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




