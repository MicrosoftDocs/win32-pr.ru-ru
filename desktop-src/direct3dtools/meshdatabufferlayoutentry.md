---
description: Представляет сведения об отдельной записи в макете буфера сетки.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Мешдатабуфферлайаутентри
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806832"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span data-ttu-id="f3848-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>Структура Мешдатабуфферлайаутентри</span><span class="sxs-lookup"><span data-stu-id="f3848-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry structure</span></span>

<span data-ttu-id="f3848-104">Представляет сведения об отдельной записи в макете буфера сетки.</span><span class="sxs-lookup"><span data-stu-id="f3848-104">Represents information about a single entry in the buffer layout of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3848-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3848-105">Syntax</span></span>


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a><span data-ttu-id="f3848-106">Члены</span><span class="sxs-lookup"><span data-stu-id="f3848-106">Members</span></span>

<span data-ttu-id="f3848-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="f3848-107">**pName**</span></span>  
<span data-ttu-id="f3848-108">Строка COM, содержащая имя записи.</span><span class="sxs-lookup"><span data-stu-id="f3848-108">A COM string containing the name of the entry.</span></span>

<span data-ttu-id="f3848-109">**нумкомпонентс**</span><span class="sxs-lookup"><span data-stu-id="f3848-109">**numComponents**</span></span>  
<span data-ttu-id="f3848-110">Количество однородных компонентов (значений), составляющих эту запись.</span><span class="sxs-lookup"><span data-stu-id="f3848-110">The number of homogenous components (values) that make up this entry.</span></span>

<span data-ttu-id="f3848-111">**Позиционирование**</span><span class="sxs-lookup"><span data-stu-id="f3848-111">**isPosition**</span></span>  
<span data-ttu-id="f3848-112">значение true, если запись является позицией; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="f3848-112">true if the entry is a position; otherwise, false.</span></span>

<span data-ttu-id="f3848-113">**format**</span><span class="sxs-lookup"><span data-stu-id="f3848-113">**format**</span></span>  
<span data-ttu-id="f3848-114">Формат данных записи (Register).</span><span class="sxs-lookup"><span data-stu-id="f3848-114">The data format of the entry (register).</span></span> <span data-ttu-id="f3848-115">Дополнительные сведения см. в разделе \_ перечисление форматов регистров.</span><span class="sxs-lookup"><span data-stu-id="f3848-115">For more information, see the REGISTER\_FORMAT enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3848-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f3848-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f3848-117">Header</span><span class="sxs-lookup"><span data-stu-id="f3848-117">Header</span></span></p></td><td><span data-ttu-id="f3848-118">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="f3848-118">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



