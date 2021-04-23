---
description: Представляет гистограмму текстуры.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Структура Пиксенгинехистограм
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c19b77c962121949cc2495170061fee3adcecfc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140107"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span data-ttu-id="02766-103"><span id="vspixengine.pixenginehistogram"></span>Структура Пиксенгинехистограм</span><span class="sxs-lookup"><span data-stu-id="02766-103"><span id="vspixengine.pixenginehistogram"></span>PixEngineHistogram structure</span></span>

<span data-ttu-id="02766-104">Представляет гистограмму текстуры.</span><span class="sxs-lookup"><span data-stu-id="02766-104">Represents a histogram of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="02766-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02766-105">Syntax</span></span>


```C++
} PixEngineHistogram;
```

## <a name="members"></a><span data-ttu-id="02766-106">Члены</span><span class="sxs-lookup"><span data-stu-id="02766-106">Members</span></span>

<span data-ttu-id="02766-107">**хоризонталмин**</span><span class="sxs-lookup"><span data-stu-id="02766-107">**horizontalMin**</span></span>  
<span data-ttu-id="02766-108">Минимальное значение для каждого из компонентов X, Y, Z и W в горизонтальной оси (домене) гистограммы.</span><span class="sxs-lookup"><span data-stu-id="02766-108">The minimum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="02766-109">**хоризонталмакс**</span><span class="sxs-lookup"><span data-stu-id="02766-109">**horizontalMax**</span></span>  
<span data-ttu-id="02766-110">Максимальное значение для каждого из компонентов X, Y, Z и W в горизонтальной оси (домене) гистограммы.</span><span class="sxs-lookup"><span data-stu-id="02766-110">The maximum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="02766-111">**вертикалмин**</span><span class="sxs-lookup"><span data-stu-id="02766-111">**verticalMin**</span></span>  
<span data-ttu-id="02766-112">Минимальное значение для каждого из компонентов X, Y, Z и W в вертикальной оси (диапазон) гистограммы.</span><span class="sxs-lookup"><span data-stu-id="02766-112">The minimum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="02766-113">**вертикалмакс**</span><span class="sxs-lookup"><span data-stu-id="02766-113">**verticalMax**</span></span>  
<span data-ttu-id="02766-114">Максимальное значение для каждого из компонентов X, Y, Z и W в вертикальной оси (диапазон) гистограммы.</span><span class="sxs-lookup"><span data-stu-id="02766-114">The maximum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="02766-115">**dataLength**</span><span class="sxs-lookup"><span data-stu-id="02766-115">**dataLength**</span></span>  
<span data-ttu-id="02766-116">Число выборок, рассматриваемых в гистограмме.</span><span class="sxs-lookup"><span data-stu-id="02766-116">The number of samples considered in the histogram.</span></span>

## <a name="requirements"></a><span data-ttu-id="02766-117">Требования</span><span class="sxs-lookup"><span data-stu-id="02766-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="02766-118">Header</span><span class="sxs-lookup"><span data-stu-id="02766-118">Header</span></span></p></td><td><span data-ttu-id="02766-119">Вспиксенгине. h</span><span class="sxs-lookup"><span data-stu-id="02766-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



