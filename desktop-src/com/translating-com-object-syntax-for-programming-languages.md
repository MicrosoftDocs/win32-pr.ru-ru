---
title: Преобразование синтаксиса COM-объектов для языков программирования
description: Преобразование синтаксиса COM-объектов для языков программирования
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888235"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a><span data-ttu-id="dcf56-103">Преобразование синтаксиса COM-объектов для языков программирования</span><span class="sxs-lookup"><span data-stu-id="dcf56-103">Translating COM Object Syntax for Programming Languages</span></span>

<span data-ttu-id="dcf56-104">Чтобы вызвать COM-объект из приложения, написанного на языке программирования, отличном от того, который использовался для написания COM-объекта, необходимо сначала преобразовать синтаксис объекта в язык программирования.</span><span class="sxs-lookup"><span data-stu-id="dcf56-104">To call a COM object from an application written in a programming language other than the one used to write the COM object, you must first translate the object's syntax to your programming language.</span></span> <span data-ttu-id="dcf56-105">Это можно сделать, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="dcf56-105">This can be done using the following steps:</span></span>

1.  <span data-ttu-id="dcf56-106">Просмотрите библиотеку типов COM-объекта в синтаксисе языка программирования.</span><span class="sxs-lookup"><span data-stu-id="dcf56-106">View the COM object's type library in your programming language's syntax.</span></span> <span data-ttu-id="dcf56-107">Это позволяет использовать описания классов, интерфейсов, методов, свойств и событий объекта в используемом синтаксисе языка.</span><span class="sxs-lookup"><span data-stu-id="dcf56-107">Doing this provides you with descriptions of the object's classes, interfaces, methods, properties and events in the language syntax you use.</span></span>

    <span data-ttu-id="dcf56-108">Продукты для разработчиков Microsoft предоставляют несколько средств, помогающих просматривать и преобразовывать библиотеки типов.</span><span class="sxs-lookup"><span data-stu-id="dcf56-108">Microsoft developer products provide several tools to assist you in viewing and converting type libraries.</span></span> <span data-ttu-id="dcf56-109">Дополнительные сведения см. в статьях [средства просмотра и преобразования библиотеки типов](type-library-viewers-and-conversion-tools.md) , а [средства для разработчиков использование библиотек типов](how-developer-tools-use-type-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="dcf56-109">For more information, see [Type Library Viewers and Conversion Tools](type-library-viewers-and-conversion-tools.md) and [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

    <span data-ttu-id="dcf56-110">После просмотра библиотеки типов объектов на предпочтительном языке программирования можно сравнить его синтаксис с тем, который содержится в документации по объекту.</span><span class="sxs-lookup"><span data-stu-id="dcf56-110">Once you can view the object's type library in your preferred programming language, you can compare its syntax to that in the documentation for the object.</span></span> <span data-ttu-id="dcf56-111">Если объект документирован на языке программирования, отличном от того, который используется, типы данных и синтаксис могут отличаться, но описания параметров, возвращаемые значения и функциональность объекта должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="dcf56-111">If the object is documented in a programming language other than the one you are using, the data types and syntax may differ, but descriptions of parameters, return values, and the object's functionality should be the same.</span></span>

2.  <span data-ttu-id="dcf56-112">Примите во внимание любые особые соображения, касающиеся перевода на язык программирования.</span><span class="sxs-lookup"><span data-stu-id="dcf56-112">Take into account any special considerations for translating to your programming language.</span></span>

    <span data-ttu-id="dcf56-113">Поскольку каждый язык программирования определяет концепции, которые могут не иметь эквивалента в других языках, некоторые функции объекта могут работать иначе на другом языке или вообще не быть доступными.</span><span class="sxs-lookup"><span data-stu-id="dcf56-113">Because each programming language defines concepts that may not have an equivalent in other languages, some of an object's functionality may work differently in another language, or not be available at all.</span></span> <span data-ttu-id="dcf56-114">Например, Visual Basic язык программирования не распознает типы данных C++ без знака, например **унсигнедâ Long**.</span><span class="sxs-lookup"><span data-stu-id="dcf56-114">For example, the Visual Basic programming language does not recognize C++ unsigned data types, such as **unsignedÂ long**.</span></span> <span data-ttu-id="dcf56-115">Приложение, написанное на Visual Basic, не может использовать методы COM, которые принимают или возвращают переменные неподписанных типов данных.</span><span class="sxs-lookup"><span data-stu-id="dcf56-115">An application written in Visual Basic cannot use COM methods that accept or return unsigned data type variables.</span></span>

3.  <span data-ttu-id="dcf56-116">Добавьте скомпилированный код COM-объекта в проект.</span><span class="sxs-lookup"><span data-stu-id="dcf56-116">Add the COM object's compiled code to your project.</span></span> <span data-ttu-id="dcf56-117">Скомпилированный код обычно содержится в файле. dll или. ocx.</span><span class="sxs-lookup"><span data-stu-id="dcf56-117">The compiled code is typically contained in a .dll or .ocx file.</span></span> <span data-ttu-id="dcf56-118">Этот шаг необходим для того, чтобы компилятор распознал классы COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="dcf56-118">This step is necessary for the compiler to recognize the COM object's classes.</span></span> <span data-ttu-id="dcf56-119">После добавления COM-объекта приложение может использовать его классы и интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="dcf56-119">After you add the COM object, your application can use its classes and interfaces.</span></span>

<span data-ttu-id="dcf56-120">В следующих разделах описывается преобразование и использование COM-объектов на различных языках программирования.</span><span class="sxs-lookup"><span data-stu-id="dcf56-120">The following topics describe how to translate and use COM objects in a variety of programming languages:</span></span>

-   [<span data-ttu-id="dcf56-121">Преобразование в C++</span><span class="sxs-lookup"><span data-stu-id="dcf56-121">Translating to C++</span></span>](translating-to-c--.md)
-   [<span data-ttu-id="dcf56-122">Перевод в Visual Basic</span><span class="sxs-lookup"><span data-stu-id="dcf56-122">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
-   [<span data-ttu-id="dcf56-123">Перевод на Java</span><span class="sxs-lookup"><span data-stu-id="dcf56-123">Translating to Java</span></span>](translating-to-java.md)

<span data-ttu-id="dcf56-124">В этих разделах описываются средства и процессы преобразования, предоставляемые продуктами Майкрософт для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="dcf56-124">These topics describe conversion tools and processes provided by Microsoft developer products.</span></span> <span data-ttu-id="dcf56-125">Инструкции по программированию COM-объектов с помощью средств разработки, созданных другими компаниями, см. в документации по средствам разработки.</span><span class="sxs-lookup"><span data-stu-id="dcf56-125">For instructions on how to program COM objects using development tools created by other companies, see those development tools' documentation.</span></span>

 

 




