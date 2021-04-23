---
description: Создание локализованных определений классов — это процесс в три этапа.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Создание локализованных определений классов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105713307"
---
# <a name="creating-localized-class-definitions"></a><span data-ttu-id="5b960-103">Создание локализованных определений классов</span><span class="sxs-lookup"><span data-stu-id="5b960-103">Creating Localized Class Definitions</span></span>

<span data-ttu-id="5b960-104">Создание локализованных определений классов — это процесс в три этапа.</span><span class="sxs-lookup"><span data-stu-id="5b960-104">Creating localized class definitions is a three-step process.</span></span> <span data-ttu-id="5b960-105">Начните с написания MOF-кода, определяющего классы, включая все квалификаторы, которые должны быть локализованы.</span><span class="sxs-lookup"><span data-stu-id="5b960-105">You start by writing MOF code that defines the classes, including all qualifiers that must be localized.</span></span> <span data-ttu-id="5b960-106">Этот исходный файл называется файлом "Master MOF", так как он содержит все квалификаторы и свойства, определяющие класс.</span><span class="sxs-lookup"><span data-stu-id="5b960-106">This original file is called the "master MOF" file because it contains all of the qualifiers and properties that define the class.</span></span>

<span data-ttu-id="5b960-107">Затем используйте [компилятор MOF](mofcomp.md) , чтобы создать языковые версии MOF-файла, зависящие от языка и языка.</span><span class="sxs-lookup"><span data-stu-id="5b960-107">Next, use the [MOF compiler](mofcomp.md) to create the language-neutral and language-specific versions of the MOF file.</span></span> <span data-ttu-id="5b960-108">Компилятор MOF размещает базовое описание класса в новом MOF-файле и создает локализованную версию MOF-файла, который содержит только свойства и квалификаторы, которые должны быть локализованы.</span><span class="sxs-lookup"><span data-stu-id="5b960-108">The MOF compiler places the basic class description in a new MOF file and creates a localized version of the MOF file that contains only the properties and qualifiers that must be localized.</span></span> <span data-ttu-id="5b960-109">Несмотря на то, что версии MOF-файла, зависящие от языка и языка, могут иметь одинаковое имя файла, следует использовать расширение МФЛ, чтобы указать, что файл содержит локализованные сведения.</span><span class="sxs-lookup"><span data-stu-id="5b960-109">Although the language-specific and language-neutral versions of the MOF file can have the same file name, you should use a .mfl file name extension to indicate that the file contains localized information.</span></span> <span data-ttu-id="5b960-110">При необходимости можно локализовать файл. МФЛ в другие языковые стандарты.</span><span class="sxs-lookup"><span data-stu-id="5b960-110">You can localize the .mfl file to other locales, if necessary.</span></span> <span data-ttu-id="5b960-111">Для хранения определений классов в репозитории CIM требуется дополнительный шаг использования компилятора MOF для компиляции как нейтрального к определенному языку, так и MOF-файлов, зависящих от языка.</span><span class="sxs-lookup"><span data-stu-id="5b960-111">Storing the class definitions in the CIM repository requires an additional step of using the MOF compiler to compile both the language-neutral and the language-specific MOF files.</span></span>

<span data-ttu-id="5b960-112">Следующие шаги описывают создание и сохранение локализованного определения класса.</span><span class="sxs-lookup"><span data-stu-id="5b960-112">The following steps describe how to create and store a localized class definition.</span></span>

<span data-ttu-id="5b960-113">**Создание и сохранение локализованного определения класса**</span><span class="sxs-lookup"><span data-stu-id="5b960-113">**To create and store a localized class definition**</span></span>

1.  <span data-ttu-id="5b960-114">Создайте главный MOF-файл, определяющий классы, которые нужно локализовать.</span><span class="sxs-lookup"><span data-stu-id="5b960-114">Create the master MOF file that defines the classes that you want localized.</span></span>

    <span data-ttu-id="5b960-115">Сохраните этот MOF-код в файл с именем Мастермоф. mof.</span><span class="sxs-lookup"><span data-stu-id="5b960-115">Save this MOF code in a file called Mastermof.mof.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  <span data-ttu-id="5b960-116">Создайте языковые версии MOF-файла, зависящие от языка, и язык, выполнив компиляцию файла Мастермоф. mof.</span><span class="sxs-lookup"><span data-stu-id="5b960-116">Create language-neutral and language-specific versions of the MOF file by compiling the MasterMOF.mof file.</span></span>

    <span data-ttu-id="5b960-117">Введите следующую команду в командной строке, чтобы скомпилировать файл Мастермоф. mof.</span><span class="sxs-lookup"><span data-stu-id="5b960-117">Type the following command at a command prompt to compile the MasterMOF.mof file.</span></span>

    <span data-ttu-id="5b960-118">**mofcomp-MOF: Лнмоф. mof-МФЛ: Лсмоф. МФЛ-поправка: MS \_ 409 мастермоф. mof**</span><span class="sxs-lookup"><span data-stu-id="5b960-118">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

3.  <span data-ttu-id="5b960-119">Скомпилируйте файлы, не зависящие от языка (Лнмоф. MOF) и зависящие от языка (Лсмоф. МФЛ), и храните сведения о классах в репозитории CIM.</span><span class="sxs-lookup"><span data-stu-id="5b960-119">Compile the language-neutral (Lnmof.mof) and language-specific (Lsmof.mfl) files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="5b960-120">Введите следующие команды в командной строке, чтобы сохранить сведения о классе в репозитории CIM.</span><span class="sxs-lookup"><span data-stu-id="5b960-120">Type the following commands at a command prompt to store the class information in the CIM repository.</span></span>

    <span data-ttu-id="5b960-121">**Mofcomp Лнмоф. mof**</span><span class="sxs-lookup"><span data-stu-id="5b960-121">**Mofcomp Lnmof.mof**</span></span>

    <span data-ttu-id="5b960-122">**Mofcomp Лсмоф. МФЛ**</span><span class="sxs-lookup"><span data-stu-id="5b960-122">**Mofcomp Lsmof.mfl**</span></span>

    <span data-ttu-id="5b960-123">После компиляции этих файлов в корневом \\ пространстве имен и в корневом \\ \\ \_ пространстве имен MS 409 будет определено определение класса, не зависящее от языка.</span><span class="sxs-lookup"><span data-stu-id="5b960-123">After you compile these files, you will have a language-neutral class definition in the root\\test namespace and a localized class definition in the root\\test\\ms\_409 namespace.</span></span> <span data-ttu-id="5b960-124">Дополнительные сведения о компиляции локализованных MOF-файлов см. в разделе [Компиляция локализованных MOF-файлов](compiling-localized-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="5b960-124">For more information about compiling localized MOF files, see [Compiling Localized MOF files](compiling-localized-mof-files.md).</span></span>

 

 



