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
# <a name="working-with-pictures"></a>Работа с изображениями

В этом разделе описано, как настроить изображения с помощью свойства [System. Windows. Forms. PictureBox. сиземоде](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) и как отображать рисунки в Microsoft Visual Studio .NET.

## <a name="the-sizemode-property"></a>Свойство Сиземоде

Можно указать, как изображение помещается в элементе управления с помощью свойства [сиземоде](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) . Свойство Сиземоде доступно как в управляемой библиотеке, так и в библиотеке автоматизации. С помощью Сиземоде можно:

-   Изменение размера границ элемента управления в соответствии с изображением.
-   Растяжение изображения в соответствии с границами элементов управления.
-   Центрирование изображения внутри границ элемента управления.
-   Привязка изображения к левому верхнему краю элемента управления без изменения размера изображения или элемента управления (некоторые изображения могут быть недоступны для просмотра, если не изменить размер изображения или элемента управления).

## <a name="working-with-pictures-in-visual-studio-net"></a>Работа с изображениями в Visual Studio .NET

Для отображения изображения во время разработки в Visual Studio .NET:

1.  Перетащите элемент управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) в форму или дважды щелкните элемент управления InkPicture на панели элементов.
2.  В окне **Свойства** выберите свойство **Image** и нажмите кнопку с многоточием, чтобы открыть диалоговое окно **Открыть** .
3.  Если вы ищете конкретный тип файла (например, JPG-файлы), выберите его в поле **файлы типа** .
4.  Выберите файл, который требуется отобразить.

Чтобы очистить изображение во время разработки:

1.  В окне **Свойства** выберите свойство **изображение** и щелкните правой кнопкой мыши эскиз изображения.
2.  Выберите **Сбросить**.

Элемент управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) отображается по умолчанию без каких-либо границ. Можно предоставить стандартную или трехмерную границу с помощью свойства [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) , чтобы отличить поле InkPicture от остальной части формы, даже если оно не содержит изображения.

Изображение можно отобразить во время выполнения с помощью метода [фромфиле](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) объекта [System. Drawing. Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) :


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



Можно также включить фоновое изображение со свойством [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) объекта наследуемого [изображения](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) . Однако размер этого изображения изменить нельзя.

 

 
