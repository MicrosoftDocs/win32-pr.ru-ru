---
description: Объясняет, как создать элемент управления для математических входных данных.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Создание элемента управления для математических входных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550727"
---
# <a name="creating-a-math-input-control"></a><span data-ttu-id="fd159-103">Создание элемента управления для математических входных данных</span><span class="sxs-lookup"><span data-stu-id="fd159-103">Creating a Math Input Control</span></span>

<span data-ttu-id="fd159-104">Чтобы создать элемент управления математическими данными, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="fd159-104">To create the math input control, you must:</span></span>

-   [<span data-ttu-id="fd159-105">Включение заголовков и библиотек для элемента управления математическими данными</span><span class="sxs-lookup"><span data-stu-id="fd159-105">Include Headers and Libraries for the Math Input Control</span></span>](#include-headers-and-libraries-for-the-math-input-control)
-   [<span data-ttu-id="fd159-106">Объявление указателя управления и вызов CoInitialize для указателя управления</span><span class="sxs-lookup"><span data-stu-id="fd159-106">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [<span data-ttu-id="fd159-107">Отображение элемента управления</span><span class="sxs-lookup"><span data-stu-id="fd159-107">Show the Control</span></span>](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a><span data-ttu-id="fd159-108">Включение заголовков и библиотек для элемента управления математическими данными</span><span class="sxs-lookup"><span data-stu-id="fd159-108">Include Headers and Libraries for the Math Input Control</span></span>

<span data-ttu-id="fd159-109">Следующий код следует поместить в верхнюю часть кода, где будет использоваться элемент управления Math.</span><span class="sxs-lookup"><span data-stu-id="fd159-109">The following code should be placed at the top of your code where you will be using the math input control.</span></span>


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



<span data-ttu-id="fd159-110">Этот код добавит поддержку элемента управления Math для ввода в приложение.</span><span class="sxs-lookup"><span data-stu-id="fd159-110">This code will add support for the math input control to your application.</span></span>

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a><span data-ttu-id="fd159-111">Объявление указателя управления и вызов CoInitialize для указателя управления</span><span class="sxs-lookup"><span data-stu-id="fd159-111">Declare the Control Pointer and Call CoInitialize on the Control Pointer</span></span>

<span data-ttu-id="fd159-112">После включения заголовков для элемента управления можно объявить управляющий указатель и вызвать для него функцию CoInitialize, чтобы создать маркер для интерфейса ввода математических элементов.</span><span class="sxs-lookup"><span data-stu-id="fd159-112">After you have included the headers for your control, you can declare the control pointer and can call CoInitialize on it to create a handle to the math input control interface.</span></span> <span data-ttu-id="fd159-113">Следующий код можно поместить в класс или как глобальную переменную в реализации приложения:</span><span class="sxs-lookup"><span data-stu-id="fd159-113">The following code can be placed in a class or as a global variable in your application's implementation:</span></span>


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



<span data-ttu-id="fd159-114">В следующем коде показано, как можно вызвать функцию CoInitialize для указателя управления.</span><span class="sxs-lookup"><span data-stu-id="fd159-114">The following code shows how you can call CoInitialize on the control pointer.</span></span>


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



<span data-ttu-id="fd159-115">После вызова функции CoInitialize на управляющем указателе у вас есть ссылка на этот элемент управления и у него есть доступ к методам элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fd159-115">After calling CoInitialize on the control pointer, you have a reference to the control and can access the control's methods.</span></span> <span data-ttu-id="fd159-116">Например, можно включить расширенный набор элементов управления, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="fd159-116">For example, you could enable the extended set of controls as shown in the following example.</span></span>


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a><span data-ttu-id="fd159-117">Отображение элемента управления</span><span class="sxs-lookup"><span data-stu-id="fd159-117">Show the Control</span></span>

<span data-ttu-id="fd159-118">Элемент управления не будет автоматически отображаться после его создания.</span><span class="sxs-lookup"><span data-stu-id="fd159-118">The control will not automatically appear after you create it.</span></span> <span data-ttu-id="fd159-119">Чтобы отобразить элемент управления, вызовите метод " [**отобразить**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) " для ссылки на элемент управления, созданной на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="fd159-119">To show the control, call the [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) method on the control reference that you created in the previous step.</span></span> <span data-ttu-id="fd159-120">В следующем коде показано, как можно вызвать метод [**представления**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="fd159-120">The following code demonstrates how the [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) method can be called.</span></span>


```
   hr = g_spMIC->Show();
   
```



<span data-ttu-id="fd159-121">После того как элемент управления отобразится, он будет выглядеть примерно так, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="fd159-121">After the control shows, it will look something like the following illustration.</span></span>

![снимок экрана с элементом управления математическими данными](images/mic.png)

<span data-ttu-id="fd159-123">Обратите внимание, что я включил расширенный набор кнопок, чтобы были доступны **операции** **повтора** и Отмена.</span><span class="sxs-lookup"><span data-stu-id="fd159-123">Note that I have enabled the extended set of buttons so that **Redo** and **Undo** are available.</span></span>

 

 
