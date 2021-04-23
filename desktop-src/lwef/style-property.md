---
title: Свойство Style
description: Свойство Style
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330072"
---
# <a name="style-property"></a><span data-ttu-id="c896d-103">Свойство Style</span><span class="sxs-lookup"><span data-stu-id="c896d-103">Style Property</span></span>

<span data-ttu-id="c896d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c896d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c896d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Nописание**</span><span class="sxs-lookup"><span data-stu-id="c896d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c896d-106">Возвращает или задает стиль вывода слова для символа.</span><span class="sxs-lookup"><span data-stu-id="c896d-106">Returns or sets the character's word balloon output style.</span></span>

</dd> <dt>

<span data-ttu-id="c896d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="c896d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c896d-108">\*агент. ***Символы ("*** чарактерид \* \* *"). Стиль всплывающего* \*  \[  =   окна\]</span><span class="sxs-lookup"><span data-stu-id="c896d-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Balloon.Style** \[ = *Style*\]</span></span>



| <span data-ttu-id="c896d-109">Отделение</span><span class="sxs-lookup"><span data-stu-id="c896d-109">Part</span></span>    | <span data-ttu-id="c896d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c896d-110">Description</span></span>                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c896d-111">*Style*</span><span class="sxs-lookup"><span data-stu-id="c896d-111">*Style*</span></span> | <span data-ttu-id="c896d-112">Целое число, представляющее стиль вывода всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="c896d-112">An integer that represents the balloon's output style.</span></span> <span data-ttu-id="c896d-113">Параметр стиля — это битовое значение битов, соответствующих: всплывающее сообщение (бит 0), размер к тексту (бит 1), автоматическое скрытие (бит 2), автоматическая скорость (бит 3), число символов в строках (бит 16-23) и число строк (бит 24-31).</span><span class="sxs-lookup"><span data-stu-id="c896d-113">The style setting is a bitfield with bits corresponding to: balloon-on (bit 0), size-to-text (bit 1), auto-hide (bit 2), auto-pace (bit 3), number of characters per lines (bits 16-23), and number of lines (bits 24-31).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c896d-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c896d-114">Remarks</span></span>

