---
title: Файл определения обложки
description: Файл определения обложки
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Обложки проигрывателя Windows Media, файлы определения обложки
- обложки, файлы определения обложки
- файлы для обложек, определение обложки
- файлы определения обложки, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700631"
---
# <a name="skin-definition-file"></a><span data-ttu-id="ba5c0-107">Файл определения обложки</span><span class="sxs-lookup"><span data-stu-id="ba5c0-107">Skin Definition File</span></span>

<span data-ttu-id="ba5c0-108">Файлы определения обложки содержат основные инструкции для того, что делает Обложка и где можно найти другие файлы, используемые обложкой.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-108">Skin definition files contain the basic instructions for what the skin does and where other files used by the skin can be found.</span></span> <span data-ttu-id="ba5c0-109">Для обложки может существовать только один файл определения обложки с расширением WMS.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-109">There can only be one skin definition file for a skin, and it has a .wms file name extension.</span></span>

<span data-ttu-id="ba5c0-110">Инструкции в файле определения обложки записываются в язык XML (XML), что аналогично HTML.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-110">The instructions in the skin definition file are written in Extensible Markup Language (XML), which is similar to HTML.</span></span> <span data-ttu-id="ba5c0-111">Если вы использовали HTML для создания веб-страниц, вы обнаружите, что XML знаком.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-111">If you have used HTML to create webpages, you will find that XML looks familiar.</span></span>

<span data-ttu-id="ba5c0-112">XML-код в файле определения обложки использует набор специальных тегов элементов для определения частей пользовательского интерфейса обложки.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-112">The XML in the skin definition file uses a set of special element tags to define parts of the skin user interface.</span></span> <span data-ttu-id="ba5c0-113">Например, элемент [Button](button-element.md) определяет, как будет вести себя кнопка, где она будет и как она будет выглядеть.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-113">For example, the [BUTTON](button-element.md) element defines how a button will behave, where it will go, and what it will look like.</span></span>

<span data-ttu-id="ba5c0-114">Каждый тег элемента имеет определенные атрибуты.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-114">Each element tag has specific attributes.</span></span> <span data-ttu-id="ba5c0-115">Например, элемент [Button](button-element.md) имеет атрибут **Image** , который определяет, где можно найти изображение для кнопки.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-115">For example, the [BUTTON](button-element.md) element has an **image** attribute that defines where the picture for the button can be found.</span></span> <span data-ttu-id="ba5c0-116">Это похоже на HTML, где у элемента BODY будет атрибут **bgcolor** , определяющий цвет фона HTML-страницы.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-116">This is similar to HTML, where the BODY element will have a **bgcolor** attribute that defines the background color of the HTML page.</span></span> <span data-ttu-id="ba5c0-117">Подробные сведения обо всех элементах обложки и их атрибутах см. в разделе [Справочник по программированию обложки](skin-programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ba5c0-117">Detailed information about all skin elements and their attributes is included in the [Skin Programming Reference](skin-programming-reference.md) section.</span></span>

<span data-ttu-id="ba5c0-118">В XML есть несколько простых правил, которые необходимо знать для создания обложек.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-118">XML has a few simple rules that you need to know to create skins.</span></span> <span data-ttu-id="ba5c0-119">В отличие от HTML, XML требует точного соблюдения правил.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-119">Unlike HTML, XML requires you to follow the rules exactly.</span></span>

## <a name="enclose-elements-with-angle-brackets"></a><span data-ttu-id="ba5c0-120">Заключите элементы в угловые скобки</span><span class="sxs-lookup"><span data-stu-id="ba5c0-120">Enclose Elements with Angle Brackets</span></span>

<span data-ttu-id="ba5c0-121">Все элементы заключены в угловые скобки; Например, элемент **Button** имеет следующий тип:</span><span class="sxs-lookup"><span data-stu-id="ba5c0-121">All elements are enclosed by angle brackets; for example, the **BUTTON** element is typed like this:</span></span>


```C++
<BUTTON>

```



<span data-ttu-id="ba5c0-122">Не нужно вводить слово "BUTTON" во всех прописных буквах, но соглашение о вводе имен элементов в верхнем регистре используется в коде примера этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-122">You do not need to type the word "BUTTON" in all uppercase letters, but the convention of typing element names in all uppercase is used in the example code of this SDK.</span></span>

## <a name="put-attributes-before-the-closing-bracket"></a><span data-ttu-id="ba5c0-123">Размещение атрибутов перед закрывающей скобкой</span><span class="sxs-lookup"><span data-stu-id="ba5c0-123">Put Attributes Before the Closing Bracket</span></span>

<span data-ttu-id="ba5c0-124">Все атрибуты для определенного элемента должны быть добавлены перед закрывающей угловой скобкой.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-124">All attributes for a particular element must be included before the closing angle bracket.</span></span> <span data-ttu-id="ba5c0-125">Атрибут состоит из имени атрибута, за которым следует знак равенства (=) и значение атрибута в кавычках.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-125">An attribute consists of the attribute name followed by an equal sign (=) and the value of the attribute in quotes.</span></span>


```C++
<BUTTON image="mypic.jpg">

```



