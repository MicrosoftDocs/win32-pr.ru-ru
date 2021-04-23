---
description: Функция AreFileApisANSI определяет, использует ли функция файлового ввода-вывода кодовую страницу кодировки ANSI или OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Определение кодовой страницы текущей кодировки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910163"
---
# <a name="determining-the-current-character-set-code-page"></a><span data-ttu-id="d3ad3-103">Определение кодовой страницы текущей кодировки</span><span class="sxs-lookup"><span data-stu-id="d3ad3-103">Determining the Current Character Set Code Page</span></span>

<span data-ttu-id="d3ad3-104">Функция [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) определяет, использует ли функция файлового ввода-вывода кодовую страницу кодировки ANSI или OEM.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-104">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span> <span data-ttu-id="d3ad3-105">Функция [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) заставляет функции использовать кодовую страницу ANSI.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-105">The [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) function causes the functions to use the ANSI code page.</span></span> <span data-ttu-id="d3ad3-106">Функция [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) заставляет функции использовать кодовую страницу OEM.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-106">The [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) function causes the functions to use the OEM code page.</span></span>

<span data-ttu-id="d3ad3-107">По умолчанию функции файлового ввода-вывода используют имена файлов ANSI.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-107">By default, file I/O functions use ANSI file names.</span></span> <span data-ttu-id="d3ad3-108">Функции, экспортированные Kernel32.dll, которые принимают или возвращают имена файлов, затрагиваются параметром кодовой страницы файла.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-108">Functions exported by Kernel32.dll that accept or return file names are affected by the file code page setting.</span></span>

<span data-ttu-id="d3ad3-109">И [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) , и [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) устанавливают кодовую страницу для каждого процесса, а не для каждого потока или для каждого компьютера.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-109">Both [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) and [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) set the code page per process, rather than per thread or per computer.</span></span>

 

 



