---
description: Свойство Двдуникуеид извлекает созданное системой число, уникально идентифицирующее текущий диск.
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: Двдуникуеид, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894693"
---
# <a name="dvduniqueid-property"></a><span data-ttu-id="ce164-103">Двдуникуеид, свойство</span><span class="sxs-lookup"><span data-stu-id="ce164-103">DVDUniqueID Property</span></span>

> [!Note]  
> <span data-ttu-id="ce164-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ce164-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ce164-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="ce164-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ce164-106">`DVDUniqueID`Свойство получает созданное системой число, уникально идентифицирующее текущий диск.</span><span class="sxs-lookup"><span data-stu-id="ce164-106">The `DVDUniqueID` property retrieves a system-generated number that uniquely identifies the current disc.</span></span>

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a><span data-ttu-id="ce164-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce164-107">Return Value</span></span>

<span data-ttu-id="ce164-108">Возвращает целочисленное значение, уникально идентифицирующее текущий диск.</span><span class="sxs-lookup"><span data-stu-id="ce164-108">Returns an integer value that uniquely identifies the current disc.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce164-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce164-109">Remarks</span></span>

<span data-ttu-id="ce164-110">Это свойство доступно только для чтения и не имеет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce164-110">This property is read-only with no default value.</span></span> <span data-ttu-id="ce164-111">Идентификатор идентификатора (ID) не уникален, но он уникален для всех практических целей.</span><span class="sxs-lookup"><span data-stu-id="ce164-111">The identifier (ID) number is not absolutely unique, but it is unique for all practical purposes.</span></span> <span data-ttu-id="ce164-112">Этот идентификатор применяется ко всем реплицируемым копиям диска. Иными словами, все копии указанного фильма имеют одинаковый идентификатор.</span><span class="sxs-lookup"><span data-stu-id="ce164-112">The ID applies to all replicated copies of a disc. In other words, all copies of a specific movie have the same ID.</span></span> <span data-ttu-id="ce164-113">ИДЕНТИФИКАТОР основан на размерах файлов, датах и других данных, а не на значении БКА.</span><span class="sxs-lookup"><span data-stu-id="ce164-113">The ID is based on file sizes, dates, and other information, and not the BCA value.</span></span>

 

 



