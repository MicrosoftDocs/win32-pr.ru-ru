---
title: UI_PKEY_FontProperties_DeltaSize
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ делтасизе.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67778a710de8f69e0aea1134c12fb9ee3ebe0133
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444395"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="80d5c-103">UI \_ PKEY \_ фонтпропертиес \_ делтасизе</span><span class="sxs-lookup"><span data-stu-id="80d5c-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="80d5c-104">Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ делтасизе.</span><span class="sxs-lookup"><span data-stu-id="80d5c-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="80d5c-105">Remarks</span><span class="sxs-lookup"><span data-stu-id="80d5c-105">Remarks</span></span>

<span data-ttu-id="80d5c-106">UI \_ PKEY \_ фонтпропертиес \_ делтасизе используется приложением в случаях, когда невозможно указать для приложения значение **размера шрифта**, например, если выбрано выполнение хетероженеаусли размера текста.</span><span class="sxs-lookup"><span data-stu-id="80d5c-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="80d5c-107">Элемент управления " **Размер шрифта** " имеет значение "пустой", а UI \_ PKEY \_ фонтпропертиес \_ делтасизе используется для записи взаимодействия пользователя с кнопками " **увеличение шрифта** " и " **Сжатие шрифта** ".</span><span class="sxs-lookup"><span data-stu-id="80d5c-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="80d5c-108">UI \_ PKEY \_ фонтпропертиес \_ Делтасизе входит в [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span><span class="sxs-lookup"><span data-stu-id="80d5c-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="80d5c-109">На следующем снимке экрана показаны кнопки **увеличение размера шрифта** и **Сжатие шрифта** на ленте [**фонтконтрол**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="80d5c-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![снимок экрана с кнопками увеличения и уменьшения размера шрифта в фонтконтрол.](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="80d5c-111">В следующей таблице описаны значения свойств.</span><span class="sxs-lookup"><span data-stu-id="80d5c-111">The following table describes the property values.</span></span>



|     <span data-ttu-id="80d5c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="80d5c-112">Value</span></span>                 |  <span data-ttu-id="80d5c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="80d5c-113">Description</span></span>                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="80d5c-114">Нажата кнопка " **увеличить шрифт** ".</span><span class="sxs-lookup"><span data-stu-id="80d5c-114">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="80d5c-115">Нажата кнопка " **Сжать шрифт** ".</span><span class="sxs-lookup"><span data-stu-id="80d5c-115">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="80d5c-116">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="80d5c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80d5c-117">Свойства элемента управления "Шрифт"</span><span class="sxs-lookup"><span data-stu-id="80d5c-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="80d5c-118">**фонтделтасизе пользовательского интерфейса \_**</span><span class="sxs-lookup"><span data-stu-id="80d5c-118">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="80d5c-119">Элемент управления шрифтами</span><span class="sxs-lookup"><span data-stu-id="80d5c-119">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 