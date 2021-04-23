---
description: ICEM07 проверяет, что порядок файлов в таблице последовательности соответствует порядку файлов в MergeModule.CABinet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910384"
---
# <a name="icem07"></a><span data-ttu-id="cf2fd-103">ICEM07</span><span class="sxs-lookup"><span data-stu-id="cf2fd-103">ICEM07</span></span>

<span data-ttu-id="cf2fd-104">ICEM07 проверяет, что порядок файлов в таблице последовательности соответствует порядку файлов в [MergeModule.CABinet](mergemodule-cabinet.md).</span><span class="sxs-lookup"><span data-stu-id="cf2fd-104">ICEM07 verifies that the order of files in the sequence table matches the order of files in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span>

<span data-ttu-id="cf2fd-105">Модуль слияния ICEs хранится в файле слияния Module. CUB, который называется Мержемод. CUB, а не в файле. CUB, содержащем значение ICEs, используемое для проверки пакета.</span><span class="sxs-lookup"><span data-stu-id="cf2fd-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="cf2fd-106">Результат</span><span class="sxs-lookup"><span data-stu-id="cf2fd-106">Result</span></span>

<span data-ttu-id="cf2fd-107">ICEM07 отправляет сообщение об ошибке, если порядок файлов в таблице файлов не соответствует порядку в CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="cf2fd-107">ICEM07 posts an error if the order of files in the File table does not match the order in the cabinet file.</span></span>

## <a name="example"></a><span data-ttu-id="cf2fd-108">Пример</span><span class="sxs-lookup"><span data-stu-id="cf2fd-108">Example</span></span>

<span data-ttu-id="cf2fd-109">IC0M07 выводит следующее сообщение об ошибке для приведенного примера.</span><span class="sxs-lookup"><span data-stu-id="cf2fd-109">IC0M07 would post the following error message for the example shown.</span></span>

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[<span data-ttu-id="cf2fd-110">Таблица файлов</span><span class="sxs-lookup"><span data-stu-id="cf2fd-110">File Table</span></span>](file-table.md)



| <span data-ttu-id="cf2fd-111">Файл</span><span class="sxs-lookup"><span data-stu-id="cf2fd-111">File</span></span>          | <span data-ttu-id="cf2fd-112">Последовательность</span><span class="sxs-lookup"><span data-stu-id="cf2fd-112">Sequence</span></span> |
|---------------|----------|
| <span data-ttu-id="cf2fd-113">Файл а. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="cf2fd-113">FileA.*GUID1*</span></span> | <span data-ttu-id="cf2fd-114">1</span><span class="sxs-lookup"><span data-stu-id="cf2fd-114">1</span></span>        |
| <span data-ttu-id="cf2fd-115">Филеб. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="cf2fd-115">FileB.*GUID1*</span></span> | <span data-ttu-id="cf2fd-116">8</span><span class="sxs-lookup"><span data-stu-id="cf2fd-116">8</span></span>        |
| <span data-ttu-id="cf2fd-117">Филек. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="cf2fd-117">FileC.*GUID1*</span></span> | <span data-ttu-id="cf2fd-118">52</span><span class="sxs-lookup"><span data-stu-id="cf2fd-118">52</span></span>       |



 

<span data-ttu-id="cf2fd-119">Внедренный [MergeModule.CABinet](mergemodule-cabinet.md)</span><span class="sxs-lookup"><span data-stu-id="cf2fd-119">Embedded [MergeModule.CABinet](mergemodule-cabinet.md)</span></span>



| <span data-ttu-id="cf2fd-120">Файл</span><span class="sxs-lookup"><span data-stu-id="cf2fd-120">File</span></span>          |
|---------------|
| <span data-ttu-id="cf2fd-121">Файл а. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="cf2fd-121">FileA.*GUID1*</span></span> |
| <span data-ttu-id="cf2fd-122">Филек. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="cf2fd-122">FileC.*GUID1*</span></span> |
| <span data-ttu-id="cf2fd-123">Подан. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="cf2fd-123">FileD.*GUID1*</span></span> |
| <span data-ttu-id="cf2fd-124">Филеб. *GUID1*</span><span class="sxs-lookup"><span data-stu-id="cf2fd-124">FileB.*GUID1*</span></span> |



 

<span data-ttu-id="cf2fd-125">Хотя порядковые номера файлов в таблице файлов не должны быть последовательными, а в CAB-файле могут содержаться дополнительные файлы, относительная последовательность всех файлов в таблице File должна соответствовать порядку в [MergeModule.CABinet](mergemodule-cabinet.md).</span><span class="sxs-lookup"><span data-stu-id="cf2fd-125">Although the file sequence numbers in the file table do not have to be consecutive, and extra files can exist in the cabinet file, the relative sequence of all files in the File table must match the order in [MergeModule.CABinet](mergemodule-cabinet.md).</span></span> <span data-ttu-id="cf2fd-126">Чтобы устранить эту ошибку, измените порядковый номер Филеб на Филек, чтобы он совпадал с порядком файлов в CAB-файле, или перестройте CAB-файл с файлами в правильном порядке.</span><span class="sxs-lookup"><span data-stu-id="cf2fd-126">To fix this error, change the sequence number of FileB to come after FileC to match the file order in the CAB, or rebuild the CAB with the files in the correct order.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf2fd-127">См. также</span><span class="sxs-lookup"><span data-stu-id="cf2fd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf2fd-128">Ссылка на модуль слияния ICE</span><span class="sxs-lookup"><span data-stu-id="cf2fd-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



