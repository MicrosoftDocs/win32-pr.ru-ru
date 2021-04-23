---
description: Представляет поля макета ввода для буфера вершин, по одному на поле в буфере вершин.
MS-HAID: vspixengine.InputLayoutStruct
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Инпутлайаутструкт
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC7AAC2F-FDB1-4AD8-9B87-A97EE557FEAC
api_name:
- InputLayoutStruct
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1369d80d202682b67eacbb184b215d9da1711874
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710601"
---
# <a name="span-idvspixengineinputlayoutstructspaninputlayoutstruct-structure"></a><span data-ttu-id="02a88-103"><span id="vspixengine.inputlayoutstruct"></span>Структура Инпутлайаутструкт</span><span class="sxs-lookup"><span data-stu-id="02a88-103"><span id="vspixengine.inputlayoutstruct"></span>InputLayoutStruct structure</span></span>

<span data-ttu-id="02a88-104">Представляет поля макета ввода для буфера вершин, по одному на поле в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="02a88-104">Represents the input layout fields of a vertex buffer, one per field in the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="02a88-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02a88-105">Syntax</span></span>


```C++
} InputLayoutStruct;
```

## <a name="members"></a><span data-ttu-id="02a88-106">Члены</span><span class="sxs-lookup"><span data-stu-id="02a88-106">Members</span></span>

<span data-ttu-id="02a88-107">**семантикнаме**</span><span class="sxs-lookup"><span data-stu-id="02a88-107">**SemanticName**</span></span>  
<span data-ttu-id="02a88-108">Строка COM, содержащая имя связанной семантики.</span><span class="sxs-lookup"><span data-stu-id="02a88-108">A COM string containing the name of the associated semantic.</span></span>

<span data-ttu-id="02a88-109">**семантиЦиндекс**</span><span class="sxs-lookup"><span data-stu-id="02a88-109">**SemanticIndex**</span></span>  
<span data-ttu-id="02a88-110">Индекс связанной семантики.</span><span class="sxs-lookup"><span data-stu-id="02a88-110">The index of the associated semantic.</span></span>

<span data-ttu-id="02a88-111">**Формат**</span><span class="sxs-lookup"><span data-stu-id="02a88-111">**Format**</span></span>  
<span data-ttu-id="02a88-112">Формат поля.</span><span class="sxs-lookup"><span data-stu-id="02a88-112">The format of the field.</span></span> <span data-ttu-id="02a88-113">Дополнительные сведения см. в разделе \_ перечисление формата DXGI.</span><span class="sxs-lookup"><span data-stu-id="02a88-113">For more information see the DXGI\_FORMAT enumeration.</span></span>

<span data-ttu-id="02a88-114">**инпутслот**</span><span class="sxs-lookup"><span data-stu-id="02a88-114">**InputSlot**</span></span>  
<span data-ttu-id="02a88-115">Связанный входной слот.</span><span class="sxs-lookup"><span data-stu-id="02a88-115">The associated input slot.</span></span>

<span data-ttu-id="02a88-116">**алигнедбитеоффсет**</span><span class="sxs-lookup"><span data-stu-id="02a88-116">**AlignedByteOffset**</span></span>  

<span data-ttu-id="02a88-117">**инпутслоткласс**</span><span class="sxs-lookup"><span data-stu-id="02a88-117">**InputSlotClass**</span></span>  

<span data-ttu-id="02a88-118">**инстанцедатастепрате**</span><span class="sxs-lookup"><span data-stu-id="02a88-118">**InstanceDataStepRate**</span></span>  

## <a name="requirements"></a><span data-ttu-id="02a88-119">Требования</span><span class="sxs-lookup"><span data-stu-id="02a88-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="02a88-120">Header</span><span class="sxs-lookup"><span data-stu-id="02a88-120">Header</span></span></p></td><td><span data-ttu-id="02a88-121">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="02a88-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



