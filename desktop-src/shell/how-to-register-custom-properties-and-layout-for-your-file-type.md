---
description: После знакомства с режимом результатов поиска, режимом просмотра и шаблонами макета можно зарегистрировать пользовательский список свойств для типа файлов. Чтобы зарегистрировать пользовательский список свойств и шаблон макета для типа файла, выполните следующие действия.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Регистрация пользовательских свойств и макета для типа файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da55d0a90d4dd0f3ca109a3ca9f628a3c0912520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997698"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="7b2be-103">Регистрация пользовательских свойств и макета для типа файлов</span><span class="sxs-lookup"><span data-stu-id="7b2be-103">How to Register Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="7b2be-104">После знакомства с режимом результатов поиска, режимом просмотра и шаблонами макета можно зарегистрировать пользовательский список свойств для типа файлов.</span><span class="sxs-lookup"><span data-stu-id="7b2be-104">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="7b2be-105">Чтобы зарегистрировать пользовательский список свойств и шаблон макета для типа файла, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="7b2be-105">To register a custom property list and layout pattern for your file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="7b2be-106">Инструкции</span><span class="sxs-lookup"><span data-stu-id="7b2be-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="7b2be-107">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="7b2be-107">Step 1:</span></span>

<span data-ttu-id="7b2be-108">Выберите один из четырех шаблонов макета: альфа, бета, гамма или Дельта.</span><span class="sxs-lookup"><span data-stu-id="7b2be-108">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>

### <a name="step-2"></a><span data-ttu-id="7b2be-109">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="7b2be-109">Step 2:</span></span>

<span data-ttu-id="7b2be-110">Рассмотрим следующие правила форматирования, которые применяются одинаково ко всем четырем шаблонам макета:</span><span class="sxs-lookup"><span data-stu-id="7b2be-110">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>

-   <span data-ttu-id="7b2be-111">Свойство 1 всегда отображается в более крупном размере шрифта.</span><span class="sxs-lookup"><span data-stu-id="7b2be-111">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="7b2be-112">Крупный размер шрифта, обычно используемый для имени элемента, но также может использоваться для свойства привязки или другого элемента.</span><span class="sxs-lookup"><span data-stu-id="7b2be-112">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
-   <span data-ttu-id="7b2be-113">Свойство 4 предназначено для фрагментов в шаблонах макета Alpha, бета-версии и гаммы.</span><span class="sxs-lookup"><span data-stu-id="7b2be-113">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="7b2be-114">Это свойство выделяет больше пространства в этих шаблонах и отображается серым цветом шрифта, а не черным, как и другие свойства, чтобы помочь ему выделить.</span><span class="sxs-lookup"><span data-stu-id="7b2be-114">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
-   <span data-ttu-id="7b2be-115">Приведенные ниже размеры пикселов находятся в относительных пикселях, а размер включает значок или эскиз слева от свойств и расстояние между значком/эскизом и прямоугольником выделения.</span><span class="sxs-lookup"><span data-stu-id="7b2be-115">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
-   <span data-ttu-id="7b2be-116">Большинство свойств имеют минимальный отображаемый размер.</span><span class="sxs-lookup"><span data-stu-id="7b2be-116">Most properties have a minimum display size.</span></span> <span data-ttu-id="7b2be-117">Поэтому они не будут отображаться, если для них недостаточно места в определенном размере представления.</span><span class="sxs-lookup"><span data-stu-id="7b2be-117">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="7b2be-118">Минимальный размер обычно составляет 100 пикселей в ширину.</span><span class="sxs-lookup"><span data-stu-id="7b2be-118">The minimum size is usually 100 pixels wide.</span></span>
-   <span data-ttu-id="7b2be-119">Каждый шаблон макета определяет количество строк и число свойств в каждой строке.</span><span class="sxs-lookup"><span data-stu-id="7b2be-119">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>

### <a name="step-3"></a><span data-ttu-id="7b2be-120">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="7b2be-120">Step 3:</span></span>

<span data-ttu-id="7b2be-121">Определите, какие свойства должны отображаться в макете, и какое свойство должно отображаться в каждом расположении.</span><span class="sxs-lookup"><span data-stu-id="7b2be-121">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="7b2be-122">При принятии решения о том, какое свойство должно отображаться в каждой из позиций макета, учитывайте стандартную длину свойства, его важность для пользователя и необходимость удаления, если размер окна слишком мал для размещения всех свойств.</span><span class="sxs-lookup"><span data-stu-id="7b2be-122">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>

### <a name="step-4"></a><span data-ttu-id="7b2be-123">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="7b2be-123">Step 4:</span></span>

<span data-ttu-id="7b2be-124">Зарегистрируйте шаблон макета и список свойств для типа файла или элемента, добавив следующие ключи в раздел реестра ProgID для типа файла или элемента (в этом примере — для типа файла. XYZ).</span><span class="sxs-lookup"><span data-stu-id="7b2be-124">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a><span data-ttu-id="7b2be-125">Шаг 5.</span><span class="sxs-lookup"><span data-stu-id="7b2be-125">Step 5:</span></span>

<span data-ttu-id="7b2be-126">Обратите внимание на следующие рекомендации по форматированию для регистрации свойств:</span><span class="sxs-lookup"><span data-stu-id="7b2be-126">Observe the following formatting guidelines for registering properties:</span></span>

-   <span data-ttu-id="7b2be-127">Каждая регистрация начинается с `prop:`</span><span class="sxs-lookup"><span data-stu-id="7b2be-127">Each registration starts with `prop:`</span></span>
-   <span data-ttu-id="7b2be-128">Для каждого свойства требуется полное имя свойства.</span><span class="sxs-lookup"><span data-stu-id="7b2be-128">Each property requires the full property name.</span></span>
-   <span data-ttu-id="7b2be-129">Свойства разделяются точкой с запятой без пробела.</span><span class="sxs-lookup"><span data-stu-id="7b2be-129">Properties are separated by a semicolon with no space.</span></span>
-   <span data-ttu-id="7b2be-130">Свойства отображаются в порядке, определенном выбранным шаблоном макета.</span><span class="sxs-lookup"><span data-stu-id="7b2be-130">Properties are displayed in the order defined by the selected layout pattern.</span></span>
-   <span data-ttu-id="7b2be-131">`~` Указывает, что не следует отображать метку свойства.</span><span class="sxs-lookup"><span data-stu-id="7b2be-131">`~` indicates that the property label should not be displayed.</span></span>
-   <span data-ttu-id="7b2be-132">`~System.LayoutPattern.PlaceHolder` следует использовать, если вы хотите оставить пустое свойство, указанное в шаблоне макета.</span><span class="sxs-lookup"><span data-stu-id="7b2be-132">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

<span data-ttu-id="7b2be-133">В следующем примере раздела реестра показаны эти рекомендации по форматированию.</span><span class="sxs-lookup"><span data-stu-id="7b2be-133">The following sample registry key illustrates these formatting guidelines.</span></span>

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

<span data-ttu-id="7b2be-134">Возможные значения для (Контентвиевмодефорбровсе) включают следующее: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`</span><span class="sxs-lookup"><span data-stu-id="7b2be-134">Possible values for (ContentViewModeForBrowse) include the following: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`</span></span>

 

 



