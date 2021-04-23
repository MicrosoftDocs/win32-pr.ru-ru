---
title: Элемент Color
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | Элемент Color
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Элемент Color проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c73aa9fe2c7f731e872c4a2e235bf9c0e29ce05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698994"
---
# <a name="color-element"></a><span data-ttu-id="082e9-105">Элемент Color</span><span class="sxs-lookup"><span data-stu-id="082e9-105">Color Element</span></span>

> [!Note]  
> <span data-ttu-id="082e9-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="082e9-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="082e9-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="082e9-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="082e9-108">Элемент Color указывает цвет фона для кнопок навигации в Интернет-магазине, текст кнопки и панель задач функции.</span><span class="sxs-lookup"><span data-stu-id="082e9-108">The Color element specifies the background color for online store navigation buttons, button text, and the Features taskbar.</span></span>

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a><span data-ttu-id="082e9-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="082e9-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="082e9-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="082e9-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (required)</span></span>
</dt> <dd>

<span data-ttu-id="082e9-111">Шестнадцатеричное значение цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="082e9-111">Hexadecimal RGB color value.</span></span> <span data-ttu-id="082e9-112">Задает цвет фона для кнопок и панели задач.</span><span class="sxs-lookup"><span data-stu-id="082e9-112">Specifies the background color for buttons and the taskbar.</span></span>

</dd> <dt>

<span data-ttu-id="082e9-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**Медиаплайертекст** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="082e9-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (required)</span></span>
</dt> <dd>

<span data-ttu-id="082e9-114">Шестнадцатеричное значение цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="082e9-114">Hexadecimal RGB color value.</span></span> <span data-ttu-id="082e9-115">Задает цвет для текста кнопки.</span><span class="sxs-lookup"><span data-stu-id="082e9-115">Specifies the color for the button text.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="082e9-116">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="082e9-116">Parent/Child Elements</span></span>



| <span data-ttu-id="082e9-117">Иерархия</span><span class="sxs-lookup"><span data-stu-id="082e9-117">Hierarchy</span></span>       | <span data-ttu-id="082e9-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="082e9-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="082e9-119">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="082e9-119">Parent elements</span></span> | <span data-ttu-id="082e9-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="082e9-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="082e9-121">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="082e9-121">Child elements</span></span>  | <span data-ttu-id="082e9-122">Нет</span><span class="sxs-lookup"><span data-stu-id="082e9-122">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="082e9-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="082e9-123">Remarks</span></span>

<span data-ttu-id="082e9-124">Значение по умолчанию для **MediaPlayer** — \# 7C9AD6.</span><span class="sxs-lookup"><span data-stu-id="082e9-124">The default value for **MediaPlayer** is \#7C9AD6.</span></span> <span data-ttu-id="082e9-125">Значение по умолчанию для **медиаплайертекст** — \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="082e9-125">The default value for **MediaPlayerText** is \#FFFFFF.</span></span>

<span data-ttu-id="082e9-126">Не забудьте использовать цвета, которые упрощают чтение текста кнопки пользователем.</span><span class="sxs-lookup"><span data-stu-id="082e9-126">Be sure to use colors that make it easy for the user to read the button text.</span></span> <span data-ttu-id="082e9-127">Например, следует избегать использования белого текста кнопки на светлых цветных кнопках.</span><span class="sxs-lookup"><span data-stu-id="082e9-127">For example, you should avoid using white button text on light colored buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="082e9-128">Требования</span><span class="sxs-lookup"><span data-stu-id="082e9-128">Requirements</span></span>



| <span data-ttu-id="082e9-129">Требование</span><span class="sxs-lookup"><span data-stu-id="082e9-129">Requirement</span></span> | <span data-ttu-id="082e9-130">Значение</span><span class="sxs-lookup"><span data-stu-id="082e9-130">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="082e9-131">Версия</span><span class="sxs-lookup"><span data-stu-id="082e9-131">Version</span></span><br/> | <span data-ttu-id="082e9-132">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="082e9-132">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="082e9-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="082e9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="082e9-134">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="082e9-134">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="082e9-135">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="082e9-135">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="082e9-136">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="082e9-136">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





