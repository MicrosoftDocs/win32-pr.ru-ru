---
description: Дата и время MS-DOS — это Упакованные 16-разрядные значения, указывающие месяц, день, год и время суток последней записи в файл MS-DOS.
ms.assetid: 948e6d77-dd01-4c90-9ef0-af143972c3fa
title: Дата и время MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d401c731c9a3f5127511e28adf846c929a89a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662544"
---
# <a name="ms-dos-date-and-time"></a><span data-ttu-id="382e5-103">Дата и время MS-DOS</span><span class="sxs-lookup"><span data-stu-id="382e5-103">MS-DOS Date and Time</span></span>

<span data-ttu-id="382e5-104">**Дата** и **время** MS-DOS — это Упакованные 16-разрядные значения, указывающие месяц, день, год и время суток последней записи в файл MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="382e5-104">**MS-DOS date** and **MS-DOS time** are packed 16-bit values that specify the month, day, year, and time of day an MS-DOS file was last written to.</span></span> <span data-ttu-id="382e5-105">MS-DOS записывает дату и время, когда приложение MS-DOS создает или записывает в файл.</span><span class="sxs-lookup"><span data-stu-id="382e5-105">MS-DOS records the date and time whenever an MS-DOS application creates or writes to a file.</span></span> <span data-ttu-id="382e5-106">Приложения MS-DOS извлекают эту дату и время с помощью функций MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="382e5-106">MS-DOS applications retrieve this date and time using MS-DOS functions.</span></span> <span data-ttu-id="382e5-107">При использовании функции [**функции getFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) для извлечения времени файла для файлов, созданных MS-DOS, **функции getFileTime** автоматически преобразует даты и время MS-DOS в время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="382e5-107">When you use the [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) function to retrieve the file times for files that were created by MS-DOS, **GetFileTime** automatically converts MS-DOS dates and times to UTC-based times.</span></span>

<span data-ttu-id="382e5-108">При возникновении даты и времени MS-DOS, которые не были преобразованы, можно преобразовать ее в время на основе времени в формате UTC с помощью функции [**досдатетиметофилетиме**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) .</span><span class="sxs-lookup"><span data-stu-id="382e5-108">If you encounter an MS-DOS date and time that has not been converted, you can convert it to a UTC-based time by using the [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) function.</span></span> <span data-ttu-id="382e5-109">Эта функция копирует преобразованные дату и время в структуру [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="382e5-109">This function copies the converted date and time to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="382e5-110">Значение можно преобразовать обратно в дату и время MS-DOS с помощью функции [**филетиметодосдатетиме**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) .</span><span class="sxs-lookup"><span data-stu-id="382e5-110">You can convert the value back to an MS-DOS date and time by using the [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) function.</span></span>

 

 
