---
title: VERSION, инструкция
description: Определяет сведения о версии ресурса, который может использоваться инструментами, считывающими и записывающими файлы ресурсов.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Меню инструкций версии и другие ресурсы
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784047"
---
# <a name="version-statement"></a><span data-ttu-id="2f567-104">VERSION, инструкция</span><span class="sxs-lookup"><span data-stu-id="2f567-104">VERSION statement</span></span>

<span data-ttu-id="2f567-105">Определяет сведения о версии ресурса, который может использоваться инструментами, считывающими и записывающими файлы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2f567-105">Defines version information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="2f567-106">Указанное значение *DWORD* отображается вместе с ресурсом в скомпилированном виде. RES — файл.</span><span class="sxs-lookup"><span data-stu-id="2f567-106">The specified *dword* value appears with the resource in the compiled .RES file.</span></span> <span data-ttu-id="2f567-107">Однако значение не сохраняется в исполняемом файле и не имеет значимости для системы.</span><span class="sxs-lookup"><span data-stu-id="2f567-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="2f567-108">Оператор **Version** появляется перед началом тела определения ресурса [**ускорителей**](accelerators-resource.md), [**диаложекс**](dialogex-resource.md), [**меню**](menu-resource.md), [**RCDATA**](rcdata-resource.md)или [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="2f567-108">The **VERSION** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="2f567-109">Указанное значение применяется только к этому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2f567-109">The specified value applies only to that resource.</span></span>

``` syntax
VERSION dword
```

<dl> <dt>

<span data-ttu-id="2f567-110"><span id="dword"></span><span id="DWORD"></span>*DWORD*</span><span class="sxs-lookup"><span data-stu-id="2f567-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="2f567-111">Определяемое пользователем значение **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="2f567-111">A user-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2f567-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f567-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f567-113">**Accelerator**</span><span class="sxs-lookup"><span data-stu-id="2f567-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="2f567-114">**ПОКАЗАТЕЛИ**</span><span class="sxs-lookup"><span data-stu-id="2f567-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="2f567-115">**ЯЗЫКЕ**</span><span class="sxs-lookup"><span data-stu-id="2f567-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="2f567-116">**МЕНЮ**</span><span class="sxs-lookup"><span data-stu-id="2f567-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="2f567-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="2f567-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="2f567-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="2f567-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




