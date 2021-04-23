---
description: Направляет компилятор MOF для разделения MOF-файла на зависящие от языка и языковые версии.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: поправка директивы pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811423"
---
# <a name="pragma-amendment"></a><span data-ttu-id="42cba-103">поправка директивы pragma</span><span class="sxs-lookup"><span data-stu-id="42cba-103">pragma amendment</span></span>

<span data-ttu-id="42cba-104">Команда препроцессора " **директива pragma** Reprocess" направляет компилятор MOF для разделения MOF-файла на зависящие от языка и языковые версии.</span><span class="sxs-lookup"><span data-stu-id="42cba-104">The **pragma amendment** preprocessor command directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> <span data-ttu-id="42cba-105">MOF-файл, зависящий от языка, перемещает измененные квалификаторы в пространство имен для определенного языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="42cba-105">The language-specific MOF file moves amended qualifiers to a namespace for a specific locale.</span></span> <span data-ttu-id="42cba-106">Затем вы компилируете файлы MOF, не зависящие от языка и на языке, для хранения сведений о классах в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="42cba-106">You then compile the language-specific and language-neutral MOF files to store class information in the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="42cba-107">Примеры</span><span class="sxs-lookup"><span data-stu-id="42cba-107">Examples</span></span>

<span data-ttu-id="42cba-108">В следующем примере показано, как создать MOF-файл, содержащий измененные квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="42cba-108">The following example shows how to create a MOF file that contains amended qualifiers.</span></span> <span data-ttu-id="42cba-109">Затем MOF-код можно скомпилировать с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="42cba-109">You can then compile the MOF code with the following command:</span></span>

<span data-ttu-id="42cba-110">**mofcomp** **-MOF: лнмоф. mof** **-МФЛ: лсмоф. МФЛ** **мастермоф. mof**</span><span class="sxs-lookup"><span data-stu-id="42cba-110">**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**</span></span>

<span data-ttu-id="42cba-111">Эта команда предписывает компилятору MOF создать два MOF-файла из исходного Мастермоф. mof.</span><span class="sxs-lookup"><span data-stu-id="42cba-111">The command instructs the MOF compiler to produce two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="42cba-112">Компилятор MOF создает не зависящую от языка версию MOF-файла с именем Лнмоф. mof, при этом удаляются все зависящие от языка элементы.</span><span class="sxs-lookup"><span data-stu-id="42cba-112">The MOF compiler produces a language-neutral version of the MOF file, called Lnmof.mof, with all language-specific items removed.</span></span> <span data-ttu-id="42cba-113">Компилятор также создает второй, зависящий от языка MOF-файл с именем Лсмоф. МФЛ, который содержит только те элементы, которые необходимо локализовать.</span><span class="sxs-lookup"><span data-stu-id="42cba-113">The compiler also creates a second, language-specific MOF file called Lsmof.mfl that contains only items that you must localize.</span></span>

> [!Note]  
> <span data-ttu-id="42cba-114">При разделении MOF-файла **с квалификатором или с помощью** **директивы pragma** reby необходимо указать параметры **-MOF** и **-МФЛ** .</span><span class="sxs-lookup"><span data-stu-id="42cba-114">When you are splitting a MOF file with the **amendment** qualifier or the **pragma amendment** command, you must specify the **-MOF** and **-MFL** options.</span></span> <span data-ttu-id="42cba-115">В противном случае компилятор не создает никаких выходных файлов.</span><span class="sxs-lookup"><span data-stu-id="42cba-115">Otherwise, the compiler does not generate any output files.</span></span> <span data-ttu-id="42cba-116">Затем необходимо скомпилировать два выходных файла, чтобы сделать сведения о классе доступными для инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="42cba-116">You must then compile the two output files to make the class information available to WMI.</span></span>

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
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



## <a name="requirements"></a><span data-ttu-id="42cba-117">Требования</span><span class="sxs-lookup"><span data-stu-id="42cba-117">Requirements</span></span>



| <span data-ttu-id="42cba-118">Требование</span><span class="sxs-lookup"><span data-stu-id="42cba-118">Requirement</span></span> | <span data-ttu-id="42cba-119">Значение</span><span class="sxs-lookup"><span data-stu-id="42cba-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="42cba-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42cba-120">Minimum supported client</span></span><br/> | <span data-ttu-id="42cba-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42cba-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="42cba-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42cba-122">Minimum supported server</span></span><br/> | <span data-ttu-id="42cba-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42cba-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42cba-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42cba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42cba-125">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="42cba-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




