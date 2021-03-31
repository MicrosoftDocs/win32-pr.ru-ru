---
title: Средство Command-Line Жаватлб
description: Средство Command-Line Жаватлб
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779964"
---
# <a name="javatlb-command-line-tool"></a><span data-ttu-id="d99c8-103">Средство Command-Line Жаватлб</span><span class="sxs-lookup"><span data-stu-id="d99c8-103">JavaTLB Command-Line Tool</span></span>

<span data-ttu-id="d99c8-104">Жаватлб является компонентом Visual J++ 5,0.</span><span class="sxs-lookup"><span data-stu-id="d99c8-104">JavaTLB is a component of Visual J++ 5.0.</span></span> <span data-ttu-id="d99c8-105">Жаватлб — это приложение командной строки, которое создает файлы классов для COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="d99c8-105">JavaTLB is a command-line application that generates class files for a COM object.</span></span> <span data-ttu-id="d99c8-106">Методы, содержащие типы данных, которые не могут быть точно и безопасно представлены в Java, не преобразуются.</span><span class="sxs-lookup"><span data-stu-id="d99c8-106">Methods that contain data types that cannot be accurately and safely represented in Java are not converted.</span></span>

<span data-ttu-id="d99c8-107">В отличие от [мастера библиотеки типов Java](java-type-library-wizard.md), жаватлб не создает файл сводки, содержащий сведения о библиотеке типов Java.</span><span class="sxs-lookup"><span data-stu-id="d99c8-107">Unlike the [Java Type Library Wizard](java-type-library-wizard.md), JavaTLB does not generate a summary file containing the Java type library information.</span></span>

<span data-ttu-id="d99c8-108">Чтобы создать файлы классов Java для одного COM-объекта, из командной строки выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d99c8-108">To generate Java class files for a single COM object, from the command prompt run:</span></span>

<span data-ttu-id="d99c8-109"> *имя файла* жаватлб</span><span class="sxs-lookup"><span data-stu-id="d99c8-109">**javatlb** *filename*</span></span>

<span data-ttu-id="d99c8-110">где *filename*— имя файла, содержащего библиотеку типов.</span><span class="sxs-lookup"><span data-stu-id="d99c8-110">where *filename* is the name of the file that contains the type library.</span></span> <span data-ttu-id="d99c8-111">Этот файл может иметь любое из следующих расширений имен файлов:. tlb,. OLB,. ocx,. dll или. exe.</span><span class="sxs-lookup"><span data-stu-id="d99c8-111">This file may have any of the following file name extensions: .tlb, .olb, .ocx, .dll, or .exe.</span></span>

<span data-ttu-id="d99c8-112">Чтобы создать файлы классов Java для нескольких COM-объектов, в командной строке выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d99c8-112">To generate Java class files for multiple COM objects, from the command prompt run:</span></span>

<span data-ttu-id="d99c8-113">\**жаватлб @ \* \* \* TextFile*</span><span class="sxs-lookup"><span data-stu-id="d99c8-113">\**javatlb @\*\*\*TextFile*</span></span>

<span data-ttu-id="d99c8-114">где *TextFile* — это имя текстового файла, содержащего список файлов, содержащих библиотеки типов COM-объектов.</span><span class="sxs-lookup"><span data-stu-id="d99c8-114">where *TextFile* is the name of a text file that contains a list of the files containing the COM object's type libraries.</span></span>

> [!Note]  
> <span data-ttu-id="d99c8-115">В Visual J++ 6,0 средство командной строки Жаватлб заменяется [средством жактивекс](jactivex-command-line-tool.md).</span><span class="sxs-lookup"><span data-stu-id="d99c8-115">In Visual J++ 6.0, the JavaTLB command-line tool is replaced by the [JActiveX tool](jactivex-command-line-tool.md).</span></span> <span data-ttu-id="d99c8-116">Дополнительные сведения см. в документации по Visual J++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="d99c8-116">For more information, see the Visual J++ 6.0 documentation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d99c8-117">См. также</span><span class="sxs-lookup"><span data-stu-id="d99c8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d99c8-118">Перевод на Java</span><span class="sxs-lookup"><span data-stu-id="d99c8-118">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




