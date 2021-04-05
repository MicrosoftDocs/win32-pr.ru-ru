---
title: Оператор характеристик
description: Определяет сведения о ресурсе, который может использоваться инструментами, считывающими и записывающими файлы определения ресурсов.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Меню операторов характеристик и другие ресурсы
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104068980"
---
# <a name="characteristics-statement"></a><span data-ttu-id="8527c-104">Оператор характеристик</span><span class="sxs-lookup"><span data-stu-id="8527c-104">CHARACTERISTICS statement</span></span>

<span data-ttu-id="8527c-105">Определяет сведения о ресурсе, который может использоваться инструментами, считывающими и записывающими файлы определения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8527c-105">Defines information about a resource that can be used by tools that read and write resource-definition files.</span></span> <span data-ttu-id="8527c-106">Указанное значение **DWORD** отображается вместе с ресурсом в файле Compiled. Res.</span><span class="sxs-lookup"><span data-stu-id="8527c-106">The specified **DWORD** value appears with the resource in the compiled .res file.</span></span> <span data-ttu-id="8527c-107">Однако значение не сохраняется в исполняемом файле и не имеет значимости для системы.</span><span class="sxs-lookup"><span data-stu-id="8527c-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="8527c-108">Оператор **характеристик** отображается перед началом тела описания [**ускорителей**](accelerators-resource.md), [**диалогового окна**](dialog-resource.md), [**меню**](menu-resource.md), [**RCDATA**](rcdata-resource.md)или определения ресурса [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="8527c-108">The **CHARACTERISTICS** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOG**](dialog-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="8527c-109">Указанное значение применяется только к этому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="8527c-109">The specified value applies only to that resource.</span></span>

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span data-ttu-id="8527c-110"><span id="dword"></span><span id="DWORD"></span>*DWORD*</span><span class="sxs-lookup"><span data-stu-id="8527c-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="8527c-111">Определяемое пользователем значение **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8527c-111">User-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="8527c-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8527c-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8527c-113">**Accelerator**</span><span class="sxs-lookup"><span data-stu-id="8527c-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="8527c-114">**Откроется**</span><span class="sxs-lookup"><span data-stu-id="8527c-114">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="8527c-115">**ЯЗЫКЕ**</span><span class="sxs-lookup"><span data-stu-id="8527c-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="8527c-116">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="8527c-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="8527c-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="8527c-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="8527c-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="8527c-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




