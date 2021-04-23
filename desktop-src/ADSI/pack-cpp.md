---
title: Распаковк. CPP
description: В примере компонента поставщика пример кода для упаковки и распаковки типов данных в вариантах находится в виде файла Pack. cpp.
ms.assetid: 4da8f191-5742-4618-86dd-e7031a67ac79
ms.tgt_platform: multiple
keywords:
- Pack. cpp ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f40276d4528c343e4e9b86142ce3aeea2cf41d89
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772932"
---
# <a name="packcpp"></a><span data-ttu-id="24c57-104">Распаковк. CPP</span><span class="sxs-lookup"><span data-stu-id="24c57-104">PACK.CPP</span></span>

<span data-ttu-id="24c57-105">В примере компонента поставщика пример кода для упаковки и распаковки типов данных в вариантах находится в виде файла Pack. cpp.</span><span class="sxs-lookup"><span data-stu-id="24c57-105">In the example provider component, a code example of packing and unpacking data types into VARIANTs is found in pack.cpp.</span></span> <span data-ttu-id="24c57-106">Следующие функции используются, когда свойства загружаются в кэш свойств и удаляются из него:</span><span class="sxs-lookup"><span data-stu-id="24c57-106">The following functions are used when properties are loaded to, and removed from, the property cache:</span></span>

-   <span data-ttu-id="24c57-107">**паккстрингинвариант**</span><span class="sxs-lookup"><span data-stu-id="24c57-107">**PackStringinVariant**</span></span>
-   <span data-ttu-id="24c57-108">**унпаккстрингинвариант**</span><span class="sxs-lookup"><span data-stu-id="24c57-108">**UnpackStringinVariant**</span></span>
-   <span data-ttu-id="24c57-109">**пакклонгинвариант**</span><span class="sxs-lookup"><span data-stu-id="24c57-109">**PackLONGinVariant**</span></span>
-   <span data-ttu-id="24c57-110">**унпакклонгфромвариант**</span><span class="sxs-lookup"><span data-stu-id="24c57-110">**UnpackLONGfromVariant**</span></span>
-   <span data-ttu-id="24c57-111">**паккдатеинвариант**</span><span class="sxs-lookup"><span data-stu-id="24c57-111">**PackDATEinVariant**</span></span>
-   <span data-ttu-id="24c57-112">**унпаккдатеинвариант**</span><span class="sxs-lookup"><span data-stu-id="24c57-112">**UnpackDATEinVariant**</span></span>
-   <span data-ttu-id="24c57-113">**Пакквариант \_ булинвариант**</span><span class="sxs-lookup"><span data-stu-id="24c57-113">**PackVARIANT\_BOOLinVariant**</span></span>
-   <span data-ttu-id="24c57-114">**Унпакквариант \_ булфромвариант**</span><span class="sxs-lookup"><span data-stu-id="24c57-114">**UnpackVARIANT\_BOOLfromVariant**</span></span>
-   <span data-ttu-id="24c57-115">**пакквариантинвариант**</span><span class="sxs-lookup"><span data-stu-id="24c57-115">**PackVARIANTinVariant**</span></span>
-   <span data-ttu-id="24c57-116">**унпакквариантфромвариант**</span><span class="sxs-lookup"><span data-stu-id="24c57-116">**UnpackVARIANTfromVariant**</span></span>

 

 




