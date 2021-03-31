---
description: ICE71 проверяет, содержит ли таблица мультимедиа запись с DiskId, равным 1.
ms.assetid: b48c2f3f-24ef-48a8-849f-7abed69c0fc9
title: ICE71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c6e136362caa13da2b6305e3d8c3ca9c3a5c7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999242"
---
# <a name="ice71"></a><span data-ttu-id="2735e-103">ICE71</span><span class="sxs-lookup"><span data-stu-id="2735e-103">ICE71</span></span>

<span data-ttu-id="2735e-104">ICE71 проверяет, содержит ли [Таблица мультимедиа](media-table.md) запись с DiskId, равным 1.</span><span class="sxs-lookup"><span data-stu-id="2735e-104">ICE71 verifies that the [Media table](media-table.md) contains an entry with DiskId equal to 1.</span></span> <span data-ttu-id="2735e-105">(Установщик Windows предполагает, что пакет MSI находится на диске 1.)</span><span class="sxs-lookup"><span data-stu-id="2735e-105">(Windows Installer assumes that the .msi package is on disk 1.)</span></span>

## <a name="result"></a><span data-ttu-id="2735e-106">Результат</span><span class="sxs-lookup"><span data-stu-id="2735e-106">Result</span></span>

<span data-ttu-id="2735e-107">ICE71 возвращает ошибку, если таблица мультимедиа не содержит запись с DiskId, равным 1.</span><span class="sxs-lookup"><span data-stu-id="2735e-107">ICE71 returns an error if the Media table does not contain an entry with DiskId equal to 1.</span></span>

## <a name="example"></a><span data-ttu-id="2735e-108">Пример</span><span class="sxs-lookup"><span data-stu-id="2735e-108">Example</span></span>

<span data-ttu-id="2735e-109">ICE71 сообщает об ошибке в приведенном примере.</span><span class="sxs-lookup"><span data-stu-id="2735e-109">ICE71 reports the following error for the example shown.</span></span>

``` syntax
The Media table requires an entry with DiskId=1. First DiskId is '2'.
```

<span data-ttu-id="2735e-110">T0 исправить эту ошибку, измените DiskId записи, в которой хранится пакет, равным 1.</span><span class="sxs-lookup"><span data-stu-id="2735e-110">T0 fix this error, change the DiskId of the entry where the package is stored to 1.</span></span>

<span data-ttu-id="2735e-111">[Таблица мультимедиа](media-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="2735e-111">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="2735e-112">DiskId</span><span class="sxs-lookup"><span data-stu-id="2735e-112">DiskId</span></span> |
|--------|
| <span data-ttu-id="2735e-113">2</span><span class="sxs-lookup"><span data-stu-id="2735e-113">2</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="2735e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="2735e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2735e-115">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="2735e-115">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



