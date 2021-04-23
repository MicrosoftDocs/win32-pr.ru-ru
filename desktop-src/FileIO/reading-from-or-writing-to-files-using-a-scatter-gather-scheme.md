---
description: Описывает схему разбивки на части для чтения или записи несмежных фрагментов данных за одну операцию.
ms.assetid: ae5d83ca-f219-4fcc-ad06-bc242ba95372
title: Чтение или запись в файлы с помощью схемы Scatter-Gather
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7db31dd73dd0b498436548a867dd92ff248805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664048"
---
# <a name="reading-from-or-writing-to-files-using-a-scatter-gather-scheme"></a><span data-ttu-id="a09d5-103">Чтение или запись в файлы с помощью схемы Scatter-Gather</span><span class="sxs-lookup"><span data-stu-id="a09d5-103">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>

<span data-ttu-id="a09d5-104">Схема разбивки на части использует операционную систему для доставки в одной операции нескольких дискретных блоков данных (например, записей базы данных) из файла в отдельные несмежные буферы в памяти.</span><span class="sxs-lookup"><span data-stu-id="a09d5-104">A scatter-gather scheme uses the operating system to deliver in one operation multiple discrete chunks of data (such as database records) from a file to separate, noncontiguous buffers in memory.</span></span> <span data-ttu-id="a09d5-105">Схема рассеивания также записывает данные из несмежных буферов за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="a09d5-105">A scatter-gather scheme also writes the data from noncontiguous buffers in one operation.</span></span>

<span data-ttu-id="a09d5-106">Приложение может реализовать схему разбивки на области с помощью функций [**реадфилескаттер**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) и [**вритефилегасер**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) .</span><span class="sxs-lookup"><span data-stu-id="a09d5-106">An application can implement a scatter-gather scheme by using the [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter) and [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather) functions.</span></span>

 

 



