---
title: TEXT. wordWrap
description: Атрибут wordWrap указывает или получает значение, обозначающее включение или отключение переноса по словам.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- Проигрыватель Windows Media TEXT. wordWrap
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649002"
---
# <a name="textwordwrap"></a><span data-ttu-id="483e3-104">TEXT. wordWrap</span><span class="sxs-lookup"><span data-stu-id="483e3-104">TEXT.wordWrap</span></span>

<span data-ttu-id="483e3-105">Атрибут **WordWrap** указывает или получает значение, обозначающее включение или отключение переноса по словам.</span><span class="sxs-lookup"><span data-stu-id="483e3-105">The **wordWrap** attribute specifies or retrieves a value indicating whether word wrap is enabled or disabled.</span></span>

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a><span data-ttu-id="483e3-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="483e3-106">Possible Values</span></span>

<span data-ttu-id="483e3-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="483e3-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="483e3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="483e3-108">Value</span></span> | <span data-ttu-id="483e3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="483e3-109">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="483e3-110">true</span><span class="sxs-lookup"><span data-stu-id="483e3-110">true</span></span>  | <span data-ttu-id="483e3-111">Перенос по словам включен.</span><span class="sxs-lookup"><span data-stu-id="483e3-111">Word wrap is enabled.</span></span>                                                                             |
| <span data-ttu-id="483e3-112">false</span><span class="sxs-lookup"><span data-stu-id="483e3-112">false</span></span> | <span data-ttu-id="483e3-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="483e3-113">Default.</span></span> <span data-ttu-id="483e3-114">Перенос по словам отключен.</span><span class="sxs-lookup"><span data-stu-id="483e3-114">Word wrap is disabled.</span></span> <span data-ttu-id="483e3-115">Если текст не умещается в элементе управления, текст обрезается.</span><span class="sxs-lookup"><span data-stu-id="483e3-115">If the text does not fit within the control, the text is cropped.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="483e3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="483e3-116">Remarks</span></span>

<span data-ttu-id="483e3-117">Элемент управления "текст" не разделяет слова друг от друга.</span><span class="sxs-lookup"><span data-stu-id="483e3-117">The Text control does not split words apart.</span></span> <span data-ttu-id="483e3-118">Если слово выходит за пределы ширины элемента управления, для перемещения слова на следующую строку применяется перенос по словам.</span><span class="sxs-lookup"><span data-stu-id="483e3-118">If a word extends beyond the width of the control, word wrap is employed to move the word to the next line.</span></span> <span data-ttu-id="483e3-119">Если одно слово длиннее, чем ширина элемента управления, это слово обрезается и занимает одну строку.</span><span class="sxs-lookup"><span data-stu-id="483e3-119">If a single word is longer than the control width, that word is clipped and occupies a single line.</span></span>

<span data-ttu-id="483e3-120">Если атрибут **Width** не указан, то параметр **WordWrap** игнорируется, а размер текстового элемента управления изменяется, а не обтекает текст.</span><span class="sxs-lookup"><span data-stu-id="483e3-120">If the **width** attribute is not specified, **wordWrap** is ignored and the Text control will resize rather than wrapping the text.</span></span>

<span data-ttu-id="483e3-121">Если в определенных местах требуются разрывы строк, их необходимо явно указать в **значении** , используя "&\# 13;" или " \\ r".</span><span class="sxs-lookup"><span data-stu-id="483e3-121">If line breaks are desired in particular locations, they must be explicitly specified in **value** using "&\#13;" or "\\r".</span></span> <span data-ttu-id="483e3-122">Если последняя форма используется при непосредственном указании значения, строка должна иметь префикс "JScript:", а фактическое значение должно быть заключено в одинарные кавычки, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="483e3-122">If the latter form is used when specifying the value directly, the string must be prefixed with "JScript:" and the actual value must be surrounded by single quotes, as shown below.</span></span> <span data-ttu-id="483e3-123">Это необязательно, если значение задается динамически в обработчике событий.</span><span class="sxs-lookup"><span data-stu-id="483e3-123">This is not necessary if the value is set dynamically from within an event handler.</span></span>

<span data-ttu-id="483e3-124">Если для свойства **WordWrap** задано значение true, а **Подсказка** не указана, подсказка отобразит полный текст атрибута **value** .</span><span class="sxs-lookup"><span data-stu-id="483e3-124">If **wordWrap** is set to true and **toolTip** is not specified, the ToolTip will display the full text of the **value** attribute.</span></span> <span data-ttu-id="483e3-125">Если подсказка не нужна, установите для **подсказки** значение "" (пустая строка).</span><span class="sxs-lookup"><span data-stu-id="483e3-125">If no ToolTip is desired, set **toolTip** to "" (empty string).</span></span>

## <a name="examples"></a><span data-ttu-id="483e3-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="483e3-126">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="483e3-127">Требования</span><span class="sxs-lookup"><span data-stu-id="483e3-127">Requirements</span></span>



| <span data-ttu-id="483e3-128">Требование</span><span class="sxs-lookup"><span data-stu-id="483e3-128">Requirement</span></span> | <span data-ttu-id="483e3-129">Значение</span><span class="sxs-lookup"><span data-stu-id="483e3-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="483e3-130">Версия</span><span class="sxs-lookup"><span data-stu-id="483e3-130">Version</span></span><br/> | <span data-ttu-id="483e3-131">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="483e3-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="483e3-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="483e3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="483e3-133">**Амбиентаттрибутес. Width**</span><span class="sxs-lookup"><span data-stu-id="483e3-133">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> <dt>

[<span data-ttu-id="483e3-134">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="483e3-134">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="483e3-135">**TEXT. toolTip**</span><span class="sxs-lookup"><span data-stu-id="483e3-135">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="483e3-136">**TEXT. Value**</span><span class="sxs-lookup"><span data-stu-id="483e3-136">**TEXT.value**</span></span>](text-value.md)
</dt> </dl>

 

 





