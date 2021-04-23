---
title: UI_PKEY_FontProperties_DeltaSize
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ делтасизе.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070020"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="6493f-103">UI \_ PKEY \_ фонтпропертиес \_ делтасизе</span><span class="sxs-lookup"><span data-stu-id="6493f-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="6493f-104">Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ делтасизе.</span><span class="sxs-lookup"><span data-stu-id="6493f-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="6493f-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6493f-105">Remarks</span></span>

<span data-ttu-id="6493f-106">UI \_ PKEY \_ фонтпропертиес \_ делтасизе используется приложением в случаях, когда невозможно указать для приложения значение **размера шрифта**, например, если выбрано выполнение хетероженеаусли размера текста.</span><span class="sxs-lookup"><span data-stu-id="6493f-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="6493f-107">Элемент управления " **Размер шрифта** " имеет значение "пустой", а UI \_ PKEY \_ фонтпропертиес \_ делтасизе используется для записи взаимодействия пользователя с кнопками " **увеличение шрифта** " и " **Сжатие шрифта** ".</span><span class="sxs-lookup"><span data-stu-id="6493f-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="6493f-108">UI \_ PKEY \_ фонтпропертиес \_ Делтасизе входит в [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span><span class="sxs-lookup"><span data-stu-id="6493f-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="6493f-109">На следующем снимке экрана показаны кнопки **увеличение размера шрифта** и **Сжатие шрифта** на ленте [**фонтконтрол**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="6493f-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![снимок экрана с кнопками увеличения и уменьшения размера шрифта в фонтконтрол.](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="6493f-111">В следующей таблице описаны значения свойств.</span><span class="sxs-lookup"><span data-stu-id="6493f-111">The following table describes the property values.</span></span>



|                           |                                 |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="6493f-112">Нажата кнопка " **увеличить шрифт** ".</span><span class="sxs-lookup"><span data-stu-id="6493f-112">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="6493f-113">Нажата кнопка " **Сжать шрифт** ".</span><span class="sxs-lookup"><span data-stu-id="6493f-113">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6493f-114">См. также</span><span class="sxs-lookup"><span data-stu-id="6493f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6493f-115">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="6493f-115">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="6493f-116">**фонтделтасизе пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="6493f-116">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="6493f-117">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="6493f-117">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 