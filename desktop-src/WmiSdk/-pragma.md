---
description: Аналогично параметру командной строки. Однако вам не нужно вводить \# команду директивы pragma каждый раз при компиляции MOF-файла.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693553"
---
# <a name="pragma"></a><span data-ttu-id="ea626-104">\#pragma</span><span class="sxs-lookup"><span data-stu-id="ea626-104">\#pragma</span></span>

<span data-ttu-id="ea626-105">Команда препроцессора **\# pragma** аналогична параметру командной строки.</span><span class="sxs-lookup"><span data-stu-id="ea626-105">The **\#pragma** preprocessor command is similar to a command-line switch.</span></span> <span data-ttu-id="ea626-106">Однако вам не нужно вводить команду **\# директивы pragma** каждый раз при компиляции MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="ea626-106">However, you do not need to reenter a **\#pragma** command each time you compile a MOF file.</span></span> <span data-ttu-id="ea626-107">В следующем примере показан синтаксис команды **\# pragma** :</span><span class="sxs-lookup"><span data-stu-id="ea626-107">The following example illustrates **\#pragma** command syntax:</span></span>


```mof
#pragma [command]
```



<span data-ttu-id="ea626-108">Обычно команда **\# pragma** размещается в начале MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="ea626-108">You usually place a **\#pragma** command at the beginning of a MOF file.</span></span> <span data-ttu-id="ea626-109">Однако в тексте MOF-кода можно поместить некоторые команды, например **\# директиву pragma** .</span><span class="sxs-lookup"><span data-stu-id="ea626-109">However, you can place some commands, such as the **\#pragma** command, in the body of your MOF code.</span></span> <span data-ttu-id="ea626-110">В следующем примере показаны команды **\# директивы pragma** , указывающие компилятору MOF, что необходимо разместить классы и экземпляры в корневом \\ пространстве имен CIMV2 и скомпилировать файл, в котором команды включаются во время восстановления репозитория:</span><span class="sxs-lookup"><span data-stu-id="ea626-110">The following example shows **\#pragma** commands that indicate to the MOF compiler that it must place classes and instances in the root\\cimv2 namespace and compile the file in which the commands are included during repository recovery:</span></span>


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



<span data-ttu-id="ea626-111">Ниже перечислены доступные команды **\# директивы pragma** .</span><span class="sxs-lookup"><span data-stu-id="ea626-111">The following lists the available **\#pragma** commands.</span></span>



| <span data-ttu-id="ea626-112">Get-Help</span><span class="sxs-lookup"><span data-stu-id="ea626-112">Command</span></span>                                         | <span data-ttu-id="ea626-113">Описание</span><span class="sxs-lookup"><span data-stu-id="ea626-113">Description</span></span>                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea626-114">**дополнительного соглашения**</span><span class="sxs-lookup"><span data-stu-id="ea626-114">**amendment**</span></span>](pragma-amendment.md)           | <span data-ttu-id="ea626-115">Направляет компилятор MOF для разделения MOF-файла на зависящие от языка и языковые версии.</span><span class="sxs-lookup"><span data-stu-id="ea626-115">Directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> |
| [<span data-ttu-id="ea626-116">**данные автовосстановления**</span><span class="sxs-lookup"><span data-stu-id="ea626-116">**autorecover**</span></span>](pragma-autorecover.md)       | <span data-ttu-id="ea626-117">Добавляет MOF-файл в список файлов, скомпилированных во время восстановления репозитория.</span><span class="sxs-lookup"><span data-stu-id="ea626-117">Adds a MOF file to the list of files compiled during repository recovery.</span></span>                             |
| [<span data-ttu-id="ea626-118">**классфлагс**</span><span class="sxs-lookup"><span data-stu-id="ea626-118">**classflags**</span></span>](pragma-classflags.md)         | <span data-ttu-id="ea626-119">Управляет способом создания или обновления классов в зависимости от указанных флагов.</span><span class="sxs-lookup"><span data-stu-id="ea626-119">Controls the way classes are created or updated depending on the flags specified.</span></span>                     |
| [<span data-ttu-id="ea626-120">**делетекласс**</span><span class="sxs-lookup"><span data-stu-id="ea626-120">**deleteclass**</span></span>](pragma-deleteclass.md)       | <span data-ttu-id="ea626-121">Удаляет существующий класс и его экземпляры из репозитория.</span><span class="sxs-lookup"><span data-stu-id="ea626-121">Deletes an existing class and its instances from the repository.</span></span>                                      |
| [<span data-ttu-id="ea626-122">**DeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="ea626-122">**deleteinstance**</span></span>](pragma-deleteinstance.md) | <span data-ttu-id="ea626-123">Удаляет существующий экземпляр класса из репозитория.</span><span class="sxs-lookup"><span data-stu-id="ea626-123">Deletes an existing instance of a class from the repository.</span></span>                                          |
| [<span data-ttu-id="ea626-124">**инстанцефлагс**</span><span class="sxs-lookup"><span data-stu-id="ea626-124">**instanceflags**</span></span>](pragma-instanceflags.md)   | <span data-ttu-id="ea626-125">Управляет способом создания или обновления экземпляров в зависимости от указанных флагов.</span><span class="sxs-lookup"><span data-stu-id="ea626-125">Controls the way instances are created or updated depending on the flags specified.</span></span>                   |
| [<span data-ttu-id="ea626-126">**имен**</span><span class="sxs-lookup"><span data-stu-id="ea626-126">**namespace**</span></span>](pragma-namespace.md)           | <span data-ttu-id="ea626-127">Запрашивает загрузку MOF-файла компилятором в пространство имен, указанное как *намеспацепас*.</span><span class="sxs-lookup"><span data-stu-id="ea626-127">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="ea626-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ea626-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea626-129">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="ea626-129">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



