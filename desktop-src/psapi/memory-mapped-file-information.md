---
title: Сведения о файле Memory-Mapped
description: Сопоставленный в память файл (или сопоставление файлов) является результатом связывания содержимого файла с частью виртуального адресного пространства процесса. Его можно использовать для совместного использования файла или памяти между двумя или более процессами.
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134395"
---
# <a name="memory-mapped-file-information"></a><span data-ttu-id="49463-104">Сведения о файле Memory-Mapped</span><span class="sxs-lookup"><span data-stu-id="49463-104">Memory-Mapped File Information</span></span>

<span data-ttu-id="49463-105">*Сопоставленный в память файл* (или *Сопоставление файлов*) является результатом связывания содержимого файла с частью виртуального адресного пространства процесса.</span><span class="sxs-lookup"><span data-stu-id="49463-105">A *memory-mapped file* (or *file mapping*) is the result of associating a file's contents with a portion of the virtual address space of a process.</span></span> <span data-ttu-id="49463-106">Его можно использовать для совместного использования файла или памяти между двумя или более процессами.</span><span class="sxs-lookup"><span data-stu-id="49463-106">It can be used to share a file or memory between two or more processes.</span></span>

<span data-ttu-id="49463-107">Функция [**жетмаппедфиленаме**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) получает обработчик процесса и указатель на адрес в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="49463-107">The [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) function receives a process handle and a pointer to an address as input.</span></span> <span data-ttu-id="49463-108">Если адрес находится в размещенном в памяти файле в виртуальном адресном пространстве процесса, функция возвращает имя отображенного в памяти файла.</span><span class="sxs-lookup"><span data-stu-id="49463-108">If the address is within a memory-mapped file in the virtual address space of the process, the function returns the name of the memory-mapped file.</span></span> <span data-ttu-id="49463-109">Имена файлов, возвращаемые **жетмаппедфиленаме** , используют форму устройства, а не буквы диска.</span><span class="sxs-lookup"><span data-stu-id="49463-109">The file names returned by **GetMappedFileName** use device form, rather than drive letters.</span></span> <span data-ttu-id="49463-110">Например, имя файла c: \\ WinNT \\ system32 \\ CType. NLS будет выглядеть следующим образом в форме устройства:</span><span class="sxs-lookup"><span data-stu-id="49463-110">For example, the file name c:\\winnt\\system32\\ctype.nls would look like this in device form:</span></span>

<span data-ttu-id="49463-111">\\Устройство \\ Harddisk0 \\ Partition1 \\ WinNT \\ system32 \\ CType. NLS</span><span class="sxs-lookup"><span data-stu-id="49463-111">\\Device\\Harddisk0\\Partition1\\WINNT\\System32\\ctype.nls</span></span>

<span data-ttu-id="49463-112">Дополнительные сведения о файлах, отображенных в памяти, см. в разделе [Сопоставление файлов](/windows/desktop/Memory/file-mapping).</span><span class="sxs-lookup"><span data-stu-id="49463-112">For more information about memory-mapped files, see [File Mapping](/windows/desktop/Memory/file-mapping).</span></span> <span data-ttu-id="49463-113">Пример преобразования имен файлов в форме устройства в буквы диска см. в разделе [Получение имени файла из маркера файла](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span><span class="sxs-lookup"><span data-stu-id="49463-113">For an example that converts file names in device form to drive letters, see [Obtaining a File Name From a File Handle](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span></span>

 

 