<span data-ttu-id="ba5c0-126">Не нужно вводить слово «Image» в нижнем регистре, но в примере кода этого пакета SDK используется соглашение о вводе имен атрибутов в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-126">You do not need to type the word "image" in lowercase, but the convention of typing attribute names in lowercase is used in the example code of this SDK.</span></span> <span data-ttu-id="ba5c0-127">Также обратите внимание, что значение атрибута заключается в кавычки.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-127">Also note that the value of the attribute is enclosed in quotation marks.</span></span>

## <a name="opening-and-closing-elements"></a><span data-ttu-id="ba5c0-128">Открытие и закрытие элементов</span><span class="sxs-lookup"><span data-stu-id="ba5c0-128">Opening and Closing Elements</span></span>

<span data-ttu-id="ba5c0-129">Некоторые элементы группируются внутри другого элемента.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-129">Some elements are grouped together inside another element.</span></span> <span data-ttu-id="ba5c0-130">Например, элемент **BUTTONGROUP** не имеет смысла, если только вы не используете один или несколько элементов **буттонелемент** .</span><span class="sxs-lookup"><span data-stu-id="ba5c0-130">For example, the **BUTTONGROUP** element does not make a lot of sense unless you use one or more **BUTTONELEMENT** elements with it.</span></span> <span data-ttu-id="ba5c0-131">Чтобы сделать группирование понятным, необходимо иметь открывающий и закрывающий тег для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-131">To make the grouping clear, you need to have an opening and closing tag for each element.</span></span> <span data-ttu-id="ba5c0-132">Открывающий тег — это просто имя элемента и все связанные с ним атрибуты, заключенные в угловые скобки.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-132">The opening tag is just the element name and any related attributes, surrounded by angle brackets.</span></span> <span data-ttu-id="ba5c0-133">Закрывающий тег — это имя элемента, перед которым ставится косая черта (/), а затем заключено угловые скобки.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-133">The closing tag is the element name, preceded by a forward slash (/), and then enclosed by angle brackets.</span></span> <span data-ttu-id="ba5c0-134">Например, открывающий тег элемента **BUTTONGROUP** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ba5c0-134">For example, the **BUTTONGROUP** element opening tag looks like this:</span></span>


```C++
<BUTTONGROUP>

```



<span data-ttu-id="ba5c0-135">Закрывающий тег **BUTTONGROUP** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ba5c0-135">The closing **BUTTONGROUP** tag looks like this:</span></span>


```C++
</BUTTONGROUP>

```



<span data-ttu-id="ba5c0-136">Теги **буттонелемент** можно поместить между открывающим и закрывающим тегами элемента **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="ba5c0-136">You would put the **BUTTONELEMENT** tags between the opening and closing **BUTTONGROUP** element tags.</span></span> <span data-ttu-id="ba5c0-137">Пример:</span><span class="sxs-lookup"><span data-stu-id="ba5c0-137">For example:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a><span data-ttu-id="ba5c0-138">Закрытие элементов</span><span class="sxs-lookup"><span data-stu-id="ba5c0-138">Closing Off Elements</span></span>

<span data-ttu-id="ba5c0-139">Если в элементе нет других элементов, необходимо поставить косую черту в конце имени элемента непосредственно перед закрывающей угловой скобкой.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-139">If an element has no other elements inside it, you must put a forward slash at the end of the element name just before the closing angle bracket.</span></span> <span data-ttu-id="ba5c0-140">Например, в приведенном выше коде каждый элемент **буттонелемент** имеет косую черту, указывающую, что в нем нет других вложенных элементов.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-140">For example, in the code above, each **BUTTONELEMENT** element has a forward slash to indicate that there are no other elements nested within it.</span></span>

<span data-ttu-id="ba5c0-141">Иными словами, необходимо либо иметь закрывающий тег элемента, либо закрыть элемент с косой чертой.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-141">In other words, you must either have a closing element tag or close off your element with a forward slash.</span></span>

<span data-ttu-id="ba5c0-142">Это верно:</span><span class="sxs-lookup"><span data-stu-id="ba5c0-142">This is correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="ba5c0-143">Это неверно:</span><span class="sxs-lookup"><span data-stu-id="ba5c0-143">This is not correct:</span></span>


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="ba5c0-144">Это также неверно:</span><span class="sxs-lookup"><span data-stu-id="ba5c0-144">This is also not correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



<span data-ttu-id="ba5c0-145">В следующем разделе приведены дополнительные сведения о файлах определения обложки.</span><span class="sxs-lookup"><span data-stu-id="ba5c0-145">The following section provides more information about skin definition files:</span></span>

-   [<span data-ttu-id="ba5c0-146">Структура файла определения обложки</span><span class="sxs-lookup"><span data-stu-id="ba5c0-146">Skin Definition File Structure</span></span>](skin-definition-file-structure.md)

## <a name="related-topics"></a><span data-ttu-id="ba5c0-147">См. также</span><span class="sxs-lookup"><span data-stu-id="ba5c0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba5c0-148">**Файлы обложки**</span><span class="sxs-lookup"><span data-stu-id="ba5c0-148">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




