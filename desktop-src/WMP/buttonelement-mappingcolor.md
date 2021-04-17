---
title: БУТТОНЕЛЕМЕНТ. Маппингколор
description: Атрибут Маппингколор указывает или получает ключ цвета, определяющий этот БУТТОНЕЛЕМЕНТ в BUTTONGROUP.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- Проигрыватель Windows Media БУТТОНЕЛЕМЕНТ. Маппингколор
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694593"
---
# <a name="buttonelementmappingcolor"></a><span data-ttu-id="9de5b-104">БУТТОНЕЛЕМЕНТ. Маппингколор</span><span class="sxs-lookup"><span data-stu-id="9de5b-104">BUTTONELEMENT.mappingColor</span></span>

<span data-ttu-id="9de5b-105">Атрибут **маппингколор** указывает или получает ключ цвета, определяющий этот **буттонелемент** в **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="9de5b-105">The **mappingColor** attribute specifies or retrieves the color key that identifies this **BUTTONELEMENT** in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a><span data-ttu-id="9de5b-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="9de5b-106">Possible Values</span></span>

<span data-ttu-id="9de5b-107">Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9de5b-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="9de5b-108">У него нет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9de5b-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9de5b-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9de5b-109">Remarks</span></span>

<span data-ttu-id="9de5b-110">Этот атрибут определяет цвет области в группе кнопок **маппингимаже** , которая соответствует этому элементу Button.</span><span class="sxs-lookup"><span data-stu-id="9de5b-110">This attribute specifies the color of the region in the button group **mappingImage** that corresponds to this button element.</span></span> <span data-ttu-id="9de5b-111">Все щелчки в этом регионе обрабатываются этим элементом кнопки.</span><span class="sxs-lookup"><span data-stu-id="9de5b-111">All clicks on this region are handled by this button element.</span></span>

<span data-ttu-id="9de5b-112">Если указан недопустимый цвет, **буттонелемент** не активируется.</span><span class="sxs-lookup"><span data-stu-id="9de5b-112">If an invalid color is specified, the **BUTTONELEMENT** is not activated.</span></span>

## <a name="examples"></a><span data-ttu-id="9de5b-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="9de5b-113">Examples</span></span>

<span data-ttu-id="9de5b-114">Следующий пример представляет собой полный файл определения обложки, иллюстрирующий использование некоторых атрибутов **буттонелемент** .</span><span class="sxs-lookup"><span data-stu-id="9de5b-114">The following sample is a complete skin definition file that illustrates how some of the **BUTTONELEMENT** attributes are used.</span></span> <span data-ttu-id="9de5b-115">Его можно найти в каталоге Samples, который был установлен вместе с пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="9de5b-115">It can be found in the Samples directory that was installed with the SDK.</span></span>


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="9de5b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9de5b-116">Requirements</span></span>



| <span data-ttu-id="9de5b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9de5b-117">Requirement</span></span> | <span data-ttu-id="9de5b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9de5b-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9de5b-119">Версия</span><span class="sxs-lookup"><span data-stu-id="9de5b-119">Version</span></span><br/> | <span data-ttu-id="9de5b-120">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="9de5b-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9de5b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9de5b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9de5b-122">**Ссылка на цвет**</span><span class="sxs-lookup"><span data-stu-id="9de5b-122">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="9de5b-123">**БУТТОНЕЛЕМЕНТ, элемент**</span><span class="sxs-lookup"><span data-stu-id="9de5b-123">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="9de5b-124">**BUTTONGROUP. Маппингимаже**</span><span class="sxs-lookup"><span data-stu-id="9de5b-124">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





