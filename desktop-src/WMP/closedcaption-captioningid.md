---
title: Клоседкаптион. Каптионингид
description: Свойство Каптионингид указывает или получает имя элемента, отображающего субтитры.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- Проигрыватель Windows Media Клоседкаптион. Каптионингид
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694377"
---
# <a name="closedcaptioncaptioningid"></a><span data-ttu-id="6bf9f-104">Клоседкаптион. Каптионингид</span><span class="sxs-lookup"><span data-stu-id="6bf9f-104">ClosedCaption.captioningID</span></span>

<span data-ttu-id="6bf9f-105">Свойство **каптионингид** указывает или получает имя элемента, отображающего субтитры.</span><span class="sxs-lookup"><span data-stu-id="6bf9f-105">The **captioningID** property specifies or retrieves the name of the element displaying the captioning.</span></span>

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a><span data-ttu-id="6bf9f-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="6bf9f-106">Possible Values</span></span>

<span data-ttu-id="6bf9f-107">Это свойство является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6bf9f-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bf9f-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bf9f-108">Remarks</span></span>

<span data-ttu-id="6bf9f-109">Указанное имя элемента может быть любым HTML-элементом на веб-странице, если он поддерживает атрибут innerHTML.</span><span class="sxs-lookup"><span data-stu-id="6bf9f-109">The element name specified can be any HTML element in the webpage as long as it supports the innerHTML attribute.</span></span> <span data-ttu-id="6bf9f-110">Если веб-страница содержит несколько кадров, имя элемента может ссылаться только на элемент в том же кадре, что и элемент управления проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="6bf9f-110">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Player control.</span></span>

<span data-ttu-id="6bf9f-111">**Проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.</span><span class="sxs-lookup"><span data-stu-id="6bf9f-111">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="6bf9f-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="6bf9f-112">Examples</span></span>

<span data-ttu-id="6bf9f-113">В следующем примере Microsoft JScript используется *клоседкаптион*. **каптионингид** , чтобы выбрать область веб-страницы, используемую для вывода субтитров.</span><span class="sxs-lookup"><span data-stu-id="6bf9f-113">The following Microsoft JScript example uses *ClosedCaption*.**captioningID** to choose the area of a webpage used to display captions.</span></span> <span data-ttu-id="6bf9f-114">Были созданы два элемента HTML DIV с ИДЕНТИФИКАТОРом = CC1 и ID = CC2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="6bf9f-114">Two HTML DIV elements were created, with ID = CC1 and ID = CC2, respectively.</span></span> <span data-ttu-id="6bf9f-115">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="6bf9f-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a><span data-ttu-id="6bf9f-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6bf9f-116">Requirements</span></span>



| <span data-ttu-id="6bf9f-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6bf9f-117">Requirement</span></span> | <span data-ttu-id="6bf9f-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6bf9f-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6bf9f-119">Версия</span><span class="sxs-lookup"><span data-stu-id="6bf9f-119">Version</span></span><br/> | <span data-ttu-id="6bf9f-120">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="6bf9f-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6bf9f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6bf9f-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="6bf9f-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bf9f-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bf9f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bf9f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bf9f-124">**Добавление субтитров к цифровым носителям**</span><span class="sxs-lookup"><span data-stu-id="6bf9f-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="6bf9f-125">**Объект Клоседкаптион**</span><span class="sxs-lookup"><span data-stu-id="6bf9f-125">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





