---
description: Представляет сведения о кадре в стеке вызовов.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Каллстаккфраме
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbe527c59a64e91f46a390344ea576c7560ef1f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105691980"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span data-ttu-id="c8106-103"><span id="vspixengine.callstackframe"></span>Структура Каллстаккфраме</span><span class="sxs-lookup"><span data-stu-id="c8106-103"><span id="vspixengine.callstackframe"></span>CallStackFrame structure</span></span>

<span data-ttu-id="c8106-104">Представляет сведения о кадре в стеке вызовов.</span><span class="sxs-lookup"><span data-stu-id="c8106-104">Represents information about a frame on the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8106-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8106-105">Syntax</span></span>


```C++
} CallStackFrame;
```

## <a name="members"></a><span data-ttu-id="c8106-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c8106-106">Members</span></span>

<span data-ttu-id="c8106-107">**functionName**</span><span class="sxs-lookup"><span data-stu-id="c8106-107">**functionName**</span></span>  
<span data-ttu-id="c8106-108">Строка COM, содержащая имя связанной функции.</span><span class="sxs-lookup"><span data-stu-id="c8106-108">A COM string containing the name of the associated function.</span></span>

<span data-ttu-id="c8106-109">**sourceFile**</span><span class="sxs-lookup"><span data-stu-id="c8106-109">**sourceFile**</span></span>  
<span data-ttu-id="c8106-110">Строка COM, содержащая файл FilePath связанного исходного файла.</span><span class="sxs-lookup"><span data-stu-id="c8106-110">A COM string containing the filepath of the associated source file.</span></span>

<span data-ttu-id="c8106-111">**moduleName**</span><span class="sxs-lookup"><span data-stu-id="c8106-111">**moduleName**</span></span>  
<span data-ttu-id="c8106-112">Строка COM, содержащая имя связанного модуля кода.</span><span class="sxs-lookup"><span data-stu-id="c8106-112">A COM string containing the name of the associated code module.</span></span>

<span data-ttu-id="c8106-113">**lineNumber**</span><span class="sxs-lookup"><span data-stu-id="c8106-113">**lineNumber**</span></span>  
<span data-ttu-id="c8106-114">Номер связанной строки.</span><span class="sxs-lookup"><span data-stu-id="c8106-114">The associated line number.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8106-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c8106-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c8106-116">Header</span><span class="sxs-lookup"><span data-stu-id="c8106-116">Header</span></span></p></td><td><span data-ttu-id="c8106-117">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="c8106-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



