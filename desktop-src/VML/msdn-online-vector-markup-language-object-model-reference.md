---
title: Справочник по объектной модели VML
description: В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070527"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="48d83-104">Справочник по объектной модели VML</span><span class="sxs-lookup"><span data-stu-id="48d83-104">VML Object Model Reference</span></span>

<span data-ttu-id="48d83-105">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="48d83-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="48d83-106">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="48d83-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="48d83-107">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="48d83-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="48d83-108">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="48d83-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="48d83-109">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="48d83-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="48d83-110">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="48d83-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="48d83-111">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="48d83-111">In this topic:</span></span>

-   [<span data-ttu-id="48d83-112">Введение</span><span class="sxs-lookup"><span data-stu-id="48d83-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="48d83-113">Пример</span><span class="sxs-lookup"><span data-stu-id="48d83-113">Example</span></span>](#example)
-   [<span data-ttu-id="48d83-114">Настройка VML</span><span class="sxs-lookup"><span data-stu-id="48d83-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="48d83-115">Справочник по объектной модели VML</span><span class="sxs-lookup"><span data-stu-id="48d83-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="48d83-116">Shape, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="48d83-117">Вложенные элементы элемента Shape</span><span class="sxs-lookup"><span data-stu-id="48d83-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="48d83-118">Элемент Background</span><span class="sxs-lookup"><span data-stu-id="48d83-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="48d83-119">Элемент объемной фигуры</span><span class="sxs-lookup"><span data-stu-id="48d83-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="48d83-120">Fill, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="48d83-121">Group, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="48d83-122">Имажедата, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="48d83-123">Элемент Path</span><span class="sxs-lookup"><span data-stu-id="48d83-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="48d83-124">Элемент Shadow</span><span class="sxs-lookup"><span data-stu-id="48d83-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="48d83-125">Элемент асимметрии</span><span class="sxs-lookup"><span data-stu-id="48d83-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="48d83-126">Элемент Stroke</span><span class="sxs-lookup"><span data-stu-id="48d83-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="48d83-127">Текстпас, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="48d83-128">Типы данных, используемые в объектной модели VML</span><span class="sxs-lookup"><span data-stu-id="48d83-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="48d83-129">Введение</span><span class="sxs-lookup"><span data-stu-id="48d83-129">Introduction</span></span>

<span data-ttu-id="48d83-130">[Язык VML (VML)](https://www.w3.org/TR/NOTE-datetime.html) — это текстовый язык, который использует [XML](https://www.w3.org/TR/REC-xml.mdl) для расширения HTML с целью отображения векторных графических данных.</span><span class="sxs-lookup"><span data-stu-id="48d83-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="48d83-131">VML модель DOM (DOM) определяет программный интерфейс для управления элементами документа.</span><span class="sxs-lookup"><span data-stu-id="48d83-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="48d83-132">Это позволяет пользователю динамически создавать и изменять векторную графику с помощью интерфейса, не зависящего от платформы и языка.</span><span class="sxs-lookup"><span data-stu-id="48d83-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="48d83-133">Модель DOM VML соответствует спецификации [модель DOM](https://www.w3.org/TR/REC-DOM-Level-1/) .</span><span class="sxs-lookup"><span data-stu-id="48d83-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="48d83-134">VML использует элемент [Shape](#shape-element) в качестве базового стандартного блока для векторных графических изображений.</span><span class="sxs-lookup"><span data-stu-id="48d83-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="48d83-135">После создания фигуры можно изменить форму с помощью атрибутов или вложенных подэлементов.</span><span class="sxs-lookup"><span data-stu-id="48d83-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="48d83-136">Например, чтобы изменить цвет фигуры, назначьте атрибуту **FillColor** значение цвета.</span><span class="sxs-lookup"><span data-stu-id="48d83-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="48d83-137">Некоторые атрибуты фигуры также являются [подэлементами](/windows) и имеют собственные атрибуты, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="48d83-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="48d83-138">Фон</span><span class="sxs-lookup"><span data-stu-id="48d83-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="48d83-139">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="48d83-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="48d83-140">Заполнить</span><span class="sxs-lookup"><span data-stu-id="48d83-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="48d83-141">Группа</span><span class="sxs-lookup"><span data-stu-id="48d83-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="48d83-142">имажедата</span><span class="sxs-lookup"><span data-stu-id="48d83-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="48d83-143">Путь</span><span class="sxs-lookup"><span data-stu-id="48d83-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="48d83-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="48d83-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="48d83-145">Отклонение</span><span class="sxs-lookup"><span data-stu-id="48d83-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="48d83-146">Водок</span><span class="sxs-lookup"><span data-stu-id="48d83-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="48d83-147">текстпас</span><span class="sxs-lookup"><span data-stu-id="48d83-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="48d83-148">Объектная модель VML использует несколько [типов данных](/windows) для определения параметров.</span><span class="sxs-lookup"><span data-stu-id="48d83-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="48d83-149">Типы данных с префиксом "VG" являются перечислениями, а с префиксом "ИВГ" — объектами.</span><span class="sxs-lookup"><span data-stu-id="48d83-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="48d83-150">Щелкните здесь для вывода списка.</span><span class="sxs-lookup"><span data-stu-id="48d83-150">Click here for a list.</span></span> <span data-ttu-id="48d83-151">Дополнительные типы с указанными параметрами перечислены в списке.</span><span class="sxs-lookup"><span data-stu-id="48d83-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="48d83-152">Пример</span><span class="sxs-lookup"><span data-stu-id="48d83-152">Example</span></span>

<span data-ttu-id="48d83-153">В следующем коде на языке VBScript показано, как создать простую фигуру:</span><span class="sxs-lookup"><span data-stu-id="48d83-153">The following VBScript code shows how to create a simple shape:</span></span>


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



<span data-ttu-id="48d83-154">В приведенном выше примере фигура создается с помощью модель DOM метода **CreateElement**.</span><span class="sxs-lookup"><span data-stu-id="48d83-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="48d83-155">Фигура представляет собой предопределенную фигуру в формате VML.</span><span class="sxs-lookup"><span data-stu-id="48d83-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="48d83-156">Несмотря на то, что объект существует, он не может быть частью документа, пока он не будет присоединен к документу.</span><span class="sxs-lookup"><span data-stu-id="48d83-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="48d83-157">С помощью метода **AppendChild** Rect становится дочерним элементом элемента **div** с именем мидив.</span><span class="sxs-lookup"><span data-stu-id="48d83-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="48d83-158">Несколько минимальных атрибутов стиля («**Расположение**», « **Ширина**», « **Высота**», « **сверху**», « **слева**») устанавливаются для присвоения форме определенного размера.</span><span class="sxs-lookup"><span data-stu-id="48d83-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="48d83-159">Наконец, цвет присваивается атрибуту **FillColor** .</span><span class="sxs-lookup"><span data-stu-id="48d83-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="48d83-160">Обратите внимание, что можно использовать любой язык сценариев или любой язык, который может работать с интерфейсами модель DOM.</span><span class="sxs-lookup"><span data-stu-id="48d83-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="48d83-161">Настройка VML</span><span class="sxs-lookup"><span data-stu-id="48d83-161">Setting up VML</span></span>

<span data-ttu-id="48d83-162">Одна реализация VML осуществляется через Microsoft Internet Explorer 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="48d83-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="48d83-163">Чтобы правильно настроить объект отрисовки на веб-странице, необходимо выполнить следующие добавления:</span><span class="sxs-lookup"><span data-stu-id="48d83-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="48d83-164">Схема должна быть настроена в начальной</span><span class="sxs-lookup"><span data-stu-id="48d83-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="48d83-165">тег следующим образом:</span><span class="sxs-lookup"><span data-stu-id="48d83-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="48d83-166">Режим подготовки к просмотру должен быть частью стиля документа:</span><span class="sxs-lookup"><span data-stu-id="48d83-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="48d83-167">Ниже показан пример веб-страницы HTML, настроенной правильно для VML, отображающей динамическое создание фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



<span data-ttu-id="48d83-168">Обратите внимание, что в бета-версиях требуется тег объекта ActiveX и другой стиль поведения.</span><span class="sxs-lookup"><span data-stu-id="48d83-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="48d83-169">Справочник по объектной модели VML</span><span class="sxs-lookup"><span data-stu-id="48d83-169">VML OM Reference</span></span>

<span data-ttu-id="48d83-170">Эта ссылка определяет элемент [Shape](#shape-element) , [подэлементы](/windows)и [типы данных](/windows) , используемые объектной моделью VML.</span><span class="sxs-lookup"><span data-stu-id="48d83-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="48d83-171">Shape, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-171">Shape element</span></span>

<span data-ttu-id="48d83-172">Фигуры — это стандартные блоки графических изображений, определяемые язык VML (VML).</span><span class="sxs-lookup"><span data-stu-id="48d83-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="48d83-173">Фигура является элементом верхнего уровня, и несколько подэлементов помогают определить природу каждой фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="48d83-174">VML предоставляет стандартные фигуры:</span><span class="sxs-lookup"><span data-stu-id="48d83-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="48d83-175">**Атрибуты фигур**</span><span class="sxs-lookup"><span data-stu-id="48d83-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="48d83-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="48d83-176">**Arc**</span></span>
-   <span data-ttu-id="48d83-177">**Соединитель**</span><span class="sxs-lookup"><span data-stu-id="48d83-177">**Curve**</span></span>
-   <span data-ttu-id="48d83-178">**Line**</span><span class="sxs-lookup"><span data-stu-id="48d83-178">**Line**</span></span>
-   <span data-ttu-id="48d83-179">**Линию**</span><span class="sxs-lookup"><span data-stu-id="48d83-179">**PolyLine**</span></span>
-   <span data-ttu-id="48d83-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="48d83-180">**Rect**</span></span>
-   <span data-ttu-id="48d83-181">**раундрект**</span><span class="sxs-lookup"><span data-stu-id="48d83-181">**RoundRect**</span></span>



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-182">Разница</span><span class="sxs-lookup"><span data-stu-id="48d83-182">Adj</span></span>          | <span data-ttu-id="48d83-183">[Ивгаджустментс](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="48d83-184">Разделенный запятыми список чисел, которые являются параметрами для формул руководств, определяющих путь к фигуре.</span><span class="sxs-lookup"><span data-stu-id="48d83-184">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="48d83-185">Значения можно опустить, чтобы разрешить использование значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="48d83-185">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="48d83-186">Может быть до 8 значений коррекции.</span><span class="sxs-lookup"><span data-stu-id="48d83-186">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="48d83-187">Alt</span><span class="sxs-lookup"><span data-stu-id="48d83-187">Alt</span></span>          | <span data-ttu-id="48d83-188">Строка.</span><span class="sxs-lookup"><span data-stu-id="48d83-188">String.</span></span> <span data-ttu-id="48d83-189">Альтернативный текст, связанный с фигурой.</span><span class="sxs-lookup"><span data-stu-id="48d83-189">Alternative text associated with shape.</span></span> <span data-ttu-id="48d83-190">Используется для неграфического обзора.</span><span class="sxs-lookup"><span data-stu-id="48d83-190">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="48d83-191">Кнопка</span><span class="sxs-lookup"><span data-stu-id="48d83-191">Button</span></span>       | <span data-ttu-id="48d83-192">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-192">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-193">Отображает поведение кнопки при нажатии.</span><span class="sxs-lookup"><span data-stu-id="48d83-193">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="48d83-194">бвмоде</span><span class="sxs-lookup"><span data-stu-id="48d83-194">BWMode</span></span>       | <span data-ttu-id="48d83-195">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="48d83-196">Определяет, как форма будет отображаться в виде черно-белого представления в приложениях или при печати на черно-белых принтерах.</span><span class="sxs-lookup"><span data-stu-id="48d83-196">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="48d83-197">К значениям относятся: **Цвет**, **Авто**, **оттенки серого**, **лигхтграйскале**, **инверсеграй**, **грайаутлине**, **блакктекстандлинес**, **HighContrast**, **черный**, **белый**, **нерисованный**.</span><span class="sxs-lookup"><span data-stu-id="48d83-197">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="48d83-198">Значение по умолчанию: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="48d83-198">Default: **Auto**.</span></span> |
| <span data-ttu-id="48d83-199">бвнормал</span><span class="sxs-lookup"><span data-stu-id="48d83-199">BWNormal</span></span>     | <span data-ttu-id="48d83-200">Вгблакквхитемоде.</span><span class="sxs-lookup"><span data-stu-id="48d83-200">VgBlackWhiteMode.</span></span> <span data-ttu-id="48d83-201">Если Бвмоде имеет значение Auto, это свойство обращается к, чтобы отобразить форму в нормальном черном и белом режиме.</span><span class="sxs-lookup"><span data-stu-id="48d83-201">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="48d83-202">К значениям относятся: **Цвет**, **Авто**, **оттенки серого**, **лигхтграйскале**, **инверсеграй**, **грайаутлине**, **блакктекстандлинес**, **HighContrast**, **черный**, **белый**, **нерисованный**.</span><span class="sxs-lookup"><span data-stu-id="48d83-202">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="48d83-203">Значение по умолчанию: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="48d83-203">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="48d83-204">бвпуре</span><span class="sxs-lookup"><span data-stu-id="48d83-204">BWPure</span></span>       | <span data-ttu-id="48d83-205">Вгблакквхитемоде.</span><span class="sxs-lookup"><span data-stu-id="48d83-205">VgBlackWhiteMode.</span></span> <span data-ttu-id="48d83-206">Если Бвмоде имеет значение Auto, это свойство обращается к, чтобы отобразить фигуру в чистом B/W.</span><span class="sxs-lookup"><span data-stu-id="48d83-206">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="48d83-207">К значениям относятся: **Цвет**, **Авто**, **оттенки серого**, **лигхтграйскале**, **инверсеграй**, **грайаутлине**, **блакктекстандлинес**, **HighContrast**, **черный**, **белый**, **нерисованный**.</span><span class="sxs-lookup"><span data-stu-id="48d83-207">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="48d83-208">Значение по умолчанию: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="48d83-208">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="48d83-209">чилдшапес</span><span class="sxs-lookup"><span data-stu-id="48d83-209">ChildShapes</span></span>  | <span data-ttu-id="48d83-210">Ивгграупшапес.</span><span class="sxs-lookup"><span data-stu-id="48d83-210">IVgGroupShapes.</span></span> <span data-ttu-id="48d83-211">Коллекция других фигур в этой группе.</span><span class="sxs-lookup"><span data-stu-id="48d83-211">A collection of other shapes in this group.</span></span> <span data-ttu-id="48d83-212">Эта коллекция поддерживает стандартную длину и методы элементов.</span><span class="sxs-lookup"><span data-stu-id="48d83-212">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="48d83-213">чромакэй</span><span class="sxs-lookup"><span data-stu-id="48d83-213">Chromakey</span></span>    | <span data-ttu-id="48d83-214">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="48d83-215">Значение цвета, которое будет прозрачным и показывать все, что находится за фигурой.</span><span class="sxs-lookup"><span data-stu-id="48d83-215">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="48d83-216">Control1</span><span class="sxs-lookup"><span data-stu-id="48d83-216">Control1</span></span>     | <span data-ttu-id="48d83-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="48d83-218">Контрольная точка для кривой.</span><span class="sxs-lookup"><span data-stu-id="48d83-218">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="48d83-219">Control2</span><span class="sxs-lookup"><span data-stu-id="48d83-219">Control2</span></span>     | <span data-ttu-id="48d83-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="48d83-221">Контрольная точка для кривой.</span><span class="sxs-lookup"><span data-stu-id="48d83-221">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="48d83-222">курдоригин</span><span class="sxs-lookup"><span data-stu-id="48d83-222">CoordOrigin</span></span>  | <span data-ttu-id="48d83-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Координаты в левом верхнем углу прямоугольника контейнера.</span><span class="sxs-lookup"><span data-stu-id="48d83-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="48d83-224">Диапазон от 0 до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="48d83-224">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="48d83-225">курдсизе</span><span class="sxs-lookup"><span data-stu-id="48d83-225">CoordSize</span></span>    | <span data-ttu-id="48d83-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="48d83-227">Ширина и высота пространства координат внутри ссылочного прямоугольника этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-227">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="48d83-228">Если он не указан, то он совпадает с шириной и высотой прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="48d83-228">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="48d83-229">Диапазон от 0 до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="48d83-229">Range from 0 to infinity.</span></span> <span data-ttu-id="48d83-230">Значение по умолчанию: 1000, 1000.</span><span class="sxs-lookup"><span data-stu-id="48d83-230">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="48d83-231">ендангле</span><span class="sxs-lookup"><span data-stu-id="48d83-231">EndAngle</span></span>     | <span data-ttu-id="48d83-232">[Вганглеиндегрис](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="48d83-233">Конечный угол фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-233">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="48d83-234">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="48d83-234">Extrusion</span></span>    | <span data-ttu-id="48d83-235">Ивжекструсион.</span><span class="sxs-lookup"><span data-stu-id="48d83-235">IVgExtrusion.</span></span> <span data-ttu-id="48d83-236">Задает значение объекта объема для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-236">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="48d83-237">Дополнительные сведения см. в элементе объемной [фигуры](msdn-online-vml-extrusion-element.md) .</span><span class="sxs-lookup"><span data-stu-id="48d83-237">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="48d83-238">Заполнить</span><span class="sxs-lookup"><span data-stu-id="48d83-238">Fill</span></span>         | <span data-ttu-id="48d83-239">Вгфиллформат.</span><span class="sxs-lookup"><span data-stu-id="48d83-239">VgFillFormat.</span></span> <span data-ttu-id="48d83-240">Задает значение заливки для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-240">Specifies the fill value for this shape.</span></span> <span data-ttu-id="48d83-241">Дополнительные сведения см. в элементе [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="48d83-241">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="48d83-242">FillColor</span><span class="sxs-lookup"><span data-stu-id="48d83-242">FillColor</span></span>    | <span data-ttu-id="48d83-243">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="48d83-244">Основной цвет кисти, используемой для заполнения контура этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-244">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="48d83-245">Указал</span><span class="sxs-lookup"><span data-stu-id="48d83-245">Filled</span></span>       | <span data-ttu-id="48d83-246">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-246">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-247">Если значение — true, то путь, определяющий фигуру, будет заполнен.</span><span class="sxs-lookup"><span data-stu-id="48d83-247">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="48d83-248">По умолчанию он заполняется сплошным цветом, если отсутствует вложенный элемент Fill, указывающий более сложные свойства заливки.</span><span class="sxs-lookup"><span data-stu-id="48d83-248">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="48d83-249">Если значение равно false, заливка прозрачна.</span><span class="sxs-lookup"><span data-stu-id="48d83-249">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="48d83-250">Перевернуть</span><span class="sxs-lookup"><span data-stu-id="48d83-250">Flip</span></span>         | <span data-ttu-id="48d83-251">Вгфлипориентатион.</span><span class="sxs-lookup"><span data-stu-id="48d83-251">VgFlipOrientation.</span></span> <span data-ttu-id="48d83-252">Значения: X Y XY Икс</span><span class="sxs-lookup"><span data-stu-id="48d83-252">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="48d83-253">форцедаш</span><span class="sxs-lookup"><span data-stu-id="48d83-253">ForceDash</span></span>    | <span data-ttu-id="48d83-254">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-254">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-255">Указывает, что пунктирная структура должна быть визуализирована, если нет линии и заливка для фигуры отсутствует.</span><span class="sxs-lookup"><span data-stu-id="48d83-255">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="48d83-256">Это поведение обычно полезно для того, чтобы сделать невидимые фигуры видимыми при редактировании приложений, чтобы их можно было выбирать и использовать, например, на карте изображений.</span><span class="sxs-lookup"><span data-stu-id="48d83-256">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="48d83-257">Формулы</span><span class="sxs-lookup"><span data-stu-id="48d83-257">Formulas</span></span>     | <span data-ttu-id="48d83-258">Ивгформулас.</span><span class="sxs-lookup"><span data-stu-id="48d83-258">IVgFormulas.</span></span> <span data-ttu-id="48d83-259">Массив формул, определяющих фигуру.</span><span class="sxs-lookup"><span data-stu-id="48d83-259">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="48d83-260">Исходный тип</span><span class="sxs-lookup"><span data-stu-id="48d83-260">From</span></span>         | <span data-ttu-id="48d83-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="48d83-262">Начальная точка линии.</span><span class="sxs-lookup"><span data-stu-id="48d83-262">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="48d83-263">Полный</span><span class="sxs-lookup"><span data-stu-id="48d83-263">HRef</span></span>         | <span data-ttu-id="48d83-264">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-264">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-265">URL-адрес для перехода при щелчке этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-265">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="48d83-266">ImageData</span><span class="sxs-lookup"><span data-stu-id="48d83-266">ImageData</span></span>    | <span data-ttu-id="48d83-267">Ивгимажедата.</span><span class="sxs-lookup"><span data-stu-id="48d83-267">IVgImageData.</span></span> <span data-ttu-id="48d83-268">Сведения об изображении, если фигура является изображением.</span><span class="sxs-lookup"><span data-stu-id="48d83-268">Image information if the shape is a picture.</span></span> <span data-ttu-id="48d83-269">Дополнительные сведения см. в элементе Имажедата.</span><span class="sxs-lookup"><span data-stu-id="48d83-269">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="48d83-270">онед</span><span class="sxs-lookup"><span data-stu-id="48d83-270">OnEd</span></span>         | <span data-ttu-id="48d83-271">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-271">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-272">Скрывает все маркеры, кроме верхнего левого и нижнего правого, как в маркерах для сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="48d83-272">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="48d83-273">Непрозрачность</span><span class="sxs-lookup"><span data-stu-id="48d83-273">Opacity</span></span>      | <span data-ttu-id="48d83-274">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="48d83-275">Непрозрачность всей фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-275">The opacity of the entire shape.</span></span> <span data-ttu-id="48d83-276">Число от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="48d83-276">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="48d83-277">Путь</span><span class="sxs-lookup"><span data-stu-id="48d83-277">Path</span></span>         | <span data-ttu-id="48d83-278">Ивгпас.</span><span class="sxs-lookup"><span data-stu-id="48d83-278">IVgPath.</span></span> <span data-ttu-id="48d83-279">Строка, содержащая команды, определяющие путь.</span><span class="sxs-lookup"><span data-stu-id="48d83-279">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="48d83-280">точки</span><span class="sxs-lookup"><span data-stu-id="48d83-280">Points</span></span>       | <span data-ttu-id="48d83-281">[Ивгпоинтс](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="48d83-282">Коллекция точек, определяющих фигуру.</span><span class="sxs-lookup"><span data-stu-id="48d83-282">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="48d83-283">Печать</span><span class="sxs-lookup"><span data-stu-id="48d83-283">Print</span></span>        | <span data-ttu-id="48d83-284">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-284">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-285">Если значение — true, эта фигура предназначена для печати.</span><span class="sxs-lookup"><span data-stu-id="48d83-285">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="48d83-286">Поворот</span><span class="sxs-lookup"><span data-stu-id="48d83-286">Rotation</span></span>     | <span data-ttu-id="48d83-287">[Вганглеиндегрис](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="48d83-288">Задает поворот фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-288">Sets rotation of shape.</span></span> <span data-ttu-id="48d83-289">Значение распространяется на стиль фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-289">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="48d83-290">Масштабирование</span><span class="sxs-lookup"><span data-stu-id="48d83-290">Scale</span></span>        | <span data-ttu-id="48d83-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="48d83-292">Масштаб фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-292">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="48d83-293">Shadow</span><span class="sxs-lookup"><span data-stu-id="48d83-293">Shadow</span></span>       | <span data-ttu-id="48d83-294">Ивгшадов.</span><span class="sxs-lookup"><span data-stu-id="48d83-294">IVgShadow.</span></span> <span data-ttu-id="48d83-295">Задает тень для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-295">Specifies the shadow for this shape.</span></span> <span data-ttu-id="48d83-296">Дополнительные сведения см. в элементе [shadow](msdn-online-vml-shadow-element.md) .</span><span class="sxs-lookup"><span data-stu-id="48d83-296">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="48d83-297">спт</span><span class="sxs-lookup"><span data-stu-id="48d83-297">Spt</span></span>          | <span data-ttu-id="48d83-298">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="48d83-298">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="48d83-299">StartAngle и заканчивая</span><span class="sxs-lookup"><span data-stu-id="48d83-299">StartAngle</span></span>   | <span data-ttu-id="48d83-300">[Вганглеиндегрис](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="48d83-301">Начальный угол фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-301">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="48d83-302">Stroke</span><span class="sxs-lookup"><span data-stu-id="48d83-302">Stroke</span></span>       | <span data-ttu-id="48d83-303">Вгстрокеформат.</span><span class="sxs-lookup"><span data-stu-id="48d83-303">VgStrokeFormat.</span></span> <span data-ttu-id="48d83-304">Дополнительные сведения см. в разделе элемент Stroke.</span><span class="sxs-lookup"><span data-stu-id="48d83-304">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="48d83-305">строкеколор</span><span class="sxs-lookup"><span data-stu-id="48d83-305">StrokeColor</span></span>  | <span data-ttu-id="48d83-306">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="48d83-307">Основной цвет кисти, используемой для обводки контура этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-307">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="48d83-308">Заштриховывать</span><span class="sxs-lookup"><span data-stu-id="48d83-308">Stroked</span></span>      | <span data-ttu-id="48d83-309">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-309">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-310">Если значение равно true, то путь, определяющий фигуру, будет обводкой.</span><span class="sxs-lookup"><span data-stu-id="48d83-310">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="48d83-311">строкевеигхт</span><span class="sxs-lookup"><span data-stu-id="48d83-311">StrokeWeight</span></span> | <span data-ttu-id="48d83-312">[Вгленгс](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-312">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="48d83-313">Ширина кисти, используемой для обводки контура.</span><span class="sxs-lookup"><span data-stu-id="48d83-313">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="48d83-314">Диапазоны от 0 до 1584.</span><span class="sxs-lookup"><span data-stu-id="48d83-314">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="48d83-315">текстпас</span><span class="sxs-lookup"><span data-stu-id="48d83-315">TextPath</span></span>     | <span data-ttu-id="48d83-316">Ивгтекстпас.</span><span class="sxs-lookup"><span data-stu-id="48d83-316">IVgTextPath.</span></span> <span data-ttu-id="48d83-317">Указывает объект Текстпас фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-317">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="48d83-318">Дополнительные сведения см. в элементе [текстпас](msdn-online-vml-textpath-element.md) .</span><span class="sxs-lookup"><span data-stu-id="48d83-318">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="48d83-319">Кому</span><span class="sxs-lookup"><span data-stu-id="48d83-319">To</span></span>           | <span data-ttu-id="48d83-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="48d83-321">Конечная точка линии.</span><span class="sxs-lookup"><span data-stu-id="48d83-321">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="48d83-322">Тип</span><span class="sxs-lookup"><span data-stu-id="48d83-322">Type</span></span>         | <span data-ttu-id="48d83-323">Строка.</span><span class="sxs-lookup"><span data-stu-id="48d83-323">String.</span></span> <span data-ttu-id="48d83-324">Тип фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-324">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="48d83-325">Вложенные элементы элемента Shape</span><span class="sxs-lookup"><span data-stu-id="48d83-325">Subelements of the Shape Element</span></span>

<span data-ttu-id="48d83-326">Следующие подэлементы являются частью объектной модели VML.</span><span class="sxs-lookup"><span data-stu-id="48d83-326">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="48d83-327">Фон</span><span class="sxs-lookup"><span data-stu-id="48d83-327">Background</span></span>](#background-element)
-   [<span data-ttu-id="48d83-328">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="48d83-328">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="48d83-329">Заполнить</span><span class="sxs-lookup"><span data-stu-id="48d83-329">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="48d83-330">Группа</span><span class="sxs-lookup"><span data-stu-id="48d83-330">Group</span></span>](#group-element)
-   [<span data-ttu-id="48d83-331">имажедата</span><span class="sxs-lookup"><span data-stu-id="48d83-331">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="48d83-332">Путь</span><span class="sxs-lookup"><span data-stu-id="48d83-332">Path</span></span>](#path-element)
-   [<span data-ttu-id="48d83-333">Shadow</span><span class="sxs-lookup"><span data-stu-id="48d83-333">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="48d83-334">Отклонение</span><span class="sxs-lookup"><span data-stu-id="48d83-334">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="48d83-335">Водок</span><span class="sxs-lookup"><span data-stu-id="48d83-335">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="48d83-336">текстпас</span><span class="sxs-lookup"><span data-stu-id="48d83-336">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="48d83-337">Элемент Background</span><span class="sxs-lookup"><span data-stu-id="48d83-337">Background element</span></span>

<span data-ttu-id="48d83-338">Описывает заливку фона страницы с помощью заливки VML.</span><span class="sxs-lookup"><span data-stu-id="48d83-338">Describes the fill of the background of a page using VML fills.</span></span>

<span data-ttu-id="48d83-339">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="48d83-339">**Attributes**</span></span>



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-340">бвмоде</span><span class="sxs-lookup"><span data-stu-id="48d83-340">BWMode</span></span>    | <span data-ttu-id="48d83-341">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="48d83-342">Определяет, как форма будет отображаться в виде черно-белого представления в приложениях или при печати.</span><span class="sxs-lookup"><span data-stu-id="48d83-342">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="48d83-343">бвнормал</span><span class="sxs-lookup"><span data-stu-id="48d83-343">BWNormal</span></span>  | <span data-ttu-id="48d83-344">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="48d83-345">Если Бвмоде имеет значение Auto, это свойство обращается к, чтобы отобразить форму в нормальном черном и белом режиме.</span><span class="sxs-lookup"><span data-stu-id="48d83-345">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="48d83-346">бвпуре</span><span class="sxs-lookup"><span data-stu-id="48d83-346">BWPure</span></span>    | <span data-ttu-id="48d83-347">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="48d83-348">Если Бвмоде имеет значение Auto, это свойство обращается к, чтобы отобразить фигуру в чисто черном и белом режиме.</span><span class="sxs-lookup"><span data-stu-id="48d83-348">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="48d83-349">Заполнить</span><span class="sxs-lookup"><span data-stu-id="48d83-349">Fill</span></span>      | <span data-ttu-id="48d83-350">Вгфиллформат.</span><span class="sxs-lookup"><span data-stu-id="48d83-350">VgFillFormat.</span></span> <span data-ttu-id="48d83-351">Задает заливку для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-351">Specifies the fill for this shape.</span></span> <span data-ttu-id="48d83-352">Дополнительные сведения см. в разделе элемент [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="48d83-352">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="48d83-353">FillColor</span><span class="sxs-lookup"><span data-stu-id="48d83-353">FillColor</span></span> | <span data-ttu-id="48d83-354">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="48d83-355">Основной цвет кисти, используемой для заполнения контура этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-355">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="48d83-356">Повторяющееся значение цвета в элементе Fill.</span><span class="sxs-lookup"><span data-stu-id="48d83-356">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="48d83-357">По умолчанию цвет белый.</span><span class="sxs-lookup"><span data-stu-id="48d83-357">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="48d83-358">Элемент объемной фигуры</span><span class="sxs-lookup"><span data-stu-id="48d83-358">Extrusion element</span></span>

<span data-ttu-id="48d83-359">Описывает трехмерную часть фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-359">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="48d83-360">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="48d83-360">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-361">ауторотатионцентер</span><span class="sxs-lookup"><span data-stu-id="48d83-361">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="48d83-362"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-363">Если значение равно true, центр вращения группы трехмерных объектов (фактически существует только один объект в группе) автоматически определяется как центр группы. в противном случае он определяется параметрами Ротатионцентер, которые являются частью фигуры с 0, 0, равным центру.</span><span class="sxs-lookup"><span data-stu-id="48d83-363">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-364">Глубина</span><span class="sxs-lookup"><span data-stu-id="48d83-364">BackDepth</span></span></td>
<td><span data-ttu-id="48d83-365"><a href="msdn-online-vml-vglength.md"><strong>Вгленгс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="48d83-366">Величина обратной придания.</span><span class="sxs-lookup"><span data-stu-id="48d83-366">Amount of backward extrusion.</span></span> <span data-ttu-id="48d83-367">В диапазоне от 0 до 32767.</span><span class="sxs-lookup"><span data-stu-id="48d83-367">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-368">Brightness</span><span class="sxs-lookup"><span data-stu-id="48d83-368">Brightness</span></span></td>
<td><span data-ttu-id="48d83-369"><a href="#data-types-used-in-the-vml-object-model">Вгпоситивенумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="48d83-370">Общая яркость сцены.</span><span class="sxs-lookup"><span data-stu-id="48d83-370">Overall brightness of the scene.</span></span> <span data-ttu-id="48d83-371">Значение по умолчанию — &quot; 20 000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-371">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-372">Цвет</span><span class="sxs-lookup"><span data-stu-id="48d83-372">Color</span></span></td>
<td><span data-ttu-id="48d83-373"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="48d83-374">Цвет объема.</span><span class="sxs-lookup"><span data-stu-id="48d83-374">The color of the extrusion.</span></span> <span data-ttu-id="48d83-375">Используется, только если Колормоде является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="48d83-375">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="48d83-376">В противном случае функция Auto устанавливает цвет эффектов объемной фигуры так же, как FillColor.</span><span class="sxs-lookup"><span data-stu-id="48d83-376">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-377">колормоде</span><span class="sxs-lookup"><span data-stu-id="48d83-377">ColorMode</span></span></td>
<td><span data-ttu-id="48d83-378">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="48d83-378">Vg3DColorMode.</span></span> <span data-ttu-id="48d83-379">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-379">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-380">Auto (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-380">Auto (default)</span></span></li>
<li><span data-ttu-id="48d83-381">Особые настройки</span><span class="sxs-lookup"><span data-stu-id="48d83-381">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-382">Рассеянность</span><span class="sxs-lookup"><span data-stu-id="48d83-382">Diffusity</span></span></td>
<td><span data-ttu-id="48d83-383"><a href="#data-types-used-in-the-vml-object-model">Вгпоситивенумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="48d83-384">Отношение инцидента к рассеянному свету.</span><span class="sxs-lookup"><span data-stu-id="48d83-384">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="48d83-385">Значения меньше 1,0 являются нормальными, но значения, превышающие один, могут создавать интересные эффекты.</span><span class="sxs-lookup"><span data-stu-id="48d83-385">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-386">Edge</span><span class="sxs-lookup"><span data-stu-id="48d83-386">Edge</span></span></td>
<td><span data-ttu-id="48d83-387"><a href="msdn-online-vml-vglength.md">Вгленгс</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="48d83-388">Задает размер смоделированного скругленного края.</span><span class="sxs-lookup"><span data-stu-id="48d83-388">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="48d83-389">В диапазоне от 0 до 32767 в PTS с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="48d83-389">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="48d83-390">Значение по умолчанию — &quot; выбрано 1pt &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-390">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-391">Аспект</span><span class="sxs-lookup"><span data-stu-id="48d83-391">Facet</span></span></td>
<td><span data-ttu-id="48d83-392"><a href="#data-types-used-in-the-vml-object-model">Вгпоситивенумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="48d83-393">Задает аспект сцены.</span><span class="sxs-lookup"><span data-stu-id="48d83-393">Sets the facet of the scene.</span></span> <span data-ttu-id="48d83-394">Значение по умолчанию — &quot; 30 000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-394">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-395">форедепс</span><span class="sxs-lookup"><span data-stu-id="48d83-395">ForeDepth</span></span></td>
<td><span data-ttu-id="48d83-396"><a href="msdn-online-vml-vglength.md">Вгленгс</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="48d83-397">Объем пересылки.</span><span class="sxs-lookup"><span data-stu-id="48d83-397">Amount of forward extrusion.</span></span> <span data-ttu-id="48d83-398">В диапазоне от 0 до 32767.</span><span class="sxs-lookup"><span data-stu-id="48d83-398">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-399">лигхтфаце</span><span class="sxs-lookup"><span data-stu-id="48d83-399">LightFace</span></span></td>
<td><span data-ttu-id="48d83-400"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-401">Детермимес, будет ли лицевая сторона объекта отвечать на изменения в трехмерном освещении, например при повороте объекта.</span><span class="sxs-lookup"><span data-stu-id="48d83-401">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-402">лигхсарш</span><span class="sxs-lookup"><span data-stu-id="48d83-402">LightHarsh</span></span></td>
<td><span data-ttu-id="48d83-403"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-404">Харша освещение для основного источника света.</span><span class="sxs-lookup"><span data-stu-id="48d83-404">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="48d83-405">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="48d83-405">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-406">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="48d83-406">LightHarsh2</span></span></td>
<td><span data-ttu-id="48d83-407"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-408">Харша освещение для дополнительного источника света.</span><span class="sxs-lookup"><span data-stu-id="48d83-408">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="48d83-409">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="48d83-409">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-410">лигхтлевел</span><span class="sxs-lookup"><span data-stu-id="48d83-410">LightLevel</span></span></td>
<td><span data-ttu-id="48d83-411"><a href="#data-types-used-in-the-vml-object-model">Вгнумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="48d83-412">Интенсивность основного источника освещения.</span><span class="sxs-lookup"><span data-stu-id="48d83-412">Intensity of the primary light source.</span></span> <span data-ttu-id="48d83-413">Значение по умолчанию — &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-413">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-414">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="48d83-414">LightLevel2</span></span></td>
<td><span data-ttu-id="48d83-415"><a href="#data-types-used-in-the-vml-object-model">Вгнумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="48d83-416">Интенсивность вторичного источника освещения.</span><span class="sxs-lookup"><span data-stu-id="48d83-416">Intensity of the secondary light source.</span></span> <span data-ttu-id="48d83-417">Значение по умолчанию — &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-417">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-418">лигхтпоситион</span><span class="sxs-lookup"><span data-stu-id="48d83-418">LightPosition</span></span></td>
<td><span data-ttu-id="48d83-419">Объект.</span><span class="sxs-lookup"><span data-stu-id="48d83-419">Vector3D.</span></span> <span data-ttu-id="48d83-420">Расположение основного источника освещения.</span><span class="sxs-lookup"><span data-stu-id="48d83-420">Position of the primary light source.</span></span> <span data-ttu-id="48d83-421">Значение по умолчанию — &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-421">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-422">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="48d83-422">LightPosition2</span></span></td>
<td><span data-ttu-id="48d83-423">Объект.</span><span class="sxs-lookup"><span data-stu-id="48d83-423">Vector3D.</span></span> <span data-ttu-id="48d83-424">Расположение вторичного источника освещения.</span><span class="sxs-lookup"><span data-stu-id="48d83-424">Position of the secondary light source.</span></span> <span data-ttu-id="48d83-425">Значение по умолчанию — &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-425">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-426">локкротатионцентер</span><span class="sxs-lookup"><span data-stu-id="48d83-426">LockRotationCenter</span></span></td>
<td><span data-ttu-id="48d83-427"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-428">&quot;Локкротатионцентер &quot; означает, что поворот группы определяется как угловой угол [1] градусов вокруг оси y на странице, за которым следует угол поворота [0] градусов относительно оси x.</span><span class="sxs-lookup"><span data-stu-id="48d83-428">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="48d83-429">Если Локкротатионцентер имеет значение false, поворот определяется как угол в градусах с направлением вниз относительно вектора, определенного ориентацией.</span><span class="sxs-lookup"><span data-stu-id="48d83-429">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="48d83-430">Например, локкротатионцентер = false ориентатионангле = 45 Orientation = (0, 1, 0) эквивалентно локкротатионцентер = true ротатионангле = (0, 45).</span><span class="sxs-lookup"><span data-stu-id="48d83-430">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-431">Металлические</span><span class="sxs-lookup"><span data-stu-id="48d83-431">Metal</span></span></td>
<td><span data-ttu-id="48d83-432"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-433">Приводит к тому, что отраженный свет отражается цветом материала вместо цвета источника, что делает объект более металлным.</span><span class="sxs-lookup"><span data-stu-id="48d83-433">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-434">Включено</span><span class="sxs-lookup"><span data-stu-id="48d83-434">On</span></span></td>
<td><span data-ttu-id="48d83-435"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-436">Включает и выключает отображение воздействия на объемные придания.</span><span class="sxs-lookup"><span data-stu-id="48d83-436">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-437">Orientation</span><span class="sxs-lookup"><span data-stu-id="48d83-437">Orientation</span></span></td>
<td><span data-ttu-id="48d83-438">Объект.</span><span class="sxs-lookup"><span data-stu-id="48d83-438">Vector3D.</span></span> <span data-ttu-id="48d83-439">Ориентация камеры.</span><span class="sxs-lookup"><span data-stu-id="48d83-439">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-440">ориентатионангле</span><span class="sxs-lookup"><span data-stu-id="48d83-440">OrientationAngle</span></span></td>
<td><span data-ttu-id="48d83-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">Вганглеиндегрис</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="48d83-442">Угол между ориентацией камеры и плоскости XY.</span><span class="sxs-lookup"><span data-stu-id="48d83-442">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-443">Плоскости</span><span class="sxs-lookup"><span data-stu-id="48d83-443">Plane</span></span></td>
<td><span data-ttu-id="48d83-444">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="48d83-444">Vg3DExtrudePlane.</span></span> <span data-ttu-id="48d83-445">Позволяет проделать объемы от плоскостей ортогональной плоскости экрана.</span><span class="sxs-lookup"><span data-stu-id="48d83-445">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="48d83-446">Требуется указать Форедепс и depth в единицах рисования вместо емус.</span><span class="sxs-lookup"><span data-stu-id="48d83-446">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="48d83-447">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-447">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-448">ТОЧЕЧ</span><span class="sxs-lookup"><span data-stu-id="48d83-448">XY</span></span></li>
<li><span data-ttu-id="48d83-449">зкс</span><span class="sxs-lookup"><span data-stu-id="48d83-449">ZX</span></span></li>
<li><span data-ttu-id="48d83-450">из</span><span class="sxs-lookup"><span data-stu-id="48d83-450">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-451">Render</span><span class="sxs-lookup"><span data-stu-id="48d83-451">Render</span></span></td>
<td><span data-ttu-id="48d83-452">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="48d83-452">Vg3DRenderMode.</span></span> <span data-ttu-id="48d83-453">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-453">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-454">Solid (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-454">Solid (default)</span></span></li>
<li><span data-ttu-id="48d83-455">Каркасной модели</span><span class="sxs-lookup"><span data-stu-id="48d83-455">WireFrame</span></span></li>
<li><span data-ttu-id="48d83-456">баундингкубе</span><span class="sxs-lookup"><span data-stu-id="48d83-456">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-457">RotationAngle (Угол поворота)</span><span class="sxs-lookup"><span data-stu-id="48d83-457">RotationAngle</span></span></td>
<td><span data-ttu-id="48d83-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="48d83-459">AngleX, Angle или Англез управляются атрибутом Шаперотатион.</span><span class="sxs-lookup"><span data-stu-id="48d83-459">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-460">ротатионцентер</span><span class="sxs-lookup"><span data-stu-id="48d83-460">RotationCenter</span></span></td>
<td><span data-ttu-id="48d83-461">Объект.</span><span class="sxs-lookup"><span data-stu-id="48d83-461">Vector3D.</span></span> <span data-ttu-id="48d83-462">Центр вращения.</span><span class="sxs-lookup"><span data-stu-id="48d83-462">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-463">Коэффициента блеска</span><span class="sxs-lookup"><span data-stu-id="48d83-463">Shininess</span></span></td>
<td><span data-ttu-id="48d83-464"><a href="#data-types-used-in-the-vml-object-model">Вгпоситивенумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="48d83-465">Определяет, как работает зеркальное отражение Concentrated или распределения.</span><span class="sxs-lookup"><span data-stu-id="48d83-465">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="48d83-466">Высокое значение будет равно 8 – 10 и приблизительно равно зеркалу, а низкое значение — от 2 до 3 и приблизительно секуинед одежда.</span><span class="sxs-lookup"><span data-stu-id="48d83-466">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="48d83-467">Рекомендуется использовать значения от 3 до 7.</span><span class="sxs-lookup"><span data-stu-id="48d83-467">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="48d83-468">При высоком значении будут отражаться источники освещения.</span><span class="sxs-lookup"><span data-stu-id="48d83-468">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-469">скевамт</span><span class="sxs-lookup"><span data-stu-id="48d83-469">SkewAmt</span></span></td>
<td><span data-ttu-id="48d83-470"><a href="#data-types-used-in-the-vml-object-model">Вгперцентаже</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="48d83-471">Если тип — Parallel, атрибут определяет величину наклона.</span><span class="sxs-lookup"><span data-stu-id="48d83-471">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="48d83-472">В диапазоне от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="48d83-472">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-473">скевангле</span><span class="sxs-lookup"><span data-stu-id="48d83-473">SkewAngle</span></span></td>
<td><span data-ttu-id="48d83-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">Вганглеиндегрис</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="48d83-475">Если тип — Parallel, атрибут определяет степень наклона.</span><span class="sxs-lookup"><span data-stu-id="48d83-475">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="48d83-476">Значение по умолчанию — &quot; 45 &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-476">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-477">Отраженность</span><span class="sxs-lookup"><span data-stu-id="48d83-477">Specularity</span></span></td>
<td><span data-ttu-id="48d83-478"><a href="#data-types-used-in-the-vml-object-model">Вгпоситивенумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="48d83-479">Отношение инцидента к отраженно отраженному свету.</span><span class="sxs-lookup"><span data-stu-id="48d83-479">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="48d83-480">Значения меньше 1,0 являются нормальными, но значения, превышающие один, могут создавать интересные эффекты.</span><span class="sxs-lookup"><span data-stu-id="48d83-480">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-481">Тип</span><span class="sxs-lookup"><span data-stu-id="48d83-481">Type</span></span></td>
<td><span data-ttu-id="48d83-482">Вжекструсионтипе.</span><span class="sxs-lookup"><span data-stu-id="48d83-482">VgExtrusionType.</span></span> <span data-ttu-id="48d83-483">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-483">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-484">Parallel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-484">Parallel (default)</span></span></li>
<li><span data-ttu-id="48d83-485">Перспектива</span><span class="sxs-lookup"><span data-stu-id="48d83-485">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-486">Окна</span><span class="sxs-lookup"><span data-stu-id="48d83-486">Viewpoint</span></span></td>
<td><span data-ttu-id="48d83-487">Объект.</span><span class="sxs-lookup"><span data-stu-id="48d83-487">Vector3D.</span></span> <span data-ttu-id="48d83-488">Точка, из которой просматривается сцена.</span><span class="sxs-lookup"><span data-stu-id="48d83-488">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-489">виевпоинторигин</span><span class="sxs-lookup"><span data-stu-id="48d83-489">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="48d83-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="48d83-491">Могут иметь значения от 0,5 до-0,5 для позиционирования источника точки зрения в ограничивающем прямоугольнике фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-491">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="48d83-492">Fill, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-492">Fill element</span></span>

<span data-ttu-id="48d83-493">Описывает, как должен быть заполнен контур для заливки более сложным, чем сплошной цвет.</span><span class="sxs-lookup"><span data-stu-id="48d83-493">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="48d83-494">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="48d83-494">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-495">алигншапе</span><span class="sxs-lookup"><span data-stu-id="48d83-495">AlignShape</span></span></td>
<td><span data-ttu-id="48d83-496"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-497">Выровняйте изображение с фигурой.</span><span class="sxs-lookup"><span data-stu-id="48d83-497">Align the image with the shape.</span></span> <span data-ttu-id="48d83-498">Если значение равно false, выровняйте изображение с помощью окна.</span><span class="sxs-lookup"><span data-stu-id="48d83-498">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-499">Angle</span><span class="sxs-lookup"><span data-stu-id="48d83-499">Angle</span></span></td>
<td><span data-ttu-id="48d83-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">Вганглеиндегрис</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="48d83-501">Угол, вдоль которого переходит градиент.</span><span class="sxs-lookup"><span data-stu-id="48d83-501">The angle along which the gradient goes.</span></span> <span data-ttu-id="48d83-502">0 градусов находится вдоль горизонтальной оси слева направо.</span><span class="sxs-lookup"><span data-stu-id="48d83-502">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-503">Аспект</span><span class="sxs-lookup"><span data-stu-id="48d83-503">Aspect</span></span></td>
<td><span data-ttu-id="48d83-504"><strong>Вгаспекттипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-504"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="48d83-505">Атрибут ImageSize будет скорректирован для сохранения аспекта изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-505">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="48d83-506">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="48d83-506">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="48d83-507">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-507">Value</span></span></th>
<th><span data-ttu-id="48d83-508">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-508">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-509">Игнорировать</span><span class="sxs-lookup"><span data-stu-id="48d83-509">Ignore</span></span></td>
<td><span data-ttu-id="48d83-510">Пропускать проблемы с аспектами.</span><span class="sxs-lookup"><span data-stu-id="48d83-510">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-511">Задать</span><span class="sxs-lookup"><span data-stu-id="48d83-511">AtLeast</span></span></td>
<td><span data-ttu-id="48d83-512">Размер изображения не меньше размера изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-512">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-513">атмост</span><span class="sxs-lookup"><span data-stu-id="48d83-513">AtMost</span></span></td>
<td><span data-ttu-id="48d83-514">Изображение не превышает размер изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-514">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-515">Цвет</span><span class="sxs-lookup"><span data-stu-id="48d83-515">Color</span></span></td>
<td><span data-ttu-id="48d83-516"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a> Основной цвет заливки.</span><span class="sxs-lookup"><span data-stu-id="48d83-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="48d83-517">То же, что и атрибут FillColor в фигуре.</span><span class="sxs-lookup"><span data-stu-id="48d83-517">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-518">Color2</span><span class="sxs-lookup"><span data-stu-id="48d83-518">Color2</span></span></td>
<td><span data-ttu-id="48d83-519"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="48d83-520">Вторичный цвет заливки, если тип изображения — Pattern или градиентная заливка.</span><span class="sxs-lookup"><span data-stu-id="48d83-520">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-521">Цвета</span><span class="sxs-lookup"><span data-stu-id="48d83-521">Colors</span></span></td>
<td><span data-ttu-id="48d83-522"><a href="#data-types-used-in-the-vml-object-model">Ивгградиентколораррай</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="48d83-523">Промежуточные цвета в градиенте и их относительные позиции вдоль градиента, например, &quot; 30% красного, 70% голубого, 90% зеленого цвета &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-523">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="48d83-524">Основной цвет (атрибут цвета в фигуре) равен 0% и вторичному цвету (атрибут color2) равен 100%.</span><span class="sxs-lookup"><span data-stu-id="48d83-524">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-525">Фокус</span><span class="sxs-lookup"><span data-stu-id="48d83-525">Focus</span></span></td>
<td><span data-ttu-id="48d83-526"><a href="#data-types-used-in-the-vml-object-model">Вгсигнедперцентаже</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="48d83-527">Фокальная точка для линейной градиентной заливки.</span><span class="sxs-lookup"><span data-stu-id="48d83-527">Focal point for linear gradient fill.</span></span> <span data-ttu-id="48d83-528">Значения переходят от-100 до + 100.</span><span class="sxs-lookup"><span data-stu-id="48d83-528">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-529">фокуспоситион</span><span class="sxs-lookup"><span data-stu-id="48d83-529">FocusPosition</span></span></td>
<td><span data-ttu-id="48d83-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="48d83-531">Позиция самого внутреннего прямоугольника для радиальных градиентов.</span><span class="sxs-lookup"><span data-stu-id="48d83-531">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="48d83-532">Вектор представляет собой дробную часть (0,0-1,0) ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-532">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-533">фокуссизе</span><span class="sxs-lookup"><span data-stu-id="48d83-533">FocusSize</span></span></td>
<td><span data-ttu-id="48d83-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Размер самого внутреннего прямоугольника для радиальных градиентов.</span><span class="sxs-lookup"><span data-stu-id="48d83-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="48d83-535">Вектор представляет собой дробную часть (0,0 – 1,0) ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-535">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-536">Метод</span><span class="sxs-lookup"><span data-stu-id="48d83-536">Method</span></span></td>
<td><span data-ttu-id="48d83-537">Вгсигматипе.</span><span class="sxs-lookup"><span data-stu-id="48d83-537">VgSigmaType.</span></span> <span data-ttu-id="48d83-538">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="48d83-538">Values include:</span></span>
<ul>
<li><span data-ttu-id="48d83-539">Нет</span><span class="sxs-lookup"><span data-stu-id="48d83-539">None</span></span></li>
<li><span data-ttu-id="48d83-540">Линейная</span><span class="sxs-lookup"><span data-stu-id="48d83-540">Linear</span></span></li>
<li><span data-ttu-id="48d83-541">Sigma</span><span class="sxs-lookup"><span data-stu-id="48d83-541">Sigma</span></span></li>
<li><span data-ttu-id="48d83-542">Любой</span><span class="sxs-lookup"><span data-stu-id="48d83-542">Any</span></span></li>
</ul>
<p><span data-ttu-id="48d83-543">Значение по умолчанию — Сигма.</span><span class="sxs-lookup"><span data-stu-id="48d83-543">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-544">Включено</span><span class="sxs-lookup"><span data-stu-id="48d83-544">On</span></span></td>
<td><span data-ttu-id="48d83-545"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-546">Включает отображение экрана.</span><span class="sxs-lookup"><span data-stu-id="48d83-546">Turns fill display on.</span></span> <span data-ttu-id="48d83-547">То же, что и атрибут Fill в Shape.</span><span class="sxs-lookup"><span data-stu-id="48d83-547">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-548">Непрозрачность</span><span class="sxs-lookup"><span data-stu-id="48d83-548">Opacity</span></span></td>
<td><span data-ttu-id="48d83-549"><a href="msdn-online-vml-vgfraction-data-type.md">Вгфрактион</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="48d83-550">Непрозрачность заливки.</span><span class="sxs-lookup"><span data-stu-id="48d83-550">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-551">Opacity2</span><span class="sxs-lookup"><span data-stu-id="48d83-551">Opacity2</span></span></td>
<td><span data-ttu-id="48d83-552"><a href="msdn-online-vml-vgfraction-data-type.md">Вгфрактион</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="48d83-553">Дополнительная непрозрачность для градиентов.</span><span class="sxs-lookup"><span data-stu-id="48d83-553">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-554">Исходный домен</span><span class="sxs-lookup"><span data-stu-id="48d83-554">Origin</span></span></td>
<td><span data-ttu-id="48d83-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="48d83-556">Точка относительно левого верхнего угла изображения, которое обрабатывается как источник изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-556">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="48d83-557">По умолчанию используется центр изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-557">Default is the center of the image.</span></span> <span data-ttu-id="48d83-558">Вектор представляет собой дробную часть (от 0,0 до 1,0) ширины и высоты изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-558">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-559">Положение</span><span class="sxs-lookup"><span data-stu-id="48d83-559">Position</span></span></td>
<td><span data-ttu-id="48d83-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="48d83-561">Наведите указатель на ссылочный прямоугольник фигуры, чтобы разместить точку начала изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-561">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="48d83-562">По умолчанию используется центр прямоугольника контейнера.</span><span class="sxs-lookup"><span data-stu-id="48d83-562">Default is the center of the container rectangle.</span></span> <span data-ttu-id="48d83-563">Вектор представляет собой дробную часть (0,0-1,0) ширины и высоты изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-563">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-564">Размер</span><span class="sxs-lookup"><span data-stu-id="48d83-564">Size</span></span></td>
<td><span data-ttu-id="48d83-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="48d83-566">Размер изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-566">The size of the image.</span></span> <span data-ttu-id="48d83-567">Значение по умолчанию — размер изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="48d83-567">Default is pixel size of the image.</span></span> <span data-ttu-id="48d83-568">Может указываться в абсолютных координатах или в процентах.</span><span class="sxs-lookup"><span data-stu-id="48d83-568">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-569">Источник</span><span class="sxs-lookup"><span data-stu-id="48d83-569">Src</span></span></td>
<td><span data-ttu-id="48d83-570"><a href="#data-types-used-in-the-vml-object-model">Строка</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-570"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="48d83-571">URL-адрес изображения, загружаемого для изображений и узорных заливок.</span><span class="sxs-lookup"><span data-stu-id="48d83-571">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="48d83-572">Этот атрибут всегда должен присутствовать и указывать на допустимые данные изображения для отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-572">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-573">Тип</span><span class="sxs-lookup"><span data-stu-id="48d83-573">Type</span></span></td>
<td><span data-ttu-id="48d83-574">Вгфиллтипе.</span><span class="sxs-lookup"><span data-stu-id="48d83-574">VgFillType.</span></span> <span data-ttu-id="48d83-575">Принимается один из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="48d83-575">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="48d83-576">Историческая справка</span><span class="sxs-lookup"><span data-stu-id="48d83-576">Background</span></span></li>
<li><span data-ttu-id="48d83-577">Frame</span><span class="sxs-lookup"><span data-stu-id="48d83-577">Frame</span></span></li>
<li><span data-ttu-id="48d83-578">Градиент</span><span class="sxs-lookup"><span data-stu-id="48d83-578">Gradient</span></span></li>
<li><span data-ttu-id="48d83-579">градиентцентер</span><span class="sxs-lookup"><span data-stu-id="48d83-579">GradientCenter</span></span></li>
<li><span data-ttu-id="48d83-580">градиентрадиал</span><span class="sxs-lookup"><span data-stu-id="48d83-580">GradientRadial</span></span></li>
<li><span data-ttu-id="48d83-581">градиенттитле</span><span class="sxs-lookup"><span data-stu-id="48d83-581">GradientTitle</span></span></li>
<li><span data-ttu-id="48d83-582">градиентунскалед</span><span class="sxs-lookup"><span data-stu-id="48d83-582">GradientUnscaled</span></span></li>
<li><span data-ttu-id="48d83-583">Модель</span><span class="sxs-lookup"><span data-stu-id="48d83-583">Pattern</span></span></li>
<li><span data-ttu-id="48d83-584">Сплошная</span><span class="sxs-lookup"><span data-stu-id="48d83-584">Solid</span></span></li>
<li><span data-ttu-id="48d83-585">Tile</span><span class="sxs-lookup"><span data-stu-id="48d83-585">Tile</span></span></li>
</ul>
<span data-ttu-id="48d83-586">Для плитки, шаблона и фрейма необходимо предоставить атрибуты изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-586">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="48d83-587">Для градиента и Градиентрадиал требуется предоставить атрибуты градиента.</span><span class="sxs-lookup"><span data-stu-id="48d83-587">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="48d83-588">Group, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-588">Group element</span></span>

<span data-ttu-id="48d83-589">Группа — это коллекция отдельных фигур, которые могут быть размещены и преобразованы как единое целое.</span><span class="sxs-lookup"><span data-stu-id="48d83-589">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-590">Элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-590">Item</span></span>   | <span data-ttu-id="48d83-591">[Ивгшапе](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-592">Указанный элемент в массиве фигур.</span><span class="sxs-lookup"><span data-stu-id="48d83-592">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="48d83-593">Длина</span><span class="sxs-lookup"><span data-stu-id="48d83-593">Length</span></span> | <span data-ttu-id="48d83-594">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-594">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-595">Число фигур в этой группе.</span><span class="sxs-lookup"><span data-stu-id="48d83-595">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="48d83-596">Имажедата, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-596">Imagedata element</span></span>

<span data-ttu-id="48d83-597">Описывает изображение, которое подготавливается к просмотру поверх фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-597">Describes a picture to be rendered on top of a shape.</span></span>



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-598">билевел</span><span class="sxs-lookup"><span data-stu-id="48d83-598">BiLevel</span></span>     | <span data-ttu-id="48d83-599">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-599">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-600">Отображать изображение только в двух цветах (обычно это черно-белое).</span><span class="sxs-lookup"><span data-stu-id="48d83-600">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="48d83-601">блакклевел</span><span class="sxs-lookup"><span data-stu-id="48d83-601">BlackLevel</span></span>  | <span data-ttu-id="48d83-602">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="48d83-603">Позволяет настроить уровень, чтобы черный цвет отображался как истинный черный, а все остальные цвета отображались как оттенки выше черного цвета.</span><span class="sxs-lookup"><span data-stu-id="48d83-603">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="48d83-604">чромакэй</span><span class="sxs-lookup"><span data-stu-id="48d83-604">Chromakey</span></span>   | <span data-ttu-id="48d83-605">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="48d83-606">Прозрачный цвет изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-606">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="48d83-607">кропботтом</span><span class="sxs-lookup"><span data-stu-id="48d83-607">CropBottom</span></span>  | <span data-ttu-id="48d83-608">[Вгнумбер](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-609">Обрезать расстояние от нижней границы изображения в процентах от размера изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-609">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="48d83-610">кроплефт</span><span class="sxs-lookup"><span data-stu-id="48d83-610">CropLeft</span></span>    | <span data-ttu-id="48d83-611">[Вгнумбер](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-612">Обрезка расстояния от левого края изображения, выраженного в виде доли размера изображения (от 0,0 до 1,0).</span><span class="sxs-lookup"><span data-stu-id="48d83-612">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="48d83-613">Однако поддерживается «out-кадрирование», поэтому поддерживаются значения меньше 0 и больше 1. Например,-5, 20 — обрезать границы, 25X размер изображения с 4/5 на одной стороне изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-613">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="48d83-614">кропригхт</span><span class="sxs-lookup"><span data-stu-id="48d83-614">CropRight</span></span>   | <span data-ttu-id="48d83-615">[Вгнумбер](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-616">Обрезать расстояние справа от рисунка, выраженное в процентах от размера изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-616">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="48d83-617">кроптоп</span><span class="sxs-lookup"><span data-stu-id="48d83-617">CropTop</span></span>     | <span data-ttu-id="48d83-618">[Вгнумбер](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-619">Обрезать расстояние от верхнего края изображения, выраженное в процентах от размера изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-619">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="48d83-620">ембоссколор</span><span class="sxs-lookup"><span data-stu-id="48d83-620">EmbossColor</span></span> | <span data-ttu-id="48d83-621">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="48d83-622">Это значение задается в процентах от цвета тени для создания эффекта рельефного изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-622">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="48d83-623">Выигрыш</span><span class="sxs-lookup"><span data-stu-id="48d83-623">Gain</span></span>        | <span data-ttu-id="48d83-624">[Вгпоситивенумбер](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-625">Корректирует интенсивность всех цветов.</span><span class="sxs-lookup"><span data-stu-id="48d83-625">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="48d83-626">По сути, определяет, насколько ярко будет белый цвет.</span><span class="sxs-lookup"><span data-stu-id="48d83-626">Essentially sets how bright white will be.</span></span> <span data-ttu-id="48d83-627">В диапазоне от 0 до 32767.</span><span class="sxs-lookup"><span data-stu-id="48d83-627">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="48d83-628">Gamma</span><span class="sxs-lookup"><span data-stu-id="48d83-628">Gamma</span></span>       | <span data-ttu-id="48d83-629">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="48d83-630">Гамма-коррекция.</span><span class="sxs-lookup"><span data-stu-id="48d83-630">Gamma correction.</span></span> <span data-ttu-id="48d83-631">Увеличение этого числа повышает контрастность изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-631">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="48d83-632">GrayScale</span><span class="sxs-lookup"><span data-stu-id="48d83-632">GrayScale</span></span>   | <span data-ttu-id="48d83-633">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-633">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-634">Отображать изображение в оттенках серого.</span><span class="sxs-lookup"><span data-stu-id="48d83-634">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="48d83-635">Источник</span><span class="sxs-lookup"><span data-stu-id="48d83-635">Src</span></span>         | <span data-ttu-id="48d83-636">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-636">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-637">URL-адрес изображения, загружаемого для изображений и узорных заливок.</span><span class="sxs-lookup"><span data-stu-id="48d83-637">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="48d83-638">Этот атрибут всегда должен присутствовать и указывать на допустимые данные изображения для отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-638">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="48d83-639">Path, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-639">Path element</span></span>

<span data-ttu-id="48d83-640">Определяет путь, составляющий фигуру, с помощью строки, содержащей обширный набор команд "перемещение пером".</span><span class="sxs-lookup"><span data-stu-id="48d83-640">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-641">лимо</span><span class="sxs-lookup"><span data-stu-id="48d83-641">Limo</span></span></td>
<td><span data-ttu-id="48d83-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="48d83-643">Определяет точку растяжения фигуры. Например, для фигуры Giraffe точка Лимо будет находиться на горловине, поэтому при изменении размера фигуры объект горловина будет растянут, а оставшаяся часть фигуры сохранит свои размеры.</span><span class="sxs-lookup"><span data-stu-id="48d83-643">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-644">текстбоксрект</span><span class="sxs-lookup"><span data-stu-id="48d83-644">TextBoxRect</span></span></td>
<td><span data-ttu-id="48d83-645"><a href="#data-types-used-in-the-vml-object-model">Ивгфикседректанглеаррай</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="48d83-646">Массив, содержащий прямоугольники, определяющие, где должен идти текст.</span><span class="sxs-lookup"><span data-stu-id="48d83-646">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-647">V</span><span class="sxs-lookup"><span data-stu-id="48d83-647">V</span></span></td>
<td><span data-ttu-id="48d83-648"><a href="#data-types-used-in-the-vml-object-model">Строка</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-648"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="48d83-649">Соответствует атрибуту v в теге Path.</span><span class="sxs-lookup"><span data-stu-id="48d83-649">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="48d83-650">Обратите внимание, что путь может соответствовать атрибуту или элементу Path.</span><span class="sxs-lookup"><span data-stu-id="48d83-650">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-651">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-651">Value</span></span></td>
<td><span data-ttu-id="48d83-652"><a href="#data-types-used-in-the-vml-object-model">Строка</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-652"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="48d83-653">Текстовое представление команд, определяющих путь.</span><span class="sxs-lookup"><span data-stu-id="48d83-653">A text representation of the commands that define the path.</span></span> <span data-ttu-id="48d83-654">Значения координат X или y могут быть ссылкой на формулу в форме &quot; @# &quot; , где # — это порядковый номер формулы, например &quot; @2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-654">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="48d83-655">Эта строка атрибута состоит из обширного набора команд, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="48d83-655">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="48d83-656">Get-Help</span><span class="sxs-lookup"><span data-stu-id="48d83-656">Command</span></span></th>
<th><span data-ttu-id="48d83-657">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-657">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-658">AE (англиллипсето)</span><span class="sxs-lookup"><span data-stu-id="48d83-658">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="48d83-659"><strong>центрированный</strong>(x, y) <strong>Размер</strong>(w, h) <strong>начальный угол</strong>, <strong>конечный угол</strong></span><span class="sxs-lookup"><span data-stu-id="48d83-659"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="48d83-660">Нарисуйте сегмент эллипса.</span><span class="sxs-lookup"><span data-stu-id="48d83-660">Draw a segment of an ellipse.</span></span> <span data-ttu-id="48d83-661">Прямая линия рисуется от текущей точки к начальной точке сегмента.</span><span class="sxs-lookup"><span data-stu-id="48d83-661">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-662">Al (англилипсе)</span><span class="sxs-lookup"><span data-stu-id="48d83-662">al (angleelipse)</span></span></td>
<td><span data-ttu-id="48d83-663">То же, что и AE, за исключением того, что в начальную точку сегмента присутствует подразумеваемое значение m.</span><span class="sxs-lookup"><span data-stu-id="48d83-663">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-664">AR (Дуга)</span><span class="sxs-lookup"><span data-stu-id="48d83-664">ar (arc)</span></span></td>
<td><span data-ttu-id="48d83-665">То же, что и в.</span><span class="sxs-lookup"><span data-stu-id="48d83-665">Same as at.</span></span> <span data-ttu-id="48d83-666">Однако новый вложенный путь начинается неявным m в начальной точке дуги.</span><span class="sxs-lookup"><span data-stu-id="48d83-666">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-667">в (аркто)</span><span class="sxs-lookup"><span data-stu-id="48d83-667">at (arcto)</span></span></td>
<td><span data-ttu-id="48d83-668"><strong>слева</strong>, <strong>сверху</strong>, <strong>справа</strong>, <strong>снизу</strong>, <strong>Начало</strong>(x, y), <strong>конец</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="48d83-668"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="48d83-669">Первые четыре значения определяют ограничивающий прямоугольник эллипса.</span><span class="sxs-lookup"><span data-stu-id="48d83-669">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="48d83-670">Последние четыре определяют два радиальных вектора.</span><span class="sxs-lookup"><span data-stu-id="48d83-670">The last four define two radial vectors.</span></span> <span data-ttu-id="48d83-671">Рисуется сегмент эллипса, который начинается с угла, определенного начальным вектором, и заканчивается на угол, определенный конечным вектором.</span><span class="sxs-lookup"><span data-stu-id="48d83-671">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="48d83-672">Прямая линия рисуется от текущей точки до начала дуги. Дуга всегда отображается в направлении против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="48d83-672">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-673">c (курвето)</span><span class="sxs-lookup"><span data-stu-id="48d83-673">c (curveto)</span></span></td>
<td><span data-ttu-id="48d83-674"><strong>Control1</strong>(x, y) <strong>control2</strong>(x, y) <strong>к</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="48d83-674"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="48d83-675">Рисование кривой Безье третьего порядка от текущей точки до координат, заданных последними двумя параметрами, контрольные точки, заданные первыми четырьмя параметрами.</span><span class="sxs-lookup"><span data-stu-id="48d83-675">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="48d83-676">Текущая точка преобразуется в конечную точку Безье.</span><span class="sxs-lookup"><span data-stu-id="48d83-676">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-677">e (конец)</span><span class="sxs-lookup"><span data-stu-id="48d83-677">e (end)</span></span></td>
<td><span data-ttu-id="48d83-678">Завершение текущего набора вложенных путей.</span><span class="sxs-lookup"><span data-stu-id="48d83-678">End the current set of subpaths.</span></span> <span data-ttu-id="48d83-679">Заданный набор вложенных путей (разделенных End) заполняется с помощью еофилл.</span><span class="sxs-lookup"><span data-stu-id="48d83-679">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="48d83-680">Последующие наборы вложенных путей заполняются независимо друг от друга и накладываются на существующие.</span><span class="sxs-lookup"><span data-stu-id="48d83-680">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-681">l (lineTo)</span><span class="sxs-lookup"><span data-stu-id="48d83-681">l (lineto)</span></span></td>
<td><span data-ttu-id="48d83-682">x, y</span><span class="sxs-lookup"><span data-stu-id="48d83-682">x,y</span></span><br/> <span data-ttu-id="48d83-683">Нарисуйте линию от текущей точки до заданной координаты x, y, которая станет новой текущей точкой.</span><span class="sxs-lookup"><span data-stu-id="48d83-683">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="48d83-684">Для формирования ломаной линии можно указать дополнительные пары координат, например &quot; l 10, 13, 45, 27, 89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-684">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-685">m (MoveTo)</span><span class="sxs-lookup"><span data-stu-id="48d83-685">m (moveto)</span></span></td>
<td><span data-ttu-id="48d83-686">x, y</span><span class="sxs-lookup"><span data-stu-id="48d83-686">x,y</span></span><br/> <span data-ttu-id="48d83-687">Запуск нового вложенного пути в заданной координате x, y.</span><span class="sxs-lookup"><span data-stu-id="48d83-687">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-688">NF (без заливки)</span><span class="sxs-lookup"><span data-stu-id="48d83-688">nf (nofill)</span></span></td>
<td><span data-ttu-id="48d83-689">Текущий набор вложенных путей (разделенных End) не будет заполнен.</span><span class="sxs-lookup"><span data-stu-id="48d83-689">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-690">NS (Stroke)</span><span class="sxs-lookup"><span data-stu-id="48d83-690">ns (nostroke)</span></span></td>
<td><span data-ttu-id="48d83-691">Текущий набор вложенных путей (разделенных End) не будет обводкой.</span><span class="sxs-lookup"><span data-stu-id="48d83-691">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-692">QB (куадратикбезиер)</span><span class="sxs-lookup"><span data-stu-id="48d83-692">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="48d83-693">(<strong>контролпоинт</strong>(x, y)) \*,<strong>End</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="48d83-693">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="48d83-694">Определяет одну или несколько кривых Безье второго типа с помощью контрольных точек и конечной точки.</span><span class="sxs-lookup"><span data-stu-id="48d83-694">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="48d83-695">Промежуточные (кривые) точки получаются путем интерполяции между последовательными контрольными точками, аналогичными шрифтам TrueType.</span><span class="sxs-lookup"><span data-stu-id="48d83-695">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="48d83-696">Вложенный путь не обязательно должен быть начальным, в этом случае вложенный контур закрывается, а последняя точка определяет начальную точку.</span><span class="sxs-lookup"><span data-stu-id="48d83-696">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-697">ККС (еллиптикалкуадранткс)</span><span class="sxs-lookup"><span data-stu-id="48d83-697">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="48d83-698"><strong>конец</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="48d83-698"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="48d83-699">Квартальный эллипс рисуется от текущей точки до заданной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="48d83-699">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="48d83-700">Первичный сегмент изначально отношения к линии, параллельной оси x; т. е. сегмент начинается горизонтально.</span><span class="sxs-lookup"><span data-stu-id="48d83-700">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-701">ки (еллиптикалкуадранти)</span><span class="sxs-lookup"><span data-stu-id="48d83-701">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="48d83-702"><strong>конец</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="48d83-702"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="48d83-703">То же, что и ККС, за исключением того, что эллиптический сегмент изначально отношения в линию, параллельную оси y; т. е. сегмент начинается по вертикали.</span><span class="sxs-lookup"><span data-stu-id="48d83-703">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-704">r (рлинето)</span><span class="sxs-lookup"><span data-stu-id="48d83-704">r (rlineto)</span></span></td>
<td><span data-ttu-id="48d83-705">x, y</span><span class="sxs-lookup"><span data-stu-id="48d83-705">x,y</span></span> <br/> <span data-ttu-id="48d83-706">Нарисуйте линию из текущей точки в относительную координату (кпкс + x, КПИ + y).</span><span class="sxs-lookup"><span data-stu-id="48d83-706">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="48d83-707">Если заданы дополнительные пары координат, каждая новая точка будет вычисляться относительно последней.</span><span class="sxs-lookup"><span data-stu-id="48d83-707">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-708">t (рмовето)</span><span class="sxs-lookup"><span data-stu-id="48d83-708">t (rmoveto)</span></span></td>
<td><span data-ttu-id="48d83-709">x, y</span><span class="sxs-lookup"><span data-stu-id="48d83-709">x,y</span></span><br/> <span data-ttu-id="48d83-710">Начать новый вложенный путь в относительных координатах (кпкс + x, КПИ + y), где кпкс, КПИ является текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="48d83-710">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-711">v (курвето)</span><span class="sxs-lookup"><span data-stu-id="48d83-711">v (curveto)</span></span></td>
<td><span data-ttu-id="48d83-712"><strong>Control1</strong>(x, y) <strong>control2</strong>(x, y) <strong>к</strong> (x, y)</span><span class="sxs-lookup"><span data-stu-id="48d83-712"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="48d83-713">Кривая Безье третьего порядка с заданными координатами относительно текущей точки.</span><span class="sxs-lookup"><span data-stu-id="48d83-713">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="48d83-714">Все точки вычисляются относительно одной и той же начальной точки.</span><span class="sxs-lookup"><span data-stu-id="48d83-714">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-715">WA (клокквисеаркто)</span><span class="sxs-lookup"><span data-stu-id="48d83-715">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="48d83-716">То же, что и, но дуга рисуется в направлении по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="48d83-716">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-717">WR (клокквисеарк)</span><span class="sxs-lookup"><span data-stu-id="48d83-717">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="48d83-718">То же, что и AR, но рисуется в направлении по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="48d83-718">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-719">x (закрытие)</span><span class="sxs-lookup"><span data-stu-id="48d83-719">x (close)</span></span></td>
<td><span data-ttu-id="48d83-720">Закрытие текущего вложенного пути путем рисования прямой линии от текущей точки до исходной точки MoveTo.</span><span class="sxs-lookup"><span data-stu-id="48d83-720">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="48d83-721">Элемент Shadow</span><span class="sxs-lookup"><span data-stu-id="48d83-721">Shadow element</span></span>

<span data-ttu-id="48d83-722">Описывает эффект тени на фигуре.</span><span class="sxs-lookup"><span data-stu-id="48d83-722">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-723">Цвет</span><span class="sxs-lookup"><span data-stu-id="48d83-723">Color</span></span></td>
<td><span data-ttu-id="48d83-724"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="48d83-725">Цвет основной тени.</span><span class="sxs-lookup"><span data-stu-id="48d83-725">Color of the primary shadow.</span></span> <span data-ttu-id="48d83-726">Значение по умолчанию — RGB (128128128)</span><span class="sxs-lookup"><span data-stu-id="48d83-726">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-727">Color2</span><span class="sxs-lookup"><span data-stu-id="48d83-727">Color2</span></span></td>
<td><span data-ttu-id="48d83-728"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="48d83-729">Цвет второй тени или выделенный фрагмент с рельефной или утопленной тенью.</span><span class="sxs-lookup"><span data-stu-id="48d83-729">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="48d83-730">Значение по умолчанию — RGB (203203203).</span><span class="sxs-lookup"><span data-stu-id="48d83-730">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-731">Матрица</span><span class="sxs-lookup"><span data-stu-id="48d83-731">Matrix</span></span></td>
<td><span data-ttu-id="48d83-732"><a href="#data-types-used-in-the-vml-object-model">Ивгскевматрикс</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="48d83-733">Матрица преобразования перспективы в форме, &quot; скскс, СКСИ, Сикс, сии, px, корректировка &quot; [s = масштаб, p = перспектива].</span><span class="sxs-lookup"><span data-stu-id="48d83-733">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="48d83-734">Элементы s определяют, как тень должна масштабироваться относительно фигуры, а элементы p определяют, как тень должна отклоняться относительно фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-734">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="48d83-735">Например, следующая матрица изменяет размер фигуры на коэффициент, равный 2, и наклоняет его на множитель 4 во всех направлениях.</span><span class="sxs-lookup"><span data-stu-id="48d83-735">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="48d83-736">&quot;2, 2, 2, 2, 4, 4&quot;</span><span class="sxs-lookup"><span data-stu-id="48d83-736">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="48d83-737">Эта матрица используется только в том случае, если для тени задан тип "Перспектива".</span><span class="sxs-lookup"><span data-stu-id="48d83-737">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-738">Неясными</span><span class="sxs-lookup"><span data-stu-id="48d83-738">Obscured</span></span></td>
<td><span data-ttu-id="48d83-739"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-740">Тень может быть видна, если фигура не заполнена.</span><span class="sxs-lookup"><span data-stu-id="48d83-740">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="48d83-741">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="48d83-741">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-742">Offset</span><span class="sxs-lookup"><span data-stu-id="48d83-742">Offset</span></span></td>
<td><span data-ttu-id="48d83-743"><a href="#data-types-used-in-the-vml-object-model">Ивгскевоффсет</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="48d83-744">Величина смещения x, y от расположения фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-744">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="48d83-745">Значение по умолчанию — &quot; 2pt, 2PT &quot; .</span><span class="sxs-lookup"><span data-stu-id="48d83-745">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-746">Offset2</span><span class="sxs-lookup"><span data-stu-id="48d83-746">Offset2</span></span></td>
<td><span data-ttu-id="48d83-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="48d83-748">Величина смещения x, y секунд от расположения фигуры? s.</span><span class="sxs-lookup"><span data-stu-id="48d83-748">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="48d83-749">Значения — это либо абсолютное измерение, либо дробное значение Shape (от-0,5 до + 0,5).</span><span class="sxs-lookup"><span data-stu-id="48d83-749">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-750">Включено</span><span class="sxs-lookup"><span data-stu-id="48d83-750">On</span></span></td>
<td><span data-ttu-id="48d83-751"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-752">Включает и выключает отображение тени.</span><span class="sxs-lookup"><span data-stu-id="48d83-752">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-753">Непрозрачность</span><span class="sxs-lookup"><span data-stu-id="48d83-753">Opacity</span></span></td>
<td><span data-ttu-id="48d83-754"><a href="msdn-online-vml-vgfraction-data-type.md">Вгфрактион</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="48d83-755">Непрозрачность тени.</span><span class="sxs-lookup"><span data-stu-id="48d83-755">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-756">Исходный домен</span><span class="sxs-lookup"><span data-stu-id="48d83-756">Origin</span></span></td>
<td><span data-ttu-id="48d83-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Пара дробных значений Shape с-0,5 по + 0,5.</span><span class="sxs-lookup"><span data-stu-id="48d83-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-758">Тип</span><span class="sxs-lookup"><span data-stu-id="48d83-758">Type</span></span></td>
<td><span data-ttu-id="48d83-759"><a href="#data-types-used-in-the-vml-object-model">Вгшадовтипе</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="48d83-760">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-760">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-761">Single (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-761">Single (default)</span></span></li>
<li><span data-ttu-id="48d83-762">Double</span><span class="sxs-lookup"><span data-stu-id="48d83-762">Double</span></span></li>
<li><span data-ttu-id="48d83-763">Перспектива</span><span class="sxs-lookup"><span data-stu-id="48d83-763">Perspective</span></span></li>
<li><span data-ttu-id="48d83-764">шаперелативе</span><span class="sxs-lookup"><span data-stu-id="48d83-764">ShapeRelative</span></span></li>
<li><span data-ttu-id="48d83-765">дравингрелативе</span><span class="sxs-lookup"><span data-stu-id="48d83-765">DrawingRelative</span></span></li>
<li><span data-ttu-id="48d83-766">Emboss</span><span class="sxs-lookup"><span data-stu-id="48d83-766">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="48d83-767">Элемент асимметрии</span><span class="sxs-lookup"><span data-stu-id="48d83-767">Skew element</span></span>

<span data-ttu-id="48d83-768">Описывает эффекты наклона перспективы на фигуре.</span><span class="sxs-lookup"><span data-stu-id="48d83-768">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="48d83-769">Наклон применяется к векторным графическим данным, а не к данным изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-769">The skew is applied to vector graphic data, not image data.</span></span>



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-770">Матрица</span><span class="sxs-lookup"><span data-stu-id="48d83-770">Matrix</span></span> | <span data-ttu-id="48d83-771">[Ивгскевматрикс](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-772">Матрица преобразования перспективы в форме "скскс, СКСИ, Сикс, сии, px, корректировка" \[ s = масштаб, p = перспектива " \] .</span><span class="sxs-lookup"><span data-stu-id="48d83-772">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="48d83-773">Если значение offset в абсолютных единицах, то px, корректировка производится в ЕС ^-1 единиц; в противном случае это обратная часть размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-773">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="48d83-774">Offset</span><span class="sxs-lookup"><span data-stu-id="48d83-774">Offset</span></span> | <span data-ttu-id="48d83-775">[Ивгскевоффсет](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-776">Величина смещения x, y от расположения фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-776">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="48d83-777">Значение по умолчанию — "2PT, 2PT".</span><span class="sxs-lookup"><span data-stu-id="48d83-777">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="48d83-778">Включено</span><span class="sxs-lookup"><span data-stu-id="48d83-778">On</span></span>     | <span data-ttu-id="48d83-779">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-779">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-780">Включает или выключает отображение наклона.</span><span class="sxs-lookup"><span data-stu-id="48d83-780">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="48d83-781">Исходный домен</span><span class="sxs-lookup"><span data-stu-id="48d83-781">Origin</span></span> | <span data-ttu-id="48d83-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="48d83-783">Пара дробных значений Shape с-0,5 по + 0,5.</span><span class="sxs-lookup"><span data-stu-id="48d83-783">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="48d83-784">Элемент Stroke</span><span class="sxs-lookup"><span data-stu-id="48d83-784">Stroke element</span></span>

<span data-ttu-id="48d83-785">Описывает, как нарисовать контур, если требуется нечто за сплошной линией с сплошным цветом.</span><span class="sxs-lookup"><span data-stu-id="48d83-785">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-786">Цвет</span><span class="sxs-lookup"><span data-stu-id="48d83-786">Color</span></span></td>
<td><span data-ttu-id="48d83-787"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-788">Цвет линии.</span><span class="sxs-lookup"><span data-stu-id="48d83-788">The color of the line.</span></span> <span data-ttu-id="48d83-789">Аналогичен атрибуту Строкеколор в фигуре, но переопределяет его.</span><span class="sxs-lookup"><span data-stu-id="48d83-789">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-790">Color2</span><span class="sxs-lookup"><span data-stu-id="48d83-790">Color2</span></span></td>
<td><span data-ttu-id="48d83-791"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="48d83-792">Вторичный цвет.</span><span class="sxs-lookup"><span data-stu-id="48d83-792">Secondary color.</span></span> <span data-ttu-id="48d83-793">Используется, если объекта FillType является шаблоном.</span><span class="sxs-lookup"><span data-stu-id="48d83-793">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-794">DashStyle</span><span class="sxs-lookup"><span data-stu-id="48d83-794">DashStyle</span></span></td>
<td><span data-ttu-id="48d83-795"><strong>Вглинедашстиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-795"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="48d83-796">Формат пунктирного стиля.</span><span class="sxs-lookup"><span data-stu-id="48d83-796">Dash style format.</span></span> <span data-ttu-id="48d83-797">Может представлять собой конкретное значение или последовательность чисел с определяемым пользователем шаблоном штриха.</span><span class="sxs-lookup"><span data-stu-id="48d83-797">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="48d83-798">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-798">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-799">Solid (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-799">Solid (default)</span></span></li>
<li><span data-ttu-id="48d83-800">шортдаш</span><span class="sxs-lookup"><span data-stu-id="48d83-800">ShortDash</span></span></li>
<li><span data-ttu-id="48d83-801">шортдот</span><span class="sxs-lookup"><span data-stu-id="48d83-801">ShortDot</span></span></li>
<li><span data-ttu-id="48d83-802">шортдашдот</span><span class="sxs-lookup"><span data-stu-id="48d83-802">ShortDashDot</span></span></li>
<li><span data-ttu-id="48d83-803">шортдашдотдот</span><span class="sxs-lookup"><span data-stu-id="48d83-803">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="48d83-804">Точки</span><span class="sxs-lookup"><span data-stu-id="48d83-804">Dot</span></span></li>
<li><span data-ttu-id="48d83-805">Штрих</span><span class="sxs-lookup"><span data-stu-id="48d83-805">Dash</span></span></li>
<li><span data-ttu-id="48d83-806">DashDot</span><span class="sxs-lookup"><span data-stu-id="48d83-806">DashDot</span></span></li>
<li><span data-ttu-id="48d83-807">лонгдаш</span><span class="sxs-lookup"><span data-stu-id="48d83-807">LongDash</span></span></li>
<li><span data-ttu-id="48d83-808">лонгдашдот</span><span class="sxs-lookup"><span data-stu-id="48d83-808">LongDashDot</span></span></li>
<li><span data-ttu-id="48d83-809">лонгдашдотдот</span><span class="sxs-lookup"><span data-stu-id="48d83-809">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-810">ендарров</span><span class="sxs-lookup"><span data-stu-id="48d83-810">EndArrow</span></span></td>
<td><span data-ttu-id="48d83-811"><strong>Вгарровхеадстиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-811"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="48d83-812">Стрелка для конца строки.</span><span class="sxs-lookup"><span data-stu-id="48d83-812">Arrowhead for the end of the line.</span></span> <span data-ttu-id="48d83-813">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-813">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-814">Нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-814">None (default)</span></span></li>
<li><span data-ttu-id="48d83-815">Блокировать</span><span class="sxs-lookup"><span data-stu-id="48d83-815">Block</span></span></li>
<li><span data-ttu-id="48d83-816">Классический</span><span class="sxs-lookup"><span data-stu-id="48d83-816">Classic</span></span></li>
<li><span data-ttu-id="48d83-817">Ромб</span><span class="sxs-lookup"><span data-stu-id="48d83-817">Diamond</span></span></li>
<li><span data-ttu-id="48d83-818">Овал</span><span class="sxs-lookup"><span data-stu-id="48d83-818">Oval</span></span></li>
<li><span data-ttu-id="48d83-819">Открыть</span><span class="sxs-lookup"><span data-stu-id="48d83-819">Open</span></span></li>
<li><span data-ttu-id="48d83-820">Шеврон</span><span class="sxs-lookup"><span data-stu-id="48d83-820">Chevron</span></span></li>
<li><span data-ttu-id="48d83-821">даублечеврон</span><span class="sxs-lookup"><span data-stu-id="48d83-821">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-822">ендарровленгс</span><span class="sxs-lookup"><span data-stu-id="48d83-822">EndArrowLength</span></span></td>
<td><span data-ttu-id="48d83-823"><strong>Вгарровхеадленгс</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-823"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="48d83-824">Длина наконечника для конца строки.</span><span class="sxs-lookup"><span data-stu-id="48d83-824">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="48d83-825">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-825">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-826">Short</span><span class="sxs-lookup"><span data-stu-id="48d83-826">Short</span></span></li>
<li><span data-ttu-id="48d83-827">Среднее (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-827">Medium (default)</span></span></li>
<li><span data-ttu-id="48d83-828">Long</span><span class="sxs-lookup"><span data-stu-id="48d83-828">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-829">ендарроввидс</span><span class="sxs-lookup"><span data-stu-id="48d83-829">EndArrowWidth</span></span></td>
<td><span data-ttu-id="48d83-830"><strong>Вгарровхеадвидс</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-830"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="48d83-831">Ширина наконечника для конца строки.</span><span class="sxs-lookup"><span data-stu-id="48d83-831">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="48d83-832">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-832">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-833">Разрабатываем</span><span class="sxs-lookup"><span data-stu-id="48d83-833">Narrow</span></span></li>
<li><span data-ttu-id="48d83-834">Среднее (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-834">Medium (default)</span></span></li>
<li><span data-ttu-id="48d83-835">Широкий</span><span class="sxs-lookup"><span data-stu-id="48d83-835">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-836">ендкап</span><span class="sxs-lookup"><span data-stu-id="48d83-836">EndCap</span></span></td>
<td><span data-ttu-id="48d83-837"><strong>Вглининдкапстиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-837"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="48d83-838">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-838">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-839">плоский</span><span class="sxs-lookup"><span data-stu-id="48d83-839">Flat</span></span></li>
<li><span data-ttu-id="48d83-840">Square</span><span class="sxs-lookup"><span data-stu-id="48d83-840">Square</span></span></li>
<li><span data-ttu-id="48d83-841">Round</span><span class="sxs-lookup"><span data-stu-id="48d83-841">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-842">Объекта FillType</span><span class="sxs-lookup"><span data-stu-id="48d83-842">FillType</span></span></td>
<td><span data-ttu-id="48d83-843"><strong>Вглинефиллтипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-843"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="48d83-844">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-844">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-845">Solid (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-845">Solid (default)</span></span></li>
<li><span data-ttu-id="48d83-846">Tile</span><span class="sxs-lookup"><span data-stu-id="48d83-846">Tile</span></span></li>
<li><span data-ttu-id="48d83-847">Модель</span><span class="sxs-lookup"><span data-stu-id="48d83-847">Pattern</span></span></li>
<li><span data-ttu-id="48d83-848">Frame</span><span class="sxs-lookup"><span data-stu-id="48d83-848">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-849">имажеалигншапе</span><span class="sxs-lookup"><span data-stu-id="48d83-849">ImageAlignShape</span></span></td>
<td><span data-ttu-id="48d83-850"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-851">Выровняйте изображение с фигурой.</span><span class="sxs-lookup"><span data-stu-id="48d83-851">Align the image with the shape.</span></span> <span data-ttu-id="48d83-852">Если значение равно false, выровняйте изображение с помощью окна.</span><span class="sxs-lookup"><span data-stu-id="48d83-852">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-853">имажеаспект</span><span class="sxs-lookup"><span data-stu-id="48d83-853">ImageAspect</span></span></td>
<td><span data-ttu-id="48d83-854"><strong>Вгаспекттипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-854"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="48d83-855">Атрибут ImageSize будет скорректирован для сохранения аспекта изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-855">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="48d83-856">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="48d83-856">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="48d83-857">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-857">Value</span></span></th>
<th><span data-ttu-id="48d83-858">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-858">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-859">Игнорировать</span><span class="sxs-lookup"><span data-stu-id="48d83-859">Ignore</span></span></td>
<td><span data-ttu-id="48d83-860">Пропускать проблемы с аспектами.</span><span class="sxs-lookup"><span data-stu-id="48d83-860">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-861">Задать</span><span class="sxs-lookup"><span data-stu-id="48d83-861">AtLeast</span></span></td>
<td><span data-ttu-id="48d83-862">Размер изображения не меньше размера изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-862">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-863">атмост</span><span class="sxs-lookup"><span data-stu-id="48d83-863">AtMost</span></span></td>
<td><span data-ttu-id="48d83-864">Изображение не превышает размер изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-864">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-865">ImageSize</span><span class="sxs-lookup"><span data-stu-id="48d83-865">ImageSize</span></span></td>
<td><span data-ttu-id="48d83-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="48d83-867">Размер изображения для формирования кисти.</span><span class="sxs-lookup"><span data-stu-id="48d83-867">Size of the image to form the brush with.</span></span> <span data-ttu-id="48d83-868">Значение по умолчанию — размер образа.</span><span class="sxs-lookup"><span data-stu-id="48d83-868">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-869">жоинстиле</span><span class="sxs-lookup"><span data-stu-id="48d83-869">JoinStyle</span></span></td>
<td><span data-ttu-id="48d83-870"><strong>Вглинежоинстиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-870"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="48d83-871">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-871">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-872">Round (скругленное соединение)</span><span class="sxs-lookup"><span data-stu-id="48d83-872">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="48d83-873">Багетная рамка (Багетная стыка)</span><span class="sxs-lookup"><span data-stu-id="48d83-873">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="48d83-874">Угловой (угловой стык)</span><span class="sxs-lookup"><span data-stu-id="48d83-874">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-875">линестиле</span><span class="sxs-lookup"><span data-stu-id="48d83-875">LineStyle</span></span></td>
<td><span data-ttu-id="48d83-876"><strong>Вглинестиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-876"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="48d83-877">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-877">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-878">Single</span><span class="sxs-lookup"><span data-stu-id="48d83-878">Single</span></span></li>
<li><span data-ttu-id="48d83-879">Синсин (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="48d83-879">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="48d83-880">Синсикк (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="48d83-880">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="48d83-881">Сикксин (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="48d83-881">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="48d83-882">Сиккбетвинсин (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="48d83-882">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-883">митерлимит</span><span class="sxs-lookup"><span data-stu-id="48d83-883">MiterLimit</span></span></td>
<td><span data-ttu-id="48d83-884"><a href="msdn-online-vml-vglength.md">Длина</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-884"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="48d83-885">Максимальное расстояние между внутренней точкой и внешней точкой соединения.</span><span class="sxs-lookup"><span data-stu-id="48d83-885">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="48d83-886">Это число является кратным ширине линии.</span><span class="sxs-lookup"><span data-stu-id="48d83-886">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="48d83-887">В диапазоне от 0 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="48d83-887">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-888">Включено</span><span class="sxs-lookup"><span data-stu-id="48d83-888">On</span></span></td>
<td><span data-ttu-id="48d83-889"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="48d83-890">Включает и выключает отображение линии.</span><span class="sxs-lookup"><span data-stu-id="48d83-890">Turns the display of the line on and off.</span></span> <span data-ttu-id="48d83-891">Аналогичен атрибуту Stroke в фигуре, но переопределяет его.</span><span class="sxs-lookup"><span data-stu-id="48d83-891">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-892">Непрозрачность</span><span class="sxs-lookup"><span data-stu-id="48d83-892">Opacity</span></span></td>
<td><span data-ttu-id="48d83-893"><a href="msdn-online-vml-vgfraction-data-type.md">Вгфрактион</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="48d83-894">Непрозрачность штриха.</span><span class="sxs-lookup"><span data-stu-id="48d83-894">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-895">Источник</span><span class="sxs-lookup"><span data-stu-id="48d83-895">Src</span></span></td>
<td><span data-ttu-id="48d83-896">Строка.</span><span class="sxs-lookup"><span data-stu-id="48d83-896">String.</span></span> <span data-ttu-id="48d83-897">URL-адрес изображения, загружаемого для изображений и узорных заливок.</span><span class="sxs-lookup"><span data-stu-id="48d83-897">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="48d83-898">Этот атрибут всегда должен присутствовать и указывать на допустимые данные изображения для отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="48d83-898">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-899">стартарров</span><span class="sxs-lookup"><span data-stu-id="48d83-899">StartArrow</span></span></td>
<td><span data-ttu-id="48d83-900"><strong>Вгарровхеадстиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-900"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="48d83-901">Стрелка для начала строки.</span><span class="sxs-lookup"><span data-stu-id="48d83-901">Arrowhead for the start of the line.</span></span> <span data-ttu-id="48d83-902">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-902">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-903">Нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-903">None (default)</span></span></li>
<li><span data-ttu-id="48d83-904">Блокировать</span><span class="sxs-lookup"><span data-stu-id="48d83-904">Block</span></span></li>
<li><span data-ttu-id="48d83-905">Классический</span><span class="sxs-lookup"><span data-stu-id="48d83-905">Classic</span></span></li>
<li><span data-ttu-id="48d83-906">Ромб</span><span class="sxs-lookup"><span data-stu-id="48d83-906">Diamond</span></span></li>
<li><span data-ttu-id="48d83-907">Овал</span><span class="sxs-lookup"><span data-stu-id="48d83-907">Oval</span></span></li>
<li><span data-ttu-id="48d83-908">Открыть</span><span class="sxs-lookup"><span data-stu-id="48d83-908">Open</span></span></li>
<li><span data-ttu-id="48d83-909">Шеврон</span><span class="sxs-lookup"><span data-stu-id="48d83-909">Chevron</span></span></li>
<li><span data-ttu-id="48d83-910">даублечеврон</span><span class="sxs-lookup"><span data-stu-id="48d83-910">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-911">стартарровленгс</span><span class="sxs-lookup"><span data-stu-id="48d83-911">StartArrowLength</span></span></td>
<td><span data-ttu-id="48d83-912">Вгарровхеадленгс.</span><span class="sxs-lookup"><span data-stu-id="48d83-912">VgArrowHeadLength.</span></span> <span data-ttu-id="48d83-913">Длина наконечника для начала строки.</span><span class="sxs-lookup"><span data-stu-id="48d83-913">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="48d83-914">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-914">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-915">Short</span><span class="sxs-lookup"><span data-stu-id="48d83-915">Short</span></span></li>
<li><span data-ttu-id="48d83-916">Среднее (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48d83-916">Medium (default)</span></span></li>
<li><span data-ttu-id="48d83-917">Long</span><span class="sxs-lookup"><span data-stu-id="48d83-917">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-918">стартарроввидс</span><span class="sxs-lookup"><span data-stu-id="48d83-918">StartArrowWidth</span></span></td>
<td><span data-ttu-id="48d83-919">Вгарровхеадвидс.</span><span class="sxs-lookup"><span data-stu-id="48d83-919">VgArrowheadWidth.</span></span> <span data-ttu-id="48d83-920">Ширина стрелки для начала строки.</span><span class="sxs-lookup"><span data-stu-id="48d83-920">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="48d83-921">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-921">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-922">Узкий средний (по умолчанию) широкий</span><span class="sxs-lookup"><span data-stu-id="48d83-922">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-923">Вес</span><span class="sxs-lookup"><span data-stu-id="48d83-923">Weight</span></span></td>
<td><span data-ttu-id="48d83-924"><a href="msdn-online-vml-vglength.md">Вгленгс</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="48d83-925">Ширина линии.</span><span class="sxs-lookup"><span data-stu-id="48d83-925">Width of line.</span></span> <span data-ttu-id="48d83-926">В диапазоне от 0 до 1584.</span><span class="sxs-lookup"><span data-stu-id="48d83-926">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="48d83-927">Атрибут DashStyle позволяет пользователю указать пользовательский шаблон штриха.</span><span class="sxs-lookup"><span data-stu-id="48d83-927">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="48d83-928">Это делается с помощью ряда чисел.</span><span class="sxs-lookup"><span data-stu-id="48d83-928">This is done using a series of numbers.</span></span> <span data-ttu-id="48d83-929">Стили штриха определяются с точки зрения длины тире (рисуемой части штриха) и длины пробела между тире.</span><span class="sxs-lookup"><span data-stu-id="48d83-929">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="48d83-930">Длины задаются относительно ширины линии; Длина &quot; 1 &quot; равна ширине линии.</span><span class="sxs-lookup"><span data-stu-id="48d83-930">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="48d83-931">К каждому штриху применяется стиль Ендкап, а стили стрелок — нет.</span><span class="sxs-lookup"><span data-stu-id="48d83-931">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="48d83-932">Строка сначала определяет длину тире, а затем длину пробела.</span><span class="sxs-lookup"><span data-stu-id="48d83-932">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="48d83-933">Это может повторяться для формирования сложных стилей штрихов.</span><span class="sxs-lookup"><span data-stu-id="48d83-933">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="48d83-934">Строка всегда должна содержать пару цифр. Если оно содержит нечетное число чисел, Последнее может быть не учитывается.</span><span class="sxs-lookup"><span data-stu-id="48d83-934">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="48d83-935">В следующей таблице перечислены некоторые типичные значения и описание предполагаемого воздействия.</span><span class="sxs-lookup"><span data-stu-id="48d83-935">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="48d83-936">&quot;0 &quot; означает, что точка должна быть фаурфолд симметричной (с круглым ендкапс, она должна быть круговой).</span><span class="sxs-lookup"><span data-stu-id="48d83-936">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="48d83-937">Если строка ендкап плоская, средство просмотра должно выбрать по возможности встроенный штрих по операционной системе (т. е. быстро нарисовать).</span><span class="sxs-lookup"><span data-stu-id="48d83-937">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="48d83-938">Ниже приведены некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="48d83-938">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-939">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="48d83-939">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="48d83-940">короткие дефисы (каждое тире и расстояние между ними вдвое больше ширины строки)</span><span class="sxs-lookup"><span data-stu-id="48d83-940">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-941">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="48d83-941">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="48d83-942">точка (каждое тире является шириной строки, а каждое пространство вдвое равно ширине строки)</span><span class="sxs-lookup"><span data-stu-id="48d83-942">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-943">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="48d83-943">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="48d83-944">тире (каждое тире в четыре раза превышает ширину строки, тогда как каждое пространство вдвое равно ширине строки)</span><span class="sxs-lookup"><span data-stu-id="48d83-944">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-945">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="48d83-945">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="48d83-946">длинное тире</span><span class="sxs-lookup"><span data-stu-id="48d83-946">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-947">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="48d83-947">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="48d83-948">тире, точка</span><span class="sxs-lookup"><span data-stu-id="48d83-948">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-949">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="48d83-949">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="48d83-950">длинное тире, точка</span><span class="sxs-lookup"><span data-stu-id="48d83-950">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-951">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="48d83-951">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="48d83-952">длинное тире-пунктирная точка</span><span class="sxs-lookup"><span data-stu-id="48d83-952">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="48d83-953">Текстпас, элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-953">TextPath element</span></span>

<span data-ttu-id="48d83-954">Описывает Векторный путь на основе предоставляемых текстовых данных, шрифта и стилей.</span><span class="sxs-lookup"><span data-stu-id="48d83-954">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="48d83-955">Текстовый путь деформации, чтобы соответствовать элементу **пути** , если он указан.</span><span class="sxs-lookup"><span data-stu-id="48d83-955">The text path is warped to conform to a **Path** element if supplied.</span></span>



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-956">фитпас</span><span class="sxs-lookup"><span data-stu-id="48d83-956">FitPath</span></span>  | <span data-ttu-id="48d83-957">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-957">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-958">Изменяет размер текста для заполнения пути, на котором он находится.</span><span class="sxs-lookup"><span data-stu-id="48d83-958">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="48d83-959">фитшапе</span><span class="sxs-lookup"><span data-stu-id="48d83-959">FitShape</span></span> | <span data-ttu-id="48d83-960">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-960">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-961">Растягивает текстовый контур до границ поля фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-961">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="48d83-962">Включено</span><span class="sxs-lookup"><span data-stu-id="48d83-962">On</span></span>       | <span data-ttu-id="48d83-963">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-963">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-964">Определяет, отображаются ли пути к символам.</span><span class="sxs-lookup"><span data-stu-id="48d83-964">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="48d83-965">Строка</span><span class="sxs-lookup"><span data-stu-id="48d83-965">String</span></span>   | <span data-ttu-id="48d83-966">Строка.</span><span class="sxs-lookup"><span data-stu-id="48d83-966">String.</span></span> <span data-ttu-id="48d83-967">Текст, отображаемый в виде текстового пути.</span><span class="sxs-lookup"><span data-stu-id="48d83-967">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="48d83-968">Trim</span><span class="sxs-lookup"><span data-stu-id="48d83-968">Trim</span></span>     | <span data-ttu-id="48d83-969">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-969">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-970">Удаляет все дополнительные пространства, зарезервированные для верхних и нижних колонтитулов, если не используется.</span><span class="sxs-lookup"><span data-stu-id="48d83-970">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="48d83-971">®</span><span class="sxs-lookup"><span data-stu-id="48d83-971">XScale</span></span>   | <span data-ttu-id="48d83-972">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-972">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-973">Используйте непосредственное измерение x вместо измерения вдоль пути.</span><span class="sxs-lookup"><span data-stu-id="48d83-973">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="48d83-974">Типы данных, используемые в объектной модели VML</span><span class="sxs-lookup"><span data-stu-id="48d83-974">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="48d83-975">Объектная модель VML использует следующие типы данных.</span><span class="sxs-lookup"><span data-stu-id="48d83-975">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="48d83-976">Double</span><span class="sxs-lookup"><span data-stu-id="48d83-976">Double</span></span>](/windows)
-   [<span data-ttu-id="48d83-977">Фиксированный формат</span><span class="sxs-lookup"><span data-stu-id="48d83-977">Fixed</span></span>](/windows)
-   [<span data-ttu-id="48d83-978">Integer</span><span class="sxs-lookup"><span data-stu-id="48d83-978">Integer</span></span>](/windows)
-   [<span data-ttu-id="48d83-979">ивгаджустментс</span><span class="sxs-lookup"><span data-stu-id="48d83-979">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="48d83-980">ивгколор</span><span class="sxs-lookup"><span data-stu-id="48d83-980">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="48d83-981">ивжекуатион</span><span class="sxs-lookup"><span data-stu-id="48d83-981">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="48d83-982">ивгфикседректангле</span><span class="sxs-lookup"><span data-stu-id="48d83-982">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="48d83-983">ивгфикседректанглеаррай</span><span class="sxs-lookup"><span data-stu-id="48d83-983">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="48d83-984">ивгформула</span><span class="sxs-lookup"><span data-stu-id="48d83-984">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="48d83-985">ивгформулас</span><span class="sxs-lookup"><span data-stu-id="48d83-985">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="48d83-986">ивгградиентколораррай</span><span class="sxs-lookup"><span data-stu-id="48d83-986">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="48d83-987">ивгпоинтс</span><span class="sxs-lookup"><span data-stu-id="48d83-987">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="48d83-988">ивгскевматрикс</span><span class="sxs-lookup"><span data-stu-id="48d83-988">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="48d83-989">ивгскевоффсет</span><span class="sxs-lookup"><span data-stu-id="48d83-989">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="48d83-990">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="48d83-990">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="48d83-991">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="48d83-991">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="48d83-992">Длина</span><span class="sxs-lookup"><span data-stu-id="48d83-992">Length</span></span>](/windows)
-   [<span data-ttu-id="48d83-993">Measure</span><span class="sxs-lookup"><span data-stu-id="48d83-993">Measure</span></span>](/windows)
-   [<span data-ttu-id="48d83-994">String</span><span class="sxs-lookup"><span data-stu-id="48d83-994">String</span></span>](/windows)
-   [<span data-ttu-id="48d83-995">вгблакквхитемоде</span><span class="sxs-lookup"><span data-stu-id="48d83-995">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="48d83-996">вгфрактион</span><span class="sxs-lookup"><span data-stu-id="48d83-996">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="48d83-997">вгтристате</span><span class="sxs-lookup"><span data-stu-id="48d83-997">VgTriState</span></span>](/windows)

<span data-ttu-id="48d83-998">**Тип данных Double**</span><span class="sxs-lookup"><span data-stu-id="48d83-998">**Double data type**</span></span>

<span data-ttu-id="48d83-999">Целое число двойной точности с диапазоном от-Infinity до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="48d83-999">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="48d83-1000">**Фиксированный тип данных**</span><span class="sxs-lookup"><span data-stu-id="48d83-1000">**Fixed data type**</span></span>

<span data-ttu-id="48d83-1001">Число с плавающей запятой с диапазоном от-32 766,0 до 32 766,0.</span><span class="sxs-lookup"><span data-stu-id="48d83-1001">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="48d83-1002">**Тип данных Integer**</span><span class="sxs-lookup"><span data-stu-id="48d83-1002">**Integer data type**</span></span>

<span data-ttu-id="48d83-1003">Целое число с диапазоном от-Infinity до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="48d83-1003">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="48d83-1004">**Тип данных Ивгаджустментс**</span><span class="sxs-lookup"><span data-stu-id="48d83-1004">**IVgAdjustments data type**</span></span>

<span data-ttu-id="48d83-1005">Коллекция корректировок для фигуры, которую можно использовать для изменения размеров фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-1005">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="48d83-1006">Корректировки можно использовать как временные заполнители или по любой причине для использования переменных.</span><span class="sxs-lookup"><span data-stu-id="48d83-1006">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="48d83-1007">В коллекции доступно только 8 корректировок.</span><span class="sxs-lookup"><span data-stu-id="48d83-1007">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="48d83-1008">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1008">Attributes</span></span> | <span data-ttu-id="48d83-1009">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1009">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-1010">Exists</span><span class="sxs-lookup"><span data-stu-id="48d83-1010">Exists</span></span>     | <span data-ttu-id="48d83-1011">[Ивгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="48d83-1012">Определяет, существует ли указанная корректировка.</span><span class="sxs-lookup"><span data-stu-id="48d83-1012">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="48d83-1013">Обратите внимание, что необходимо использовать индекс. то есть для получения существования элемента должен использоваться существующий (Item).</span><span class="sxs-lookup"><span data-stu-id="48d83-1013">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="48d83-1014">Элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-1014">Item</span></span>       | <span data-ttu-id="48d83-1015">[Длинное целое](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1015">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1016">Массив корректировок, индексируемых от 0 до 7.</span><span class="sxs-lookup"><span data-stu-id="48d83-1016">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="48d83-1017">Обратите внимание, что корректировки могут быть указаны с SPARC. то есть значения промежуточных массивов могут не всегда заполняться.</span><span class="sxs-lookup"><span data-stu-id="48d83-1017">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="48d83-1018">Например, элементы 1, 3 и 5 могут иметь значения длиной 3, для которых задан элемент (0), элемент (2) и элемент (4).</span><span class="sxs-lookup"><span data-stu-id="48d83-1018">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="48d83-1019">Чтобы узнать, существует ли элемент, используйте атрибут EXISTS.</span><span class="sxs-lookup"><span data-stu-id="48d83-1019">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="48d83-1020">Длина</span><span class="sxs-lookup"><span data-stu-id="48d83-1020">Length</span></span>     | <span data-ttu-id="48d83-1021">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1021">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1022">Число корректировок.</span><span class="sxs-lookup"><span data-stu-id="48d83-1022">Number of adjustments.</span></span> <span data-ttu-id="48d83-1023">Не может быть больше 8.</span><span class="sxs-lookup"><span data-stu-id="48d83-1023">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="48d83-1024">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-1024">Value</span></span>      | <span data-ttu-id="48d83-1025">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1025">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1026">Текстовое представление числовых значений с запятыми между каждым числом.</span><span class="sxs-lookup"><span data-stu-id="48d83-1026">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="48d83-1027">**ивгколор**</span><span class="sxs-lookup"><span data-stu-id="48d83-1027">**IVgColor**</span></span>

<span data-ttu-id="48d83-1028">Задает цвет.</span><span class="sxs-lookup"><span data-stu-id="48d83-1028">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48d83-1029">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1029">Attributes</span></span></th>
<th><span data-ttu-id="48d83-1030">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1030">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-1031">RGB</span><span class="sxs-lookup"><span data-stu-id="48d83-1031">RGB</span></span></td>
<td><span data-ttu-id="48d83-1032"><strong>Вгргбтипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1032"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="48d83-1033">Значение RGB (Long) цвета.</span><span class="sxs-lookup"><span data-stu-id="48d83-1033">RGB value (Long) of the color.</span></span> <span data-ttu-id="48d83-1034">Допустим только в том случае, если тип — RGB.</span><span class="sxs-lookup"><span data-stu-id="48d83-1034">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1035">R</span><span class="sxs-lookup"><span data-stu-id="48d83-1035">R</span></span></td>
<td><span data-ttu-id="48d83-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="48d83-1037">Красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="48d83-1037">Red component of the color.</span></span> <span data-ttu-id="48d83-1038">Может находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="48d83-1038">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1039">G</span><span class="sxs-lookup"><span data-stu-id="48d83-1039">G</span></span></td>
<td><span data-ttu-id="48d83-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="48d83-1041">Зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="48d83-1041">Green component of the color.</span></span> <span data-ttu-id="48d83-1042">Может находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="48d83-1042">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1043">B</span><span class="sxs-lookup"><span data-stu-id="48d83-1043">B</span></span></td>
<td><span data-ttu-id="48d83-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="48d83-1045">Синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="48d83-1045">Blue component of the color.</span></span> <span data-ttu-id="48d83-1046">Может находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="48d83-1046">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1047">Строка</span><span class="sxs-lookup"><span data-stu-id="48d83-1047">String</span></span></td>
<td><span data-ttu-id="48d83-1048"><a href="#data-types-used-in-the-vml-object-model">Строка</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1048"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="48d83-1049">Текстовое представление цвета.</span><span class="sxs-lookup"><span data-stu-id="48d83-1049">Text representation of the color.</span></span> <span data-ttu-id="48d83-1050">Поддерживаются следующие именованные типы цветов:</span><span class="sxs-lookup"><span data-stu-id="48d83-1050">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="48d83-1051">Черный (#000000)</span><span class="sxs-lookup"><span data-stu-id="48d83-1051">Black (#000000)</span></span></li>
<li><span data-ttu-id="48d83-1052">Серебро (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="48d83-1052">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="48d83-1053">Серый (#808080)</span><span class="sxs-lookup"><span data-stu-id="48d83-1053">Gray (#808080)</span></span></li>
<li><span data-ttu-id="48d83-1054">Белый (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="48d83-1054">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="48d83-1055">Каштановый (#800000)</span><span class="sxs-lookup"><span data-stu-id="48d83-1055">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="48d83-1056">Красный (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="48d83-1056">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="48d83-1057">Сиреневый (#800080)</span><span class="sxs-lookup"><span data-stu-id="48d83-1057">Purple (#800080)</span></span></li>
<li><span data-ttu-id="48d83-1058">Фучсиа (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="48d83-1058">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="48d83-1059">Зеленый (#008000)</span><span class="sxs-lookup"><span data-stu-id="48d83-1059">Green (#008000)</span></span></li>
<li><span data-ttu-id="48d83-1060">Травяной (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="48d83-1060">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="48d83-1061">Оливковый (#808000)</span><span class="sxs-lookup"><span data-stu-id="48d83-1061">Olive (#808000)</span></span></li>
<li><span data-ttu-id="48d83-1062">Желтый (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="48d83-1062">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="48d83-1063">ВМФ (#000080)</span><span class="sxs-lookup"><span data-stu-id="48d83-1063">Navy (#000080)</span></span></li>
<li><span data-ttu-id="48d83-1064">Синий (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="48d83-1064">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="48d83-1065">Бирюзовый (#008080)</span><span class="sxs-lookup"><span data-stu-id="48d83-1065">Teal (#008080)</span></span></li>
<li><span data-ttu-id="48d83-1066">Голубой (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="48d83-1066">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1067">Тип</span><span class="sxs-lookup"><span data-stu-id="48d83-1067">Type</span></span></td>
<td><span data-ttu-id="48d83-1068"><strong>Вгколортипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1068"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="48d83-1069">Тип цвета.</span><span class="sxs-lookup"><span data-stu-id="48d83-1069">Type of color.</span></span> <span data-ttu-id="48d83-1070">Один из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="48d83-1070">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="48d83-1071">Смешанный</span><span class="sxs-lookup"><span data-stu-id="48d83-1071">Mixed</span></span></li>
<li><span data-ttu-id="48d83-1072">именованная</span><span class="sxs-lookup"><span data-stu-id="48d83-1072">Named</span></span></li>
<li><span data-ttu-id="48d83-1073">RGB</span><span class="sxs-lookup"><span data-stu-id="48d83-1073">RGB</span></span></li>
<li><span data-ttu-id="48d83-1074">Схема</span><span class="sxs-lookup"><span data-stu-id="48d83-1074">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="48d83-1075">**ивжекуатион**</span><span class="sxs-lookup"><span data-stu-id="48d83-1075">**IVgEquation**</span></span>

<span data-ttu-id="48d83-1076">Формулы, используемые для формул.</span><span class="sxs-lookup"><span data-stu-id="48d83-1076">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-1077">Операция</span><span class="sxs-lookup"><span data-stu-id="48d83-1077">Operation</span></span></td>
<td><span data-ttu-id="48d83-1078"><strong>Вжекуатионоператионтипе</strong> Имя операции, выполняемой с параметрами.</span><span class="sxs-lookup"><span data-stu-id="48d83-1078"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="48d83-1079">В уравнении можно использовать следующие операции:</span><span class="sxs-lookup"><span data-stu-id="48d83-1079">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="48d83-1080">Операция</span><span class="sxs-lookup"><span data-stu-id="48d83-1080">Operation</span></span></th>
<th><span data-ttu-id="48d83-1081">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1081">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-1082">Abs</span><span class="sxs-lookup"><span data-stu-id="48d83-1082">Abs</span></span></td>
<td><span data-ttu-id="48d83-1083">Абсолютное значение.</span><span class="sxs-lookup"><span data-stu-id="48d83-1083">Absolute value.</span></span> <br/> <span data-ttu-id="48d83-1084"><strong>ABS</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="48d83-1084"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1085">Atan2</span><span class="sxs-lookup"><span data-stu-id="48d83-1085">Atan2</span></span></td>
<td><span data-ttu-id="48d83-1086">Полярная арифметика — результаты в единицах фильтра (градусы умножаются на 65536).</span><span class="sxs-lookup"><span data-stu-id="48d83-1086">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="48d83-1087"><strong>atan2</strong>(P1, v)</span><span class="sxs-lookup"><span data-stu-id="48d83-1087"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1088">Cos</span><span class="sxs-lookup"><span data-stu-id="48d83-1088">Cos</span></span></td>
<td><span data-ttu-id="48d83-1089">Косинус, аргумент в единицах демона (градусы, умноженные на 65536).</span><span class="sxs-lookup"><span data-stu-id="48d83-1089">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="48d83-1090">v \* <strong>COS</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="48d83-1090">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1091">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="48d83-1091">Cosatan2</span></span></td>
<td><span data-ttu-id="48d83-1092">Сохраняет полную точность в промежуточном вычислении.</span><span class="sxs-lookup"><span data-stu-id="48d83-1092">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="48d83-1093">v \* <strong>cos (atan2 (</strong> P2, P1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="48d83-1093">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1094">Эллипс</span><span class="sxs-lookup"><span data-stu-id="48d83-1094">Ellipse</span></span></td>
<td><span data-ttu-id="48d83-1095">Эллипс</span><span class="sxs-lookup"><span data-stu-id="48d83-1095">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1096">If</span><span class="sxs-lookup"><span data-stu-id="48d83-1096">If</span></span></td>
<td><span data-ttu-id="48d83-1097">If проверка условия.</span><span class="sxs-lookup"><span data-stu-id="48d83-1097">If Condition test.</span></span> <span data-ttu-id="48d83-1098">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="48d83-1098">v > 0 <strong>?</strong></span></span> <span data-ttu-id="48d83-1099">P1: P2</span><span class="sxs-lookup"><span data-stu-id="48d83-1099">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1100">Макс.</span><span class="sxs-lookup"><span data-stu-id="48d83-1100">Max</span></span></td>
<td><span data-ttu-id="48d83-1101">Большее из двух значений.</span><span class="sxs-lookup"><span data-stu-id="48d83-1101">The greater of two values.</span></span> <br/> <span data-ttu-id="48d83-1102"><strong>Max</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="48d83-1102"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1103">Mid</span><span class="sxs-lookup"><span data-stu-id="48d83-1103">Mid</span></span></td>
<td><span data-ttu-id="48d83-1104">Среднее (v + P1)/2</span><span class="sxs-lookup"><span data-stu-id="48d83-1104">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1105">Min</span><span class="sxs-lookup"><span data-stu-id="48d83-1105">Min</span></span></td>
<td><span data-ttu-id="48d83-1106">Меньшее из двух значений.</span><span class="sxs-lookup"><span data-stu-id="48d83-1106">The lesser of two values.</span></span> <span data-ttu-id="48d83-1107"><strong>min</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="48d83-1107"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1108">Mod</span><span class="sxs-lookup"><span data-stu-id="48d83-1108">Mod</span></span></td>
<td><span data-ttu-id="48d83-1109">Вычисление модуля.</span><span class="sxs-lookup"><span data-stu-id="48d83-1109">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1110">Продукт</span><span class="sxs-lookup"><span data-stu-id="48d83-1110">Product</span></span></td>
<td><span data-ttu-id="48d83-1111">Используется для умножения и деления.</span><span class="sxs-lookup"><span data-stu-id="48d83-1111">Used for multiplication and division.</span></span> <span data-ttu-id="48d83-1112">v \* P1/P2</span><span class="sxs-lookup"><span data-stu-id="48d83-1112">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1113">Sin</span><span class="sxs-lookup"><span data-stu-id="48d83-1113">Sin</span></span></td>
<td><span data-ttu-id="48d83-1114">Синус, аргумент в единицах фильтра (градусов, умноженный на 65536).</span><span class="sxs-lookup"><span data-stu-id="48d83-1114">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="48d83-1115">v \* <strong>sin</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="48d83-1115">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1116">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="48d83-1116">Sinatan2</span></span></td>
<td><span data-ttu-id="48d83-1117">Сохраняет полную точность в промежуточном вычислении.</span><span class="sxs-lookup"><span data-stu-id="48d83-1117">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="48d83-1118">v \* <strong>sin</strong>(<strong>atan2</strong>(P2, P1))</span><span class="sxs-lookup"><span data-stu-id="48d83-1118">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1119">Sqrt</span><span class="sxs-lookup"><span data-stu-id="48d83-1119">Sqrt</span></span></td>
<td><span data-ttu-id="48d83-1120">Результат является положительным и округляется вниз.</span><span class="sxs-lookup"><span data-stu-id="48d83-1120">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="48d83-1121"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="48d83-1121"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1122">SUM</span><span class="sxs-lookup"><span data-stu-id="48d83-1122">Sum</span></span></td>
<td><span data-ttu-id="48d83-1123">Используется для сложения и вычитания.</span><span class="sxs-lookup"><span data-stu-id="48d83-1123">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="48d83-1124">v + P1 P2</span><span class="sxs-lookup"><span data-stu-id="48d83-1124">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1125">сумангле</span><span class="sxs-lookup"><span data-stu-id="48d83-1125">Sumangle</span></span></td>
<td><span data-ttu-id="48d83-1126">Существующий угол (масштабируется на 65536), где P1 и P2 находятся в градусах.</span><span class="sxs-lookup"><span data-stu-id="48d83-1126">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="48d83-1127">v + P1 \* 65536 + P2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="48d83-1127">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1128">Tan</span><span class="sxs-lookup"><span data-stu-id="48d83-1128">Tan</span></span></td>
<td><span data-ttu-id="48d83-1129">Тангенс, аргумент находится в единицах демона (градусов, умноженные на 65536).</span><span class="sxs-lookup"><span data-stu-id="48d83-1129">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="48d83-1130">v \* Tan (P1)</span><span class="sxs-lookup"><span data-stu-id="48d83-1130">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1131">Val</span><span class="sxs-lookup"><span data-stu-id="48d83-1131">Val</span></span></td>
<td><span data-ttu-id="48d83-1132">Определяет значение Guide из другого значения.</span><span class="sxs-lookup"><span data-stu-id="48d83-1132">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1133">Параметр1</span><span class="sxs-lookup"><span data-stu-id="48d83-1133">Param1</span></span></td>
<td><span data-ttu-id="48d83-1134"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1134"><strong>Integer</strong>.</span></span> <span data-ttu-id="48d83-1135">Первый параметр.</span><span class="sxs-lookup"><span data-stu-id="48d83-1135">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1136">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="48d83-1136">Paramtype1</span></span></td>
<td><span data-ttu-id="48d83-1137"><strong>Вгформулапарамтипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1137"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="48d83-1138">Тип первого параметра.</span><span class="sxs-lookup"><span data-stu-id="48d83-1138">The type of the first parameter.</span></span> <span data-ttu-id="48d83-1139">Поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="48d83-1139">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="48d83-1140">Тип</span><span class="sxs-lookup"><span data-stu-id="48d83-1140">Type</span></span></th>
<th><span data-ttu-id="48d83-1141">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-1142">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-1142">Value</span></span></td>
<td><span data-ttu-id="48d83-1143">Параметр является простым значением.</span><span class="sxs-lookup"><span data-stu-id="48d83-1143">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1144">аджустментреференце</span><span class="sxs-lookup"><span data-stu-id="48d83-1144">AdjustmentReference</span></span></td>
<td><span data-ttu-id="48d83-1145">Параметр является ссылкой на корректировку.</span><span class="sxs-lookup"><span data-stu-id="48d83-1145">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="48d83-1146">Например, если первый параметр равен 1, будет использоваться значение первой корректировки.</span><span class="sxs-lookup"><span data-stu-id="48d83-1146">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1147">формулареференце</span><span class="sxs-lookup"><span data-stu-id="48d83-1147">FormulaReference</span></span></td>
<td><span data-ttu-id="48d83-1148">Параметр является результатом ссылки на результат предыдущей формулы.</span><span class="sxs-lookup"><span data-stu-id="48d83-1148">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="48d83-1149">Например, если первый параметр равен 2, будет использоваться результат формулы 2.</span><span class="sxs-lookup"><span data-stu-id="48d83-1149">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1150">Param2</span><span class="sxs-lookup"><span data-stu-id="48d83-1150">Param2</span></span></td>
<td><span data-ttu-id="48d83-1151"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1151"><strong>Integer</strong>.</span></span> <span data-ttu-id="48d83-1152">Второй параметр.</span><span class="sxs-lookup"><span data-stu-id="48d83-1152">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1153">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="48d83-1153">Paramtype2</span></span></td>
<td><span data-ttu-id="48d83-1154"><strong>Вгформулапарамтипе</strong> Тип параметра 2.</span><span class="sxs-lookup"><span data-stu-id="48d83-1154"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1155">Val</span><span class="sxs-lookup"><span data-stu-id="48d83-1155">Val</span></span></td>
<td><span data-ttu-id="48d83-1156"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1156"><strong>Integer</strong>.</span></span> <span data-ttu-id="48d83-1157">Результат.</span><span class="sxs-lookup"><span data-stu-id="48d83-1157">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1158">Valtype2</span><span class="sxs-lookup"><span data-stu-id="48d83-1158">Valtype2</span></span></td>
<td><span data-ttu-id="48d83-1159"><strong>Вгформулапарамтипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1159"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="48d83-1160">Тип результата.</span><span class="sxs-lookup"><span data-stu-id="48d83-1160">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="48d83-1161">**ивгфикседректангле**</span><span class="sxs-lookup"><span data-stu-id="48d83-1161">**IVgFixedRectangle**</span></span>

<span data-ttu-id="48d83-1162">Задает фиксированный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="48d83-1162">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="48d83-1163">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1163">Attributes</span></span> | <span data-ttu-id="48d83-1164">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1164">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-1165">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-1165">Value</span></span>      | <span data-ttu-id="48d83-1166">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1166">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1167">Текстовое значение, указывающее путь.</span><span class="sxs-lookup"><span data-stu-id="48d83-1167">Text value specifying the path.</span></span>         |
| <span data-ttu-id="48d83-1168">Левый</span><span class="sxs-lookup"><span data-stu-id="48d83-1168">Left</span></span>       | <span data-ttu-id="48d83-1169">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1169">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1170">Крайняя левая координата прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="48d83-1170">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="48d83-1171">Начало</span><span class="sxs-lookup"><span data-stu-id="48d83-1171">Top</span></span>        | <span data-ttu-id="48d83-1172">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1172">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1173">Самая верхняя координата прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="48d83-1173">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="48d83-1174">Правый</span><span class="sxs-lookup"><span data-stu-id="48d83-1174">Right</span></span>      | <span data-ttu-id="48d83-1175">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1175">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1176">Крайняя правая координата прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="48d83-1176">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="48d83-1177">Нижнее</span><span class="sxs-lookup"><span data-stu-id="48d83-1177">Bottom</span></span>     | <span data-ttu-id="48d83-1178">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1178">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1179">Самое нижнее координата прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="48d83-1179">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="48d83-1180">**ивгфикседректанглеаррай**</span><span class="sxs-lookup"><span data-stu-id="48d83-1180">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="48d83-1181">Массив фиксированных прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="48d83-1181">Array of fixed rectangles.</span></span>



| <span data-ttu-id="48d83-1182">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1182">Attributes</span></span> | <span data-ttu-id="48d83-1183">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1183">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-1184">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-1184">Value</span></span>      | <span data-ttu-id="48d83-1185">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1185">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1186">Текстовое представление массива.</span><span class="sxs-lookup"><span data-stu-id="48d83-1186">Text representation of array.</span></span>                           |
| <span data-ttu-id="48d83-1187">Длина</span><span class="sxs-lookup"><span data-stu-id="48d83-1187">Length</span></span>     | <span data-ttu-id="48d83-1188">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1188">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1189">Число прямоугольников в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="48d83-1189">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="48d83-1190">Элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-1190">Item</span></span>       | <span data-ttu-id="48d83-1191">[Ивгфикседректангле](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1192">Объект Rectangle по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="48d83-1192">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="48d83-1193">Тип данных **ивгформула**</span><span class="sxs-lookup"><span data-stu-id="48d83-1193">**IVgFormula** data type</span></span>

<span data-ttu-id="48d83-1194">Определения формул, которые могут варьировать путь к фигуре или использоваться для других вычислений.</span><span class="sxs-lookup"><span data-stu-id="48d83-1194">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="48d83-1195">Формулы могут основываться на атрибуте « **года** » фигуры, который может изменяться.</span><span class="sxs-lookup"><span data-stu-id="48d83-1195">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="48d83-1196">Формулы также могут ссылаться на другие формулы.</span><span class="sxs-lookup"><span data-stu-id="48d83-1196">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="48d83-1197">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1197">Attributes</span></span> | <span data-ttu-id="48d83-1198">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1198">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-1199">екн</span><span class="sxs-lookup"><span data-stu-id="48d83-1199">Eqn</span></span>        | <span data-ttu-id="48d83-1200">[Ивжекуатион](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1201">Каждая формула определяет одно значение в результате вычисления выражения.</span><span class="sxs-lookup"><span data-stu-id="48d83-1201">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="48d83-1202">Выражение определяется этим атрибутом и имеет общую форму операции, за которым следует до трех аргументов, которые могут быть значениями коррекции (например, \# 2), результатами предыдущих формул (например, @2 ), фиксированных чисел или предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="48d83-1202">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="48d83-1203">**Тип данных Ивгформулас**</span><span class="sxs-lookup"><span data-stu-id="48d83-1203">**IVgFormulas data type**</span></span>

<span data-ttu-id="48d83-1204">Коллекция объектов формулы.</span><span class="sxs-lookup"><span data-stu-id="48d83-1204">A collection of formula objects.</span></span>



| <span data-ttu-id="48d83-1205">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1205">Attributes</span></span> | <span data-ttu-id="48d83-1206">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1206">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-1207">Длина</span><span class="sxs-lookup"><span data-stu-id="48d83-1207">Length</span></span>     | <span data-ttu-id="48d83-1208">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1208">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1209">Число объектов формулы в коллекции.</span><span class="sxs-lookup"><span data-stu-id="48d83-1209">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="48d83-1210">Элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-1210">Item</span></span>       | <span data-ttu-id="48d83-1211">[Ивгформула](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1212">Определенная формула.</span><span class="sxs-lookup"><span data-stu-id="48d83-1212">A specific formula.</span></span> <span data-ttu-id="48d83-1213">Обратите внимание, что массив формул может наследоваться ФОМ типа Shape.</span><span class="sxs-lookup"><span data-stu-id="48d83-1213">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="48d83-1214">**ивгградиентколораррай**</span><span class="sxs-lookup"><span data-stu-id="48d83-1214">**IVgGradientColorArray**</span></span>

<span data-ttu-id="48d83-1215">Массив цветов, определяющий градиент (смешанный диапазон цветов).</span><span class="sxs-lookup"><span data-stu-id="48d83-1215">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="48d83-1216">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1216">Attributes</span></span> | <span data-ttu-id="48d83-1217">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1217">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-1218">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-1218">Value</span></span>      | <span data-ttu-id="48d83-1219">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1219">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1220">Задает массив цветов. Например, "Red. 2; зеленый. 4; черный. 7 "</span><span class="sxs-lookup"><span data-stu-id="48d83-1220">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="48d83-1221">Длина</span><span class="sxs-lookup"><span data-stu-id="48d83-1221">Length</span></span>     | <span data-ttu-id="48d83-1222">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1222">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1223">Число цветов в массиве.</span><span class="sxs-lookup"><span data-stu-id="48d83-1223">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="48d83-1224">Методы</span><span class="sxs-lookup"><span data-stu-id="48d83-1224">Methods</span></span>     | <span data-ttu-id="48d83-1225">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1225">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-1226">аддколор</span><span class="sxs-lookup"><span data-stu-id="48d83-1226">AddColor</span></span>    | <span data-ttu-id="48d83-1227">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="48d83-1228">Добавляет новый цвет в конечной точке, указанной в параметре дробь.</span><span class="sxs-lookup"><span data-stu-id="48d83-1228">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="48d83-1229">Новый цвет является белым по умолчанию и является возвращаемым значением.</span><span class="sxs-lookup"><span data-stu-id="48d83-1229">The new color is white by default and is the return value.</span></span> <span data-ttu-id="48d83-1230">Затем можно изменить цвет по ссылке.</span><span class="sxs-lookup"><span data-stu-id="48d83-1230">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="48d83-1231">ремовеколор</span><span class="sxs-lookup"><span data-stu-id="48d83-1231">RemoveColor</span></span> | <span data-ttu-id="48d83-1232">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="48d83-1233">Удаляет цвет в конечной точке, указанной в параметре дробь.</span><span class="sxs-lookup"><span data-stu-id="48d83-1233">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="48d83-1234">Примечание. Если 0,0 или 1,0 не существует, подразумевается, а в этой точке используется белый цвет.</span><span class="sxs-lookup"><span data-stu-id="48d83-1234">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="48d83-1235">**Тип данных Ивгпоинтс**</span><span class="sxs-lookup"><span data-stu-id="48d83-1235">**IVgPoints datatype**</span></span>

<span data-ttu-id="48d83-1236">Массив точек, определяющих фигуру.</span><span class="sxs-lookup"><span data-stu-id="48d83-1236">Array of points that define a shape.</span></span>



| <span data-ttu-id="48d83-1237">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1237">Attributes</span></span> | <span data-ttu-id="48d83-1238">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1238">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d83-1239">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-1239">Value</span></span>      | <span data-ttu-id="48d83-1240">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1240">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1241">Текстовое представление массива.</span><span class="sxs-lookup"><span data-stu-id="48d83-1241">Text representation of array.</span></span>           |
| <span data-ttu-id="48d83-1242">Длина</span><span class="sxs-lookup"><span data-stu-id="48d83-1242">Length</span></span>     | <span data-ttu-id="48d83-1243">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1243">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="48d83-1244">Число точек в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="48d83-1244">Number of points in this array.</span></span>        |
| <span data-ttu-id="48d83-1245">Элемент</span><span class="sxs-lookup"><span data-stu-id="48d83-1245">Item</span></span>       | <span data-ttu-id="48d83-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="48d83-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="48d83-1247">Точка по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="48d83-1247">The point at the specified index.</span></span> |



 

<span data-ttu-id="48d83-1248">**Тип данных Ивгскевматрикс**</span><span class="sxs-lookup"><span data-stu-id="48d83-1248">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="48d83-1249">Матрица, используемая для наклона фигур, матрица преобразования перспективы в форме, "*скскс, СКСИ, Сикс, сии, px, корректировка* " \[ *s* = Scale, *p* = перспектива \] .</span><span class="sxs-lookup"><span data-stu-id="48d83-1249">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="48d83-1250">Если значение offset в абсолютных единицах, то *px,* сдвиг в единицах ЕС ^-1. в противном случае это обратная часть размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-1250">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="48d83-1251">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1251">Attributes</span></span>   | <span data-ttu-id="48d83-1252">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1252">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="48d83-1253">кстокс</span><span class="sxs-lookup"><span data-stu-id="48d83-1253">XtoX</span></span>         | <span data-ttu-id="48d83-1254">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1254">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="48d83-1255">итокс</span><span class="sxs-lookup"><span data-stu-id="48d83-1255">YtoX</span></span>         | <span data-ttu-id="48d83-1256">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1256">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="48d83-1257">кстой</span><span class="sxs-lookup"><span data-stu-id="48d83-1257">XtoY</span></span>         | <span data-ttu-id="48d83-1258">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1258">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="48d83-1259">итой</span><span class="sxs-lookup"><span data-stu-id="48d83-1259">YtoY</span></span>         | <span data-ttu-id="48d83-1260">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1260">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="48d83-1261">перспективекс</span><span class="sxs-lookup"><span data-stu-id="48d83-1261">PerspectiveX</span></span> | <span data-ttu-id="48d83-1262">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1262">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="48d83-1263">Перспектива</span><span class="sxs-lookup"><span data-stu-id="48d83-1263">PerspectiveY</span></span> | <span data-ttu-id="48d83-1264">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="48d83-1264">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="48d83-1265">**ивгскевоффсет**</span><span class="sxs-lookup"><span data-stu-id="48d83-1265">**IVgSkewOffset**</span></span>

<span data-ttu-id="48d83-1266">Задает смещение наклона.</span><span class="sxs-lookup"><span data-stu-id="48d83-1266">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48d83-1267">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1267">Attributes</span></span></th>
<th><span data-ttu-id="48d83-1268">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-1269">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-1269">Value</span></span></td>
<td><span data-ttu-id="48d83-1270"><a href="#data-types-used-in-the-vml-object-model">Строка</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1270"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="48d83-1271">Текстовое представление смещения.</span><span class="sxs-lookup"><span data-stu-id="48d83-1271">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1272">X</span><span class="sxs-lookup"><span data-stu-id="48d83-1272">X</span></span></td>
<td><span data-ttu-id="48d83-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="48d83-1274">Компонент X.</span><span class="sxs-lookup"><span data-stu-id="48d83-1274">X component.</span></span> <span data-ttu-id="48d83-1275">Процент или мера.</span><span class="sxs-lookup"><span data-stu-id="48d83-1275">Percentage or measure.</span></span> <span data-ttu-id="48d83-1276">Если единицы нет, то тип Шаперелативе является подразумеваемым. в противном случае подразумевается абсолютный тип.</span><span class="sxs-lookup"><span data-stu-id="48d83-1276">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1277">Да</span><span class="sxs-lookup"><span data-stu-id="48d83-1277">Y</span></span></td>
<td><span data-ttu-id="48d83-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="48d83-1279">Компонент Y.</span><span class="sxs-lookup"><span data-stu-id="48d83-1279">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1280">Тип</span><span class="sxs-lookup"><span data-stu-id="48d83-1280">Type</span></span></td>
<td><span data-ttu-id="48d83-1281"><strong>Вгскевтрансформтипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1281"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="48d83-1282">Указывает тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="48d83-1282">Specifies the type of transformation.</span></span> <span data-ttu-id="48d83-1283">Допустимые значения — целочисленные точки в диапазоне от-Infinity до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="48d83-1283">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="48d83-1284">Тип</span><span class="sxs-lookup"><span data-stu-id="48d83-1284">Type</span></span></th>
<th><span data-ttu-id="48d83-1285">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-1286">шаперелативе</span><span class="sxs-lookup"><span data-stu-id="48d83-1286">ShapeRelative</span></span></td>
<td><span data-ttu-id="48d83-1287">Значения смещения задаются в процентах (коэффициентах) размера исходной фигуры. Например, значение 0,5 означает смещение половины размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="48d83-1287">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1288">Абсолютный</span><span class="sxs-lookup"><span data-stu-id="48d83-1288">Absolute</span></span></td>
<td><span data-ttu-id="48d83-1289">Значения являются абсолютными единицами.</span><span class="sxs-lookup"><span data-stu-id="48d83-1289">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="48d83-1290">**Тип данных IVgVector2D**</span><span class="sxs-lookup"><span data-stu-id="48d83-1290">**IVgVector2D data type**</span></span>

<span data-ttu-id="48d83-1291">Задает двухмерный вектор, состоящий из двух чисел **типа Double** .</span><span class="sxs-lookup"><span data-stu-id="48d83-1291">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48d83-1292">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="48d83-1292">Attributes</span></span></th>
<th><span data-ttu-id="48d83-1293">Описание</span><span class="sxs-lookup"><span data-stu-id="48d83-1293">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-1294">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-1294">Value</span></span></td>
<td><span data-ttu-id="48d83-1295"><strong>Строка</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1295"><strong>String</strong>.</span></span> <span data-ttu-id="48d83-1296">Текстовое представление обоих векторных чисел, разделенных пробелом.</span><span class="sxs-lookup"><span data-stu-id="48d83-1296">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1297">X</span><span class="sxs-lookup"><span data-stu-id="48d83-1297">X</span></span></td>
<td><span data-ttu-id="48d83-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="48d83-1299">Компонент X этого вектора.</span><span class="sxs-lookup"><span data-stu-id="48d83-1299">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1300">Да</span><span class="sxs-lookup"><span data-stu-id="48d83-1300">Y</span></span></td>
<td><span data-ttu-id="48d83-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="48d83-1302">Компонент Y этого вектора.</span><span class="sxs-lookup"><span data-stu-id="48d83-1302">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1303">Тип</span><span class="sxs-lookup"><span data-stu-id="48d83-1303">Type</span></span></td>
<td><span data-ttu-id="48d83-1304"><strong>Вгвектортипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1304"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="48d83-1305">Для этого вектора ожидались единицы.</span><span class="sxs-lookup"><span data-stu-id="48d83-1305">Expected units for this vector.</span></span> <span data-ttu-id="48d83-1306">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-1306">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-1307">Мера</span><span class="sxs-lookup"><span data-stu-id="48d83-1307">Measure</span></span></li>
<li><span data-ttu-id="48d83-1308">Длина</span><span class="sxs-lookup"><span data-stu-id="48d83-1308">Length</span></span></li>
<li><span data-ttu-id="48d83-1309">англеиндегрис</span><span class="sxs-lookup"><span data-stu-id="48d83-1309">AngleInDegrees</span></span></li>
<li><span data-ttu-id="48d83-1310">Fraction</span><span class="sxs-lookup"><span data-stu-id="48d83-1310">Fraction</span></span></li>
<li><span data-ttu-id="48d83-1311">Целое число в процентах</span><span class="sxs-lookup"><span data-stu-id="48d83-1311">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="48d83-1312">**Тип данных IVgVector3D**</span><span class="sxs-lookup"><span data-stu-id="48d83-1312">**IVgVector3D data type**</span></span>

<span data-ttu-id="48d83-1313">Задает трехмерный вектор, состоящий из трех чисел **типа Double** .</span><span class="sxs-lookup"><span data-stu-id="48d83-1313">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48d83-1314">Значение</span><span class="sxs-lookup"><span data-stu-id="48d83-1314">Value</span></span></td>
<td><span data-ttu-id="48d83-1315"><strong>Строка</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1315"><strong>String</strong>.</span></span> <span data-ttu-id="48d83-1316">Текстовое представление трех векторных чисел, разделенных пробелом.</span><span class="sxs-lookup"><span data-stu-id="48d83-1316">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1317">X</span><span class="sxs-lookup"><span data-stu-id="48d83-1317">X</span></span></td>
<td><span data-ttu-id="48d83-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="48d83-1319">Компонент X этого вектора.</span><span class="sxs-lookup"><span data-stu-id="48d83-1319">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1320">Да</span><span class="sxs-lookup"><span data-stu-id="48d83-1320">Y</span></span></td>
<td><span data-ttu-id="48d83-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="48d83-1322">Компонент Y этого вектора.</span><span class="sxs-lookup"><span data-stu-id="48d83-1322">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="48d83-1323">Z</span><span class="sxs-lookup"><span data-stu-id="48d83-1323">Z</span></span></td>
<td><span data-ttu-id="48d83-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="48d83-1325">Компонент Z этого вектора.</span><span class="sxs-lookup"><span data-stu-id="48d83-1325">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="48d83-1326">Тип</span><span class="sxs-lookup"><span data-stu-id="48d83-1326">Type</span></span></td>
<td><span data-ttu-id="48d83-1327"><strong>Вгвектортипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="48d83-1327"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="48d83-1328">Для этого вектора ожидались единицы.</span><span class="sxs-lookup"><span data-stu-id="48d83-1328">Expected units for this vector.</span></span> <span data-ttu-id="48d83-1329">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-1329">Values are:</span></span>
<ul>
<li><span data-ttu-id="48d83-1330">Мера</span><span class="sxs-lookup"><span data-stu-id="48d83-1330">Measure</span></span></li>
<li><span data-ttu-id="48d83-1331">Длина</span><span class="sxs-lookup"><span data-stu-id="48d83-1331">Length</span></span></li>
<li><span data-ttu-id="48d83-1332">англеиндегрис</span><span class="sxs-lookup"><span data-stu-id="48d83-1332">AngleInDegrees</span></span></li>
<li><span data-ttu-id="48d83-1333">Fraction</span><span class="sxs-lookup"><span data-stu-id="48d83-1333">Fraction</span></span></li>
<li><span data-ttu-id="48d83-1334">Число</span><span class="sxs-lookup"><span data-stu-id="48d83-1334">Number</span></span></li>
<li><span data-ttu-id="48d83-1335">Процент</span><span class="sxs-lookup"><span data-stu-id="48d83-1335">Percentage</span></span></li>
<li><span data-ttu-id="48d83-1336">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="48d83-1336">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="48d83-1337">**Тип данных length**</span><span class="sxs-lookup"><span data-stu-id="48d83-1337">**Length data type**</span></span>

<span data-ttu-id="48d83-1338">Число с плавающей запятой с диапазоном от 0 до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="48d83-1338">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="48d83-1339">**Тип данных Measure**</span><span class="sxs-lookup"><span data-stu-id="48d83-1339">**Measure data type**</span></span>

<span data-ttu-id="48d83-1340">Число с плавающей запятой от-Infinity до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="48d83-1340">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="48d83-1341">**Тип данных String**</span><span class="sxs-lookup"><span data-stu-id="48d83-1341">**String data type**</span></span>

<span data-ttu-id="48d83-1342">Символьные данные любой длины.</span><span class="sxs-lookup"><span data-stu-id="48d83-1342">Character data of any length.</span></span>

<span data-ttu-id="48d83-1343">**вгблакквхитемоде**</span><span class="sxs-lookup"><span data-stu-id="48d83-1343">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="48d83-1344">Режим рендеринга для черного и белого.</span><span class="sxs-lookup"><span data-stu-id="48d83-1344">Rendering mode for black and white.</span></span> <span data-ttu-id="48d83-1345">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="48d83-1345">Possible values are:</span></span>

-   <span data-ttu-id="48d83-1346">**Цвет**</span><span class="sxs-lookup"><span data-stu-id="48d83-1346">**Color**</span></span>
-   <span data-ttu-id="48d83-1347">**Автоматически**</span><span class="sxs-lookup"><span data-stu-id="48d83-1347">**Auto**</span></span>
-   <span data-ttu-id="48d83-1348">**Оттенки серого**</span><span class="sxs-lookup"><span data-stu-id="48d83-1348">**GrayScale**</span></span>
-   <span data-ttu-id="48d83-1349">**лигхтграйскале**</span><span class="sxs-lookup"><span data-stu-id="48d83-1349">**LightGrayScale**</span></span>
-   <span data-ttu-id="48d83-1350">**инверсеграй**</span><span class="sxs-lookup"><span data-stu-id="48d83-1350">**InverseGray**</span></span>
-   <span data-ttu-id="48d83-1351">**грайаутлине**</span><span class="sxs-lookup"><span data-stu-id="48d83-1351">**GrayOutline**</span></span>
-   <span data-ttu-id="48d83-1352">**блакктекстандлинес**</span><span class="sxs-lookup"><span data-stu-id="48d83-1352">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="48d83-1353">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="48d83-1353">**HighContrast**</span></span>
-   <span data-ttu-id="48d83-1354">**Черный**</span><span class="sxs-lookup"><span data-stu-id="48d83-1354">**Black**</span></span>
-   <span data-ttu-id="48d83-1355">**Белый**</span><span class="sxs-lookup"><span data-stu-id="48d83-1355">**White**</span></span>
-   <span data-ttu-id="48d83-1356">**Не вырисовано**</span><span class="sxs-lookup"><span data-stu-id="48d83-1356">**Undrawn**</span></span>

<span data-ttu-id="48d83-1357">**Тип данных Вгфрактион**</span><span class="sxs-lookup"><span data-stu-id="48d83-1357">**VgFraction data type**</span></span>

<span data-ttu-id="48d83-1358">Число с плавающей запятой с диапазоном от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="48d83-1358">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="48d83-1359">Доли также могут быть указаны в процентах; Например, "50%".</span><span class="sxs-lookup"><span data-stu-id="48d83-1359">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="48d83-1360">**Тип данных Вгтристате**</span><span class="sxs-lookup"><span data-stu-id="48d83-1360">**VgTriState datatype**</span></span>

<span data-ttu-id="48d83-1361">Перечисление, используемое для значений, которые могут быть одного из трех состояний:</span><span class="sxs-lookup"><span data-stu-id="48d83-1361">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="48d83-1362">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="48d83-1362">**TRUE**</span></span>
-   <span data-ttu-id="48d83-1363">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="48d83-1363">**FALSE**</span></span>
-   <span data-ttu-id="48d83-1364">**MIXED**</span><span class="sxs-lookup"><span data-stu-id="48d83-1364">**MIXED**</span></span>