<span data-ttu-id="c896d-115">Если в качестве всплывающего элемента стиля задано значение 1, то при использовании метода [**говорите**](https://www.bing.com/search?q=**Speak**) или [**мышления**](think-method.md) отображается всплывающая подсказка, если пользователь не переопределит этот параметр на странице свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c896d-115">When the balloon-on style bit is set to 1, the word balloon appears when a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) method is used, unless the user overrides this setting in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="c896d-116">Если задано значение 0, всплывающее сообщение не отображается.</span><span class="sxs-lookup"><span data-stu-id="c896d-116">When set to 0, a balloon does not appear.</span></span>

<span data-ttu-id="c896d-117">Если для бита стиля размера в тексте задано значение 1, то всплывающая подсказка автоматически изменяет высоту всплывающего окна на текущий размер текста для оператора [**говорите**](https://www.bing.com/search?q=**Speak**) или « [**подумать**](think-method.md) ».</span><span class="sxs-lookup"><span data-stu-id="c896d-117">When the size-to-text style bit is set to 1, the word balloon automatically sizes the height of the balloon to the current size of the text for the [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement.</span></span> <span data-ttu-id="c896d-118">Если задано значение 0, Высота всплывающего окна зависит от значения свойства [**нумберофлинес**](numberoflines-property.md) .</span><span class="sxs-lookup"><span data-stu-id="c896d-118">When set to 0, the balloon's height is based on the [**NumberOfLines**](numberoflines-property.md) property setting.</span></span> <span data-ttu-id="c896d-119">Если этот бит стиля имеет значение 1 и вы пытаетесь задать свойство **нумберофлинес** , агент выдает ошибку.</span><span class="sxs-lookup"><span data-stu-id="c896d-119">If this style bit is set to 1 and you attempt to set the **NumberOfLines** property, Agent raises an error.</span></span>

<span data-ttu-id="c896d-120">Если бит стиля автоматического скрытия имеет значение 1, то при завершении речевого вывода текст всплывающего окна автоматически скрывается.</span><span class="sxs-lookup"><span data-stu-id="c896d-120">When the auto-hide style bit is set to 1, the word balloon automatically hides when spoken output completes.</span></span> <span data-ttu-id="c896d-121">Если задано значение 0, всплывающее сообщение остается видимым до следующего [**произношения**](https://www.bing.com/search?q=**Speak**) [**или вызова**](think-method.md) , если символ скрыт, либо пользователь щелкает или перетаскивает этот символ.</span><span class="sxs-lookup"><span data-stu-id="c896d-121">When set to 0, the balloon remains displayed until the next [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="c896d-122">Если для бита автоматической установки задано значение 1, то всплывающая подсказка выводится на основе текущей скорости вывода, например по одному слову за раз.</span><span class="sxs-lookup"><span data-stu-id="c896d-122">When the auto-pace style bit is set to 1, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="c896d-123">Когда вывод превышает размер всплывающего окна, первый текст автоматически прокручивается.</span><span class="sxs-lookup"><span data-stu-id="c896d-123">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="c896d-124">Если задано значение 0, весь текст, включенный в оператор « [**говорите**](https://www.bing.com/search?q=**Speak**) » или « [**подумать**](think-method.md) », отображается одновременно.</span><span class="sxs-lookup"><span data-stu-id="c896d-124">When set to 0, all text included in a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement is displayed at once.</span></span>

<span data-ttu-id="c896d-125">Значение, чтобы извлечь только четыре младших бита **и** значение, возвращаемое **Style** с 255.</span><span class="sxs-lookup"><span data-stu-id="c896d-125">To retrieve just the value of the bottom four bits, **And** the value returned by **Style** with 255.</span></span> <span data-ttu-id="c896d-126">Для задания битового значения **или** значения, возвращаемого со значением битов, которые вы хотите задать.</span><span class="sxs-lookup"><span data-stu-id="c896d-126">To set a bit value, **Or** the value returned with the value of the bits you want set.</span></span> <span data-ttu-id="c896d-127">Чтобы отключить бит **и** значение, возвращаемое с дополнением к биту, выполните одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="c896d-127">To turn a bit off, **And** the value returned with one's complement of the bit:</span></span>


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



<span data-ttu-id="c896d-128">Свойство **Style** также возвращает количество символов в строке нижнего байта верхнего слова и число строк в верхнем байте верхнего слова.</span><span class="sxs-lookup"><span data-stu-id="c896d-128">The **Style** property also returns the number of characters per line in the lower byte of the upper word and the number of lines in the high byte of the upper word.</span></span> <span data-ttu-id="c896d-129">Хотя это может быть проще в чтении с помощью свойств [**чарсперлине**](charsperline-property.md) и [**Нумберофлинес**](numberoflines-property.md), свойство **Style** также позволяет задавать эти значения.</span><span class="sxs-lookup"><span data-stu-id="c896d-129">While this can be more easily read using the [**CharsPerLine**](charsperline-property.md) and [**NumberOfLines**](numberoflines-property.md)properties, the **Style** property also enables you to set those values.</span></span>

<span data-ttu-id="c896d-130">Например, чтобы изменить число строк, очистите биты 24 – 31 с логической операцией **и** , прежде чем устанавливать новое значение в качестве произведения нового значения, равного 2 ^ 24, добавленному к существующему значению свойства **Style** .</span><span class="sxs-lookup"><span data-stu-id="c896d-130">For example, to change the number of lines, clear bits 24 to 31 with a logical **AND** operation before setting the new value as the product of the new value times 2^24, added to the existing value of the **Style** property.</span></span>


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



<span data-ttu-id="c896d-131">Чтобы задать число символов в строке, очистите биты 16 – 23 с логической операцией **и** , прежде чем устанавливать новое значение в качестве произведения нового значения со значением 2 ^ 16, добавленного к существующему значению свойства Style.</span><span class="sxs-lookup"><span data-stu-id="c896d-131">To set the number of characters per line, clear bits 16 to 23 with a logical **AND** operation before setting the new value as the product of the new value times 2^16, added to the existing value of the Style property.</span></span>


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



<span data-ttu-id="c896d-132">Свойство **Style** можно задать, даже если пользователь отключил отображение всплывающих окон с помощью вкладки свойств Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c896d-132">The **Style** property can be set even if the user has disabled balloon display using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="c896d-133">Однако значения для числа строк должны быть в диапазоне от 1 до 128, а число символов в строке должно находиться в диапазоне от 8 до 255.</span><span class="sxs-lookup"><span data-stu-id="c896d-133">However, the values for the number of lines must be between 1 and 128 and the number characters per line must be between 8 and 255.</span></span> <span data-ttu-id="c896d-134">Если указать недопустимое значение для свойства **Style** , то агент выдаст ошибку.</span><span class="sxs-lookup"><span data-stu-id="c896d-134">If you provide an invalid value for the **Style** property, Agent will raise an error.</span></span>

<span data-ttu-id="c896d-135">Это свойство применяется только к символу, используемому вашим клиентским приложением. Этот параметр не влияет на другие клиенты символов или других символов клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="c896d-135">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="c896d-136">Значения по умолчанию для этих битов стиля основываются на параметрах, когда символ компилируется с помощью редактора символов Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c896d-136">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

 

 




