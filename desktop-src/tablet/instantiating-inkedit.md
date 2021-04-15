---
description: В этом разделе описаны различные способы создания экземпляра элемента управления InkEdit.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Создание экземпляра InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde7e94566b076a4d9d6f6928fc08199ee71fa19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497649"
---
# <a name="instantiating-inkedit"></a><span data-ttu-id="d5be7-103">Создание экземпляра InkEdit</span><span class="sxs-lookup"><span data-stu-id="d5be7-103">Instantiating InkEdit</span></span>

<span data-ttu-id="d5be7-104">В этом разделе описаны различные способы создания экземпляра элемента управления [InkEdit](inkedit-control.md) .</span><span class="sxs-lookup"><span data-stu-id="d5be7-104">This topic describes the various ways that you can instantiate an [InkEdit](inkedit-control.md) control.</span></span>

## <a name="visual-basic-net-and-c"></a><span data-ttu-id="d5be7-105">Visual Basic .NET и C\#</span><span class="sxs-lookup"><span data-stu-id="d5be7-105">Visual Basic .NET and C\#</span></span>

<span data-ttu-id="d5be7-106">Если вы работаете с Microsoft Visual Basic .NET или C \# , перетащите элемент управления [InkEdit](./inkedit-control.md) с панели элементов в Visual Studio на форму или страницу, где должен отображаться элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d5be7-106">If you are working with Microsoft Visual Basic .NET or C\#, drag the [InkEdit](./inkedit-control.md) control from the Toolbox in Visual Studio to the form or page where you want the control to appear.</span></span>

## <a name="win32c"></a><span data-ttu-id="d5be7-107">Win32/C++</span><span class="sxs-lookup"><span data-stu-id="d5be7-107">Win32/C++</span></span>

<span data-ttu-id="d5be7-108">Элемент управления [InkEdit](inkedit-control-reference.md) является суперклассом для встраиваемого элемента управления с широкими возможностями редактирования 4,5 Win32 OLE.</span><span class="sxs-lookup"><span data-stu-id="d5be7-108">The [InkEdit](inkedit-control-reference.md) control is a superclass of the Rich Edit 4.5 Win32 OLE embeddable control.</span></span>

<span data-ttu-id="d5be7-109">Приложения Win32 создают экземпляр элемента управления [InkEdit](inkedit-control-reference.md) путем вызова [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) и передачи InkEdit в качестве класса окна.</span><span class="sxs-lookup"><span data-stu-id="d5be7-109">Win32 applications instantiate the [InkEdit](inkedit-control-reference.md) control by calling [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) and passing INKEDIT as the window class.</span></span> <span data-ttu-id="d5be7-110">INKEDIT определяется в соответствии с. h.</span><span class="sxs-lookup"><span data-stu-id="d5be7-110">INKEDIT is defined in InkEd.h.</span></span> <span data-ttu-id="d5be7-111">После создания элемента управления можно «поговорить» с элементом управления с сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d5be7-111">After the control is created, you can "talk" to the control with messages.</span></span> <span data-ttu-id="d5be7-112">Сообщения с расширенными возможностями редактирования (EM \_ \* ) передаются из InkEdit в форматируемый редактор без изменений; доступны все существующие функции расширенного редактирования.</span><span class="sxs-lookup"><span data-stu-id="d5be7-112">Rich Edit messages (EM\_\*) are passed from InkEdit to Rich Edit unaltered; all of the existing Rich Edit functionality is available.</span></span>

<span data-ttu-id="d5be7-113">Чтобы создать элемент управления [InkEdit](inkedit-control-reference.md) , вызовите функцию [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) , указав класс окна InkEdit.</span><span class="sxs-lookup"><span data-stu-id="d5be7-113">To create an [InkEdit](inkedit-control-reference.md) control, call the [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) function, specifying the InkEdit window class.</span></span> <span data-ttu-id="d5be7-114">Используйте [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) для регистрации InkEd.dll.</span><span class="sxs-lookup"><span data-stu-id="d5be7-114">Use [LoadLibrary()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to register InkEd.dll.</span></span> <span data-ttu-id="d5be7-115">Укажите \_ константу класса INKEDIT, определенную для параметра класса Window, и используйте стили окна, как указано в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="d5be7-115">Specify the INKEDIT\_CLASS defined constant for the window class parameter and use the window styles as specified in the following examples.</span></span>

### <a name="instantiating-a-multiline-inkedit-control"></a><span data-ttu-id="d5be7-116">Создание экземпляра элемента управления "многострочный InkEdit"</span><span class="sxs-lookup"><span data-stu-id="d5be7-116">Instantiating a Multiline InkEdit Control</span></span>


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER|ES_MULTILINE,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



### <a name="instantiating-a-single-line-inkedit-control"></a><span data-ttu-id="d5be7-117">Создание экземпляра элемента управления InkEdit Single-Line</span><span class="sxs-lookup"><span data-stu-id="d5be7-117">Instantiating a Single-Line InkEdit Control</span></span>


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



> [!Note]  
> <span data-ttu-id="d5be7-118">В отличие от функции RichEdit, перед созданием элемента управления [InkEdit](inkedit-control-reference.md) необходимо вызвать функцию [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) .</span><span class="sxs-lookup"><span data-stu-id="d5be7-118">Unlike with RichEdit, you must be sure to call [CoInitialize()](/windows/win32/api/objbase/nf-objbase-coinitialize) before creating the [InkEdit](inkedit-control-reference.md) control.</span></span> <span data-ttu-id="d5be7-119">Вызовите метод [CoUninitialize ()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) при завершении работы приложения.</span><span class="sxs-lookup"><span data-stu-id="d5be7-119">Call [CoUninitialize()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) when your application shuts down.</span></span> <span data-ttu-id="d5be7-120">После вызова метода CoUninitialize () необходимо вызвать [FreeLibrary (s \_ Хлиб)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) , чтобы уменьшить число ссылок на файл InkEdit.dll.</span><span class="sxs-lookup"><span data-stu-id="d5be7-120">After calling CoUninitialize(), you must call [FreeLibrary(s\_hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) to decrement the reference count on the InkEdit.dll file.</span></span>

 

<span data-ttu-id="d5be7-121">При использовании стиля окна [ES \_ ноиме](../controls/rich-edit-control-styles.md) встроенная поддержка исправлений недоступна.</span><span class="sxs-lookup"><span data-stu-id="d5be7-121">If you use the [ES\_NOIME](../controls/rich-edit-control-styles.md) window style, the built-in correction support is not available.</span></span> <span data-ttu-id="d5be7-122">Если не указать родительское окно, элемент управления создается как окно верхнего уровня и \_ добавляется стиль WS сисмену. Это также отключает встроенную поддержку исправления.</span><span class="sxs-lookup"><span data-stu-id="d5be7-122">If you don't specify a parent window, the control is created as a top-level window and the WS\_SYSMENU style is added; this also disables the built-in correction support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5be7-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d5be7-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5be7-124">Добавление элементов управления рукописного ввода в проект</span><span class="sxs-lookup"><span data-stu-id="d5be7-124">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
