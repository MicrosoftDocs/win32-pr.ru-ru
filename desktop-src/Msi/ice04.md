---
description: ICE04 проверяет, что порядковый номер каждого файла в таблице файлов меньше или равен значению самого крупного порядкового номера в столбце Ластсекуенце таблицы Media.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da25a23a26f8a2c49e224ad334791a6081b697b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998805"
---
# <a name="ice04"></a><span data-ttu-id="0124a-103">ICE04</span><span class="sxs-lookup"><span data-stu-id="0124a-103">ICE04</span></span>

<span data-ttu-id="0124a-104">ICE04 проверяет, что порядковый номер каждого файла в [таблице файлов](file-table.md) меньше или равен значению самого крупного порядкового номера в столбце Ластсекуенце [таблицы Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="0124a-104">ICE04 validates that the sequence number of every file in the [File table](file-table.md) is less than or equal to the largest sequence number in the LastSequence column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="0124a-105">Каждая запись в таблице Media представляет диск на исходном носителе, содержащий все файлы с порядковым номером, меньшим или равным значению в столбце Ластсекуенце и превышающий значение Ластсекуенце в записи предыдущего диска.</span><span class="sxs-lookup"><span data-stu-id="0124a-105">Each record in the Media table represents a disk on the source media containing all the files with a sequence number less than or equal to the value in the LastSequence column and greater than the LastSequence value in the record of the preceding disk.</span></span>

## <a name="result"></a><span data-ttu-id="0124a-106">Результат</span><span class="sxs-lookup"><span data-stu-id="0124a-106">Result</span></span>

<span data-ttu-id="0124a-107">ICE04 отправляет сообщение об ошибке, если существует файл с порядковым номером, превышающим самый крупный номер Ластсекуенце для исходного носителя.</span><span class="sxs-lookup"><span data-stu-id="0124a-107">ICE04 posts an error message if there is a file with a sequence number greater than the largest LastSequence number for the source media.</span></span>

## <a name="example"></a><span data-ttu-id="0124a-108">Пример</span><span class="sxs-lookup"><span data-stu-id="0124a-108">Example</span></span>

<span data-ttu-id="0124a-109">ICE04 сообщит о следующей ошибке в примере, показанном ниже:</span><span class="sxs-lookup"><span data-stu-id="0124a-109">ICE04 would report the following error for the example shown:</span></span>

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

<span data-ttu-id="0124a-110">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="0124a-110">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="0124a-111">Файл</span><span class="sxs-lookup"><span data-stu-id="0124a-111">File</span></span>   | <span data-ttu-id="0124a-112">Последовательность</span><span class="sxs-lookup"><span data-stu-id="0124a-112">Sequence</span></span> |
|--------|----------|
| <span data-ttu-id="0124a-113">MyFile</span><span class="sxs-lookup"><span data-stu-id="0124a-113">MyFile</span></span> | <span data-ttu-id="0124a-114">210</span><span class="sxs-lookup"><span data-stu-id="0124a-114">210</span></span>      |



 

<span data-ttu-id="0124a-115">[Таблица мультимедиа](media-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="0124a-115">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="0124a-116">DiskId</span><span class="sxs-lookup"><span data-stu-id="0124a-116">DiskId</span></span> | <span data-ttu-id="0124a-117">ластсекуенце</span><span class="sxs-lookup"><span data-stu-id="0124a-117">LastSequence</span></span> |
|--------|--------------|
| <span data-ttu-id="0124a-118">1</span><span class="sxs-lookup"><span data-stu-id="0124a-118">1</span></span>      | <span data-ttu-id="0124a-119">100</span><span class="sxs-lookup"><span data-stu-id="0124a-119">100</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="0124a-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0124a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0124a-121">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="0124a-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



