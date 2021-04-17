---
title: Клоседкаптион. Самистиле
description: Свойство Самистиле указывает или получает стиль закрытых субтитров.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- Проигрыватель Windows Media Клоседкаптион. Самистиле
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694871"
---
# <a name="closedcaptionsamistyle"></a><span data-ttu-id="d8e72-104">Клоседкаптион. Самистиле</span><span class="sxs-lookup"><span data-stu-id="d8e72-104">ClosedCaption.SAMIStyle</span></span>

<span data-ttu-id="d8e72-105">Свойство **самистиле** указывает или получает стиль закрытых субтитров.</span><span class="sxs-lookup"><span data-stu-id="d8e72-105">The **SAMIStyle** property specifies or retrieves the closed captioning style.</span></span>

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a><span data-ttu-id="d8e72-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d8e72-106">Possible Values</span></span>

<span data-ttu-id="d8e72-107">Это свойство является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d8e72-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e72-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8e72-108">Remarks</span></span>

<span data-ttu-id="d8e72-109">Файл SAMI может содержать несколько определений стиля формата.</span><span class="sxs-lookup"><span data-stu-id="d8e72-109">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="d8e72-110">Стили SAMI определены между тегами <STYLE> и </STYLE> в файле Sami.</span><span class="sxs-lookup"><span data-stu-id="d8e72-110">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="d8e72-111">Стиль определяется с помощью текстовой строки, предшествующей \# символу.</span><span class="sxs-lookup"><span data-stu-id="d8e72-111">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="d8e72-112">Пример:</span><span class="sxs-lookup"><span data-stu-id="d8e72-112">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



<span data-ttu-id="d8e72-113">Указывает стиль, создающий определенный шрифт.</span><span class="sxs-lookup"><span data-stu-id="d8e72-113">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="d8e72-114">Если параметр SAMI не указан, по умолчанию используется первый стиль, определенный в файле SAMI.</span><span class="sxs-lookup"><span data-stu-id="d8e72-114">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="d8e72-115">**Проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="d8e72-115">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="d8e72-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="d8e72-116">Examples</span></span>

<span data-ttu-id="d8e72-117">В следующем примере JScript создается HTML-элемент SELECT, использующий *клоседкаптион*. **Самистиле** для изменения внешнего вида текста закрытого заголовка.</span><span class="sxs-lookup"><span data-stu-id="d8e72-117">The following JScript example creates an HTML SELECT element that uses *closedCaption*.**SAMIStyle** to change the appearance of the closed caption text.</span></span> <span data-ttu-id="d8e72-118">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="d8e72-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="d8e72-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d8e72-119">Requirements</span></span>



| <span data-ttu-id="d8e72-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d8e72-120">Requirement</span></span> | <span data-ttu-id="d8e72-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d8e72-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e72-122">Версия</span><span class="sxs-lookup"><span data-stu-id="d8e72-122">Version</span></span><br/> | <span data-ttu-id="d8e72-123">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="d8e72-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d8e72-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d8e72-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="d8e72-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8e72-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8e72-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d8e72-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e72-127">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="d8e72-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="d8e72-128">**Объект Клоседкаптион**</span><span class="sxs-lookup"><span data-stu-id="d8e72-128">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





