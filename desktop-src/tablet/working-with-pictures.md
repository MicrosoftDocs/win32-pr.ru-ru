---
description: В этом разделе описано, как настроить изображения с помощью свойства System. Windows. Forms. PictureBox. Сиземоде и как отображать рисунки в Microsoft Visual Studio .NET.
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: Работа с изображениями
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a90c0d18253eaf4aea60eafc48bd1c24fcc3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692499"
---
# <a name="working-with-pictures"></a><span data-ttu-id="decbf-103">Работа с изображениями</span><span class="sxs-lookup"><span data-stu-id="decbf-103">Working with Pictures</span></span>

<span data-ttu-id="decbf-104">В этом разделе описано, как настроить изображения с помощью свойства [System. Windows. Forms. PictureBox. сиземоде](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) и как отображать рисунки в Microsoft Visual Studio .NET.</span><span class="sxs-lookup"><span data-stu-id="decbf-104">This topic describes how to adjust pictures using the [System.Windows.Forms.PictureBox.SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property, and how to display pictures in Microsoft Visual Studio .NET.</span></span>

## <a name="the-sizemode-property"></a><span data-ttu-id="decbf-105">Свойство Сиземоде</span><span class="sxs-lookup"><span data-stu-id="decbf-105">The SizeMode Property</span></span>

<span data-ttu-id="decbf-106">Можно указать, как изображение помещается в элементе управления с помощью свойства [сиземоде](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="decbf-106">You can specify how an image fits in the control with the [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property.</span></span> <span data-ttu-id="decbf-107">Свойство Сиземоде доступно как в управляемой библиотеке, так и в библиотеке автоматизации.</span><span class="sxs-lookup"><span data-stu-id="decbf-107">The SizeMode property is available in both the Managed Library and in the Automation Library.</span></span> <span data-ttu-id="decbf-108">С помощью Сиземоде можно:</span><span class="sxs-lookup"><span data-stu-id="decbf-108">With SizeMode you can:</span></span>

-   <span data-ttu-id="decbf-109">Изменение размера границ элемента управления в соответствии с изображением.</span><span class="sxs-lookup"><span data-stu-id="decbf-109">Resize the control borders to fit an image.</span></span>
-   <span data-ttu-id="decbf-110">Растяжение изображения в соответствии с границами элементов управления.</span><span class="sxs-lookup"><span data-stu-id="decbf-110">Stretch an image to fit the control borders.</span></span>
-   <span data-ttu-id="decbf-111">Центрирование изображения внутри границ элемента управления.</span><span class="sxs-lookup"><span data-stu-id="decbf-111">Center an image within the control borders.</span></span>
-   <span data-ttu-id="decbf-112">Привязка изображения к левому верхнему краю элемента управления без изменения размера изображения или элемента управления (некоторые изображения могут быть недоступны для просмотра, если не изменить размер изображения или элемента управления).</span><span class="sxs-lookup"><span data-stu-id="decbf-112">Anchor an image to the upper-left area of the control without resizing the image or control (some of the image may not be viewable if you do not resize the image or control).</span></span>

## <a name="working-with-pictures-in-visual-studio-net"></a><span data-ttu-id="decbf-113">Работа с изображениями в Visual Studio .NET</span><span class="sxs-lookup"><span data-stu-id="decbf-113">Working with Pictures in Visual Studio .NET</span></span>

<span data-ttu-id="decbf-114">Для отображения изображения во время разработки в Visual Studio .NET:</span><span class="sxs-lookup"><span data-stu-id="decbf-114">To display an image at design time in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="decbf-115">Перетащите элемент управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) в форму или дважды щелкните элемент управления InkPicture на панели элементов.</span><span class="sxs-lookup"><span data-stu-id="decbf-115">Drag an [InkPicture](/previous-versions/aa514604(v=msdn.10)) control on a form, or double-click the InkPicture control in the Toolbox.</span></span>
2.  <span data-ttu-id="decbf-116">В окне **Свойства** выберите свойство **Image** и нажмите кнопку с многоточием, чтобы открыть диалоговое окно **Открыть** .</span><span class="sxs-lookup"><span data-stu-id="decbf-116">In the **Properties** window, select the **Image** property, and then click the ellipsis button to open the **Open** dialog box.</span></span>
3.  <span data-ttu-id="decbf-117">Если вы ищете конкретный тип файла (например, JPG-файлы), выберите его в поле **файлы типа** .</span><span class="sxs-lookup"><span data-stu-id="decbf-117">If you are looking for a specific file type (for example, .jpg files), select it in the **Files of type** box.</span></span>
4.  <span data-ttu-id="decbf-118">Выберите файл, который требуется отобразить.</span><span class="sxs-lookup"><span data-stu-id="decbf-118">Select the file you want to display.</span></span>

<span data-ttu-id="decbf-119">Чтобы очистить изображение во время разработки:</span><span class="sxs-lookup"><span data-stu-id="decbf-119">To clear the picture at design time:</span></span>

1.  <span data-ttu-id="decbf-120">В окне **Свойства** выберите свойство **изображение** и щелкните правой кнопкой мыши эскиз изображения.</span><span class="sxs-lookup"><span data-stu-id="decbf-120">In the **Properties** window, select the **Image** property and right-click the thumbnail image.</span></span>
2.  <span data-ttu-id="decbf-121">Выберите **Сбросить**.</span><span class="sxs-lookup"><span data-stu-id="decbf-121">Click **Reset**.</span></span>

<span data-ttu-id="decbf-122">Элемент управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) отображается по умолчанию без каких-либо границ.</span><span class="sxs-lookup"><span data-stu-id="decbf-122">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is displayed by default without any borders.</span></span> <span data-ttu-id="decbf-123">Можно предоставить стандартную или трехмерную границу с помощью свойства [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) , чтобы отличить поле InkPicture от остальной части формы, даже если оно не содержит изображения.</span><span class="sxs-lookup"><span data-stu-id="decbf-123">You can provide a standard or three-dimensional border using the [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) property to distinguish the InkPicture box from the rest of the form, even if it contains no image.</span></span>

<span data-ttu-id="decbf-124">Изображение можно отобразить во время выполнения с помощью метода [фромфиле](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) объекта [System. Drawing. Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) :</span><span class="sxs-lookup"><span data-stu-id="decbf-124">You can display an image at run time with the [System.Drawing.Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) method:</span></span>


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



<span data-ttu-id="decbf-125">Можно также включить фоновое изображение со свойством [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) объекта наследуемого [изображения](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) . Однако размер этого изображения изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="decbf-125">You can also include a background image with the inherited [Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) property; however, that image cannot be resized.</span></span>

 

 
