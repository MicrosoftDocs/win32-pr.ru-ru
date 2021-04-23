---
description: КАБИНЕТДЛЛВЕРСИОНИНФО содержит сведения о версии для Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: Структура КАБИНЕТДЛЛВЕРСИОНИНФО
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895777"
---
# <a name="cabinetdllversioninfo-structure"></a><span data-ttu-id="2890b-103">Структура КАБИНЕТДЛЛВЕРСИОНИНФО</span><span class="sxs-lookup"><span data-stu-id="2890b-103">CABINETDLLVERSIONINFO structure</span></span>

<span data-ttu-id="2890b-104">\[Эта структура содержит сведения, необходимые только при использовании функции **дллжетверсион** , которая не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2890b-104">\[This structure contains information required only when using the **DllGetVersion** function, which is not supported.</span></span> <span data-ttu-id="2890b-105">Эта документация предоставляется только в ознакомительных целях.\]</span><span class="sxs-lookup"><span data-stu-id="2890b-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="2890b-106">**Кабинетдллверсионинфо** содержит сведения о версии для Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="2890b-106">The **CABINETDLLVERSIONINFO** contains the version information for Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="2890b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2890b-107">Syntax</span></span>


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="2890b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="2890b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2890b-109">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="2890b-109">**cbStruct**</span></span>
</dt> <dd>

<span data-ttu-id="2890b-110">Размер этой структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="2890b-110">The size of this structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2890b-111">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="2890b-111">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="2890b-112">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="2890b-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2890b-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="2890b-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="2890b-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="2890b-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2890b-115">**двфилеверсионмс**</span><span class="sxs-lookup"><span data-stu-id="2890b-115">**dwFileVersionMS**</span></span>
</dt> <dd>

<span data-ttu-id="2890b-116">Содержит наиболее значимые биты сведений о версии.</span><span class="sxs-lookup"><span data-stu-id="2890b-116">Contains the most significant bits of the version information.</span></span> <span data-ttu-id="2890b-117">Биты 0-15 содержат дополнительный номер версии, а BITS 16-31 содержит основную версию.</span><span class="sxs-lookup"><span data-stu-id="2890b-117">Bits 0-15 contain the minor version, and bits 16-31 contain the major version.</span></span>

</dd> <dt>

<span data-ttu-id="2890b-118">**двфилеверсионлс**</span><span class="sxs-lookup"><span data-stu-id="2890b-118">**dwFileVersionLS**</span></span>
</dt> <dd>

<span data-ttu-id="2890b-119">Содержит наименьшие значащие биты сведений о версии.</span><span class="sxs-lookup"><span data-stu-id="2890b-119">Contains the least significant bits of the version information.</span></span> <span data-ttu-id="2890b-120">Биты 0-15 содержат номер редакции, а BITS 16-31 содержит номер сборки.</span><span class="sxs-lookup"><span data-stu-id="2890b-120">Bits 0-15 contain the revision number, and bits 16-31 contain the build number.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2890b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2890b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2890b-122">**дллжетверсион**</span><span class="sxs-lookup"><span data-stu-id="2890b-122">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 



