---
description: Необходимо скомпилировать главный MOF-файл, чтобы создать независимые от языка и языковые MOF-файлы.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Компиляция локализованных MOF-файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ab1341a37269ba98fdbbdecaa64b5e5a119703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346765"
---
# <a name="compiling-localized-mof-files"></a><span data-ttu-id="e9690-103">Компиляция локализованных MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="e9690-103">Compiling Localized MOF Files</span></span>

<span data-ttu-id="e9690-104">Необходимо скомпилировать главный MOF-файл, чтобы создать независимые от языка и языковые MOF-файлы.</span><span class="sxs-lookup"><span data-stu-id="e9690-104">You must compile your master MOF file to create the language-neutral and language-specific MOF files.</span></span>

<span data-ttu-id="e9690-105">Введите следующую команду в командной строке, чтобы скомпилировать главный MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="e9690-105">Type the following command at a command prompt to compile a master MOF file.</span></span>

<span data-ttu-id="e9690-106">**mofcomp-MOF: Лнмоф. mof-МФЛ: Лсмоф. МФЛ-поправка: MS \_ 409 мастермоф. mof**</span><span class="sxs-lookup"><span data-stu-id="e9690-106">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

<span data-ttu-id="e9690-107">При выполнении этой команды компилятор MOF создает два MOF-файла в исходном файле Мастермоф. mof.</span><span class="sxs-lookup"><span data-stu-id="e9690-107">When you run this command, the MOF compiler creates two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="e9690-108">Компилятор MOF создает не зависящую от языка версию Лнмоф. mof, в которой удаляются все зависящие от языка элементы.</span><span class="sxs-lookup"><span data-stu-id="e9690-108">The MOF compiler produces a language-neutral version, Lnmof.mof, in which all language-specific items are removed.</span></span> <span data-ttu-id="e9690-109">Также создается вторая, зависящая от языка версия Лсмоф. mof. Этот файл содержит только элементы, которые были помечены [**исправленной**](qualifier-flavors.md) разновидностью квалификатора в файле мастермоф. mof.</span><span class="sxs-lookup"><span data-stu-id="e9690-109">A second, language-specific version, Lsmof.mof, is also created; this file contains only items that were marked with the [**Amended**](qualifier-flavors.md) Qualifier Flavor in the Mastermof.mof file.</span></span>

<span data-ttu-id="e9690-110">В следующем примере кода показано содержимое файла MOF, не зависящего от языка (Лнмоф. MOF), который создается.</span><span class="sxs-lookup"><span data-stu-id="e9690-110">The following code example shows the contents of the language-neutral MOF file (Lnmof.mof) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

<span data-ttu-id="e9690-111">В следующем примере кода показано содержимое создаваемого MOF-файла (Лсмоф. МФЛ) для конкретного языка.</span><span class="sxs-lookup"><span data-stu-id="e9690-111">The following code example shows the contents of the language-specific MOF file (Lsmof.mfl) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

<span data-ttu-id="e9690-112">При компиляции MOF-файла с [**измененным**](qualifier-flavors.md) квалификатором создаются только отдельные зависящие от языка MOF-файлы. репозиторий CIM не обновляется с учетом новых сведений о классе.</span><span class="sxs-lookup"><span data-stu-id="e9690-112">Compiling a MOF file with the [**Amended**](qualifier-flavors.md) qualifier only generates separate language-neutral and language-specific MOF files; the CIM repository is not updated with the new class information.</span></span> <span data-ttu-id="e9690-113">Необходимо использовать компилятор MOF для компиляции двух файлов MOF, созданных первой компиляцией до того, как все сведения о классе будут доступны инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="e9690-113">You must use the MOF compiler to compile the two MOF files that the first compilation produced before any class information is available to WMI.</span></span>

<span data-ttu-id="e9690-114">При компиляции главного MOF-файла в MOF-файл, зависящий от языка, переносятся только квалификаторы с [**измененной**](qualifier-flavors.md) разновидностью.</span><span class="sxs-lookup"><span data-stu-id="e9690-114">When you compile a master MOF file, only qualifiers with the [**Amended**](qualifier-flavors.md) flavor are moved to the language-specific MOF file.</span></span> <span data-ttu-id="e9690-115">Квалификаторы, не имеющие **измененной** версии, не локализуются и существуют только в определении базового класса в MOF-файле, не зависящем от языка.</span><span class="sxs-lookup"><span data-stu-id="e9690-115">Qualifiers that do not have the **Amended** flavor are not localized and only exist in the basic class definition in the language-neutral MOF file.</span></span> <span data-ttu-id="e9690-116">Нелокализованные квалификаторы можно использовать для описаний по умолчанию, если локализация недоступна.</span><span class="sxs-lookup"><span data-stu-id="e9690-116">Nonlocalized qualifiers can be used for default descriptions if localized descriptions are not available.</span></span>

<span data-ttu-id="e9690-117">Вместо [**уточнения**](qualifier-flavors.md) в качестве коммутатора для компилятора MOF можно использовать команду поправки [pragma](pragma-amendment.md) .</span><span class="sxs-lookup"><span data-stu-id="e9690-117">You can use the [pragma amendment](pragma-amendment.md) command instead of specifying [**Amended**](qualifier-flavors.md) as a switch to the MOF compiler.</span></span> <span data-ttu-id="e9690-118">Любой из этих параметров эквивалентен запросу версий MOF-файла, зависящих от языка и языка.</span><span class="sxs-lookup"><span data-stu-id="e9690-118">Either of these options are equivalent to requesting language-specific and language-neutral versions of a MOF file.</span></span> <span data-ttu-id="e9690-119">При использовании команды с параметрами pragma или **исправленного** параметра командной строки необходимо указать имена выходных файлов с помощью параметров **-МФЛ** и **-MOF** в командной строке.</span><span class="sxs-lookup"><span data-stu-id="e9690-119">If you use either the pragma amendment command or the **Amended** command-line option, you must specify the name of the output files using the **-MFL** and **-MOF** options at the command prompt.</span></span>

> [!Note]  
> <span data-ttu-id="e9690-120">Не зависящий от языка MOF-файл, создаваемый компилятором MOF, содержит десятичный эквивалент идентификатора локали, даже если это значение было указано в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="e9690-120">The language-neutral MOF file that the MOF compiler generates contains the decimal equivalent of the locale ID, even if this value was entered in hexadecimal.</span></span> <span data-ttu-id="e9690-121">В приведенном выше примере компилятор преобразует значение 0x409 в десятичное число 1033 для выходного файла Лнмоф. mof.</span><span class="sxs-lookup"><span data-stu-id="e9690-121">In the example above, the compiler has converted the value 0x409 to the decimal number 1033 for the Lnmof.mof output file.</span></span>

 

 

 



