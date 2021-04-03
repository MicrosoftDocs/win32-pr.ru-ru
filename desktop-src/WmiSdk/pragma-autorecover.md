---
description: Добавляет MOF-файл в список файлов, скомпилированных во время восстановления репозитория.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: Директива pragma автовосстановления
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
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999196"
---
# <a name="pragma-autorecover"></a><span data-ttu-id="ed382-103">Директива pragma автовосстановления</span><span class="sxs-lookup"><span data-stu-id="ed382-103">pragma autorecover</span></span>

<span data-ttu-id="ed382-104">Команда препроцессора **pragma автосохранения** добавляет MOF-файл в список файлов, скомпилированных во время восстановления репозитория.</span><span class="sxs-lookup"><span data-stu-id="ed382-104">The **pragma autorecover** preprocessor command adds a MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="ed382-105">Список MOF-файлов **автовосстановления** хранится в следующем разделе реестра:</span><span class="sxs-lookup"><span data-stu-id="ed382-105">The list of **autorecover** MOF files is stored in this registry key:</span></span>

<span data-ttu-id="ed382-106">**HKey \_ Локальное \_** \\ **программное обеспечение** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Автовосстановление MOF**</span><span class="sxs-lookup"><span data-stu-id="ed382-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**autorecover mofs**</span></span>

<span data-ttu-id="ed382-107">Инструментарий WMI проверяет целостность репозитория WMI при запуске операционной системой инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="ed382-107">WMI checks the integrity of the WMI repository when the operating system starts WMI.</span></span> <span data-ttu-id="ed382-108">Если репозиторий поврежден, WMI автоматически перестраивает репозиторий и перекомпилирует все MOF-файлы, перечисленные в этом разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="ed382-108">If the repository is damaged, WMI automatically rebuilds the repository and recompiles any MOF files listed in this key in the registry.</span></span>

<span data-ttu-id="ed382-109">Ниже описан синтаксис команды pragma автосохранения.</span><span class="sxs-lookup"><span data-stu-id="ed382-109">The following describes the syntax for the pragma autorecover command:</span></span>


```mof
#pragma autorecover
```



<span data-ttu-id="ed382-110">Однако при использовании этой команды необходимо учитывать следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="ed382-110">However, you must observe the following restrictions when using this command:</span></span>

-   <span data-ttu-id="ed382-111">Инструментарий WMI не может восстанавливать MOF-файлы, расположенные на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ed382-111">WMI cannot recover MOF files located on a remote computer.</span></span>

    <span data-ttu-id="ed382-112">Таким образом, MOF-файлы, перечисленные в этом разделе реестра, должны находиться на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ed382-112">Therefore, the MOF files listed in this registry key must reside on the local computer.</span></span>

-   <span data-ttu-id="ed382-113">Нельзя указать параметры командной строки, используемые компилятором MOF, когда WMI восстанавливает MOF-файл.</span><span class="sxs-lookup"><span data-stu-id="ed382-113">You cannot specify the command-line switches that the MOF compiler uses when WMI recovers a MOF file.</span></span>

    <span data-ttu-id="ed382-114">Поэтому в MOF-файл следует включать команды [pragma](-pragma.md) , которые делают ненужными параметры командной строки.</span><span class="sxs-lookup"><span data-stu-id="ed382-114">Therefore, you should include [pragma](-pragma.md) commands in your MOF file that make command-line switches unnecessary.</span></span> <span data-ttu-id="ed382-115">В следующем примере описан общий параметр командной строки, который не используется инструментарием WMI при восстановлении MOF-файла из этого раздела реестра: **mofcomp — н:Рут \\ Test мимоф. mof** .</span><span class="sxs-lookup"><span data-stu-id="ed382-115">The following example describes a common command-line switch that WMI does not use when recovering a MOF file from this registry key: **mofcomp -N:Root\\Test mymof.mof**</span></span>

    <span data-ttu-id="ed382-116">Однако пространство имен можно указать с помощью команды [pragma](-pragma.md) в MOF-файле.</span><span class="sxs-lookup"><span data-stu-id="ed382-116">However, you can specify the namespace using a [pragma](-pragma.md) command in the MOF file.</span></span>

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a><span data-ttu-id="ed382-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ed382-117">Requirements</span></span>



| <span data-ttu-id="ed382-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ed382-118">Requirement</span></span> | <span data-ttu-id="ed382-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ed382-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ed382-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed382-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ed382-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed382-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ed382-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed382-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ed382-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed382-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed382-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed382-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed382-125">Команды препроцессора</span><span class="sxs-lookup"><span data-stu-id="ed382-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




