---
title: TEXT. Value
description: Атрибут value указывает или получает текст, отображаемый в элементе управления "текст".
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- ТЕКСТОВЫЙ. Value — проигрыватель Windows Media
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648679"
---
# <a name="textvalue"></a><span data-ttu-id="bdeda-104">TEXT. Value</span><span class="sxs-lookup"><span data-stu-id="bdeda-104">TEXT.value</span></span>

<span data-ttu-id="bdeda-105">Атрибут **value** указывает или получает текст, отображаемый в элементе управления "текст".</span><span class="sxs-lookup"><span data-stu-id="bdeda-105">The **value** attribute specifies or retrieves the text that is displayed in the Text control.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="bdeda-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="bdeda-106">Possible Values</span></span>

<span data-ttu-id="bdeda-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bdeda-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdeda-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bdeda-108">Remarks</span></span>

<span data-ttu-id="bdeda-109">Если ширина текстового элемента управления недостаточно для того, чтобы вместить указанный текст, текст обрезается, а для демонстрации факта отображается многоточие.</span><span class="sxs-lookup"><span data-stu-id="bdeda-109">If the width of the Text control is insufficient to contain the text provided, the text is cropped, and an ellipsis is shown to illustrate the fact.</span></span> <span data-ttu-id="bdeda-110">Если атрибут **ToolTip** не задан, то полный текст будет отображаться в виде подсказки при наведении курсора мыши на элемент управления.</span><span class="sxs-lookup"><span data-stu-id="bdeda-110">If the **toolTip** attribute has not been set, the complete text will then appear as a ToolTip when the cursor hovers over the control.</span></span>

<span data-ttu-id="bdeda-111">Если ширина не указана, по умолчанию ширина элемента управления равна ширине строки.</span><span class="sxs-lookup"><span data-stu-id="bdeda-111">If a width is not specified, the default width for the control is the width of the string.</span></span>

<span data-ttu-id="bdeda-112">Если высота элемента управления не задана, высота по умолчанию — одна строка.</span><span class="sxs-lookup"><span data-stu-id="bdeda-112">If the height of the control is not specified, the default height is one line.</span></span>

<span data-ttu-id="bdeda-113">Если атрибут **WordWrap** имеет значение true и высота элемента достаточно велика для размещения другой строки текста, текст переносится на следующую строку.</span><span class="sxs-lookup"><span data-stu-id="bdeda-113">If the **wordWrap** attribute is set to true and the height of the control is enough to accommodate another line of text, the text wraps to a subsequent line.</span></span> <span data-ttu-id="bdeda-114">Заключение происходит только между словами.</span><span class="sxs-lookup"><span data-stu-id="bdeda-114">Wrapping only occurs between words.</span></span> <span data-ttu-id="bdeda-115">Разрывы строк также могут быть принудительно применены, как описано в разделе **WordWrap**.</span><span class="sxs-lookup"><span data-stu-id="bdeda-115">Line breaks may also be forced, as explained under **wordWrap**.</span></span>

## <a name="examples"></a><span data-ttu-id="bdeda-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="bdeda-116">Examples</span></span>

<span data-ttu-id="bdeda-117">Следующий пример представляет собой полный файл определения обложки, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="bdeda-117">The following sample is a complete skin definition file that illustrates how the attributes of the **TEXT** element are used.</span></span> <span data-ttu-id="bdeda-118">Его можно найти в каталоге Samples, который был установлен вместе с пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="bdeda-118">It can be found in the Samples directory that was installed with the SDK.</span></span>


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="bdeda-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bdeda-119">Requirements</span></span>



| <span data-ttu-id="bdeda-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bdeda-120">Requirement</span></span> | <span data-ttu-id="bdeda-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bdeda-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="bdeda-122">Версия</span><span class="sxs-lookup"><span data-stu-id="bdeda-122">Version</span></span><br/> | <span data-ttu-id="bdeda-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="bdeda-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bdeda-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bdeda-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdeda-125">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="bdeda-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="bdeda-126">**TEXT. toolTip**</span><span class="sxs-lookup"><span data-stu-id="bdeda-126">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="bdeda-127">**TEXT. wordWrap**</span><span class="sxs-lookup"><span data-stu-id="bdeda-127">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





