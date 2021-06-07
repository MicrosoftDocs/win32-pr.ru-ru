---
title: Справочник по объектной модели VML
description: В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9. Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c387935119babc73442e9b8f307672925bdf71d3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444825"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="d4aef-104">Справочник по объектной модели VML</span><span class="sxs-lookup"><span data-stu-id="d4aef-104">VML Object Model Reference</span></span>

<span data-ttu-id="d4aef-105">В этом разделе описывается функция VML, которая является устаревшей в Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d4aef-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d4aef-106">Веб-страницы и приложения, использующие VML, должны быть перенесены в формат SVG или другие широко поддерживаемые стандарты.</span><span class="sxs-lookup"><span data-stu-id="d4aef-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d4aef-107">По состоянию на Декабрь 2011 этот раздел был архивирован.</span><span class="sxs-lookup"><span data-stu-id="d4aef-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d4aef-108">В результате он больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d4aef-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d4aef-109">Дополнительные сведения см. в разделе [архивированное содержимое](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d4aef-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d4aef-110">Сведения, рекомендации и рекомендации по текущей версии Windows Internet Explorer см. в [центре разработчиков Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d4aef-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d4aef-111">В этом разделе:</span><span class="sxs-lookup"><span data-stu-id="d4aef-111">In this topic:</span></span>

-   [<span data-ttu-id="d4aef-112">Введение</span><span class="sxs-lookup"><span data-stu-id="d4aef-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d4aef-113">Пример</span><span class="sxs-lookup"><span data-stu-id="d4aef-113">Example</span></span>](#example)
-   [<span data-ttu-id="d4aef-114">Настройка VML</span><span class="sxs-lookup"><span data-stu-id="d4aef-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="d4aef-115">Справочник по объектной модели VML</span><span class="sxs-lookup"><span data-stu-id="d4aef-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="d4aef-116">Shape, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="d4aef-117">Вложенные элементы элемента Shape</span><span class="sxs-lookup"><span data-stu-id="d4aef-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="d4aef-118">Элемент Background</span><span class="sxs-lookup"><span data-stu-id="d4aef-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="d4aef-119">Элемент объемной фигуры</span><span class="sxs-lookup"><span data-stu-id="d4aef-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="d4aef-120">Fill, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="d4aef-121">Group, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="d4aef-122">Имажедата, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="d4aef-123">Элемент Path</span><span class="sxs-lookup"><span data-stu-id="d4aef-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="d4aef-124">Элемент Shadow</span><span class="sxs-lookup"><span data-stu-id="d4aef-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="d4aef-125">Элемент асимметрии</span><span class="sxs-lookup"><span data-stu-id="d4aef-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="d4aef-126">Элемент Stroke</span><span class="sxs-lookup"><span data-stu-id="d4aef-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="d4aef-127">Текстпас, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="d4aef-128">Типы данных, используемые в объектной модели VML</span><span class="sxs-lookup"><span data-stu-id="d4aef-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="d4aef-129">Введение</span><span class="sxs-lookup"><span data-stu-id="d4aef-129">Introduction</span></span>

<span data-ttu-id="d4aef-130">[Язык VML (VML)](https://www.w3.org/TR/NOTE-datetime.html) — это текстовый язык, который использует [XML](https://www.w3.org/TR/REC-xml.mdl) для расширения HTML с целью отображения векторных графических данных.</span><span class="sxs-lookup"><span data-stu-id="d4aef-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="d4aef-131">VML модель DOM (DOM) определяет программный интерфейс для управления элементами документа.</span><span class="sxs-lookup"><span data-stu-id="d4aef-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="d4aef-132">Это позволяет пользователю динамически создавать и изменять векторную графику с помощью интерфейса, не зависящего от платформы и языка.</span><span class="sxs-lookup"><span data-stu-id="d4aef-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="d4aef-133">Модель DOM VML соответствует спецификации [модель DOM](https://www.w3.org/TR/REC-DOM-Level-1/) .</span><span class="sxs-lookup"><span data-stu-id="d4aef-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="d4aef-134">VML использует элемент [Shape](#shape-element) в качестве базового стандартного блока для векторных графических изображений.</span><span class="sxs-lookup"><span data-stu-id="d4aef-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="d4aef-135">После создания фигуры можно изменить форму с помощью атрибутов или вложенных подэлементов.</span><span class="sxs-lookup"><span data-stu-id="d4aef-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="d4aef-136">Например, чтобы изменить цвет фигуры, назначьте атрибуту **FillColor** значение цвета.</span><span class="sxs-lookup"><span data-stu-id="d4aef-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="d4aef-137">Некоторые атрибуты фигуры также являются [подэлементами](/windows) и имеют собственные атрибуты, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="d4aef-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="d4aef-138">Фон</span><span class="sxs-lookup"><span data-stu-id="d4aef-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="d4aef-139">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="d4aef-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="d4aef-140">Заполнить</span><span class="sxs-lookup"><span data-stu-id="d4aef-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="d4aef-141">Группа</span><span class="sxs-lookup"><span data-stu-id="d4aef-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="d4aef-142">имажедата</span><span class="sxs-lookup"><span data-stu-id="d4aef-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="d4aef-143">Путь</span><span class="sxs-lookup"><span data-stu-id="d4aef-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="d4aef-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="d4aef-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="d4aef-145">Отклонение</span><span class="sxs-lookup"><span data-stu-id="d4aef-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="d4aef-146">Водок</span><span class="sxs-lookup"><span data-stu-id="d4aef-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="d4aef-147">текстпас</span><span class="sxs-lookup"><span data-stu-id="d4aef-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="d4aef-148">Объектная модель VML использует несколько [типов данных](/windows) для определения параметров.</span><span class="sxs-lookup"><span data-stu-id="d4aef-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="d4aef-149">Типы данных с префиксом "VG" являются перечислениями, а с префиксом "ИВГ" — объектами.</span><span class="sxs-lookup"><span data-stu-id="d4aef-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="d4aef-150">Щелкните здесь для вывода списка.</span><span class="sxs-lookup"><span data-stu-id="d4aef-150">Click here for a list.</span></span> <span data-ttu-id="d4aef-151">Дополнительные типы с указанными параметрами перечислены в списке.</span><span class="sxs-lookup"><span data-stu-id="d4aef-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="d4aef-152">Пример</span><span class="sxs-lookup"><span data-stu-id="d4aef-152">Example</span></span>

<span data-ttu-id="d4aef-153">В следующем коде на языке VBScript показано, как создать простую фигуру:</span><span class="sxs-lookup"><span data-stu-id="d4aef-153">The following VBScript code shows how to create a simple shape:</span></span>


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



<span data-ttu-id="d4aef-154">В приведенном выше примере фигура создается с помощью модель DOM метода **CreateElement**.</span><span class="sxs-lookup"><span data-stu-id="d4aef-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="d4aef-155">Фигура представляет собой предопределенную фигуру в формате VML.</span><span class="sxs-lookup"><span data-stu-id="d4aef-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="d4aef-156">Несмотря на то, что объект существует, он не может быть частью документа, пока он не будет присоединен к документу.</span><span class="sxs-lookup"><span data-stu-id="d4aef-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="d4aef-157">С помощью метода **AppendChild** Rect становится дочерним элементом элемента **div** с именем мидив.</span><span class="sxs-lookup"><span data-stu-id="d4aef-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="d4aef-158">Несколько минимальных атрибутов стиля («**Расположение**», « **Ширина**», « **Высота**», « **сверху**», « **слева**») устанавливаются для присвоения форме определенного размера.</span><span class="sxs-lookup"><span data-stu-id="d4aef-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="d4aef-159">Наконец, цвет присваивается атрибуту **FillColor** .</span><span class="sxs-lookup"><span data-stu-id="d4aef-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="d4aef-160">Обратите внимание, что можно использовать любой язык сценариев или любой язык, который может работать с интерфейсами модель DOM.</span><span class="sxs-lookup"><span data-stu-id="d4aef-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="d4aef-161">Настройка VML</span><span class="sxs-lookup"><span data-stu-id="d4aef-161">Setting up VML</span></span>

<span data-ttu-id="d4aef-162">Одна реализация VML осуществляется через Microsoft Internet Explorer 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="d4aef-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="d4aef-163">Чтобы правильно настроить объект отрисовки на веб-странице, необходимо выполнить следующие добавления:</span><span class="sxs-lookup"><span data-stu-id="d4aef-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="d4aef-164">Схема должна быть настроена в начальной</span><span class="sxs-lookup"><span data-stu-id="d4aef-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="d4aef-165">тег следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d4aef-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="d4aef-166">Режим подготовки к просмотру должен быть частью стиля документа:</span><span class="sxs-lookup"><span data-stu-id="d4aef-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="d4aef-167">Ниже показан пример веб-страницы HTML, настроенной правильно для VML, отображающей динамическое создание фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


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



<span data-ttu-id="d4aef-168">Обратите внимание, что в бета-версиях требуется тег объекта ActiveX и другой стиль поведения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="d4aef-169">Справочник по объектной модели VML</span><span class="sxs-lookup"><span data-stu-id="d4aef-169">VML OM Reference</span></span>

<span data-ttu-id="d4aef-170">Эта ссылка определяет элемент [Shape](#shape-element) , [подэлементы](/windows)и [типы данных](/windows) , используемые объектной моделью VML.</span><span class="sxs-lookup"><span data-stu-id="d4aef-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="d4aef-171">Shape, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-171">Shape element</span></span>

<span data-ttu-id="d4aef-172">Фигуры — это стандартные блоки графических изображений, определяемые язык VML (VML).</span><span class="sxs-lookup"><span data-stu-id="d4aef-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="d4aef-173">Фигура является элементом верхнего уровня, и несколько подэлементов помогают определить природу каждой фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="d4aef-174">VML предоставляет стандартные фигуры:</span><span class="sxs-lookup"><span data-stu-id="d4aef-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="d4aef-175">**Атрибуты фигур**</span><span class="sxs-lookup"><span data-stu-id="d4aef-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="d4aef-176">**Дуги**</span><span class="sxs-lookup"><span data-stu-id="d4aef-176">**Arc**</span></span>
-   <span data-ttu-id="d4aef-177">**Соединитель**</span><span class="sxs-lookup"><span data-stu-id="d4aef-177">**Curve**</span></span>
-   <span data-ttu-id="d4aef-178">**Line**</span><span class="sxs-lookup"><span data-stu-id="d4aef-178">**Line**</span></span>
-   <span data-ttu-id="d4aef-179">**Линию**</span><span class="sxs-lookup"><span data-stu-id="d4aef-179">**PolyLine**</span></span>
-   <span data-ttu-id="d4aef-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="d4aef-180">**Rect**</span></span>
-   <span data-ttu-id="d4aef-181">**раундрект**</span><span class="sxs-lookup"><span data-stu-id="d4aef-181">**RoundRect**</span></span>



|   <span data-ttu-id="d4aef-182">Вложенный элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-182">Subelement</span></span>           |    <span data-ttu-id="d4aef-183">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-183">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-184">Разница</span><span class="sxs-lookup"><span data-stu-id="d4aef-184">Adj</span></span>          | <span data-ttu-id="d4aef-185">[Ивгаджустментс](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="d4aef-186">Разделенный запятыми список чисел, которые являются параметрами для формул руководств, определяющих путь к фигуре.</span><span class="sxs-lookup"><span data-stu-id="d4aef-186">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="d4aef-187">Значения можно опустить, чтобы разрешить использование значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4aef-187">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="d4aef-188">Может быть до 8 значений коррекции.</span><span class="sxs-lookup"><span data-stu-id="d4aef-188">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="d4aef-189">Alt</span><span class="sxs-lookup"><span data-stu-id="d4aef-189">Alt</span></span>          | <span data-ttu-id="d4aef-190">Строка.</span><span class="sxs-lookup"><span data-stu-id="d4aef-190">String.</span></span> <span data-ttu-id="d4aef-191">Альтернативный текст, связанный с фигурой.</span><span class="sxs-lookup"><span data-stu-id="d4aef-191">Alternative text associated with shape.</span></span> <span data-ttu-id="d4aef-192">Используется для неграфического обзора.</span><span class="sxs-lookup"><span data-stu-id="d4aef-192">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d4aef-193">Кнопка</span><span class="sxs-lookup"><span data-stu-id="d4aef-193">Button</span></span>       | <span data-ttu-id="d4aef-194">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-194">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-195">Отображает поведение кнопки при нажатии.</span><span class="sxs-lookup"><span data-stu-id="d4aef-195">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d4aef-196">бвмоде</span><span class="sxs-lookup"><span data-stu-id="d4aef-196">BWMode</span></span>       | <span data-ttu-id="d4aef-197">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="d4aef-198">Определяет, как форма будет отображаться в виде черно-белого представления в приложениях или при печати на черно-белых принтерах.</span><span class="sxs-lookup"><span data-stu-id="d4aef-198">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="d4aef-199">К значениям относятся: **Цвет**, **Авто**, **оттенки серого**, **лигхтграйскале**, **инверсеграй**, **грайаутлине**, **блакктекстандлинес**, **HighContrast**, **черный**, **белый**, **нерисованный**.</span><span class="sxs-lookup"><span data-stu-id="d4aef-199">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="d4aef-200">Значение по умолчанию: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="d4aef-200">Default: **Auto**.</span></span> |
| <span data-ttu-id="d4aef-201">бвнормал</span><span class="sxs-lookup"><span data-stu-id="d4aef-201">BWNormal</span></span>     | <span data-ttu-id="d4aef-202">Вгблакквхитемоде.</span><span class="sxs-lookup"><span data-stu-id="d4aef-202">VgBlackWhiteMode.</span></span> <span data-ttu-id="d4aef-203">Если Бвмоде имеет значение Auto, это свойство обращается к, чтобы отобразить форму в нормальном черном и белом режиме.</span><span class="sxs-lookup"><span data-stu-id="d4aef-203">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="d4aef-204">К значениям относятся: **Цвет**, **Авто**, **оттенки серого**, **лигхтграйскале**, **инверсеграй**, **грайаутлине**, **блакктекстандлинес**, **HighContrast**, **черный**, **белый**, **нерисованный**.</span><span class="sxs-lookup"><span data-stu-id="d4aef-204">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="d4aef-205">Значение по умолчанию: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="d4aef-205">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="d4aef-206">бвпуре</span><span class="sxs-lookup"><span data-stu-id="d4aef-206">BWPure</span></span>       | <span data-ttu-id="d4aef-207">Вгблакквхитемоде.</span><span class="sxs-lookup"><span data-stu-id="d4aef-207">VgBlackWhiteMode.</span></span> <span data-ttu-id="d4aef-208">Если Бвмоде имеет значение Auto, это свойство обращается к, чтобы отобразить фигуру в чистом B/W.</span><span class="sxs-lookup"><span data-stu-id="d4aef-208">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="d4aef-209">К значениям относятся: **Цвет**, **Авто**, **оттенки серого**, **лигхтграйскале**, **инверсеграй**, **грайаутлине**, **блакктекстандлинес**, **HighContrast**, **черный**, **белый**, **нерисованный**.</span><span class="sxs-lookup"><span data-stu-id="d4aef-209">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="d4aef-210">Значение по умолчанию: **Auto**.</span><span class="sxs-lookup"><span data-stu-id="d4aef-210">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="d4aef-211">чилдшапес</span><span class="sxs-lookup"><span data-stu-id="d4aef-211">ChildShapes</span></span>  | <span data-ttu-id="d4aef-212">Ивгграупшапес.</span><span class="sxs-lookup"><span data-stu-id="d4aef-212">IVgGroupShapes.</span></span> <span data-ttu-id="d4aef-213">Коллекция других фигур в этой группе.</span><span class="sxs-lookup"><span data-stu-id="d4aef-213">A collection of other shapes in this group.</span></span> <span data-ttu-id="d4aef-214">Эта коллекция поддерживает стандартную длину и методы элементов.</span><span class="sxs-lookup"><span data-stu-id="d4aef-214">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d4aef-215">чромакэй</span><span class="sxs-lookup"><span data-stu-id="d4aef-215">Chromakey</span></span>    | <span data-ttu-id="d4aef-216">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="d4aef-217">Значение цвета, которое будет прозрачным и показывать все, что находится за фигурой.</span><span class="sxs-lookup"><span data-stu-id="d4aef-217">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="d4aef-218">Control1</span><span class="sxs-lookup"><span data-stu-id="d4aef-218">Control1</span></span>     | <span data-ttu-id="d4aef-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="d4aef-220">Контрольная точка для кривой.</span><span class="sxs-lookup"><span data-stu-id="d4aef-220">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d4aef-221">Control2</span><span class="sxs-lookup"><span data-stu-id="d4aef-221">Control2</span></span>     | <span data-ttu-id="d4aef-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="d4aef-223">Контрольная точка для кривой.</span><span class="sxs-lookup"><span data-stu-id="d4aef-223">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d4aef-224">курдоригин</span><span class="sxs-lookup"><span data-stu-id="d4aef-224">CoordOrigin</span></span>  | <span data-ttu-id="d4aef-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Координаты в левом верхнем углу прямоугольника контейнера.</span><span class="sxs-lookup"><span data-stu-id="d4aef-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="d4aef-226">Диапазон от 0 до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d4aef-226">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="d4aef-227">курдсизе</span><span class="sxs-lookup"><span data-stu-id="d4aef-227">CoordSize</span></span>    | <span data-ttu-id="d4aef-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="d4aef-229">Ширина и высота пространства координат внутри ссылочного прямоугольника этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-229">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="d4aef-230">Если он не указан, то он совпадает с шириной и высотой прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d4aef-230">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="d4aef-231">Диапазон от 0 до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d4aef-231">Range from 0 to infinity.</span></span> <span data-ttu-id="d4aef-232">Значение по умолчанию: 1000, 1000.</span><span class="sxs-lookup"><span data-stu-id="d4aef-232">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="d4aef-233">ендангле</span><span class="sxs-lookup"><span data-stu-id="d4aef-233">EndAngle</span></span>     | <span data-ttu-id="d4aef-234">[Вганглеиндегрис](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="d4aef-235">Конечный угол фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-235">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d4aef-236">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="d4aef-236">Extrusion</span></span>    | <span data-ttu-id="d4aef-237">Ивжекструсион.</span><span class="sxs-lookup"><span data-stu-id="d4aef-237">IVgExtrusion.</span></span> <span data-ttu-id="d4aef-238">Задает значение объекта объема для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-238">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="d4aef-239">Дополнительные сведения см. в элементе объемной [фигуры](msdn-online-vml-extrusion-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d4aef-239">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="d4aef-240">Заливка</span><span class="sxs-lookup"><span data-stu-id="d4aef-240">Fill</span></span>         | <span data-ttu-id="d4aef-241">Вгфиллформат.</span><span class="sxs-lookup"><span data-stu-id="d4aef-241">VgFillFormat.</span></span> <span data-ttu-id="d4aef-242">Задает значение заливки для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-242">Specifies the fill value for this shape.</span></span> <span data-ttu-id="d4aef-243">Дополнительные сведения см. в элементе [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d4aef-243">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="d4aef-244">FillColor</span><span class="sxs-lookup"><span data-stu-id="d4aef-244">FillColor</span></span>    | <span data-ttu-id="d4aef-245">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="d4aef-246">Основной цвет кисти, используемой для заполнения контура этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-246">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d4aef-247">Указал</span><span class="sxs-lookup"><span data-stu-id="d4aef-247">Filled</span></span>       | <span data-ttu-id="d4aef-248">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-248">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-249">Если значение — true, то путь, определяющий фигуру, будет заполнен.</span><span class="sxs-lookup"><span data-stu-id="d4aef-249">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="d4aef-250">По умолчанию он заполняется сплошным цветом, если отсутствует вложенный элемент Fill, указывающий более сложные свойства заливки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-250">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="d4aef-251">Если значение равно false, заливка прозрачна.</span><span class="sxs-lookup"><span data-stu-id="d4aef-251">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="d4aef-252">Перевернуть</span><span class="sxs-lookup"><span data-stu-id="d4aef-252">Flip</span></span>         | <span data-ttu-id="d4aef-253">Вгфлипориентатион.</span><span class="sxs-lookup"><span data-stu-id="d4aef-253">VgFlipOrientation.</span></span> <span data-ttu-id="d4aef-254">Значения: X Y XY Икс</span><span class="sxs-lookup"><span data-stu-id="d4aef-254">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d4aef-255">форцедаш</span><span class="sxs-lookup"><span data-stu-id="d4aef-255">ForceDash</span></span>    | <span data-ttu-id="d4aef-256">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-256">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-257">Указывает, что пунктирная структура должна быть визуализирована, если нет линии и заливка для фигуры отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d4aef-257">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="d4aef-258">Это поведение обычно полезно для того, чтобы сделать невидимые фигуры видимыми при редактировании приложений, чтобы их можно было выбирать и использовать, например, на карте изображений.</span><span class="sxs-lookup"><span data-stu-id="d4aef-258">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="d4aef-259">Формулы</span><span class="sxs-lookup"><span data-stu-id="d4aef-259">Formulas</span></span>     | <span data-ttu-id="d4aef-260">Ивгформулас.</span><span class="sxs-lookup"><span data-stu-id="d4aef-260">IVgFormulas.</span></span> <span data-ttu-id="d4aef-261">Массив формул, определяющих фигуру.</span><span class="sxs-lookup"><span data-stu-id="d4aef-261">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d4aef-262">Исходный тип</span><span class="sxs-lookup"><span data-stu-id="d4aef-262">From</span></span>         | <span data-ttu-id="d4aef-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="d4aef-264">Начальная точка линии.</span><span class="sxs-lookup"><span data-stu-id="d4aef-264">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d4aef-265">Полный</span><span class="sxs-lookup"><span data-stu-id="d4aef-265">HRef</span></span>         | <span data-ttu-id="d4aef-266">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-266">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-267">URL-адрес для перехода при щелчке этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-267">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d4aef-268">ImageData</span><span class="sxs-lookup"><span data-stu-id="d4aef-268">ImageData</span></span>    | <span data-ttu-id="d4aef-269">Ивгимажедата.</span><span class="sxs-lookup"><span data-stu-id="d4aef-269">IVgImageData.</span></span> <span data-ttu-id="d4aef-270">Сведения об изображении, если фигура является изображением.</span><span class="sxs-lookup"><span data-stu-id="d4aef-270">Image information if the shape is a picture.</span></span> <span data-ttu-id="d4aef-271">Дополнительные сведения см. в элементе Имажедата.</span><span class="sxs-lookup"><span data-stu-id="d4aef-271">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d4aef-272">онед</span><span class="sxs-lookup"><span data-stu-id="d4aef-272">OnEd</span></span>         | <span data-ttu-id="d4aef-273">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-273">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-274">Скрывает все маркеры, кроме верхнего левого и нижнего правого, как в маркерах для сегмента прямой линии.</span><span class="sxs-lookup"><span data-stu-id="d4aef-274">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="d4aef-275">Непрозрачность</span><span class="sxs-lookup"><span data-stu-id="d4aef-275">Opacity</span></span>      | <span data-ttu-id="d4aef-276">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="d4aef-277">Непрозрачность всей фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-277">The opacity of the entire shape.</span></span> <span data-ttu-id="d4aef-278">Число от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="d4aef-278">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d4aef-279">Путь</span><span class="sxs-lookup"><span data-stu-id="d4aef-279">Path</span></span>         | <span data-ttu-id="d4aef-280">Ивгпас.</span><span class="sxs-lookup"><span data-stu-id="d4aef-280">IVgPath.</span></span> <span data-ttu-id="d4aef-281">Строка, содержащая команды, определяющие путь.</span><span class="sxs-lookup"><span data-stu-id="d4aef-281">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d4aef-282">точки</span><span class="sxs-lookup"><span data-stu-id="d4aef-282">Points</span></span>       | <span data-ttu-id="d4aef-283">[Ивгпоинтс](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="d4aef-284">Коллекция точек, определяющих фигуру.</span><span class="sxs-lookup"><span data-stu-id="d4aef-284">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d4aef-285">Печать</span><span class="sxs-lookup"><span data-stu-id="d4aef-285">Print</span></span>        | <span data-ttu-id="d4aef-286">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-286">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-287">Если значение — true, эта фигура предназначена для печати.</span><span class="sxs-lookup"><span data-stu-id="d4aef-287">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d4aef-288">Поворот</span><span class="sxs-lookup"><span data-stu-id="d4aef-288">Rotation</span></span>     | <span data-ttu-id="d4aef-289">[Вганглеиндегрис](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="d4aef-290">Задает поворот фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-290">Sets rotation of shape.</span></span> <span data-ttu-id="d4aef-291">Значение распространяется на стиль фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-291">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="d4aef-292">Масштабирование</span><span class="sxs-lookup"><span data-stu-id="d4aef-292">Scale</span></span>        | <span data-ttu-id="d4aef-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="d4aef-294">Масштаб фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-294">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d4aef-295">Shadow</span><span class="sxs-lookup"><span data-stu-id="d4aef-295">Shadow</span></span>       | <span data-ttu-id="d4aef-296">Ивгшадов.</span><span class="sxs-lookup"><span data-stu-id="d4aef-296">IVgShadow.</span></span> <span data-ttu-id="d4aef-297">Задает тень для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-297">Specifies the shadow for this shape.</span></span> <span data-ttu-id="d4aef-298">Дополнительные сведения см. в элементе [shadow](msdn-online-vml-shadow-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d4aef-298">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d4aef-299">спт</span><span class="sxs-lookup"><span data-stu-id="d4aef-299">Spt</span></span>          | <span data-ttu-id="d4aef-300">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="d4aef-300">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d4aef-301">StartAngle и заканчивая</span><span class="sxs-lookup"><span data-stu-id="d4aef-301">StartAngle</span></span>   | <span data-ttu-id="d4aef-302">[Вганглеиндегрис](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="d4aef-303">Начальный угол фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-303">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d4aef-304">Stroke</span><span class="sxs-lookup"><span data-stu-id="d4aef-304">Stroke</span></span>       | <span data-ttu-id="d4aef-305">Вгстрокеформат.</span><span class="sxs-lookup"><span data-stu-id="d4aef-305">VgStrokeFormat.</span></span> <span data-ttu-id="d4aef-306">Дополнительные сведения см. в разделе элемент Stroke.</span><span class="sxs-lookup"><span data-stu-id="d4aef-306">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d4aef-307">строкеколор</span><span class="sxs-lookup"><span data-stu-id="d4aef-307">StrokeColor</span></span>  | <span data-ttu-id="d4aef-308">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="d4aef-309">Основной цвет кисти, используемой для обводки контура этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-309">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="d4aef-310">Заштриховывать</span><span class="sxs-lookup"><span data-stu-id="d4aef-310">Stroked</span></span>      | <span data-ttu-id="d4aef-311">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-311">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-312">Если значение равно true, то путь, определяющий фигуру, будет обводкой.</span><span class="sxs-lookup"><span data-stu-id="d4aef-312">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d4aef-313">строкевеигхт</span><span class="sxs-lookup"><span data-stu-id="d4aef-313">StrokeWeight</span></span> | <span data-ttu-id="d4aef-314">[Вгленгс](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-314">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="d4aef-315">Ширина кисти, используемой для обводки контура.</span><span class="sxs-lookup"><span data-stu-id="d4aef-315">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="d4aef-316">Диапазоны от 0 до 1584.</span><span class="sxs-lookup"><span data-stu-id="d4aef-316">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d4aef-317">текстпас</span><span class="sxs-lookup"><span data-stu-id="d4aef-317">TextPath</span></span>     | <span data-ttu-id="d4aef-318">Ивгтекстпас.</span><span class="sxs-lookup"><span data-stu-id="d4aef-318">IVgTextPath.</span></span> <span data-ttu-id="d4aef-319">Указывает объект Текстпас фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-319">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="d4aef-320">Дополнительные сведения см. в элементе [текстпас](msdn-online-vml-textpath-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d4aef-320">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="d4aef-321">Кому</span><span class="sxs-lookup"><span data-stu-id="d4aef-321">To</span></span>           | <span data-ttu-id="d4aef-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="d4aef-323">Конечная точка линии.</span><span class="sxs-lookup"><span data-stu-id="d4aef-323">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d4aef-324">Type</span><span class="sxs-lookup"><span data-stu-id="d4aef-324">Type</span></span>         | <span data-ttu-id="d4aef-325">Строка.</span><span class="sxs-lookup"><span data-stu-id="d4aef-325">String.</span></span> <span data-ttu-id="d4aef-326">Тип фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-326">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="d4aef-327">Вложенные элементы элемента Shape</span><span class="sxs-lookup"><span data-stu-id="d4aef-327">Subelements of the Shape Element</span></span>

<span data-ttu-id="d4aef-328">Следующие подэлементы являются частью объектной модели VML.</span><span class="sxs-lookup"><span data-stu-id="d4aef-328">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="d4aef-329">Фон</span><span class="sxs-lookup"><span data-stu-id="d4aef-329">Background</span></span>](#background-element)
-   [<span data-ttu-id="d4aef-330">Выдавливания</span><span class="sxs-lookup"><span data-stu-id="d4aef-330">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="d4aef-331">Заполнить</span><span class="sxs-lookup"><span data-stu-id="d4aef-331">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="d4aef-332">Группа</span><span class="sxs-lookup"><span data-stu-id="d4aef-332">Group</span></span>](#group-element)
-   [<span data-ttu-id="d4aef-333">имажедата</span><span class="sxs-lookup"><span data-stu-id="d4aef-333">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="d4aef-334">Путь</span><span class="sxs-lookup"><span data-stu-id="d4aef-334">Path</span></span>](#path-element)
-   [<span data-ttu-id="d4aef-335">Shadow</span><span class="sxs-lookup"><span data-stu-id="d4aef-335">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="d4aef-336">Отклонение</span><span class="sxs-lookup"><span data-stu-id="d4aef-336">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="d4aef-337">Водок</span><span class="sxs-lookup"><span data-stu-id="d4aef-337">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="d4aef-338">текстпас</span><span class="sxs-lookup"><span data-stu-id="d4aef-338">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="d4aef-339">Элемент Background</span><span class="sxs-lookup"><span data-stu-id="d4aef-339">Background element</span></span>

<span data-ttu-id="d4aef-340">Описывает заливку фона страницы с помощью заливки VML.</span><span class="sxs-lookup"><span data-stu-id="d4aef-340">Describes the fill of the background of a page using VML fills.</span></span>


|   <span data-ttu-id="d4aef-341">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-341">Attribute</span></span>        |   <span data-ttu-id="d4aef-342">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-342">Description</span></span>                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-343">бвмоде</span><span class="sxs-lookup"><span data-stu-id="d4aef-343">BWMode</span></span>    | <span data-ttu-id="d4aef-344">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="d4aef-345">Определяет, как форма будет отображаться в виде черно-белого представления в приложениях или при печати.</span><span class="sxs-lookup"><span data-stu-id="d4aef-345">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="d4aef-346">бвнормал</span><span class="sxs-lookup"><span data-stu-id="d4aef-346">BWNormal</span></span>  | <span data-ttu-id="d4aef-347">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="d4aef-348">Если Бвмоде имеет значение Auto, это свойство обращается к, чтобы отобразить форму в нормальном черном и белом режиме.</span><span class="sxs-lookup"><span data-stu-id="d4aef-348">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="d4aef-349">бвпуре</span><span class="sxs-lookup"><span data-stu-id="d4aef-349">BWPure</span></span>    | <span data-ttu-id="d4aef-350">[Вгблакквхитемоде](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="d4aef-351">Если Бвмоде имеет значение Auto, это свойство обращается к, чтобы отобразить фигуру в чисто черном и белом режиме.</span><span class="sxs-lookup"><span data-stu-id="d4aef-351">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="d4aef-352">Заливка</span><span class="sxs-lookup"><span data-stu-id="d4aef-352">Fill</span></span>      | <span data-ttu-id="d4aef-353">Вгфиллформат.</span><span class="sxs-lookup"><span data-stu-id="d4aef-353">VgFillFormat.</span></span> <span data-ttu-id="d4aef-354">Задает заливку для этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-354">Specifies the fill for this shape.</span></span> <span data-ttu-id="d4aef-355">Дополнительные сведения см. в разделе элемент [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d4aef-355">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="d4aef-356">FillColor</span><span class="sxs-lookup"><span data-stu-id="d4aef-356">FillColor</span></span> | <span data-ttu-id="d4aef-357">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="d4aef-358">Основной цвет кисти, используемой для заполнения контура этой фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-358">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="d4aef-359">Повторяющееся значение цвета в элементе Fill.</span><span class="sxs-lookup"><span data-stu-id="d4aef-359">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="d4aef-360">По умолчанию цвет белый.</span><span class="sxs-lookup"><span data-stu-id="d4aef-360">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="d4aef-361">Элемент объемной фигуры</span><span class="sxs-lookup"><span data-stu-id="d4aef-361">Extrusion element</span></span>

<span data-ttu-id="d4aef-362">Описывает трехмерную часть фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-362">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="d4aef-363">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="d4aef-363">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-364">ауторотатионцентер</span><span class="sxs-lookup"><span data-stu-id="d4aef-364">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="d4aef-365"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-366">Если значение равно true, центр вращения группы трехмерных объектов (фактически существует только один объект в группе) автоматически определяется как центр группы. в противном случае он определяется параметрами Ротатионцентер, которые являются частью фигуры с 0, 0, равным центру.</span><span class="sxs-lookup"><span data-stu-id="d4aef-366">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-367">Глубина</span><span class="sxs-lookup"><span data-stu-id="d4aef-367">BackDepth</span></span></td>
<td><span data-ttu-id="d4aef-368"><a href="msdn-online-vml-vglength.md"><strong>Вгленгс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="d4aef-369">Величина обратной придания.</span><span class="sxs-lookup"><span data-stu-id="d4aef-369">Amount of backward extrusion.</span></span> <span data-ttu-id="d4aef-370">В диапазоне от 0 до 32767.</span><span class="sxs-lookup"><span data-stu-id="d4aef-370">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-371">Brightness</span><span class="sxs-lookup"><span data-stu-id="d4aef-371">Brightness</span></span></td>
<td><span data-ttu-id="d4aef-372"><a href="#data-types-used-in-the-vml-object-model">Вгпоситивенумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="d4aef-373">Общая яркость сцены.</span><span class="sxs-lookup"><span data-stu-id="d4aef-373">Overall brightness of the scene.</span></span> <span data-ttu-id="d4aef-374">Значение по умолчанию — &quot; 20 000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-374">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-375">Цвет</span><span class="sxs-lookup"><span data-stu-id="d4aef-375">Color</span></span></td>
<td><span data-ttu-id="d4aef-376"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="d4aef-377">Цвет объема.</span><span class="sxs-lookup"><span data-stu-id="d4aef-377">The color of the extrusion.</span></span> <span data-ttu-id="d4aef-378">Используется, только если Колормоде является настраиваемым.</span><span class="sxs-lookup"><span data-stu-id="d4aef-378">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="d4aef-379">В противном случае функция Auto устанавливает цвет эффектов объемной фигуры так же, как FillColor.</span><span class="sxs-lookup"><span data-stu-id="d4aef-379">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-380">колормоде</span><span class="sxs-lookup"><span data-stu-id="d4aef-380">ColorMode</span></span></td>
<td><span data-ttu-id="d4aef-381">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="d4aef-381">Vg3DColorMode.</span></span> <span data-ttu-id="d4aef-382">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-382">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-383">Auto (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-383">Auto (default)</span></span></li>
<li><span data-ttu-id="d4aef-384">Особые настройки</span><span class="sxs-lookup"><span data-stu-id="d4aef-384">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-385">Рассеянность</span><span class="sxs-lookup"><span data-stu-id="d4aef-385">Diffusity</span></span></td>
<td><span data-ttu-id="d4aef-386"><a href="#data-types-used-in-the-vml-object-model">Вгпоситивенумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="d4aef-387">Отношение инцидента к рассеянному свету.</span><span class="sxs-lookup"><span data-stu-id="d4aef-387">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="d4aef-388">Значения меньше 1,0 являются нормальными, но значения, превышающие один, могут создавать интересные эффекты.</span><span class="sxs-lookup"><span data-stu-id="d4aef-388">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-389">Edge</span><span class="sxs-lookup"><span data-stu-id="d4aef-389">Edge</span></span></td>
<td><span data-ttu-id="d4aef-390"><a href="msdn-online-vml-vglength.md">Вгленгс</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-390"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="d4aef-391">Задает размер смоделированного скругленного края.</span><span class="sxs-lookup"><span data-stu-id="d4aef-391">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="d4aef-392">В диапазоне от 0 до 32767 в PTS с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d4aef-392">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="d4aef-393">Значение по умолчанию — &quot; выбрано 1pt &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-393">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-394">Аспект</span><span class="sxs-lookup"><span data-stu-id="d4aef-394">Facet</span></span></td>
<td><span data-ttu-id="d4aef-395"><a href="#data-types-used-in-the-vml-object-model">Вгпоситивенумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="d4aef-396">Задает аспект сцены.</span><span class="sxs-lookup"><span data-stu-id="d4aef-396">Sets the facet of the scene.</span></span> <span data-ttu-id="d4aef-397">Значение по умолчанию — &quot; 30 000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-397">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-398">форедепс</span><span class="sxs-lookup"><span data-stu-id="d4aef-398">ForeDepth</span></span></td>
<td><span data-ttu-id="d4aef-399"><a href="msdn-online-vml-vglength.md">Вгленгс</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-399"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="d4aef-400">Объем пересылки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-400">Amount of forward extrusion.</span></span> <span data-ttu-id="d4aef-401">В диапазоне от 0 до 32767.</span><span class="sxs-lookup"><span data-stu-id="d4aef-401">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-402">лигхтфаце</span><span class="sxs-lookup"><span data-stu-id="d4aef-402">LightFace</span></span></td>
<td><span data-ttu-id="d4aef-403"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-404">Детермимес, будет ли лицевая сторона объекта отвечать на изменения в трехмерном освещении, например при повороте объекта.</span><span class="sxs-lookup"><span data-stu-id="d4aef-404">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-405">лигхсарш</span><span class="sxs-lookup"><span data-stu-id="d4aef-405">LightHarsh</span></span></td>
<td><span data-ttu-id="d4aef-406"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-407">Харша освещение для основного источника света.</span><span class="sxs-lookup"><span data-stu-id="d4aef-407">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="d4aef-408">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="d4aef-408">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-409">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="d4aef-409">LightHarsh2</span></span></td>
<td><span data-ttu-id="d4aef-410"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-411">Харша освещение для дополнительного источника света.</span><span class="sxs-lookup"><span data-stu-id="d4aef-411">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="d4aef-412">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="d4aef-412">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-413">лигхтлевел</span><span class="sxs-lookup"><span data-stu-id="d4aef-413">LightLevel</span></span></td>
<td><span data-ttu-id="d4aef-414"><a href="#data-types-used-in-the-vml-object-model">Вгнумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="d4aef-415">Интенсивность основного источника освещения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-415">Intensity of the primary light source.</span></span> <span data-ttu-id="d4aef-416">Значение по умолчанию — &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-416">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-417">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="d4aef-417">LightLevel2</span></span></td>
<td><span data-ttu-id="d4aef-418"><a href="#data-types-used-in-the-vml-object-model">Вгнумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="d4aef-419">Интенсивность вторичного источника освещения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-419">Intensity of the secondary light source.</span></span> <span data-ttu-id="d4aef-420">Значение по умолчанию — &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-420">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-421">лигхтпоситион</span><span class="sxs-lookup"><span data-stu-id="d4aef-421">LightPosition</span></span></td>
<td><span data-ttu-id="d4aef-422">Объект.</span><span class="sxs-lookup"><span data-stu-id="d4aef-422">Vector3D.</span></span> <span data-ttu-id="d4aef-423">Расположение основного источника освещения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-423">Position of the primary light source.</span></span> <span data-ttu-id="d4aef-424">Значение по умолчанию — &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-424">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-425">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="d4aef-425">LightPosition2</span></span></td>
<td><span data-ttu-id="d4aef-426">Объект.</span><span class="sxs-lookup"><span data-stu-id="d4aef-426">Vector3D.</span></span> <span data-ttu-id="d4aef-427">Расположение вторичного источника освещения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-427">Position of the secondary light source.</span></span> <span data-ttu-id="d4aef-428">Значение по умолчанию — &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-428">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-429">локкротатионцентер</span><span class="sxs-lookup"><span data-stu-id="d4aef-429">LockRotationCenter</span></span></td>
<td><span data-ttu-id="d4aef-430"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-431">&quot;Локкротатионцентер &quot; означает, что поворот группы определяется как угловой угол [1] градусов вокруг оси y на странице, за которым следует угол поворота [0] градусов относительно оси x.</span><span class="sxs-lookup"><span data-stu-id="d4aef-431">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="d4aef-432">Если Локкротатионцентер имеет значение false, поворот определяется как угол в градусах с направлением вниз относительно вектора, определенного ориентацией.</span><span class="sxs-lookup"><span data-stu-id="d4aef-432">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="d4aef-433">Например, локкротатионцентер = false ориентатионангле = 45 Orientation = (0, 1, 0) эквивалентно локкротатионцентер = true ротатионангле = (0, 45).</span><span class="sxs-lookup"><span data-stu-id="d4aef-433">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-434">Металлические</span><span class="sxs-lookup"><span data-stu-id="d4aef-434">Metal</span></span></td>
<td><span data-ttu-id="d4aef-435"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-436">Приводит к тому, что отраженный свет отражается цветом материала вместо цвета источника, что делает объект более металлным.</span><span class="sxs-lookup"><span data-stu-id="d4aef-436">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-437">Включено</span><span class="sxs-lookup"><span data-stu-id="d4aef-437">On</span></span></td>
<td><span data-ttu-id="d4aef-438"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-439">Включает и выключает отображение воздействия на объемные придания.</span><span class="sxs-lookup"><span data-stu-id="d4aef-439">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-440">Orientation</span><span class="sxs-lookup"><span data-stu-id="d4aef-440">Orientation</span></span></td>
<td><span data-ttu-id="d4aef-441">Объект.</span><span class="sxs-lookup"><span data-stu-id="d4aef-441">Vector3D.</span></span> <span data-ttu-id="d4aef-442">Ориентация камеры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-442">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-443">ориентатионангле</span><span class="sxs-lookup"><span data-stu-id="d4aef-443">OrientationAngle</span></span></td>
<td><span data-ttu-id="d4aef-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">Вганглеиндегрис</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="d4aef-445">Угол между ориентацией камеры и плоскости XY.</span><span class="sxs-lookup"><span data-stu-id="d4aef-445">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-446">Плоскости</span><span class="sxs-lookup"><span data-stu-id="d4aef-446">Plane</span></span></td>
<td><span data-ttu-id="d4aef-447">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="d4aef-447">Vg3DExtrudePlane.</span></span> <span data-ttu-id="d4aef-448">Позволяет проделать объемы от плоскостей ортогональной плоскости экрана.</span><span class="sxs-lookup"><span data-stu-id="d4aef-448">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="d4aef-449">Требуется указать Форедепс и depth в единицах рисования вместо емус.</span><span class="sxs-lookup"><span data-stu-id="d4aef-449">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="d4aef-450">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-450">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-451">ТОЧЕЧ</span><span class="sxs-lookup"><span data-stu-id="d4aef-451">XY</span></span></li>
<li><span data-ttu-id="d4aef-452">зкс</span><span class="sxs-lookup"><span data-stu-id="d4aef-452">ZX</span></span></li>
<li><span data-ttu-id="d4aef-453">из</span><span class="sxs-lookup"><span data-stu-id="d4aef-453">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-454">Render</span><span class="sxs-lookup"><span data-stu-id="d4aef-454">Render</span></span></td>
<td><span data-ttu-id="d4aef-455">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="d4aef-455">Vg3DRenderMode.</span></span> <span data-ttu-id="d4aef-456">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-456">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-457">Solid (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-457">Solid (default)</span></span></li>
<li><span data-ttu-id="d4aef-458">Каркасной модели</span><span class="sxs-lookup"><span data-stu-id="d4aef-458">WireFrame</span></span></li>
<li><span data-ttu-id="d4aef-459">баундингкубе</span><span class="sxs-lookup"><span data-stu-id="d4aef-459">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-460">RotationAngle (Угол поворота)</span><span class="sxs-lookup"><span data-stu-id="d4aef-460">RotationAngle</span></span></td>
<td><span data-ttu-id="d4aef-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="d4aef-462">AngleX, Angle или Англез управляются атрибутом Шаперотатион.</span><span class="sxs-lookup"><span data-stu-id="d4aef-462">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-463">ротатионцентер</span><span class="sxs-lookup"><span data-stu-id="d4aef-463">RotationCenter</span></span></td>
<td><span data-ttu-id="d4aef-464">Объект.</span><span class="sxs-lookup"><span data-stu-id="d4aef-464">Vector3D.</span></span> <span data-ttu-id="d4aef-465">Центр вращения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-465">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-466">Коэффициента блеска</span><span class="sxs-lookup"><span data-stu-id="d4aef-466">Shininess</span></span></td>
<td><span data-ttu-id="d4aef-467"><a href="#data-types-used-in-the-vml-object-model">Вгпоситивенумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="d4aef-468">Определяет, как работает зеркальное отражение Concentrated или распределения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-468">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="d4aef-469">Высокое значение будет равно 8 – 10 и приблизительно равно зеркалу, а низкое значение — от 2 до 3 и приблизительно секуинед одежда.</span><span class="sxs-lookup"><span data-stu-id="d4aef-469">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="d4aef-470">Рекомендуется использовать значения от 3 до 7.</span><span class="sxs-lookup"><span data-stu-id="d4aef-470">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="d4aef-471">При высоком значении будут отражаться источники освещения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-471">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-472">скевамт</span><span class="sxs-lookup"><span data-stu-id="d4aef-472">SkewAmt</span></span></td>
<td><span data-ttu-id="d4aef-473"><a href="#data-types-used-in-the-vml-object-model">Вгперцентаже</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="d4aef-474">Если тип — Parallel, атрибут определяет величину наклона.</span><span class="sxs-lookup"><span data-stu-id="d4aef-474">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="d4aef-475">В диапазоне от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="d4aef-475">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-476">скевангле</span><span class="sxs-lookup"><span data-stu-id="d4aef-476">SkewAngle</span></span></td>
<td><span data-ttu-id="d4aef-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">Вганглеиндегрис</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="d4aef-478">Если тип — Parallel, атрибут определяет степень наклона.</span><span class="sxs-lookup"><span data-stu-id="d4aef-478">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="d4aef-479">Значение по умолчанию — &quot; 45 &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-479">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-480">Отраженность</span><span class="sxs-lookup"><span data-stu-id="d4aef-480">Specularity</span></span></td>
<td><span data-ttu-id="d4aef-481"><a href="#data-types-used-in-the-vml-object-model">Вгпоситивенумбер</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="d4aef-482">Отношение инцидента к отраженно отраженному свету.</span><span class="sxs-lookup"><span data-stu-id="d4aef-482">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="d4aef-483">Значения меньше 1,0 являются нормальными, но значения, превышающие один, могут создавать интересные эффекты.</span><span class="sxs-lookup"><span data-stu-id="d4aef-483">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-484">Type</span><span class="sxs-lookup"><span data-stu-id="d4aef-484">Type</span></span></td>
<td><span data-ttu-id="d4aef-485">Вжекструсионтипе.</span><span class="sxs-lookup"><span data-stu-id="d4aef-485">VgExtrusionType.</span></span> <span data-ttu-id="d4aef-486">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-486">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-487">Parallel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-487">Parallel (default)</span></span></li>
<li><span data-ttu-id="d4aef-488">Перспектива</span><span class="sxs-lookup"><span data-stu-id="d4aef-488">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-489">Окна</span><span class="sxs-lookup"><span data-stu-id="d4aef-489">Viewpoint</span></span></td>
<td><span data-ttu-id="d4aef-490">Объект.</span><span class="sxs-lookup"><span data-stu-id="d4aef-490">Vector3D.</span></span> <span data-ttu-id="d4aef-491">Точка, из которой просматривается сцена.</span><span class="sxs-lookup"><span data-stu-id="d4aef-491">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-492">виевпоинторигин</span><span class="sxs-lookup"><span data-stu-id="d4aef-492">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="d4aef-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="d4aef-494">Могут иметь значения от 0,5 до-0,5 для позиционирования источника точки зрения в ограничивающем прямоугольнике фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-494">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="d4aef-495">Fill, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-495">Fill element</span></span>

<span data-ttu-id="d4aef-496">Описывает, как должен быть заполнен контур для заливки более сложным, чем сплошной цвет.</span><span class="sxs-lookup"><span data-stu-id="d4aef-496">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="d4aef-497">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="d4aef-497">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-498">алигншапе</span><span class="sxs-lookup"><span data-stu-id="d4aef-498">AlignShape</span></span></td>
<td><span data-ttu-id="d4aef-499"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-500">Выровняйте изображение с фигурой.</span><span class="sxs-lookup"><span data-stu-id="d4aef-500">Align the image with the shape.</span></span> <span data-ttu-id="d4aef-501">Если значение равно false, выровняйте изображение с помощью окна.</span><span class="sxs-lookup"><span data-stu-id="d4aef-501">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-502">Angle</span><span class="sxs-lookup"><span data-stu-id="d4aef-502">Angle</span></span></td>
<td><span data-ttu-id="d4aef-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">Вганглеиндегрис</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="d4aef-504">Угол, вдоль которого переходит градиент.</span><span class="sxs-lookup"><span data-stu-id="d4aef-504">The angle along which the gradient goes.</span></span> <span data-ttu-id="d4aef-505">0 градусов находится вдоль горизонтальной оси слева направо.</span><span class="sxs-lookup"><span data-stu-id="d4aef-505">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-506">Аспект</span><span class="sxs-lookup"><span data-stu-id="d4aef-506">Aspect</span></span></td>
<td><span data-ttu-id="d4aef-507"><strong>Вгаспекттипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-507"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="d4aef-508">Атрибут ImageSize будет скорректирован для сохранения аспекта изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-508">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="d4aef-509">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="d4aef-509">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d4aef-510">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-510">Value</span></span></th>
<th><span data-ttu-id="d4aef-511">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-511">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-512">Игнорировать</span><span class="sxs-lookup"><span data-stu-id="d4aef-512">Ignore</span></span></td>
<td><span data-ttu-id="d4aef-513">Пропускать проблемы с аспектами.</span><span class="sxs-lookup"><span data-stu-id="d4aef-513">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-514">Задать</span><span class="sxs-lookup"><span data-stu-id="d4aef-514">AtLeast</span></span></td>
<td><span data-ttu-id="d4aef-515">Размер изображения не меньше размера изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-515">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-516">атмост</span><span class="sxs-lookup"><span data-stu-id="d4aef-516">AtMost</span></span></td>
<td><span data-ttu-id="d4aef-517">Изображение не превышает размер изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-517">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-518">Цвет</span><span class="sxs-lookup"><span data-stu-id="d4aef-518">Color</span></span></td>
<td><span data-ttu-id="d4aef-519"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a> Основной цвет заливки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="d4aef-520">То же, что и атрибут FillColor в фигуре.</span><span class="sxs-lookup"><span data-stu-id="d4aef-520">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-521">Color2</span><span class="sxs-lookup"><span data-stu-id="d4aef-521">Color2</span></span></td>
<td><span data-ttu-id="d4aef-522"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="d4aef-523">Вторичный цвет заливки, если тип изображения — Pattern или градиентная заливка.</span><span class="sxs-lookup"><span data-stu-id="d4aef-523">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-524">Цвета</span><span class="sxs-lookup"><span data-stu-id="d4aef-524">Colors</span></span></td>
<td><span data-ttu-id="d4aef-525"><a href="#data-types-used-in-the-vml-object-model">Ивгградиентколораррай</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="d4aef-526">Промежуточные цвета в градиенте и их относительные позиции вдоль градиента, например, &quot; 30% красного, 70% голубого, 90% зеленого цвета &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-526">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="d4aef-527">Основной цвет (атрибут цвета в фигуре) равен 0% и вторичному цвету (атрибут color2) равен 100%.</span><span class="sxs-lookup"><span data-stu-id="d4aef-527">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-528">Фокус</span><span class="sxs-lookup"><span data-stu-id="d4aef-528">Focus</span></span></td>
<td><span data-ttu-id="d4aef-529"><a href="#data-types-used-in-the-vml-object-model">Вгсигнедперцентаже</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="d4aef-530">Фокальная точка для линейной градиентной заливки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-530">Focal point for linear gradient fill.</span></span> <span data-ttu-id="d4aef-531">Значения переходят от-100 до + 100.</span><span class="sxs-lookup"><span data-stu-id="d4aef-531">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-532">фокуспоситион</span><span class="sxs-lookup"><span data-stu-id="d4aef-532">FocusPosition</span></span></td>
<td><span data-ttu-id="d4aef-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="d4aef-534">Позиция самого внутреннего прямоугольника для радиальных градиентов.</span><span class="sxs-lookup"><span data-stu-id="d4aef-534">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="d4aef-535">Вектор представляет собой дробную часть (0,0-1,0) ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-535">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-536">фокуссизе</span><span class="sxs-lookup"><span data-stu-id="d4aef-536">FocusSize</span></span></td>
<td><span data-ttu-id="d4aef-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Размер самого внутреннего прямоугольника для радиальных градиентов.</span><span class="sxs-lookup"><span data-stu-id="d4aef-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="d4aef-538">Вектор представляет собой дробную часть (0,0 – 1,0) ширины и высоты фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-538">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-539">Метод</span><span class="sxs-lookup"><span data-stu-id="d4aef-539">Method</span></span></td>
<td><span data-ttu-id="d4aef-540">Вгсигматипе.</span><span class="sxs-lookup"><span data-stu-id="d4aef-540">VgSigmaType.</span></span> <span data-ttu-id="d4aef-541">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="d4aef-541">Values include:</span></span>
<ul>
<li><span data-ttu-id="d4aef-542">Нет</span><span class="sxs-lookup"><span data-stu-id="d4aef-542">None</span></span></li>
<li><span data-ttu-id="d4aef-543">Линейная</span><span class="sxs-lookup"><span data-stu-id="d4aef-543">Linear</span></span></li>
<li><span data-ttu-id="d4aef-544">Sigma</span><span class="sxs-lookup"><span data-stu-id="d4aef-544">Sigma</span></span></li>
<li><span data-ttu-id="d4aef-545">Любой</span><span class="sxs-lookup"><span data-stu-id="d4aef-545">Any</span></span></li>
</ul>
<p><span data-ttu-id="d4aef-546">Значение по умолчанию — Сигма.</span><span class="sxs-lookup"><span data-stu-id="d4aef-546">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-547">Включено</span><span class="sxs-lookup"><span data-stu-id="d4aef-547">On</span></span></td>
<td><span data-ttu-id="d4aef-548"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-549">Включает отображение экрана.</span><span class="sxs-lookup"><span data-stu-id="d4aef-549">Turns fill display on.</span></span> <span data-ttu-id="d4aef-550">То же, что и атрибут Fill в Shape.</span><span class="sxs-lookup"><span data-stu-id="d4aef-550">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-551">Непрозрачность</span><span class="sxs-lookup"><span data-stu-id="d4aef-551">Opacity</span></span></td>
<td><span data-ttu-id="d4aef-552"><a href="msdn-online-vml-vgfraction-data-type.md">Вгфрактион</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="d4aef-553">Непрозрачность заливки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-553">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-554">Opacity2</span><span class="sxs-lookup"><span data-stu-id="d4aef-554">Opacity2</span></span></td>
<td><span data-ttu-id="d4aef-555"><a href="msdn-online-vml-vgfraction-data-type.md">Вгфрактион</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="d4aef-556">Дополнительная непрозрачность для градиентов.</span><span class="sxs-lookup"><span data-stu-id="d4aef-556">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-557">Исходный домен</span><span class="sxs-lookup"><span data-stu-id="d4aef-557">Origin</span></span></td>
<td><span data-ttu-id="d4aef-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="d4aef-559">Точка относительно левого верхнего угла изображения, которое обрабатывается как источник изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-559">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="d4aef-560">По умолчанию используется центр изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-560">Default is the center of the image.</span></span> <span data-ttu-id="d4aef-561">Вектор представляет собой дробную часть (от 0,0 до 1,0) ширины и высоты изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-561">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-562">Положение</span><span class="sxs-lookup"><span data-stu-id="d4aef-562">Position</span></span></td>
<td><span data-ttu-id="d4aef-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="d4aef-564">Наведите указатель на ссылочный прямоугольник фигуры, чтобы разместить точку начала изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-564">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="d4aef-565">По умолчанию используется центр прямоугольника контейнера.</span><span class="sxs-lookup"><span data-stu-id="d4aef-565">Default is the center of the container rectangle.</span></span> <span data-ttu-id="d4aef-566">Вектор представляет собой дробную часть (0,0-1,0) ширины и высоты изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-566">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-567">Размер</span><span class="sxs-lookup"><span data-stu-id="d4aef-567">Size</span></span></td>
<td><span data-ttu-id="d4aef-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="d4aef-569">Размер изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-569">The size of the image.</span></span> <span data-ttu-id="d4aef-570">Значение по умолчанию — размер изображения в пикселях.</span><span class="sxs-lookup"><span data-stu-id="d4aef-570">Default is pixel size of the image.</span></span> <span data-ttu-id="d4aef-571">Может указываться в абсолютных координатах или в процентах.</span><span class="sxs-lookup"><span data-stu-id="d4aef-571">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-572">Источник</span><span class="sxs-lookup"><span data-stu-id="d4aef-572">Src</span></span></td>
<td><span data-ttu-id="d4aef-573"><a href="#data-types-used-in-the-vml-object-model">Строка</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-573"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="d4aef-574">URL-адрес изображения, загружаемого для изображений и узорных заливок.</span><span class="sxs-lookup"><span data-stu-id="d4aef-574">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="d4aef-575">Этот атрибут всегда должен присутствовать и указывать на допустимые данные изображения для отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-575">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-576">Type</span><span class="sxs-lookup"><span data-stu-id="d4aef-576">Type</span></span></td>
<td><span data-ttu-id="d4aef-577">Вгфиллтипе.</span><span class="sxs-lookup"><span data-stu-id="d4aef-577">VgFillType.</span></span> <span data-ttu-id="d4aef-578">Принимается один из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="d4aef-578">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="d4aef-579">Историческая справка</span><span class="sxs-lookup"><span data-stu-id="d4aef-579">Background</span></span></li>
<li><span data-ttu-id="d4aef-580">Frame</span><span class="sxs-lookup"><span data-stu-id="d4aef-580">Frame</span></span></li>
<li><span data-ttu-id="d4aef-581">Градиент</span><span class="sxs-lookup"><span data-stu-id="d4aef-581">Gradient</span></span></li>
<li><span data-ttu-id="d4aef-582">градиентцентер</span><span class="sxs-lookup"><span data-stu-id="d4aef-582">GradientCenter</span></span></li>
<li><span data-ttu-id="d4aef-583">градиентрадиал</span><span class="sxs-lookup"><span data-stu-id="d4aef-583">GradientRadial</span></span></li>
<li><span data-ttu-id="d4aef-584">градиенттитле</span><span class="sxs-lookup"><span data-stu-id="d4aef-584">GradientTitle</span></span></li>
<li><span data-ttu-id="d4aef-585">градиентунскалед</span><span class="sxs-lookup"><span data-stu-id="d4aef-585">GradientUnscaled</span></span></li>
<li><span data-ttu-id="d4aef-586">Шаблон</span><span class="sxs-lookup"><span data-stu-id="d4aef-586">Pattern</span></span></li>
<li><span data-ttu-id="d4aef-587">Сплошная</span><span class="sxs-lookup"><span data-stu-id="d4aef-587">Solid</span></span></li>
<li><span data-ttu-id="d4aef-588">Tile</span><span class="sxs-lookup"><span data-stu-id="d4aef-588">Tile</span></span></li>
</ul>
<span data-ttu-id="d4aef-589">Для плитки, шаблона и фрейма необходимо предоставить атрибуты изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-589">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="d4aef-590">Для градиента и Градиентрадиал требуется предоставить атрибуты градиента.</span><span class="sxs-lookup"><span data-stu-id="d4aef-590">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="d4aef-591">Group, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-591">Group element</span></span>

<span data-ttu-id="d4aef-592">Группа — это коллекция отдельных фигур, которые могут быть размещены и преобразованы как единое целое.</span><span class="sxs-lookup"><span data-stu-id="d4aef-592">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|   <span data-ttu-id="d4aef-593">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-593">Attribute</span></span>        |   <span data-ttu-id="d4aef-594">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-594">Description</span></span>                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-595">Item</span><span class="sxs-lookup"><span data-stu-id="d4aef-595">Item</span></span>   | <span data-ttu-id="d4aef-596">[Ивгшапе](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-597">Указанный элемент в массиве фигур.</span><span class="sxs-lookup"><span data-stu-id="d4aef-597">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="d4aef-598">Длина</span><span class="sxs-lookup"><span data-stu-id="d4aef-598">Length</span></span> | <span data-ttu-id="d4aef-599">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-599">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-600">Число фигур в этой группе.</span><span class="sxs-lookup"><span data-stu-id="d4aef-600">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="d4aef-601">Имажедата, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-601">Imagedata element</span></span>

<span data-ttu-id="d4aef-602">Описывает изображение, которое подготавливается к просмотру поверх фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-602">Describes a picture to be rendered on top of a shape.</span></span>



|   <span data-ttu-id="d4aef-603">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-603">Attribute</span></span>        |   <span data-ttu-id="d4aef-604">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-604">Description</span></span>                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-605">билевел</span><span class="sxs-lookup"><span data-stu-id="d4aef-605">BiLevel</span></span>     | <span data-ttu-id="d4aef-606">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-606">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-607">Отображать изображение только в двух цветах (обычно это черно-белое).</span><span class="sxs-lookup"><span data-stu-id="d4aef-607">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="d4aef-608">блакклевел</span><span class="sxs-lookup"><span data-stu-id="d4aef-608">BlackLevel</span></span>  | <span data-ttu-id="d4aef-609">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="d4aef-610">Позволяет настроить уровень, чтобы черный цвет отображался как истинный черный, а все остальные цвета отображались как оттенки выше черного цвета.</span><span class="sxs-lookup"><span data-stu-id="d4aef-610">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="d4aef-611">чромакэй</span><span class="sxs-lookup"><span data-stu-id="d4aef-611">Chromakey</span></span>   | <span data-ttu-id="d4aef-612">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="d4aef-613">Прозрачный цвет изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-613">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d4aef-614">кропботтом</span><span class="sxs-lookup"><span data-stu-id="d4aef-614">CropBottom</span></span>  | <span data-ttu-id="d4aef-615">[Вгнумбер](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-616">Обрезать расстояние от нижней границы изображения в процентах от размера изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-616">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="d4aef-617">кроплефт</span><span class="sxs-lookup"><span data-stu-id="d4aef-617">CropLeft</span></span>    | <span data-ttu-id="d4aef-618">[Вгнумбер](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-619">Обрезка расстояния от левого края изображения, выраженного в виде доли размера изображения (от 0,0 до 1,0).</span><span class="sxs-lookup"><span data-stu-id="d4aef-619">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="d4aef-620">Однако поддерживается «out-кадрирование», поэтому поддерживаются значения меньше 0 и больше 1. Например,-5, 20 — обрезать границы, 25X размер изображения с 4/5 на одной стороне изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-620">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="d4aef-621">кропригхт</span><span class="sxs-lookup"><span data-stu-id="d4aef-621">CropRight</span></span>   | <span data-ttu-id="d4aef-622">[Вгнумбер](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-622">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-623">Обрезать расстояние справа от рисунка, выраженное в процентах от размера изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-623">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="d4aef-624">кроптоп</span><span class="sxs-lookup"><span data-stu-id="d4aef-624">CropTop</span></span>     | <span data-ttu-id="d4aef-625">[Вгнумбер](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-625">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-626">Обрезать расстояние от верхнего края изображения, выраженное в процентах от размера изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-626">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="d4aef-627">ембоссколор</span><span class="sxs-lookup"><span data-stu-id="d4aef-627">EmbossColor</span></span> | <span data-ttu-id="d4aef-628">[Ивгколор](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="d4aef-629">Это значение задается в процентах от цвета тени для создания эффекта рельефного изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-629">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="d4aef-630">Выигрыш</span><span class="sxs-lookup"><span data-stu-id="d4aef-630">Gain</span></span>        | <span data-ttu-id="d4aef-631">[Вгпоситивенумбер](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-632">Корректирует интенсивность всех цветов.</span><span class="sxs-lookup"><span data-stu-id="d4aef-632">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="d4aef-633">По сути, определяет, насколько ярко будет белый цвет.</span><span class="sxs-lookup"><span data-stu-id="d4aef-633">Essentially sets how bright white will be.</span></span> <span data-ttu-id="d4aef-634">В диапазоне от 0 до 32767.</span><span class="sxs-lookup"><span data-stu-id="d4aef-634">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="d4aef-635">Gamma</span><span class="sxs-lookup"><span data-stu-id="d4aef-635">Gamma</span></span>       | <span data-ttu-id="d4aef-636">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="d4aef-637">Гамма-коррекция.</span><span class="sxs-lookup"><span data-stu-id="d4aef-637">Gamma correction.</span></span> <span data-ttu-id="d4aef-638">Увеличение этого числа повышает контрастность изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-638">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="d4aef-639">GrayScale</span><span class="sxs-lookup"><span data-stu-id="d4aef-639">GrayScale</span></span>   | <span data-ttu-id="d4aef-640">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-640">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-641">Отображать изображение в оттенках серого.</span><span class="sxs-lookup"><span data-stu-id="d4aef-641">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d4aef-642">Источник</span><span class="sxs-lookup"><span data-stu-id="d4aef-642">Src</span></span>         | <span data-ttu-id="d4aef-643">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-643">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-644">URL-адрес изображения, загружаемого для изображений и узорных заливок.</span><span class="sxs-lookup"><span data-stu-id="d4aef-644">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="d4aef-645">Этот атрибут всегда должен присутствовать и указывать на допустимые данные изображения для отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-645">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="d4aef-646">Path, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-646">Path element</span></span>

<span data-ttu-id="d4aef-647">Определяет путь, составляющий фигуру, с помощью строки, содержащей обширный набор команд "перемещение пером".</span><span class="sxs-lookup"><span data-stu-id="d4aef-647">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-648">лимо</span><span class="sxs-lookup"><span data-stu-id="d4aef-648">Limo</span></span></td>
<td><span data-ttu-id="d4aef-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="d4aef-650">Определяет точку растяжения фигуры. Например, для фигуры Giraffe точка Лимо будет находиться на горловине, поэтому при изменении размера фигуры объект горловина будет растянут, а оставшаяся часть фигуры сохранит свои размеры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-650">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-651">текстбоксрект</span><span class="sxs-lookup"><span data-stu-id="d4aef-651">TextBoxRect</span></span></td>
<td><span data-ttu-id="d4aef-652"><a href="#data-types-used-in-the-vml-object-model">Ивгфикседректанглеаррай</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="d4aef-653">Массив, содержащий прямоугольники, определяющие, где должен идти текст.</span><span class="sxs-lookup"><span data-stu-id="d4aef-653">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-654">V</span><span class="sxs-lookup"><span data-stu-id="d4aef-654">V</span></span></td>
<td><span data-ttu-id="d4aef-655"><a href="#data-types-used-in-the-vml-object-model">Строка</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-655"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="d4aef-656">Соответствует атрибуту v в теге Path.</span><span class="sxs-lookup"><span data-stu-id="d4aef-656">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="d4aef-657">Обратите внимание, что путь может соответствовать атрибуту или элементу Path.</span><span class="sxs-lookup"><span data-stu-id="d4aef-657">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-658">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-658">Value</span></span></td>
<td><span data-ttu-id="d4aef-659"><a href="#data-types-used-in-the-vml-object-model">Строка</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-659"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="d4aef-660">Текстовое представление команд, определяющих путь.</span><span class="sxs-lookup"><span data-stu-id="d4aef-660">A text representation of the commands that define the path.</span></span> <span data-ttu-id="d4aef-661">Значения координат X или y могут быть ссылкой на формулу в форме &quot; @# &quot; , где # — это порядковый номер формулы, например &quot; @2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-661">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="d4aef-662">Эта строка атрибута состоит из обширного набора команд, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="d4aef-662">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d4aef-663">Команда</span><span class="sxs-lookup"><span data-stu-id="d4aef-663">Command</span></span></th>
<th><span data-ttu-id="d4aef-664">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-664">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-665">AE (англиллипсето)</span><span class="sxs-lookup"><span data-stu-id="d4aef-665">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="d4aef-666"><strong>центрированный</strong>(x, y) <strong>Размер</strong>(w, h) <strong>начальный угол</strong>, <strong>конечный угол</strong></span><span class="sxs-lookup"><span data-stu-id="d4aef-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="d4aef-667">Нарисуйте сегмент эллипса.</span><span class="sxs-lookup"><span data-stu-id="d4aef-667">Draw a segment of an ellipse.</span></span> <span data-ttu-id="d4aef-668">Прямая линия рисуется от текущей точки к начальной точке сегмента.</span><span class="sxs-lookup"><span data-stu-id="d4aef-668">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-669">Al (англилипсе)</span><span class="sxs-lookup"><span data-stu-id="d4aef-669">al (angleelipse)</span></span></td>
<td><span data-ttu-id="d4aef-670">То же, что и AE, за исключением того, что в начальную точку сегмента присутствует подразумеваемое значение m.</span><span class="sxs-lookup"><span data-stu-id="d4aef-670">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-671">AR (Дуга)</span><span class="sxs-lookup"><span data-stu-id="d4aef-671">ar (arc)</span></span></td>
<td><span data-ttu-id="d4aef-672">То же, что и в.</span><span class="sxs-lookup"><span data-stu-id="d4aef-672">Same as at.</span></span> <span data-ttu-id="d4aef-673">Однако новый вложенный путь начинается неявным m в начальной точке дуги.</span><span class="sxs-lookup"><span data-stu-id="d4aef-673">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-674">в (аркто)</span><span class="sxs-lookup"><span data-stu-id="d4aef-674">at (arcto)</span></span></td>
<td><span data-ttu-id="d4aef-675"><strong>слева</strong>, <strong>сверху</strong>, <strong>справа</strong>, <strong>снизу</strong>, <strong>Начало</strong>(x, y), <strong>конец</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="d4aef-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="d4aef-676">Первые четыре значения определяют ограничивающий прямоугольник эллипса.</span><span class="sxs-lookup"><span data-stu-id="d4aef-676">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="d4aef-677">Последние четыре определяют два радиальных вектора.</span><span class="sxs-lookup"><span data-stu-id="d4aef-677">The last four define two radial vectors.</span></span> <span data-ttu-id="d4aef-678">Рисуется сегмент эллипса, который начинается с угла, определенного начальным вектором, и заканчивается на угол, определенный конечным вектором.</span><span class="sxs-lookup"><span data-stu-id="d4aef-678">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="d4aef-679">Прямая линия рисуется от текущей точки до начала дуги. Дуга всегда отображается в направлении против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-679">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-680">c (курвето)</span><span class="sxs-lookup"><span data-stu-id="d4aef-680">c (curveto)</span></span></td>
<td><span data-ttu-id="d4aef-681"><strong>Control1</strong>(x, y) <strong>control2</strong>(x, y) <strong>к</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="d4aef-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="d4aef-682">Рисование кривой Безье третьего порядка от текущей точки до координат, заданных последними двумя параметрами, контрольные точки, заданные первыми четырьмя параметрами.</span><span class="sxs-lookup"><span data-stu-id="d4aef-682">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="d4aef-683">Текущая точка преобразуется в конечную точку Безье.</span><span class="sxs-lookup"><span data-stu-id="d4aef-683">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-684">e (конец)</span><span class="sxs-lookup"><span data-stu-id="d4aef-684">e (end)</span></span></td>
<td><span data-ttu-id="d4aef-685">Завершение текущего набора вложенных путей.</span><span class="sxs-lookup"><span data-stu-id="d4aef-685">End the current set of subpaths.</span></span> <span data-ttu-id="d4aef-686">Заданный набор вложенных путей (разделенных End) заполняется с помощью еофилл.</span><span class="sxs-lookup"><span data-stu-id="d4aef-686">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="d4aef-687">Последующие наборы вложенных путей заполняются независимо друг от друга и накладываются на существующие.</span><span class="sxs-lookup"><span data-stu-id="d4aef-687">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-688">l (lineTo)</span><span class="sxs-lookup"><span data-stu-id="d4aef-688">l (lineto)</span></span></td>
<td><span data-ttu-id="d4aef-689">x, y</span><span class="sxs-lookup"><span data-stu-id="d4aef-689">x,y</span></span><br/> <span data-ttu-id="d4aef-690">Нарисуйте линию от текущей точки до заданной координаты x, y, которая станет новой текущей точкой.</span><span class="sxs-lookup"><span data-stu-id="d4aef-690">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="d4aef-691">Для формирования ломаной линии можно указать дополнительные пары координат, например &quot; l 10, 13, 45, 27, 89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-691">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-692">m (MoveTo)</span><span class="sxs-lookup"><span data-stu-id="d4aef-692">m (moveto)</span></span></td>
<td><span data-ttu-id="d4aef-693">x, y</span><span class="sxs-lookup"><span data-stu-id="d4aef-693">x,y</span></span><br/> <span data-ttu-id="d4aef-694">Запуск нового вложенного пути в заданной координате x, y.</span><span class="sxs-lookup"><span data-stu-id="d4aef-694">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-695">NF (без заливки)</span><span class="sxs-lookup"><span data-stu-id="d4aef-695">nf (nofill)</span></span></td>
<td><span data-ttu-id="d4aef-696">Текущий набор вложенных путей (разделенных End) не будет заполнен.</span><span class="sxs-lookup"><span data-stu-id="d4aef-696">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-697">NS (Stroke)</span><span class="sxs-lookup"><span data-stu-id="d4aef-697">ns (nostroke)</span></span></td>
<td><span data-ttu-id="d4aef-698">Текущий набор вложенных путей (разделенных End) не будет обводкой.</span><span class="sxs-lookup"><span data-stu-id="d4aef-698">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-699">QB (куадратикбезиер)</span><span class="sxs-lookup"><span data-stu-id="d4aef-699">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="d4aef-700">(<strong>контролпоинт</strong>(x, y)) \*,<strong>End</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="d4aef-700">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="d4aef-701">Определяет одну или несколько кривых Безье второго типа с помощью контрольных точек и конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-701">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="d4aef-702">Промежуточные (кривые) точки получаются путем интерполяции между последовательными контрольными точками, аналогичными шрифтам TrueType.</span><span class="sxs-lookup"><span data-stu-id="d4aef-702">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="d4aef-703">Вложенный путь не обязательно должен быть начальным, в этом случае вложенный контур закрывается, а последняя точка определяет начальную точку.</span><span class="sxs-lookup"><span data-stu-id="d4aef-703">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-704">ККС (еллиптикалкуадранткс)</span><span class="sxs-lookup"><span data-stu-id="d4aef-704">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="d4aef-705"><strong>конец</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="d4aef-705"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="d4aef-706">Квартальный эллипс рисуется от текущей точки до заданной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-706">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="d4aef-707">Первичный сегмент изначально отношения к линии, параллельной оси x; т. е. сегмент начинается горизонтально.</span><span class="sxs-lookup"><span data-stu-id="d4aef-707">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-708">ки (еллиптикалкуадранти)</span><span class="sxs-lookup"><span data-stu-id="d4aef-708">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="d4aef-709"><strong>конец</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="d4aef-709"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="d4aef-710">То же, что и ККС, за исключением того, что эллиптический сегмент изначально отношения в линию, параллельную оси y; т. е. сегмент начинается по вертикали.</span><span class="sxs-lookup"><span data-stu-id="d4aef-710">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-711">r (рлинето)</span><span class="sxs-lookup"><span data-stu-id="d4aef-711">r (rlineto)</span></span></td>
<td><span data-ttu-id="d4aef-712">x, y</span><span class="sxs-lookup"><span data-stu-id="d4aef-712">x,y</span></span> <br/> <span data-ttu-id="d4aef-713">Нарисуйте линию из текущей точки в относительную координату (кпкс + x, КПИ + y).</span><span class="sxs-lookup"><span data-stu-id="d4aef-713">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="d4aef-714">Если заданы дополнительные пары координат, каждая новая точка будет вычисляться относительно последней.</span><span class="sxs-lookup"><span data-stu-id="d4aef-714">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-715">t (рмовето)</span><span class="sxs-lookup"><span data-stu-id="d4aef-715">t (rmoveto)</span></span></td>
<td><span data-ttu-id="d4aef-716">x, y</span><span class="sxs-lookup"><span data-stu-id="d4aef-716">x,y</span></span><br/> <span data-ttu-id="d4aef-717">Начать новый вложенный путь в относительных координатах (кпкс + x, КПИ + y), где кпкс, КПИ является текущей позицией.</span><span class="sxs-lookup"><span data-stu-id="d4aef-717">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-718">v (курвето)</span><span class="sxs-lookup"><span data-stu-id="d4aef-718">v (curveto)</span></span></td>
<td><span data-ttu-id="d4aef-719"><strong>Control1</strong>(x, y) <strong>control2</strong>(x, y) <strong>к</strong> (x, y)</span><span class="sxs-lookup"><span data-stu-id="d4aef-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="d4aef-720">Кривая Безье третьего порядка с заданными координатами относительно текущей точки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-720">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="d4aef-721">Все точки вычисляются относительно одной и той же начальной точки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-721">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-722">WA (клокквисеаркто)</span><span class="sxs-lookup"><span data-stu-id="d4aef-722">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="d4aef-723">То же, что и, но дуга рисуется в направлении по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="d4aef-723">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-724">WR (клокквисеарк)</span><span class="sxs-lookup"><span data-stu-id="d4aef-724">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="d4aef-725">То же, что и AR, но рисуется в направлении по часовой стрелке.</span><span class="sxs-lookup"><span data-stu-id="d4aef-725">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-726">x (закрытие)</span><span class="sxs-lookup"><span data-stu-id="d4aef-726">x (close)</span></span></td>
<td><span data-ttu-id="d4aef-727">Закрытие текущего вложенного пути путем рисования прямой линии от текущей точки до исходной точки MoveTo.</span><span class="sxs-lookup"><span data-stu-id="d4aef-727">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="d4aef-728">Элемент Shadow</span><span class="sxs-lookup"><span data-stu-id="d4aef-728">Shadow element</span></span>

<span data-ttu-id="d4aef-729">Описывает эффект тени на фигуре.</span><span class="sxs-lookup"><span data-stu-id="d4aef-729">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-730">Цвет</span><span class="sxs-lookup"><span data-stu-id="d4aef-730">Color</span></span></td>
<td><span data-ttu-id="d4aef-731"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="d4aef-732">Цвет основной тени.</span><span class="sxs-lookup"><span data-stu-id="d4aef-732">Color of the primary shadow.</span></span> <span data-ttu-id="d4aef-733">Значение по умолчанию — RGB (128128128)</span><span class="sxs-lookup"><span data-stu-id="d4aef-733">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-734">Color2</span><span class="sxs-lookup"><span data-stu-id="d4aef-734">Color2</span></span></td>
<td><span data-ttu-id="d4aef-735"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="d4aef-736">Цвет второй тени или выделенный фрагмент с рельефной или утопленной тенью.</span><span class="sxs-lookup"><span data-stu-id="d4aef-736">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="d4aef-737">Значение по умолчанию — RGB (203203203).</span><span class="sxs-lookup"><span data-stu-id="d4aef-737">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-738">Матрица</span><span class="sxs-lookup"><span data-stu-id="d4aef-738">Matrix</span></span></td>
<td><span data-ttu-id="d4aef-739"><a href="#data-types-used-in-the-vml-object-model">Ивгскевматрикс</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="d4aef-740">Матрица преобразования перспективы в форме, &quot; скскс, СКСИ, Сикс, сии, px, корректировка &quot; [s = масштаб, p = перспектива].</span><span class="sxs-lookup"><span data-stu-id="d4aef-740">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="d4aef-741">Элементы s определяют, как тень должна масштабироваться относительно фигуры, а элементы p определяют, как тень должна отклоняться относительно фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-741">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="d4aef-742">Например, следующая матрица изменяет размер фигуры на коэффициент, равный 2, и наклоняет его на множитель 4 во всех направлениях.</span><span class="sxs-lookup"><span data-stu-id="d4aef-742">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="d4aef-743">&quot;2, 2, 2, 2, 4, 4&quot;</span><span class="sxs-lookup"><span data-stu-id="d4aef-743">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="d4aef-744">Эта матрица используется только в том случае, если для тени задан тип "Перспектива".</span><span class="sxs-lookup"><span data-stu-id="d4aef-744">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-745">Неясными</span><span class="sxs-lookup"><span data-stu-id="d4aef-745">Obscured</span></span></td>
<td><span data-ttu-id="d4aef-746"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-747">Тень может быть видна, если фигура не заполнена.</span><span class="sxs-lookup"><span data-stu-id="d4aef-747">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="d4aef-748">Значение по умолчанию — False.</span><span class="sxs-lookup"><span data-stu-id="d4aef-748">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-749">Offset</span><span class="sxs-lookup"><span data-stu-id="d4aef-749">Offset</span></span></td>
<td><span data-ttu-id="d4aef-750"><a href="#data-types-used-in-the-vml-object-model">Ивгскевоффсет</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="d4aef-751">Величина смещения x, y от расположения фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-751">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="d4aef-752">Значение по умолчанию — &quot; 2pt, 2PT &quot; .</span><span class="sxs-lookup"><span data-stu-id="d4aef-752">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-753">Offset2</span><span class="sxs-lookup"><span data-stu-id="d4aef-753">Offset2</span></span></td>
<td><span data-ttu-id="d4aef-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="d4aef-755">Величина смещения x, y секунд от расположения фигуры? s.</span><span class="sxs-lookup"><span data-stu-id="d4aef-755">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="d4aef-756">Значения — это либо абсолютное измерение, либо дробное значение Shape (от-0,5 до + 0,5).</span><span class="sxs-lookup"><span data-stu-id="d4aef-756">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-757">Включено</span><span class="sxs-lookup"><span data-stu-id="d4aef-757">On</span></span></td>
<td><span data-ttu-id="d4aef-758"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-759">Включает и выключает отображение тени.</span><span class="sxs-lookup"><span data-stu-id="d4aef-759">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-760">Непрозрачность</span><span class="sxs-lookup"><span data-stu-id="d4aef-760">Opacity</span></span></td>
<td><span data-ttu-id="d4aef-761"><a href="msdn-online-vml-vgfraction-data-type.md">Вгфрактион</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="d4aef-762">Непрозрачность тени.</span><span class="sxs-lookup"><span data-stu-id="d4aef-762">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-763">Исходный домен</span><span class="sxs-lookup"><span data-stu-id="d4aef-763">Origin</span></span></td>
<td><span data-ttu-id="d4aef-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Пара дробных значений Shape с-0,5 по + 0,5.</span><span class="sxs-lookup"><span data-stu-id="d4aef-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-765">Type</span><span class="sxs-lookup"><span data-stu-id="d4aef-765">Type</span></span></td>
<td><span data-ttu-id="d4aef-766"><a href="#data-types-used-in-the-vml-object-model">Вгшадовтипе</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="d4aef-767">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-767">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-768">Single (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-768">Single (default)</span></span></li>
<li><span data-ttu-id="d4aef-769">Double</span><span class="sxs-lookup"><span data-stu-id="d4aef-769">Double</span></span></li>
<li><span data-ttu-id="d4aef-770">Перспектива</span><span class="sxs-lookup"><span data-stu-id="d4aef-770">Perspective</span></span></li>
<li><span data-ttu-id="d4aef-771">шаперелативе</span><span class="sxs-lookup"><span data-stu-id="d4aef-771">ShapeRelative</span></span></li>
<li><span data-ttu-id="d4aef-772">дравингрелативе</span><span class="sxs-lookup"><span data-stu-id="d4aef-772">DrawingRelative</span></span></li>
<li><span data-ttu-id="d4aef-773">Emboss</span><span class="sxs-lookup"><span data-stu-id="d4aef-773">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="d4aef-774">Элемент асимметрии</span><span class="sxs-lookup"><span data-stu-id="d4aef-774">Skew element</span></span>

<span data-ttu-id="d4aef-775">Описывает эффекты наклона перспективы на фигуре.</span><span class="sxs-lookup"><span data-stu-id="d4aef-775">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="d4aef-776">Наклон применяется к векторным графическим данным, а не к данным изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-776">The skew is applied to vector graphic data, not image data.</span></span>



|   <span data-ttu-id="d4aef-777">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-777">Attribute</span></span>        |   <span data-ttu-id="d4aef-778">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-778">Description</span></span>                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-779">Матрица</span><span class="sxs-lookup"><span data-stu-id="d4aef-779">Matrix</span></span> | <span data-ttu-id="d4aef-780">[Ивгскевматрикс](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-781">Матрица преобразования перспективы в форме "скскс, СКСИ, Сикс, сии, px, корректировка" \[ s = масштаб, p = перспектива " \] .</span><span class="sxs-lookup"><span data-stu-id="d4aef-781">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="d4aef-782">Если значение offset в абсолютных единицах, то px, корректировка производится в ЕС ^-1 единиц; в противном случае это обратная часть размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-782">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="d4aef-783">Offset</span><span class="sxs-lookup"><span data-stu-id="d4aef-783">Offset</span></span> | <span data-ttu-id="d4aef-784">[Ивгскевоффсет](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-785">Величина смещения x, y от расположения фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-785">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="d4aef-786">Значение по умолчанию — "2PT, 2PT".</span><span class="sxs-lookup"><span data-stu-id="d4aef-786">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="d4aef-787">Включено</span><span class="sxs-lookup"><span data-stu-id="d4aef-787">On</span></span>     | <span data-ttu-id="d4aef-788">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-788">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-789">Включает или выключает отображение наклона.</span><span class="sxs-lookup"><span data-stu-id="d4aef-789">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="d4aef-790">Исходный домен</span><span class="sxs-lookup"><span data-stu-id="d4aef-790">Origin</span></span> | <span data-ttu-id="d4aef-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="d4aef-792">Пара дробных значений Shape с-0,5 по + 0,5.</span><span class="sxs-lookup"><span data-stu-id="d4aef-792">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="d4aef-793">Элемент Stroke</span><span class="sxs-lookup"><span data-stu-id="d4aef-793">Stroke element</span></span>

<span data-ttu-id="d4aef-794">Описывает, как нарисовать контур, если требуется нечто за сплошной линией с сплошным цветом.</span><span class="sxs-lookup"><span data-stu-id="d4aef-794">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-795">Цвет</span><span class="sxs-lookup"><span data-stu-id="d4aef-795">Color</span></span></td>
<td><span data-ttu-id="d4aef-796"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-797">Цвет линии.</span><span class="sxs-lookup"><span data-stu-id="d4aef-797">The color of the line.</span></span> <span data-ttu-id="d4aef-798">Аналогичен атрибуту Строкеколор в фигуре, но переопределяет его.</span><span class="sxs-lookup"><span data-stu-id="d4aef-798">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-799">Color2</span><span class="sxs-lookup"><span data-stu-id="d4aef-799">Color2</span></span></td>
<td><span data-ttu-id="d4aef-800"><a href="msdn-online-vml-ivgcolor.md">Ивгколор</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="d4aef-801">Вторичный цвет.</span><span class="sxs-lookup"><span data-stu-id="d4aef-801">Secondary color.</span></span> <span data-ttu-id="d4aef-802">Используется, если объекта FillType является шаблоном.</span><span class="sxs-lookup"><span data-stu-id="d4aef-802">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-803">DashStyle</span><span class="sxs-lookup"><span data-stu-id="d4aef-803">DashStyle</span></span></td>
<td><span data-ttu-id="d4aef-804"><strong>Вглинедашстиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-804"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="d4aef-805">Формат пунктирного стиля.</span><span class="sxs-lookup"><span data-stu-id="d4aef-805">Dash style format.</span></span> <span data-ttu-id="d4aef-806">Может представлять собой конкретное значение или последовательность чисел с определяемым пользователем шаблоном штриха.</span><span class="sxs-lookup"><span data-stu-id="d4aef-806">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="d4aef-807">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-807">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-808">Solid (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-808">Solid (default)</span></span></li>
<li><span data-ttu-id="d4aef-809">шортдаш</span><span class="sxs-lookup"><span data-stu-id="d4aef-809">ShortDash</span></span></li>
<li><span data-ttu-id="d4aef-810">шортдот</span><span class="sxs-lookup"><span data-stu-id="d4aef-810">ShortDot</span></span></li>
<li><span data-ttu-id="d4aef-811">шортдашдот</span><span class="sxs-lookup"><span data-stu-id="d4aef-811">ShortDashDot</span></span></li>
<li><span data-ttu-id="d4aef-812">шортдашдотдот</span><span class="sxs-lookup"><span data-stu-id="d4aef-812">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="d4aef-813">Точки</span><span class="sxs-lookup"><span data-stu-id="d4aef-813">Dot</span></span></li>
<li><span data-ttu-id="d4aef-814">Штрих</span><span class="sxs-lookup"><span data-stu-id="d4aef-814">Dash</span></span></li>
<li><span data-ttu-id="d4aef-815">DashDot</span><span class="sxs-lookup"><span data-stu-id="d4aef-815">DashDot</span></span></li>
<li><span data-ttu-id="d4aef-816">лонгдаш</span><span class="sxs-lookup"><span data-stu-id="d4aef-816">LongDash</span></span></li>
<li><span data-ttu-id="d4aef-817">лонгдашдот</span><span class="sxs-lookup"><span data-stu-id="d4aef-817">LongDashDot</span></span></li>
<li><span data-ttu-id="d4aef-818">лонгдашдотдот</span><span class="sxs-lookup"><span data-stu-id="d4aef-818">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-819">ендарров</span><span class="sxs-lookup"><span data-stu-id="d4aef-819">EndArrow</span></span></td>
<td><span data-ttu-id="d4aef-820"><strong>Вгарровхеадстиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-820"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="d4aef-821">Стрелка для конца строки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-821">Arrowhead for the end of the line.</span></span> <span data-ttu-id="d4aef-822">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-822">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-823">Нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-823">None (default)</span></span></li>
<li><span data-ttu-id="d4aef-824">Блокировать</span><span class="sxs-lookup"><span data-stu-id="d4aef-824">Block</span></span></li>
<li><span data-ttu-id="d4aef-825">Классическая</span><span class="sxs-lookup"><span data-stu-id="d4aef-825">Classic</span></span></li>
<li><span data-ttu-id="d4aef-826">Ромб</span><span class="sxs-lookup"><span data-stu-id="d4aef-826">Diamond</span></span></li>
<li><span data-ttu-id="d4aef-827">Овал</span><span class="sxs-lookup"><span data-stu-id="d4aef-827">Oval</span></span></li>
<li><span data-ttu-id="d4aef-828">Открыть</span><span class="sxs-lookup"><span data-stu-id="d4aef-828">Open</span></span></li>
<li><span data-ttu-id="d4aef-829">Шеврон</span><span class="sxs-lookup"><span data-stu-id="d4aef-829">Chevron</span></span></li>
<li><span data-ttu-id="d4aef-830">даублечеврон</span><span class="sxs-lookup"><span data-stu-id="d4aef-830">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-831">ендарровленгс</span><span class="sxs-lookup"><span data-stu-id="d4aef-831">EndArrowLength</span></span></td>
<td><span data-ttu-id="d4aef-832"><strong>Вгарровхеадленгс</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-832"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="d4aef-833">Длина наконечника для конца строки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-833">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="d4aef-834">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-834">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-835">Short</span><span class="sxs-lookup"><span data-stu-id="d4aef-835">Short</span></span></li>
<li><span data-ttu-id="d4aef-836">Среднее (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-836">Medium (default)</span></span></li>
<li><span data-ttu-id="d4aef-837">Long</span><span class="sxs-lookup"><span data-stu-id="d4aef-837">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-838">ендарроввидс</span><span class="sxs-lookup"><span data-stu-id="d4aef-838">EndArrowWidth</span></span></td>
<td><span data-ttu-id="d4aef-839"><strong>Вгарровхеадвидс</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-839"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="d4aef-840">Ширина наконечника для конца строки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-840">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="d4aef-841">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-841">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-842">Разрабатываем</span><span class="sxs-lookup"><span data-stu-id="d4aef-842">Narrow</span></span></li>
<li><span data-ttu-id="d4aef-843">Среднее (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-843">Medium (default)</span></span></li>
<li><span data-ttu-id="d4aef-844">Широкий</span><span class="sxs-lookup"><span data-stu-id="d4aef-844">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-845">ендкап</span><span class="sxs-lookup"><span data-stu-id="d4aef-845">EndCap</span></span></td>
<td><span data-ttu-id="d4aef-846"><strong>Вглининдкапстиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-846"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="d4aef-847">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-847">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-848">плоский</span><span class="sxs-lookup"><span data-stu-id="d4aef-848">Flat</span></span></li>
<li><span data-ttu-id="d4aef-849">Square</span><span class="sxs-lookup"><span data-stu-id="d4aef-849">Square</span></span></li>
<li><span data-ttu-id="d4aef-850">Round</span><span class="sxs-lookup"><span data-stu-id="d4aef-850">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-851">Объекта FillType</span><span class="sxs-lookup"><span data-stu-id="d4aef-851">FillType</span></span></td>
<td><span data-ttu-id="d4aef-852"><strong>Вглинефиллтипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-852"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="d4aef-853">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-853">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-854">Solid (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-854">Solid (default)</span></span></li>
<li><span data-ttu-id="d4aef-855">Tile</span><span class="sxs-lookup"><span data-stu-id="d4aef-855">Tile</span></span></li>
<li><span data-ttu-id="d4aef-856">Шаблон</span><span class="sxs-lookup"><span data-stu-id="d4aef-856">Pattern</span></span></li>
<li><span data-ttu-id="d4aef-857">Frame</span><span class="sxs-lookup"><span data-stu-id="d4aef-857">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-858">имажеалигншапе</span><span class="sxs-lookup"><span data-stu-id="d4aef-858">ImageAlignShape</span></span></td>
<td><span data-ttu-id="d4aef-859"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-860">Выровняйте изображение с фигурой.</span><span class="sxs-lookup"><span data-stu-id="d4aef-860">Align the image with the shape.</span></span> <span data-ttu-id="d4aef-861">Если значение равно false, выровняйте изображение с помощью окна.</span><span class="sxs-lookup"><span data-stu-id="d4aef-861">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-862">имажеаспект</span><span class="sxs-lookup"><span data-stu-id="d4aef-862">ImageAspect</span></span></td>
<td><span data-ttu-id="d4aef-863"><strong>Вгаспекттипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-863"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="d4aef-864">Атрибут ImageSize будет скорректирован для сохранения аспекта изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-864">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="d4aef-865">К этим значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="d4aef-865">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d4aef-866">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-866">Value</span></span></th>
<th><span data-ttu-id="d4aef-867">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-867">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-868">Игнорировать</span><span class="sxs-lookup"><span data-stu-id="d4aef-868">Ignore</span></span></td>
<td><span data-ttu-id="d4aef-869">Пропускать проблемы с аспектами.</span><span class="sxs-lookup"><span data-stu-id="d4aef-869">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-870">Задать</span><span class="sxs-lookup"><span data-stu-id="d4aef-870">AtLeast</span></span></td>
<td><span data-ttu-id="d4aef-871">Размер изображения не меньше размера изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-871">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-872">атмост</span><span class="sxs-lookup"><span data-stu-id="d4aef-872">AtMost</span></span></td>
<td><span data-ttu-id="d4aef-873">Изображение не превышает размер изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-873">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-874">ImageSize</span><span class="sxs-lookup"><span data-stu-id="d4aef-874">ImageSize</span></span></td>
<td><span data-ttu-id="d4aef-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="d4aef-876">Размер изображения для формирования кисти.</span><span class="sxs-lookup"><span data-stu-id="d4aef-876">Size of the image to form the brush with.</span></span> <span data-ttu-id="d4aef-877">Значение по умолчанию — размер образа.</span><span class="sxs-lookup"><span data-stu-id="d4aef-877">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-878">жоинстиле</span><span class="sxs-lookup"><span data-stu-id="d4aef-878">JoinStyle</span></span></td>
<td><span data-ttu-id="d4aef-879"><strong>Вглинежоинстиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-879"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="d4aef-880">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-880">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-881">Round (скругленное соединение)</span><span class="sxs-lookup"><span data-stu-id="d4aef-881">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="d4aef-882">Багетная рамка (Багетная стыка)</span><span class="sxs-lookup"><span data-stu-id="d4aef-882">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="d4aef-883">Угловой (угловой стык)</span><span class="sxs-lookup"><span data-stu-id="d4aef-883">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-884">линестиле</span><span class="sxs-lookup"><span data-stu-id="d4aef-884">LineStyle</span></span></td>
<td><span data-ttu-id="d4aef-885"><strong>Вглинестиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-885"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="d4aef-886">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-886">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-887">Один</span><span class="sxs-lookup"><span data-stu-id="d4aef-887">Single</span></span></li>
<li><span data-ttu-id="d4aef-888">Синсин (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="d4aef-888">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="d4aef-889">Синсикк (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="d4aef-889">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="d4aef-890">Сикксин (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="d4aef-890">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="d4aef-891">Сиккбетвинсин (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="d4aef-891">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-892">митерлимит</span><span class="sxs-lookup"><span data-stu-id="d4aef-892">MiterLimit</span></span></td>
<td><span data-ttu-id="d4aef-893"><a href="msdn-online-vml-vglength.md">Длина</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-893"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="d4aef-894">Максимальное расстояние между внутренней точкой и внешней точкой соединения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-894">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="d4aef-895">Это число является кратным ширине линии.</span><span class="sxs-lookup"><span data-stu-id="d4aef-895">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="d4aef-896">В диапазоне от 0 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="d4aef-896">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-897">Включено</span><span class="sxs-lookup"><span data-stu-id="d4aef-897">On</span></span></td>
<td><span data-ttu-id="d4aef-898"><a href="msdn-online-vml-vgtristate.md">Вгтристате</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="d4aef-899">Включает и выключает отображение линии.</span><span class="sxs-lookup"><span data-stu-id="d4aef-899">Turns the display of the line on and off.</span></span> <span data-ttu-id="d4aef-900">Аналогичен атрибуту Stroke в фигуре, но переопределяет его.</span><span class="sxs-lookup"><span data-stu-id="d4aef-900">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-901">Непрозрачность</span><span class="sxs-lookup"><span data-stu-id="d4aef-901">Opacity</span></span></td>
<td><span data-ttu-id="d4aef-902"><a href="msdn-online-vml-vgfraction-data-type.md">Вгфрактион</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="d4aef-903">Непрозрачность штриха.</span><span class="sxs-lookup"><span data-stu-id="d4aef-903">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-904">Источник</span><span class="sxs-lookup"><span data-stu-id="d4aef-904">Src</span></span></td>
<td><span data-ttu-id="d4aef-905">Строка.</span><span class="sxs-lookup"><span data-stu-id="d4aef-905">String.</span></span> <span data-ttu-id="d4aef-906">URL-адрес изображения, загружаемого для изображений и узорных заливок.</span><span class="sxs-lookup"><span data-stu-id="d4aef-906">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="d4aef-907">Этот атрибут всегда должен присутствовать и указывать на допустимые данные изображения для отображения изображения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-907">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-908">стартарров</span><span class="sxs-lookup"><span data-stu-id="d4aef-908">StartArrow</span></span></td>
<td><span data-ttu-id="d4aef-909"><strong>Вгарровхеадстиле</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-909"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="d4aef-910">Стрелка для начала строки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-910">Arrowhead for the start of the line.</span></span> <span data-ttu-id="d4aef-911">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-911">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-912">Нет (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-912">None (default)</span></span></li>
<li><span data-ttu-id="d4aef-913">Блокировать</span><span class="sxs-lookup"><span data-stu-id="d4aef-913">Block</span></span></li>
<li><span data-ttu-id="d4aef-914">Классическая</span><span class="sxs-lookup"><span data-stu-id="d4aef-914">Classic</span></span></li>
<li><span data-ttu-id="d4aef-915">Ромб</span><span class="sxs-lookup"><span data-stu-id="d4aef-915">Diamond</span></span></li>
<li><span data-ttu-id="d4aef-916">Овал</span><span class="sxs-lookup"><span data-stu-id="d4aef-916">Oval</span></span></li>
<li><span data-ttu-id="d4aef-917">Открыть</span><span class="sxs-lookup"><span data-stu-id="d4aef-917">Open</span></span></li>
<li><span data-ttu-id="d4aef-918">Шеврон</span><span class="sxs-lookup"><span data-stu-id="d4aef-918">Chevron</span></span></li>
<li><span data-ttu-id="d4aef-919">даублечеврон</span><span class="sxs-lookup"><span data-stu-id="d4aef-919">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-920">стартарровленгс</span><span class="sxs-lookup"><span data-stu-id="d4aef-920">StartArrowLength</span></span></td>
<td><span data-ttu-id="d4aef-921">Вгарровхеадленгс.</span><span class="sxs-lookup"><span data-stu-id="d4aef-921">VgArrowHeadLength.</span></span> <span data-ttu-id="d4aef-922">Длина наконечника для начала строки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-922">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="d4aef-923">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-923">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-924">Short</span><span class="sxs-lookup"><span data-stu-id="d4aef-924">Short</span></span></li>
<li><span data-ttu-id="d4aef-925">Среднее (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4aef-925">Medium (default)</span></span></li>
<li><span data-ttu-id="d4aef-926">Long</span><span class="sxs-lookup"><span data-stu-id="d4aef-926">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-927">стартарроввидс</span><span class="sxs-lookup"><span data-stu-id="d4aef-927">StartArrowWidth</span></span></td>
<td><span data-ttu-id="d4aef-928">Вгарровхеадвидс.</span><span class="sxs-lookup"><span data-stu-id="d4aef-928">VgArrowheadWidth.</span></span> <span data-ttu-id="d4aef-929">Ширина стрелки для начала строки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-929">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="d4aef-930">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-930">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-931">Узкий средний (по умолчанию) широкий</span><span class="sxs-lookup"><span data-stu-id="d4aef-931">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-932">Вес</span><span class="sxs-lookup"><span data-stu-id="d4aef-932">Weight</span></span></td>
<td><span data-ttu-id="d4aef-933"><a href="msdn-online-vml-vglength.md">Вгленгс</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-933"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="d4aef-934">Ширина линии.</span><span class="sxs-lookup"><span data-stu-id="d4aef-934">Width of line.</span></span> <span data-ttu-id="d4aef-935">В диапазоне от 0 до 1584.</span><span class="sxs-lookup"><span data-stu-id="d4aef-935">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="d4aef-936">Атрибут DashStyle позволяет пользователю указать пользовательский шаблон штриха.</span><span class="sxs-lookup"><span data-stu-id="d4aef-936">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="d4aef-937">Это делается с помощью ряда чисел.</span><span class="sxs-lookup"><span data-stu-id="d4aef-937">This is done using a series of numbers.</span></span> <span data-ttu-id="d4aef-938">Стили штриха определяются с точки зрения длины тире (рисуемой части штриха) и длины пробела между тире.</span><span class="sxs-lookup"><span data-stu-id="d4aef-938">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="d4aef-939">Длины задаются относительно ширины линии; Длина &quot; 1 &quot; равна ширине линии.</span><span class="sxs-lookup"><span data-stu-id="d4aef-939">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="d4aef-940">К каждому штриху применяется стиль Ендкап, а стили стрелок — нет.</span><span class="sxs-lookup"><span data-stu-id="d4aef-940">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="d4aef-941">Строка сначала определяет длину тире, а затем длину пробела.</span><span class="sxs-lookup"><span data-stu-id="d4aef-941">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="d4aef-942">Это может повторяться для формирования сложных стилей штрихов.</span><span class="sxs-lookup"><span data-stu-id="d4aef-942">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="d4aef-943">Строка всегда должна содержать пару цифр. Если оно содержит нечетное число чисел, Последнее может быть не учитывается.</span><span class="sxs-lookup"><span data-stu-id="d4aef-943">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="d4aef-944">В следующей таблице перечислены некоторые типичные значения и описание предполагаемого воздействия.</span><span class="sxs-lookup"><span data-stu-id="d4aef-944">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="d4aef-945">&quot;0 &quot; означает, что точка должна быть фаурфолд симметричной (с круглым ендкапс, она должна быть круговой).</span><span class="sxs-lookup"><span data-stu-id="d4aef-945">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="d4aef-946">Если строка ендкап плоская, средство просмотра должно выбрать по возможности встроенный штрих по операционной системе (т. е. быстро нарисовать).</span><span class="sxs-lookup"><span data-stu-id="d4aef-946">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="d4aef-947">Ниже приведены некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-947">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-948">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="d4aef-948">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="d4aef-949">короткие дефисы (каждое тире и расстояние между ними вдвое больше ширины строки)</span><span class="sxs-lookup"><span data-stu-id="d4aef-949">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-950">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="d4aef-950">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="d4aef-951">точка (каждое тире является шириной строки, а каждое пространство вдвое равно ширине строки)</span><span class="sxs-lookup"><span data-stu-id="d4aef-951">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-952">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="d4aef-952">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="d4aef-953">тире (каждое тире в четыре раза превышает ширину строки, тогда как каждое пространство вдвое равно ширине строки)</span><span class="sxs-lookup"><span data-stu-id="d4aef-953">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-954">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="d4aef-954">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="d4aef-955">длинное тире</span><span class="sxs-lookup"><span data-stu-id="d4aef-955">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-956">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="d4aef-956">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="d4aef-957">тире, точка</span><span class="sxs-lookup"><span data-stu-id="d4aef-957">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-958">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="d4aef-958">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="d4aef-959">длинное тире, точка</span><span class="sxs-lookup"><span data-stu-id="d4aef-959">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-960">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="d4aef-960">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="d4aef-961">длинное тире-пунктирная точка</span><span class="sxs-lookup"><span data-stu-id="d4aef-961">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="d4aef-962">Текстпас, элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-962">TextPath element</span></span>

<span data-ttu-id="d4aef-963">Описывает Векторный путь на основе предоставляемых текстовых данных, шрифта и стилей.</span><span class="sxs-lookup"><span data-stu-id="d4aef-963">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="d4aef-964">Текстовый путь деформации, чтобы соответствовать элементу **пути** , если он указан.</span><span class="sxs-lookup"><span data-stu-id="d4aef-964">The text path is warped to conform to a **Path** element if supplied.</span></span>



|   <span data-ttu-id="d4aef-965">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-965">Attribute</span></span>        |   <span data-ttu-id="d4aef-966">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-966">Description</span></span>                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-967">фитпас</span><span class="sxs-lookup"><span data-stu-id="d4aef-967">FitPath</span></span>  | <span data-ttu-id="d4aef-968">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-968">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-969">Изменяет размер текста для заполнения пути, на котором он находится.</span><span class="sxs-lookup"><span data-stu-id="d4aef-969">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="d4aef-970">фитшапе</span><span class="sxs-lookup"><span data-stu-id="d4aef-970">FitShape</span></span> | <span data-ttu-id="d4aef-971">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-971">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-972">Растягивает текстовый контур до границ поля фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-972">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="d4aef-973">Включено</span><span class="sxs-lookup"><span data-stu-id="d4aef-973">On</span></span>       | <span data-ttu-id="d4aef-974">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-974">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-975">Определяет, отображаются ли пути к символам.</span><span class="sxs-lookup"><span data-stu-id="d4aef-975">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="d4aef-976">Строка</span><span class="sxs-lookup"><span data-stu-id="d4aef-976">String</span></span>   | <span data-ttu-id="d4aef-977">Строка.</span><span class="sxs-lookup"><span data-stu-id="d4aef-977">String.</span></span> <span data-ttu-id="d4aef-978">Текст, отображаемый в виде текстового пути.</span><span class="sxs-lookup"><span data-stu-id="d4aef-978">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="d4aef-979">Trim</span><span class="sxs-lookup"><span data-stu-id="d4aef-979">Trim</span></span>     | <span data-ttu-id="d4aef-980">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-980">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-981">Удаляет все дополнительные пространства, зарезервированные для верхних и нижних колонтитулов, если не используется.</span><span class="sxs-lookup"><span data-stu-id="d4aef-981">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="d4aef-982">®</span><span class="sxs-lookup"><span data-stu-id="d4aef-982">XScale</span></span>   | <span data-ttu-id="d4aef-983">[Вгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-983">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-984">Используйте непосредственное измерение x вместо измерения вдоль пути.</span><span class="sxs-lookup"><span data-stu-id="d4aef-984">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="d4aef-985">Типы данных, используемые в объектной модели VML</span><span class="sxs-lookup"><span data-stu-id="d4aef-985">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="d4aef-986">Объектная модель VML использует следующие типы данных.</span><span class="sxs-lookup"><span data-stu-id="d4aef-986">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="d4aef-987">Double</span><span class="sxs-lookup"><span data-stu-id="d4aef-987">Double</span></span>](/windows)
-   [<span data-ttu-id="d4aef-988">Фиксированный формат</span><span class="sxs-lookup"><span data-stu-id="d4aef-988">Fixed</span></span>](/windows)
-   [<span data-ttu-id="d4aef-989">Integer</span><span class="sxs-lookup"><span data-stu-id="d4aef-989">Integer</span></span>](/windows)
-   [<span data-ttu-id="d4aef-990">ивгаджустментс</span><span class="sxs-lookup"><span data-stu-id="d4aef-990">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="d4aef-991">ивгколор</span><span class="sxs-lookup"><span data-stu-id="d4aef-991">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="d4aef-992">ивжекуатион</span><span class="sxs-lookup"><span data-stu-id="d4aef-992">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="d4aef-993">ивгфикседректангле</span><span class="sxs-lookup"><span data-stu-id="d4aef-993">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="d4aef-994">ивгфикседректанглеаррай</span><span class="sxs-lookup"><span data-stu-id="d4aef-994">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="d4aef-995">ивгформула</span><span class="sxs-lookup"><span data-stu-id="d4aef-995">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="d4aef-996">ивгформулас</span><span class="sxs-lookup"><span data-stu-id="d4aef-996">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="d4aef-997">ивгградиентколораррай</span><span class="sxs-lookup"><span data-stu-id="d4aef-997">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="d4aef-998">ивгпоинтс</span><span class="sxs-lookup"><span data-stu-id="d4aef-998">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="d4aef-999">ивгскевматрикс</span><span class="sxs-lookup"><span data-stu-id="d4aef-999">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="d4aef-1000">ивгскевоффсет</span><span class="sxs-lookup"><span data-stu-id="d4aef-1000">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="d4aef-1001">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="d4aef-1001">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="d4aef-1002">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="d4aef-1002">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="d4aef-1003">Длина</span><span class="sxs-lookup"><span data-stu-id="d4aef-1003">Length</span></span>](/windows)
-   [<span data-ttu-id="d4aef-1004">Measure</span><span class="sxs-lookup"><span data-stu-id="d4aef-1004">Measure</span></span>](/windows)
-   [<span data-ttu-id="d4aef-1005">String</span><span class="sxs-lookup"><span data-stu-id="d4aef-1005">String</span></span>](/windows)
-   [<span data-ttu-id="d4aef-1006">вгблакквхитемоде</span><span class="sxs-lookup"><span data-stu-id="d4aef-1006">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="d4aef-1007">вгфрактион</span><span class="sxs-lookup"><span data-stu-id="d4aef-1007">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="d4aef-1008">вгтристате</span><span class="sxs-lookup"><span data-stu-id="d4aef-1008">VgTriState</span></span>](/windows)

<span data-ttu-id="d4aef-1009">**Тип данных Double**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1009">**Double data type**</span></span>

<span data-ttu-id="d4aef-1010">Целое число двойной точности с диапазоном от-Infinity до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1010">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="d4aef-1011">**Фиксированный тип данных**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1011">**Fixed data type**</span></span>

<span data-ttu-id="d4aef-1012">Число с плавающей запятой с диапазоном от-32 766,0 до 32 766,0.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1012">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="d4aef-1013">**Тип данных Integer**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1013">**Integer data type**</span></span>

<span data-ttu-id="d4aef-1014">Целое число с диапазоном от-Infinity до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1014">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="d4aef-1015">**Тип данных Ивгаджустментс**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1015">**IVgAdjustments data type**</span></span>

<span data-ttu-id="d4aef-1016">Коллекция корректировок для фигуры, которую можно использовать для изменения размеров фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1016">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="d4aef-1017">Корректировки можно использовать как временные заполнители или по любой причине для использования переменных.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1017">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="d4aef-1018">В коллекции доступно только 8 корректировок.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1018">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="d4aef-1019">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-1019">Attribute</span></span> | <span data-ttu-id="d4aef-1020">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1020">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-1021">Exists</span><span class="sxs-lookup"><span data-stu-id="d4aef-1021">Exists</span></span>     | <span data-ttu-id="d4aef-1022">[Ивгтристате](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="d4aef-1023">Определяет, существует ли указанная корректировка.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1023">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="d4aef-1024">Обратите внимание, что необходимо использовать индекс. то есть для получения существования элемента должен использоваться существующий (Item).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1024">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="d4aef-1025">Элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-1025">Item</span></span>       | <span data-ttu-id="d4aef-1026">[Длинное целое](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1026">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1027">Массив корректировок, индексируемых от 0 до 7.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1027">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="d4aef-1028">Обратите внимание, что корректировки могут быть указаны с SPARC. то есть значения промежуточных массивов могут не всегда заполняться.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1028">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="d4aef-1029">Например, элементы 1, 3 и 5 могут иметь значения длиной 3, для которых задан элемент (0), элемент (2) и элемент (4).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1029">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="d4aef-1030">Чтобы узнать, существует ли элемент, используйте атрибут EXISTS.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1030">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="d4aef-1031">Длина</span><span class="sxs-lookup"><span data-stu-id="d4aef-1031">Length</span></span>     | <span data-ttu-id="d4aef-1032">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1032">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1033">Число корректировок.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1033">Number of adjustments.</span></span> <span data-ttu-id="d4aef-1034">Не может быть больше 8.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1034">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d4aef-1035">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-1035">Value</span></span>      | <span data-ttu-id="d4aef-1036">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1036">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1037">Текстовое представление числовых значений с запятыми между каждым числом.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1037">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="d4aef-1038">**ивгколор**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1038">**IVgColor**</span></span>

<span data-ttu-id="d4aef-1039">Задает цвет.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1039">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4aef-1040">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d4aef-1040">Attributes</span></span></th>
<th><span data-ttu-id="d4aef-1041">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1041">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-1042">RGB</span><span class="sxs-lookup"><span data-stu-id="d4aef-1042">RGB</span></span></td>
<td><span data-ttu-id="d4aef-1043"><strong>Вгргбтипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1043"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="d4aef-1044">Значение RGB (Long) цвета.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1044">RGB value (Long) of the color.</span></span> <span data-ttu-id="d4aef-1045">Допустим только в том случае, если тип — RGB.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1045">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1046">R</span><span class="sxs-lookup"><span data-stu-id="d4aef-1046">R</span></span></td>
<td><span data-ttu-id="d4aef-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="d4aef-1048">Красный компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1048">Red component of the color.</span></span> <span data-ttu-id="d4aef-1049">Может находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1049">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1050">G</span><span class="sxs-lookup"><span data-stu-id="d4aef-1050">G</span></span></td>
<td><span data-ttu-id="d4aef-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="d4aef-1052">Зеленый компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1052">Green component of the color.</span></span> <span data-ttu-id="d4aef-1053">Может находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1053">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1054">B</span><span class="sxs-lookup"><span data-stu-id="d4aef-1054">B</span></span></td>
<td><span data-ttu-id="d4aef-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="d4aef-1056">Синий компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1056">Blue component of the color.</span></span> <span data-ttu-id="d4aef-1057">Может находиться в диапазоне от 0 до 255.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1057">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1058">Строка</span><span class="sxs-lookup"><span data-stu-id="d4aef-1058">String</span></span></td>
<td><span data-ttu-id="d4aef-1059"><a href="#data-types-used-in-the-vml-object-model">Строка</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1059"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="d4aef-1060">Текстовое представление цвета.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1060">Text representation of the color.</span></span> <span data-ttu-id="d4aef-1061">Поддерживаются следующие именованные типы цветов:</span><span class="sxs-lookup"><span data-stu-id="d4aef-1061">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="d4aef-1062">Черный (#000000)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1062">Black (#000000)</span></span></li>
<li><span data-ttu-id="d4aef-1063">Серебро (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1063">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="d4aef-1064">Серый (#808080)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1064">Gray (#808080)</span></span></li>
<li><span data-ttu-id="d4aef-1065">Белый (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1065">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="d4aef-1066">Каштановый (#800000)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1066">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="d4aef-1067">Красный (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1067">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="d4aef-1068">Сиреневый (#800080)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1068">Purple (#800080)</span></span></li>
<li><span data-ttu-id="d4aef-1069">Фучсиа (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1069">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="d4aef-1070">Зеленый (#008000)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1070">Green (#008000)</span></span></li>
<li><span data-ttu-id="d4aef-1071">Травяной (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1071">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="d4aef-1072">Оливковый (#808000)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1072">Olive (#808000)</span></span></li>
<li><span data-ttu-id="d4aef-1073">Желтый (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1073">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="d4aef-1074">ВМФ (#000080)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1074">Navy (#000080)</span></span></li>
<li><span data-ttu-id="d4aef-1075">Синий (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1075">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="d4aef-1076">Бирюзовый (#008080)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1076">Teal (#008080)</span></span></li>
<li><span data-ttu-id="d4aef-1077">Голубой (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1077">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1078">Type</span><span class="sxs-lookup"><span data-stu-id="d4aef-1078">Type</span></span></td>
<td><span data-ttu-id="d4aef-1079"><strong>Вгколортипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1079"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="d4aef-1080">Тип цвета.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1080">Type of color.</span></span> <span data-ttu-id="d4aef-1081">Один из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="d4aef-1081">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="d4aef-1082">Смешанный</span><span class="sxs-lookup"><span data-stu-id="d4aef-1082">Mixed</span></span></li>
<li><span data-ttu-id="d4aef-1083">именованная</span><span class="sxs-lookup"><span data-stu-id="d4aef-1083">Named</span></span></li>
<li><span data-ttu-id="d4aef-1084">RGB</span><span class="sxs-lookup"><span data-stu-id="d4aef-1084">RGB</span></span></li>
<li><span data-ttu-id="d4aef-1085">Схема</span><span class="sxs-lookup"><span data-stu-id="d4aef-1085">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d4aef-1086">**ивжекуатион**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1086">**IVgEquation**</span></span>

<span data-ttu-id="d4aef-1087">Формулы, используемые для формул.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1087">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-1088">Операция</span><span class="sxs-lookup"><span data-stu-id="d4aef-1088">Operation</span></span></td>
<td><span data-ttu-id="d4aef-1089"><strong>Вжекуатионоператионтипе</strong> Имя операции, выполняемой с параметрами.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1089"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="d4aef-1090">В уравнении можно использовать следующие операции:</span><span class="sxs-lookup"><span data-stu-id="d4aef-1090">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d4aef-1091">Операция</span><span class="sxs-lookup"><span data-stu-id="d4aef-1091">Operation</span></span></th>
<th><span data-ttu-id="d4aef-1092">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1092">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-1093">Abs</span><span class="sxs-lookup"><span data-stu-id="d4aef-1093">Abs</span></span></td>
<td><span data-ttu-id="d4aef-1094">Абсолютное значение.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1094">Absolute value.</span></span> <br/> <span data-ttu-id="d4aef-1095"><strong>ABS</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1095"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1096">Atan2</span><span class="sxs-lookup"><span data-stu-id="d4aef-1096">Atan2</span></span></td>
<td><span data-ttu-id="d4aef-1097">Полярная арифметика — результаты в единицах фильтра (градусы умножаются на 65536).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1097">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="d4aef-1098"><strong>atan2</strong>(P1, v)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1098"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1099">Cos</span><span class="sxs-lookup"><span data-stu-id="d4aef-1099">Cos</span></span></td>
<td><span data-ttu-id="d4aef-1100">Косинус, аргумент в единицах демона (градусы, умноженные на 65536).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1100">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="d4aef-1101">v \* <strong>COS</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1101">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1102">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="d4aef-1102">Cosatan2</span></span></td>
<td><span data-ttu-id="d4aef-1103">Сохраняет полную точность в промежуточном вычислении.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1103">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="d4aef-1104">v \* <strong>cos (atan2 (</strong> P2, P1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="d4aef-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1105">Эллипс</span><span class="sxs-lookup"><span data-stu-id="d4aef-1105">Ellipse</span></span></td>
<td><span data-ttu-id="d4aef-1106">Эллипс</span><span class="sxs-lookup"><span data-stu-id="d4aef-1106">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1107">If</span><span class="sxs-lookup"><span data-stu-id="d4aef-1107">If</span></span></td>
<td><span data-ttu-id="d4aef-1108">If проверка условия.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1108">If Condition test.</span></span> <span data-ttu-id="d4aef-1109">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="d4aef-1109">v > 0 <strong>?</strong></span></span> <span data-ttu-id="d4aef-1110">P1: P2</span><span class="sxs-lookup"><span data-stu-id="d4aef-1110">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1111">Max</span><span class="sxs-lookup"><span data-stu-id="d4aef-1111">Max</span></span></td>
<td><span data-ttu-id="d4aef-1112">Большее из двух значений.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1112">The greater of two values.</span></span> <br/> <span data-ttu-id="d4aef-1113"><strong>Max</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1113"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1114">Mid</span><span class="sxs-lookup"><span data-stu-id="d4aef-1114">Mid</span></span></td>
<td><span data-ttu-id="d4aef-1115">Среднее (v + P1)/2</span><span class="sxs-lookup"><span data-stu-id="d4aef-1115">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1116">Min</span><span class="sxs-lookup"><span data-stu-id="d4aef-1116">Min</span></span></td>
<td><span data-ttu-id="d4aef-1117">Меньшее из двух значений.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1117">The lesser of two values.</span></span> <span data-ttu-id="d4aef-1118"><strong>min</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1118"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1119">Mod</span><span class="sxs-lookup"><span data-stu-id="d4aef-1119">Mod</span></span></td>
<td><span data-ttu-id="d4aef-1120">Вычисление модуля.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1120">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1121">Продукт</span><span class="sxs-lookup"><span data-stu-id="d4aef-1121">Product</span></span></td>
<td><span data-ttu-id="d4aef-1122">Используется для умножения и деления.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1122">Used for multiplication and division.</span></span> <span data-ttu-id="d4aef-1123">v \* P1/P2</span><span class="sxs-lookup"><span data-stu-id="d4aef-1123">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1124">Sin</span><span class="sxs-lookup"><span data-stu-id="d4aef-1124">Sin</span></span></td>
<td><span data-ttu-id="d4aef-1125">Синус, аргумент в единицах фильтра (градусов, умноженный на 65536).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1125">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="d4aef-1126">v \* <strong>sin</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1126">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1127">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="d4aef-1127">Sinatan2</span></span></td>
<td><span data-ttu-id="d4aef-1128">Сохраняет полную точность в промежуточном вычислении.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1128">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="d4aef-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(P2, P1))</span><span class="sxs-lookup"><span data-stu-id="d4aef-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1130">Sqrt</span><span class="sxs-lookup"><span data-stu-id="d4aef-1130">Sqrt</span></span></td>
<td><span data-ttu-id="d4aef-1131">Результат является положительным и округляется вниз.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1131">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="d4aef-1132"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1132"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1133">SUM</span><span class="sxs-lookup"><span data-stu-id="d4aef-1133">Sum</span></span></td>
<td><span data-ttu-id="d4aef-1134">Используется для сложения и вычитания.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1134">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="d4aef-1135">v + P1 P2</span><span class="sxs-lookup"><span data-stu-id="d4aef-1135">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1136">сумангле</span><span class="sxs-lookup"><span data-stu-id="d4aef-1136">Sumangle</span></span></td>
<td><span data-ttu-id="d4aef-1137">Существующий угол (масштабируется на 65536), где P1 и P2 находятся в градусах.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1137">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="d4aef-1138">v + P1 \* 65536 + P2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="d4aef-1138">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1139">Tan</span><span class="sxs-lookup"><span data-stu-id="d4aef-1139">Tan</span></span></td>
<td><span data-ttu-id="d4aef-1140">Тангенс, аргумент находится в единицах демона (градусов, умноженные на 65536).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1140">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="d4aef-1141">v \* Tan (P1)</span><span class="sxs-lookup"><span data-stu-id="d4aef-1141">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1142">Val</span><span class="sxs-lookup"><span data-stu-id="d4aef-1142">Val</span></span></td>
<td><span data-ttu-id="d4aef-1143">Определяет значение Guide из другого значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1143">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1144">Параметр1</span><span class="sxs-lookup"><span data-stu-id="d4aef-1144">Param1</span></span></td>
<td><span data-ttu-id="d4aef-1145"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1145"><strong>Integer</strong>.</span></span> <span data-ttu-id="d4aef-1146">Первый параметр.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1146">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1147">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="d4aef-1147">Paramtype1</span></span></td>
<td><span data-ttu-id="d4aef-1148"><strong>Вгформулапарамтипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1148"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="d4aef-1149">Тип первого параметра.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1149">The type of the first parameter.</span></span> <span data-ttu-id="d4aef-1150">Поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1150">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d4aef-1151">Type</span><span class="sxs-lookup"><span data-stu-id="d4aef-1151">Type</span></span></th>
<th><span data-ttu-id="d4aef-1152">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-1153">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-1153">Value</span></span></td>
<td><span data-ttu-id="d4aef-1154">Параметр является простым значением.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1154">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1155">аджустментреференце</span><span class="sxs-lookup"><span data-stu-id="d4aef-1155">AdjustmentReference</span></span></td>
<td><span data-ttu-id="d4aef-1156">Параметр является ссылкой на корректировку.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1156">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="d4aef-1157">Например, если первый параметр равен 1, будет использоваться значение первой корректировки.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1157">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1158">формулареференце</span><span class="sxs-lookup"><span data-stu-id="d4aef-1158">FormulaReference</span></span></td>
<td><span data-ttu-id="d4aef-1159">Параметр является результатом ссылки на результат предыдущей формулы.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1159">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="d4aef-1160">Например, если первый параметр равен 2, будет использоваться результат формулы 2.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1160">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1161">Param2</span><span class="sxs-lookup"><span data-stu-id="d4aef-1161">Param2</span></span></td>
<td><span data-ttu-id="d4aef-1162"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1162"><strong>Integer</strong>.</span></span> <span data-ttu-id="d4aef-1163">Второй параметр.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1163">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1164">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="d4aef-1164">Paramtype2</span></span></td>
<td><span data-ttu-id="d4aef-1165"><strong>Вгформулапарамтипе</strong> Тип параметра 2.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1165"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1166">Val</span><span class="sxs-lookup"><span data-stu-id="d4aef-1166">Val</span></span></td>
<td><span data-ttu-id="d4aef-1167"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1167"><strong>Integer</strong>.</span></span> <span data-ttu-id="d4aef-1168">Результат.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1168">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1169">Valtype2</span><span class="sxs-lookup"><span data-stu-id="d4aef-1169">Valtype2</span></span></td>
<td><span data-ttu-id="d4aef-1170"><strong>Вгформулапарамтипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1170"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="d4aef-1171">Тип результата.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1171">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d4aef-1172">**ивгфикседректангле**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1172">**IVgFixedRectangle**</span></span>

<span data-ttu-id="d4aef-1173">Задает фиксированный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1173">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="d4aef-1174">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-1174">Attribute</span></span> | <span data-ttu-id="d4aef-1175">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1175">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-1176">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-1176">Value</span></span>      | <span data-ttu-id="d4aef-1177">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1177">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1178">Текстовое значение, указывающее путь.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1178">Text value specifying the path.</span></span>         |
| <span data-ttu-id="d4aef-1179">Левый</span><span class="sxs-lookup"><span data-stu-id="d4aef-1179">Left</span></span>       | <span data-ttu-id="d4aef-1180">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1180">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1181">Крайняя левая координата прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1181">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="d4aef-1182">Начало</span><span class="sxs-lookup"><span data-stu-id="d4aef-1182">Top</span></span>        | <span data-ttu-id="d4aef-1183">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1183">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1184">Самая верхняя координата прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1184">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="d4aef-1185">Правый</span><span class="sxs-lookup"><span data-stu-id="d4aef-1185">Right</span></span>      | <span data-ttu-id="d4aef-1186">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1186">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1187">Крайняя правая координата прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1187">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="d4aef-1188">Последние</span><span class="sxs-lookup"><span data-stu-id="d4aef-1188">Bottom</span></span>     | <span data-ttu-id="d4aef-1189">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1189">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1190">Самое нижнее координата прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1190">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="d4aef-1191">**ивгфикседректанглеаррай**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1191">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="d4aef-1192">Массив фиксированных прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1192">Array of fixed rectangles.</span></span>



| <span data-ttu-id="d4aef-1193">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-1193">Attribute</span></span> | <span data-ttu-id="d4aef-1194">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1194">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-1195">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-1195">Value</span></span>      | <span data-ttu-id="d4aef-1196">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1196">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1197">Текстовое представление массива.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1197">Text representation of array.</span></span>                           |
| <span data-ttu-id="d4aef-1198">Длина</span><span class="sxs-lookup"><span data-stu-id="d4aef-1198">Length</span></span>     | <span data-ttu-id="d4aef-1199">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1199">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1200">Число прямоугольников в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1200">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="d4aef-1201">Элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-1201">Item</span></span>       | <span data-ttu-id="d4aef-1202">[Ивгфикседректангле](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1203">Объект Rectangle по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1203">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="d4aef-1204">Тип данных **ивгформула**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1204">**IVgFormula** data type</span></span>

<span data-ttu-id="d4aef-1205">Определения формул, которые могут варьировать путь к фигуре или использоваться для других вычислений.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1205">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="d4aef-1206">Формулы могут основываться на атрибуте « **года** » фигуры, который может изменяться.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1206">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="d4aef-1207">Формулы также могут ссылаться на другие формулы.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1207">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="d4aef-1208">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-1208">Attribute</span></span>| <span data-ttu-id="d4aef-1209">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1209">Description</span></span>                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-1210">екн</span><span class="sxs-lookup"><span data-stu-id="d4aef-1210">Eqn</span></span>        | <span data-ttu-id="d4aef-1211">[Ивжекуатион](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1212">Каждая формула определяет одно значение в результате вычисления выражения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1212">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="d4aef-1213">Выражение определяется этим атрибутом и имеет общую форму операции, за которым следует до трех аргументов, которые могут быть значениями коррекции (например, \# 2), результатами предыдущих формул (например, @2 ), фиксированных чисел или предопределенных значений.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1213">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="d4aef-1214">**Тип данных Ивгформулас**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1214">**IVgFormulas data type**</span></span>

<span data-ttu-id="d4aef-1215">Коллекция объектов формулы.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1215">A collection of formula objects.</span></span>



| <span data-ttu-id="d4aef-1216">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-1216">Attribute</span></span> | <span data-ttu-id="d4aef-1217">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1217">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-1218">Длина</span><span class="sxs-lookup"><span data-stu-id="d4aef-1218">Length</span></span>     | <span data-ttu-id="d4aef-1219">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1219">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1220">Число объектов формулы в коллекции.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1220">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="d4aef-1221">Элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-1221">Item</span></span>       | <span data-ttu-id="d4aef-1222">[Ивгформула](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1223">Определенная формула.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1223">A specific formula.</span></span> <span data-ttu-id="d4aef-1224">Обратите внимание, что массив формул может наследоваться ФОМ типа Shape.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1224">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="d4aef-1225">**ивгградиентколораррай**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1225">**IVgGradientColorArray**</span></span>

<span data-ttu-id="d4aef-1226">Массив цветов, определяющий градиент (смешанный диапазон цветов).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1226">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="d4aef-1227">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-1227">Attribute</span></span> | <span data-ttu-id="d4aef-1228">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1228">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-1229">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-1229">Value</span></span>      | <span data-ttu-id="d4aef-1230">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1230">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1231">Задает массив цветов. Например, "Red. 2; зеленый. 4; черный. 7 "</span><span class="sxs-lookup"><span data-stu-id="d4aef-1231">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="d4aef-1232">Длина</span><span class="sxs-lookup"><span data-stu-id="d4aef-1232">Length</span></span>     | <span data-ttu-id="d4aef-1233">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1233">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1234">Число цветов в массиве.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1234">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="d4aef-1235">Метод</span><span class="sxs-lookup"><span data-stu-id="d4aef-1235">Method</span></span>     | <span data-ttu-id="d4aef-1236">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1236">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-1237">аддколор</span><span class="sxs-lookup"><span data-stu-id="d4aef-1237">AddColor</span></span>    | <span data-ttu-id="d4aef-1238">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="d4aef-1239">Добавляет новый цвет в конечной точке, указанной в параметре дробь.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1239">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="d4aef-1240">Новый цвет является белым по умолчанию и является возвращаемым значением.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1240">The new color is white by default and is the return value.</span></span> <span data-ttu-id="d4aef-1241">Затем можно изменить цвет по ссылке.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1241">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="d4aef-1242">ремовеколор</span><span class="sxs-lookup"><span data-stu-id="d4aef-1242">RemoveColor</span></span> | <span data-ttu-id="d4aef-1243">[Вгфрактион](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="d4aef-1244">Удаляет цвет в конечной точке, указанной в параметре дробь.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1244">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="d4aef-1245">Примечание. Если 0,0 или 1,0 не существует, подразумевается, а в этой точке используется белый цвет.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1245">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="d4aef-1246">**Тип данных Ивгпоинтс**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1246">**IVgPoints datatype**</span></span>

<span data-ttu-id="d4aef-1247">Массив точек, определяющих фигуру.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1247">Array of points that define a shape.</span></span>



| <span data-ttu-id="d4aef-1248">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-1248">Attribute</span></span> | <span data-ttu-id="d4aef-1249">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1249">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4aef-1250">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-1250">Value</span></span>      | <span data-ttu-id="d4aef-1251">[Строка](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1251">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1252">Текстовое представление массива.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1252">Text representation of array.</span></span>           |
| <span data-ttu-id="d4aef-1253">Длина</span><span class="sxs-lookup"><span data-stu-id="d4aef-1253">Length</span></span>     | <span data-ttu-id="d4aef-1254">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1254">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="d4aef-1255">Число точек в этом массиве.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1255">Number of points in this array.</span></span>        |
| <span data-ttu-id="d4aef-1256">Элемент</span><span class="sxs-lookup"><span data-stu-id="d4aef-1256">Item</span></span>       | <span data-ttu-id="d4aef-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="d4aef-1258">Точка по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1258">The point at the specified index.</span></span> |



 

<span data-ttu-id="d4aef-1259">**Тип данных Ивгскевматрикс**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1259">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="d4aef-1260">Матрица, используемая для наклона фигур, матрица преобразования перспективы в форме, "*скскс, СКСИ, Сикс, сии, px, корректировка* " \[ *s* = Scale, *p* = перспектива \] .</span><span class="sxs-lookup"><span data-stu-id="d4aef-1260">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="d4aef-1261">Если значение offset в абсолютных единицах, то *px,* сдвиг в единицах ЕС ^-1. в противном случае это обратная часть размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1261">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="d4aef-1262">attribute</span><span class="sxs-lookup"><span data-stu-id="d4aef-1262">Attribute</span></span>   | <span data-ttu-id="d4aef-1263">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1263">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="d4aef-1264">кстокс</span><span class="sxs-lookup"><span data-stu-id="d4aef-1264">XtoX</span></span>         | <span data-ttu-id="d4aef-1265">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1265">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="d4aef-1266">итокс</span><span class="sxs-lookup"><span data-stu-id="d4aef-1266">YtoX</span></span>         | <span data-ttu-id="d4aef-1267">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1267">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="d4aef-1268">кстой</span><span class="sxs-lookup"><span data-stu-id="d4aef-1268">XtoY</span></span>         | <span data-ttu-id="d4aef-1269">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1269">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="d4aef-1270">итой</span><span class="sxs-lookup"><span data-stu-id="d4aef-1270">YtoY</span></span>         | <span data-ttu-id="d4aef-1271">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1271">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="d4aef-1272">перспективекс</span><span class="sxs-lookup"><span data-stu-id="d4aef-1272">PerspectiveX</span></span> | <span data-ttu-id="d4aef-1273">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1273">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="d4aef-1274">Перспектива</span><span class="sxs-lookup"><span data-stu-id="d4aef-1274">PerspectiveY</span></span> | <span data-ttu-id="d4aef-1275">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="d4aef-1275">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="d4aef-1276">**ивгскевоффсет**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1276">**IVgSkewOffset**</span></span>

<span data-ttu-id="d4aef-1277">Задает смещение наклона.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1277">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4aef-1278">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d4aef-1278">Attributes</span></span></th>
<th><span data-ttu-id="d4aef-1279">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1279">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-1280">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-1280">Value</span></span></td>
<td><span data-ttu-id="d4aef-1281"><a href="#data-types-used-in-the-vml-object-model">Строка</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1281"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="d4aef-1282">Текстовое представление смещения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1282">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1283">X</span><span class="sxs-lookup"><span data-stu-id="d4aef-1283">X</span></span></td>
<td><span data-ttu-id="d4aef-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="d4aef-1285">Компонент X.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1285">X component.</span></span> <span data-ttu-id="d4aef-1286">Процент или мера.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1286">Percentage or measure.</span></span> <span data-ttu-id="d4aef-1287">Если единицы нет, то тип Шаперелативе является подразумеваемым. в противном случае подразумевается абсолютный тип.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1287">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1288">Y</span><span class="sxs-lookup"><span data-stu-id="d4aef-1288">Y</span></span></td>
<td><span data-ttu-id="d4aef-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="d4aef-1290">Компонент Y.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1290">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1291">Type</span><span class="sxs-lookup"><span data-stu-id="d4aef-1291">Type</span></span></td>
<td><span data-ttu-id="d4aef-1292"><strong>Вгскевтрансформтипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1292"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="d4aef-1293">Указывает тип преобразования.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1293">Specifies the type of transformation.</span></span> <span data-ttu-id="d4aef-1294">Допустимые значения — целочисленные точки в диапазоне от-Infinity до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1294">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d4aef-1295">Type</span><span class="sxs-lookup"><span data-stu-id="d4aef-1295">Type</span></span></th>
<th><span data-ttu-id="d4aef-1296">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1296">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-1297">шаперелативе</span><span class="sxs-lookup"><span data-stu-id="d4aef-1297">ShapeRelative</span></span></td>
<td><span data-ttu-id="d4aef-1298">Значения смещения задаются в процентах (коэффициентах) размера исходной фигуры. Например, значение 0,5 означает смещение половины размера фигуры.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1298">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1299">Абсолютный</span><span class="sxs-lookup"><span data-stu-id="d4aef-1299">Absolute</span></span></td>
<td><span data-ttu-id="d4aef-1300">Значения являются абсолютными единицами.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1300">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d4aef-1301">**Тип данных IVgVector2D**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1301">**IVgVector2D data type**</span></span>

<span data-ttu-id="d4aef-1302">Задает двухмерный вектор, состоящий из двух чисел **типа Double** .</span><span class="sxs-lookup"><span data-stu-id="d4aef-1302">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d4aef-1303">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d4aef-1303">Attributes</span></span></th>
<th><span data-ttu-id="d4aef-1304">Описание</span><span class="sxs-lookup"><span data-stu-id="d4aef-1304">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-1305">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-1305">Value</span></span></td>
<td><span data-ttu-id="d4aef-1306"><strong>Строка</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1306"><strong>String</strong>.</span></span> <span data-ttu-id="d4aef-1307">Текстовое представление обоих векторных чисел, разделенных пробелом.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1307">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1308">X</span><span class="sxs-lookup"><span data-stu-id="d4aef-1308">X</span></span></td>
<td><span data-ttu-id="d4aef-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="d4aef-1310">Компонент X этого вектора.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1310">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1311">Y</span><span class="sxs-lookup"><span data-stu-id="d4aef-1311">Y</span></span></td>
<td><span data-ttu-id="d4aef-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="d4aef-1313">Компонент Y этого вектора.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1313">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1314">Type</span><span class="sxs-lookup"><span data-stu-id="d4aef-1314">Type</span></span></td>
<td><span data-ttu-id="d4aef-1315"><strong>Вгвектортипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1315"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="d4aef-1316">Для этого вектора ожидались единицы.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1316">Expected units for this vector.</span></span> <span data-ttu-id="d4aef-1317">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1317">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-1318">Мера</span><span class="sxs-lookup"><span data-stu-id="d4aef-1318">Measure</span></span></li>
<li><span data-ttu-id="d4aef-1319">Длина</span><span class="sxs-lookup"><span data-stu-id="d4aef-1319">Length</span></span></li>
<li><span data-ttu-id="d4aef-1320">англеиндегрис</span><span class="sxs-lookup"><span data-stu-id="d4aef-1320">AngleInDegrees</span></span></li>
<li><span data-ttu-id="d4aef-1321">Fraction</span><span class="sxs-lookup"><span data-stu-id="d4aef-1321">Fraction</span></span></li>
<li><span data-ttu-id="d4aef-1322">Целое число в процентах</span><span class="sxs-lookup"><span data-stu-id="d4aef-1322">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d4aef-1323">**Тип данных IVgVector3D**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1323">**IVgVector3D data type**</span></span>

<span data-ttu-id="d4aef-1324">Задает трехмерный вектор, состоящий из трех чисел **типа Double** .</span><span class="sxs-lookup"><span data-stu-id="d4aef-1324">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d4aef-1325">Значение</span><span class="sxs-lookup"><span data-stu-id="d4aef-1325">Value</span></span></td>
<td><span data-ttu-id="d4aef-1326"><strong>Строка</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1326"><strong>String</strong>.</span></span> <span data-ttu-id="d4aef-1327">Текстовое представление трех векторных чисел, разделенных пробелом.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1327">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1328">X</span><span class="sxs-lookup"><span data-stu-id="d4aef-1328">X</span></span></td>
<td><span data-ttu-id="d4aef-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="d4aef-1330">Компонент X этого вектора.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1330">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1331">Y</span><span class="sxs-lookup"><span data-stu-id="d4aef-1331">Y</span></span></td>
<td><span data-ttu-id="d4aef-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="d4aef-1333">Компонент Y этого вектора.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1333">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d4aef-1334">Z</span><span class="sxs-lookup"><span data-stu-id="d4aef-1334">Z</span></span></td>
<td><span data-ttu-id="d4aef-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="d4aef-1336">Компонент Z этого вектора.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1336">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d4aef-1337">Type</span><span class="sxs-lookup"><span data-stu-id="d4aef-1337">Type</span></span></td>
<td><span data-ttu-id="d4aef-1338"><strong>Вгвектортипе</strong>.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1338"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="d4aef-1339">Для этого вектора ожидались единицы.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1339">Expected units for this vector.</span></span> <span data-ttu-id="d4aef-1340">Возможны следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1340">Values are:</span></span>
<ul>
<li><span data-ttu-id="d4aef-1341">Мера</span><span class="sxs-lookup"><span data-stu-id="d4aef-1341">Measure</span></span></li>
<li><span data-ttu-id="d4aef-1342">Длина</span><span class="sxs-lookup"><span data-stu-id="d4aef-1342">Length</span></span></li>
<li><span data-ttu-id="d4aef-1343">англеиндегрис</span><span class="sxs-lookup"><span data-stu-id="d4aef-1343">AngleInDegrees</span></span></li>
<li><span data-ttu-id="d4aef-1344">Fraction</span><span class="sxs-lookup"><span data-stu-id="d4aef-1344">Fraction</span></span></li>
<li><span data-ttu-id="d4aef-1345">Число</span><span class="sxs-lookup"><span data-stu-id="d4aef-1345">Number</span></span></li>
<li><span data-ttu-id="d4aef-1346">Процент</span><span class="sxs-lookup"><span data-stu-id="d4aef-1346">Percentage</span></span></li>
<li><span data-ttu-id="d4aef-1347">Целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="d4aef-1347">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d4aef-1348">**Тип данных length**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1348">**Length data type**</span></span>

<span data-ttu-id="d4aef-1349">Число с плавающей запятой с диапазоном от 0 до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1349">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="d4aef-1350">**Тип данных Measure**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1350">**Measure data type**</span></span>

<span data-ttu-id="d4aef-1351">Число с плавающей запятой от-Infinity до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1351">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="d4aef-1352">**Тип данных String**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1352">**String data type**</span></span>

<span data-ttu-id="d4aef-1353">Символьные данные любой длины.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1353">Character data of any length.</span></span>

<span data-ttu-id="d4aef-1354">**вгблакквхитемоде**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1354">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="d4aef-1355">Режим рендеринга для черного и белого.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1355">Rendering mode for black and white.</span></span> <span data-ttu-id="d4aef-1356">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d4aef-1356">Possible values are:</span></span>

-   <span data-ttu-id="d4aef-1357">**Цвет**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1357">**Color**</span></span>
-   <span data-ttu-id="d4aef-1358">**Автоматически**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1358">**Auto**</span></span>
-   <span data-ttu-id="d4aef-1359">**Оттенки серого**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1359">**GrayScale**</span></span>
-   <span data-ttu-id="d4aef-1360">**лигхтграйскале**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1360">**LightGrayScale**</span></span>
-   <span data-ttu-id="d4aef-1361">**инверсеграй**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1361">**InverseGray**</span></span>
-   <span data-ttu-id="d4aef-1362">**грайаутлине**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1362">**GrayOutline**</span></span>
-   <span data-ttu-id="d4aef-1363">**блакктекстандлинес**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1363">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="d4aef-1364">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1364">**HighContrast**</span></span>
-   <span data-ttu-id="d4aef-1365">**Черный**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1365">**Black**</span></span>
-   <span data-ttu-id="d4aef-1366">**Белый**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1366">**White**</span></span>
-   <span data-ttu-id="d4aef-1367">**Не вырисовано**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1367">**Undrawn**</span></span>

<span data-ttu-id="d4aef-1368">**Тип данных Вгфрактион**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1368">**VgFraction data type**</span></span>

<span data-ttu-id="d4aef-1369">Число с плавающей запятой с диапазоном от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="d4aef-1369">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="d4aef-1370">Доли также могут быть указаны в процентах; Например, "50%".</span><span class="sxs-lookup"><span data-stu-id="d4aef-1370">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="d4aef-1371">**Тип данных Вгтристате**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1371">**VgTriState datatype**</span></span>

<span data-ttu-id="d4aef-1372">Перечисление, используемое для значений, которые могут быть одного из трех состояний:</span><span class="sxs-lookup"><span data-stu-id="d4aef-1372">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="d4aef-1373">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1373">**TRUE**</span></span>
-   <span data-ttu-id="d4aef-1374">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1374">**FALSE**</span></span>
-   <span data-ttu-id="d4aef-1375">**MIXED**</span><span class="sxs-lookup"><span data-stu-id="d4aef-1375">**MIXED**</span></span>