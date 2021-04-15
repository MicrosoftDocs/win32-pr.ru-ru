---
description: Если компилятор MOF не может завершить компиляцию MOF-файла, репозиторий WMI может остаться в неопределенном состоянии.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Обработка ошибок с помощью компилятора MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498117"
---
# <a name="handling-errors-with-the-mof-compiler"></a><span data-ttu-id="b5e19-103">Обработка ошибок с помощью компилятора MOF</span><span class="sxs-lookup"><span data-stu-id="b5e19-103">Handling Errors with the MOF Compiler</span></span>

<span data-ttu-id="b5e19-104">Если компилятор MOF не может завершить компиляцию MOF-файла, репозиторий WMI может остаться в неопределенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="b5e19-104">If the MOF compiler cannot finish compiling a MOF file, the WMI repository may be left in an undefined state.</span></span> <span data-ttu-id="b5e19-105">Например, если компилируется MOF-файл и используется параметр командной строки **– Class: креатеонли** , компиляция завершается, если класс, указанный в MOF-файле, уже существует.</span><span class="sxs-lookup"><span data-stu-id="b5e19-105">For example, if you are compiling a MOF file and you use the **-class:createonly** command-line switch, the compilation terminates if a class specified in the MOF file already exists.</span></span> <span data-ttu-id="b5e19-106">Компилятор MOF хранит в репозитории все классы или экземпляры, которые были определены до точки остановки компилятора.</span><span class="sxs-lookup"><span data-stu-id="b5e19-106">The MOF compiler stores in the repository any classes or instances that were defined up to the point where the compiler stops.</span></span> <span data-ttu-id="b5e19-107">В некоторых случаях это может привести к выходу хранилища WMI в неопределенном условии.</span><span class="sxs-lookup"><span data-stu-id="b5e19-107">In some cases, this can leave the WMI repository in an undefined condition.</span></span>

<span data-ttu-id="b5e19-108">В этом случае может потребоваться отключить WMI, удалить репозиторий WMI и перестроить WMI.</span><span class="sxs-lookup"><span data-stu-id="b5e19-108">In this situation, you may need to stop WMI, delete the WMI repository, and have WMI rebuild it.</span></span> <span data-ttu-id="b5e19-109">Все MOF-файлы, содержащие [команду](preprocessor-commands.md) [**директивы pragma автовосстановления**](pragma-autorecover.md) , перестраиваются при перезапуске инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="b5e19-109">All MOF files that contain the [**pragma autorecover**](pragma-autorecover.md) [preprocessor command](preprocessor-commands.md) are rebuilt when WMI is restarted.</span></span> <span data-ttu-id="b5e19-110">Необходимо вручную перекомпилировать все MOF-файлы, не содержащие `#pragma autorecover` инструкцию.</span><span class="sxs-lookup"><span data-stu-id="b5e19-110">You must manually recompile any MOF files that do not include a `#pragma autorecover` statement.</span></span>

<span data-ttu-id="b5e19-111">Дополнительные сведения об объявлении классов и экземпляров с помощью синтаксиса MOF см. в разделе [Разработка классов MOF-файл (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="b5e19-111">For more information about how to declare classes and instances using the MOF syntax, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5e19-112">См. также</span><span class="sxs-lookup"><span data-stu-id="b5e19-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5e19-113">Компиляция MOF-файлов</span><span class="sxs-lookup"><span data-stu-id="b5e19-113">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="b5e19-114">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="b5e19-114">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="b5e19-115">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="b5e19-115">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



