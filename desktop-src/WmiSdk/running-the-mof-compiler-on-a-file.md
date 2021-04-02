---
description: 'При компиляции MOF-файла можно выбрать один из двух вариантов: с помощью служебной программы командной строки или с помощью программного интерфейса.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Запуск компилятора MOF в файле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1605544e05f59670f9e6fd73fcd8c01862b46c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263815"
---
# <a name="running-the-mof-compiler-on-a-file"></a><span data-ttu-id="ecdaf-103">Запуск компилятора MOF в файле</span><span class="sxs-lookup"><span data-stu-id="ecdaf-103">Running the MOF Compiler on a File</span></span>

<span data-ttu-id="ecdaf-104">При компиляции MOF-файла можно выбрать один из двух вариантов: с помощью служебной программы командной строки или с помощью программного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-104">You have two choices when compiling a MOF file: using the command-line utility or using a programmatic interface.</span></span>

<span data-ttu-id="ecdaf-105">До запуска компилятора MOF [**Mofcomp.exe**](mofcomp.md)поставщик не зарегистрирован в WMI и классы, созданные в MOF-файле, недоступны в [*репозитории WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="ecdaf-105">Until you run the MOF compiler, [**Mofcomp.exe**](mofcomp.md), a provider is not registered with WMI and the classes it created in the MOF file are not available in the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="ecdaf-106">В следующей процедуре описывается компиляция MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-106">The following procedure describes how to compile a MOF file.</span></span>

<span data-ttu-id="ecdaf-107">**Запуск компилятора MOF в файле из командной строки**</span><span class="sxs-lookup"><span data-stu-id="ecdaf-107">**To run the MOF compiler on a file from the command line**</span></span>

1.  <span data-ttu-id="ecdaf-108">Вызовите компилятор MOF из командной строки, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-108">Call the MOF compiler from the command line, using the following syntax.</span></span>

    <span data-ttu-id="ecdaf-109">**mofcomp** *моффиле \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="ecdaf-109">**mofcomp** *MOFfile\*\*\*.mof*\*</span></span>

    <span data-ttu-id="ecdaf-110">Компилятор MOF поддерживает различные параметры для управления особыми сценариями обработки.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-110">The MOF compiler supports a variety of switches to control special processing situations.</span></span> <span data-ttu-id="ecdaf-111">Все параметры являются необязательными, и допускается любое сочетание параметров.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-111">All of the switches are optional, and any combination of switches is allowed.</span></span> <span data-ttu-id="ecdaf-112">Однако не имеет смысла использовать некоторые параметры в сочетании с другими.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-112">However, it does not make sense to use some of the switches in combination with others.</span></span> <span data-ttu-id="ecdaf-113">Например, чтобы объединить параметры **-Class: упдатеонли** и **-Class: креатеонли** , в результате компилятор не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-113">For example, to combine the **-class:updateonly** and **-class:createonly** switches results in the compiler not performing any action.</span></span>

    <span data-ttu-id="ecdaf-114">По умолчанию Mofcomp.exe сохраняет скомпилированные классы в корневом \\ пространстве имен WMI по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-114">By default, Mofcomp.exe stores the compiled classes in the root\\default WMI namespace.</span></span> <span data-ttu-id="ecdaf-115">Обратите внимание, что пространство имен по умолчанию для Mofcomp.exe не совпадает с пространством имен по умолчанию для сценариев.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-115">Note that the default namespace for Mofcomp.exe is not the same as the default namespace for scripting.</span></span> <span data-ttu-id="ecdaf-116">Пространство имен по умолчанию для сценариев задается в элементе управления WMI на вкладке Дополнительно. Дополнительные сведения см. [в разделе Настройка безопасности пространства имен с помощью элемента управления WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="ecdaf-116">The default namespace for scripting is specified in the WMI Control on the Advanced tab. For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

    <span data-ttu-id="ecdaf-117">Изменить пространство имен, которое получает классы, можно двумя способами.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-117">You can change the namespace that receives the classes in two ways.</span></span>

    1.  <span data-ttu-id="ecdaf-118">Используйте параметр **-N** для команды **mofcomp** .</span><span class="sxs-lookup"><span data-stu-id="ecdaf-118">Use the **-N** switch for the **mofcomp** command.</span></span>
    2.  <span data-ttu-id="ecdaf-119">Вставьте \# [**пространство имен директивы pragma**](pragma-namespace.md) для команды препроцессора в MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-119">Insert the preprocessor command \#[**pragma namespace**](pragma-namespace.md) in the MOF file.</span></span>

2.  <span data-ttu-id="ecdaf-120">При необходимости можно программно скомпилировать MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="ecdaf-120">Optionally, you can compile a MOF file programmatically.</span></span> <span data-ttu-id="ecdaf-121">Дополнительные сведения см. в разделе [**имофкомпилер**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span><span class="sxs-lookup"><span data-stu-id="ecdaf-121">For more information, see [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ecdaf-122">См. также</span><span class="sxs-lookup"><span data-stu-id="ecdaf-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecdaf-123">Компиляция MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="ecdaf-123">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="ecdaf-124">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="ecdaf-124">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="ecdaf-125">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="ecdaf-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



