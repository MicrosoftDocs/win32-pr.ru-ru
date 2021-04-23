---
title: Элемент ButtonText
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | ButtonText, элемент
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Проигрыватель Windows Media, элемент ButtonText
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699276"
---
# <a name="buttontext-element"></a><span data-ttu-id="5f6b7-105">Элемент ButtonText</span><span class="sxs-lookup"><span data-stu-id="5f6b7-105">ButtonText Element</span></span>

> [!Note]  
> <span data-ttu-id="5f6b7-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5f6b7-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5f6b7-108">Элемент **ButtonText** указывает текстовую строку, отображаемую проигрывателем Windows Media для кнопки области задач.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-108">The **ButtonText** element specifies the text string that Windows Media Player displays for a task pane button.</span></span>

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a><span data-ttu-id="5f6b7-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5f6b7-109">Attributes</span></span>

<span data-ttu-id="5f6b7-110">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="5f6b7-111">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5f6b7-111">Parent/Child Elements</span></span>



| <span data-ttu-id="5f6b7-112">Иерархия</span><span class="sxs-lookup"><span data-stu-id="5f6b7-112">Hierarchy</span></span>       | <span data-ttu-id="5f6b7-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="5f6b7-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="5f6b7-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5f6b7-114">Parent elements</span></span> | <span data-ttu-id="5f6b7-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="5f6b7-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="5f6b7-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5f6b7-116">Child elements</span></span>  | <span data-ttu-id="5f6b7-117">Нет</span><span class="sxs-lookup"><span data-stu-id="5f6b7-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="5f6b7-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="5f6b7-118">Remarks</span></span>

<span data-ttu-id="5f6b7-119">Этот элемент является обязательным для каждого экземпляра **ServiceTask1**, **ServiceTask2** или **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-119">This element is required for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span>

> [!Note]  
> <span data-ttu-id="5f6b7-120">Проигрыватель Windows Media 10 содержит три области задач, в которых Интернет-магазин может отображать свои веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-120">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="5f6b7-121">Интернет-магазин может использовать одну, две или все три области задач.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-121">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="5f6b7-122">Проигрыватель Windows Media 11 имеет только одну область задач, которую пользователь может просматривать, щелкнув вкладку **Интернет-магазины** . проигрыватель Windows Media 11 игнорирует элементы **ServiceTask2** и **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="5f6b7-122">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

<span data-ttu-id="5f6b7-123">Проигрыватель Windows Media может обрезать текст кнопки в соответствии с доступным пространством.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-123">Windows Media Player may crop button text to fit the available space.</span></span> <span data-ttu-id="5f6b7-124">Проигрыватель всегда использует полужирный шрифт Tahoma размером 8 пт для этого текста.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-124">The Player always uses the Tahoma bold 8-point font for this text.</span></span> <span data-ttu-id="5f6b7-125">Есть две строки, доступные для показа текста кнопки, но проигрыватель не переносит текст из первой строки во вторую.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-125">There are two lines available to display button text, but the Player does not automatically wrap text from the first line to the second.</span></span> <span data-ttu-id="5f6b7-126">Чтобы указать разрыв строки в тексте кнопки, вставьте в текстовую строку новую строку escape-последовательности " \\ n".</span><span class="sxs-lookup"><span data-stu-id="5f6b7-126">To specify a line break in the button text, insert the new line escape sequence "\\n" in your text string.</span></span>

<span data-ttu-id="5f6b7-127">Текстовая строка также отображается в меню **goto** пользовательского интерфейса проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-127">The text string is also displayed in the **GoTo** menu in the Windows Media Player user interface.</span></span>

<span data-ttu-id="5f6b7-128">Необходимо протестировать Интернет-магазин с помощью различных параметров отображения, чтобы текст отображался правильно.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-128">You should test your online store using a variety of display settings to ensure that text displays as you expect.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f6b7-129">Требования</span><span class="sxs-lookup"><span data-stu-id="5f6b7-129">Requirements</span></span>



| <span data-ttu-id="5f6b7-130">Требование</span><span class="sxs-lookup"><span data-stu-id="5f6b7-130">Requirement</span></span> | <span data-ttu-id="5f6b7-131">Значение</span><span class="sxs-lookup"><span data-stu-id="5f6b7-131">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="5f6b7-132">Версия</span><span class="sxs-lookup"><span data-stu-id="5f6b7-132">Version</span></span><br/> | <span data-ttu-id="5f6b7-133">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5f6b7-133">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5f6b7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5f6b7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f6b7-135">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="5f6b7-135">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="5f6b7-136">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="5f6b7-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="5f6b7-137">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="5f6b7-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





