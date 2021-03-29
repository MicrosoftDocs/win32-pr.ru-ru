---
title: Средства просмотра и преобразования библиотеки типов
description: Средства просмотра и преобразования библиотеки типов
ms.assetid: 35c29e2c-3ee3-4e73-b925-6aa0ccb50a00
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bf4ac71b3c2c2ff9cc63b196485b9e0aaa4e13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773562"
---
# <a name="type-library-viewers-and-conversion-tools"></a><span data-ttu-id="a1795-103">Средства просмотра и преобразования библиотеки типов</span><span class="sxs-lookup"><span data-stu-id="a1795-103">Type Library Viewers and Conversion Tools</span></span>

<span data-ttu-id="a1795-104">Библиотеки типов содержат спецификацию для одного или нескольких элементов COM, включая классы, интерфейсы, перечисления и многое другое.</span><span class="sxs-lookup"><span data-stu-id="a1795-104">Type libraries contain the specification for one or more COM elements, including classes, interfaces, enumerations, and more.</span></span> <span data-ttu-id="a1795-105">Эти файлы хранятся в стандартном двоичном формате.</span><span class="sxs-lookup"><span data-stu-id="a1795-105">These files are stored in a standard binary format.</span></span> <span data-ttu-id="a1795-106">Библиотека типов может быть автономным файлом с расширением TLB или храниться как ресурс в исполняемом файле, который может иметь расширение. ocx,. dll или. exe.</span><span class="sxs-lookup"><span data-stu-id="a1795-106">A type library can be a stand-alone file with the .tlb file name extension, or it can be stored as a resource in an executable file, which can have an .ocx, .dll, or .exe file name extension.</span></span> <span data-ttu-id="a1795-107">Средства просмотра и преобразования библиотеки типов, описанные ниже, считывают этот формат для получения сведений об элементах COM в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="a1795-107">The type library viewers and conversion tools described following read this format to gain information about the COM elements in the library.</span></span>

<span data-ttu-id="a1795-108">Прежде чем можно будет программировать объект на определенном языке программирования, необходимо иметь возможность просматривать его библиотеку типов на этом языке.</span><span class="sxs-lookup"><span data-stu-id="a1795-108">Before you can program an object in a particular programming language, you must be able to view its type library in that language.</span></span> <span data-ttu-id="a1795-109">Это обеспечивает правильный синтаксис для классов, интерфейсов, методов, свойств и событий COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="a1795-109">Doing this provides you with the proper syntax for the classes, interfaces, methods, properties, and events of the COM object.</span></span>

<span data-ttu-id="a1795-110">Продукты Майкрософт для разработки предоставляют следующие средства, которые можно использовать для создания, извлечения и просмотра сведений о библиотеке типов.</span><span class="sxs-lookup"><span data-stu-id="a1795-110">Microsoft development products provide the following tools that you can use to generate, extract, and view type library information.</span></span>

## <a name="c"></a><span data-ttu-id="a1795-111">C++</span><span class="sxs-lookup"><span data-stu-id="a1795-111">C++</span></span>

-   [<span data-ttu-id="a1795-112">Средство просмотра объектов OLE-COM</span><span class="sxs-lookup"><span data-stu-id="a1795-112">OLE-COM Object Viewer</span></span>](ole-com-object-viewer.md)
-   [<span data-ttu-id="a1795-113">Компилятор MIDL</span><span class="sxs-lookup"><span data-stu-id="a1795-113">MIDL compiler</span></span>](midl-compiler.md)
-   [<span data-ttu-id="a1795-114">MkTypLib</span><span class="sxs-lookup"><span data-stu-id="a1795-114">MkTypLib</span></span>](mktyplib-command-line-tool.md)

## <a name="visual-basic"></a><span data-ttu-id="a1795-115">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a1795-115">Visual Basic</span></span>

-   [<span data-ttu-id="a1795-116">Обозреватель объектов Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a1795-116">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="java"></a><span data-ttu-id="a1795-117">Java</span><span class="sxs-lookup"><span data-stu-id="a1795-117">Java</span></span>

-   [<span data-ttu-id="a1795-118">жактивекс</span><span class="sxs-lookup"><span data-stu-id="a1795-118">JActiveX</span></span>](jactivex-command-line-tool.md)
-   [<span data-ttu-id="a1795-119">Мастер библиотеки типов Java</span><span class="sxs-lookup"><span data-stu-id="a1795-119">Java Type Library Wizard</span></span>](java-type-library-wizard.md)
-   [<span data-ttu-id="a1795-120">жаватлб</span><span class="sxs-lookup"><span data-stu-id="a1795-120">JavaTLB</span></span>](javatlb-command-line-tool.md)

<span data-ttu-id="a1795-121">Общие сведения о взаимодействии этих средств с библиотеками типов см. в разделе [средства для разработчиков использование библиотек типов](how-developer-tools-use-type-libraries.md).</span><span class="sxs-lookup"><span data-stu-id="a1795-121">For an overview of how these tools interact with type libraries, see [How Developer Tools Use Type Libraries](how-developer-tools-use-type-libraries.md).</span></span>

 

 




