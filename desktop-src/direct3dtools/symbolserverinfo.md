---
description: Представляет сведения о сервере символов отладки.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Симболсерверинфо
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139755"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span data-ttu-id="1fc45-103"><span id="vspixengine.symbolserverinfo"></span>Структура Симболсерверинфо</span><span class="sxs-lookup"><span data-stu-id="1fc45-103"><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo structure</span></span>

<span data-ttu-id="1fc45-104">Представляет сведения о сервере символов отладки.</span><span class="sxs-lookup"><span data-stu-id="1fc45-104">Represents information about the debug symbol server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc45-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fc45-105">Syntax</span></span>


```C++
} SymbolServerInfo;
```

## <a name="members"></a><span data-ttu-id="1fc45-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1fc45-106">Members</span></span>

<span data-ttu-id="1fc45-107">**symbolPath**</span><span class="sxs-lookup"><span data-stu-id="1fc45-107">**symbolPath**</span></span>  
<span data-ttu-id="1fc45-108">Строка COM, содержащая путь к серверу символов.</span><span class="sxs-lookup"><span data-stu-id="1fc45-108">A COM string containing the path of the symbol server.</span></span>

<span data-ttu-id="1fc45-109">**симболкачедир**</span><span class="sxs-lookup"><span data-stu-id="1fc45-109">**symbolCacheDir**</span></span>  
<span data-ttu-id="1fc45-110">Строка COM, содержащая каталог кэша сервера символов.</span><span class="sxs-lookup"><span data-stu-id="1fc45-110">A COM string containing the cache directory of the symbol server.</span></span>

<span data-ttu-id="1fc45-111">**публиксимболсервернаме**</span><span class="sxs-lookup"><span data-stu-id="1fc45-111">**publicSymbolServerName**</span></span>  
<span data-ttu-id="1fc45-112">Строка COM, содержащая открытое имя сервера символов.</span><span class="sxs-lookup"><span data-stu-id="1fc45-112">A COM string containing the public name of the symbol server.</span></span>

<span data-ttu-id="1fc45-113">**симболексклуделист**</span><span class="sxs-lookup"><span data-stu-id="1fc45-113">**symbolExcludeList**</span></span>  
<span data-ttu-id="1fc45-114">Строка COM, указывающая список исключаемых символов.</span><span class="sxs-lookup"><span data-stu-id="1fc45-114">A COM string that specifies the list of symbols to exclude.</span></span>

<span data-ttu-id="1fc45-115">**симболинклуделист**</span><span class="sxs-lookup"><span data-stu-id="1fc45-115">**symbolIncludeList**</span></span>  
<span data-ttu-id="1fc45-116">Строка COM, указывающая список включаемых символов.</span><span class="sxs-lookup"><span data-stu-id="1fc45-116">A COM string that specifies the list of symbols to include.</span></span>

<span data-ttu-id="1fc45-117">**усиксклуделист**</span><span class="sxs-lookup"><span data-stu-id="1fc45-117">**useExcludeList**</span></span>  
<span data-ttu-id="1fc45-118">значение true, если список исключений игнорируется; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="1fc45-118">true if the exclude list is ignored; otherwise, false.</span></span>

<span data-ttu-id="1fc45-119">**усемссимболсервер**</span><span class="sxs-lookup"><span data-stu-id="1fc45-119">**useMSSymbolServer**</span></span>  
<span data-ttu-id="1fc45-120">значение true, если используется сервер символов Майкрософт; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="1fc45-120">true if using Microsoft symbol server; otherwise, false.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc45-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1fc45-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1fc45-122">Header</span><span class="sxs-lookup"><span data-stu-id="1fc45-122">Header</span></span></p></td><td><span data-ttu-id="1fc45-123">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="1fc45-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



