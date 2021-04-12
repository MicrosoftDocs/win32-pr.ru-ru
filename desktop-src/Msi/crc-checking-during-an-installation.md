---
description: В установщик Windows доступен циклический контроль избыточности файлов.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Проверка CRC во время установки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265657"
---
# <a name="crc-checking-during-an-installation"></a><span data-ttu-id="8fd23-103">Проверка CRC во время установки</span><span class="sxs-lookup"><span data-stu-id="8fd23-103">CRC Checking During an Installation</span></span>

<span data-ttu-id="8fd23-104">В установщик Windows доступен циклический контроль избыточности файлов.</span><span class="sxs-lookup"><span data-stu-id="8fd23-104">A Cyclic Redundancy Check (CRC) of files is available with Windows Installer.</span></span> <span data-ttu-id="8fd23-105">Проверка CRC — это механизм проверки ошибок, аналогичный контрольной сумме, который позволяет приложению определить, были ли изменены данные в файле.</span><span class="sxs-lookup"><span data-stu-id="8fd23-105">CRC checking is an error-checking mechanism, similar to a checksum, that enables an application to determine whether the information in a file has been modified.</span></span> <span data-ttu-id="8fd23-106">После того как установщик Windows завершит копирование файла, он получает значение CRC как из исходного, так и из целевого файлов.</span><span class="sxs-lookup"><span data-stu-id="8fd23-106">After the Windows Installer finishes copying a file, it gets a CRC value from both the source and destination files.</span></span> <span data-ttu-id="8fd23-107">Установщик проверяет исходную контрольную сумму, помеченную в файле, и сравнивает ее с CRC, вычисленным на основе копии.</span><span class="sxs-lookup"><span data-stu-id="8fd23-107">The installer checks the original CRC stamped into the file and compares this to the CRC calculated from the copy.</span></span> <span data-ttu-id="8fd23-108">Проверка CRC завершается сбоем, если исходное значение CRC не равно NULL и отличается от CRC, вычисленного для копии.</span><span class="sxs-lookup"><span data-stu-id="8fd23-108">The CRC check fails if the original CRC value is non-null and is different from the CRC calculated on the copy.</span></span> <span data-ttu-id="8fd23-109">Если исходная CRC имеет значение null, проверка не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8fd23-109">If the original CRC is null, no check occurs.</span></span>

<span data-ttu-id="8fd23-110">Установщик Windows выполняет проверку CRC файла в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="8fd23-110">The Windows Installer does a CRC check on a file in the following cases:</span></span>

-   <span data-ttu-id="8fd23-111">Если [свойство мсичекккркс](msicheckcrcs.md) задано и **мсидбфилеаттрибутесчекксум** включено в поле Attributes записи файла в [таблице File](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="8fd23-111">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md).</span></span> <span data-ttu-id="8fd23-112">Установщик выполняет проверку контрольной суммы один раз после установки, дублирования или перемещения файла.</span><span class="sxs-lookup"><span data-stu-id="8fd23-112">The installer does the CRC check once after installing, duplicating, or moving the file.</span></span>
-   <span data-ttu-id="8fd23-113">Если [свойство мсичекккркс](msicheckcrcs.md) задано и **мсидбфилеаттрибутесчекксум** включено в поле Attributes записи файла в [таблице File](file-table.md), установщик выполняет проверку CRC после внесения исправлений в файл.</span><span class="sxs-lookup"><span data-stu-id="8fd23-113">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check after patching the file.</span></span>
-   <span data-ttu-id="8fd23-114">Если **мсидбфилеаттрибутесчекксум** включен в поле Attributes записи файла в [таблице File](file-table.md), установщик выполняет проверку CRC перед привязкой образов.</span><span class="sxs-lookup"><span data-stu-id="8fd23-114">If the **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check before binding images.</span></span>

<span data-ttu-id="8fd23-115">Если проверка завершается ошибкой перед привязкой образа, установщик сообщает о следующих двух ошибках в файле журнала и продолжит установку без привязки файла.</span><span class="sxs-lookup"><span data-stu-id="8fd23-115">If the check fails before binding an image, the installer reports the following two errors in the log file and continues the installation without binding the file.</span></span>



| <span data-ttu-id="8fd23-116">Код</span><span class="sxs-lookup"><span data-stu-id="8fd23-116">Code</span></span> | <span data-ttu-id="8fd23-117">Сообщение</span><span class="sxs-lookup"><span data-stu-id="8fd23-117">Message</span></span>                                               |
|------|-------------------------------------------------------|
| <span data-ttu-id="8fd23-118">2941</span><span class="sxs-lookup"><span data-stu-id="8fd23-118">2941</span></span> | <span data-ttu-id="8fd23-119">Не удалось вычислить CRC для файла \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="8fd23-119">Unable to compute the CRC for file \[2\].</span></span>             |
| <span data-ttu-id="8fd23-120">2942</span><span class="sxs-lookup"><span data-stu-id="8fd23-120">2942</span></span> | <span data-ttu-id="8fd23-121">Действие BindImage не выполнено для \[ 2 \] файла.</span><span class="sxs-lookup"><span data-stu-id="8fd23-121">BindImage action has not been executed on \[2\] file.</span></span> |



 

<span data-ttu-id="8fd23-122">Если проверка завершается сбоем после копирования, дублирования или исправления несжатого файла, установщик сообщает о следующей ошибке.</span><span class="sxs-lookup"><span data-stu-id="8fd23-122">If the check fails after an uncompressed file had been copied, duplicated, or patched, the installer reports the following error.</span></span> <span data-ttu-id="8fd23-123">Эта ошибка также сообщает о сбое проверки после копирования сжатого файла.</span><span class="sxs-lookup"><span data-stu-id="8fd23-123">This error is also reported if the check fails after a compressed file is copied.</span></span> <span data-ttu-id="8fd23-124">Если файл имеет атрибут **мсидбфилеаттрибутесвитал** , файл считается жизненно важным для установки, и пользователь получает возможность повторить попытку или отменить установку.</span><span class="sxs-lookup"><span data-stu-id="8fd23-124">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the user gets the option to retry or cancel the installation.</span></span> <span data-ttu-id="8fd23-125">Если файл помечен как некритический в столбце Attributes [таблицы File](file-table.md), пользователь может пропустить ошибку и продолжить, повторить попытку или отменить установку.</span><span class="sxs-lookup"><span data-stu-id="8fd23-125">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user may ignore the error and continue, retry, or cancel the installation.</span></span>



| <span data-ttu-id="8fd23-126">Код</span><span class="sxs-lookup"><span data-stu-id="8fd23-126">Code</span></span> | <span data-ttu-id="8fd23-127">Сообщение</span><span class="sxs-lookup"><span data-stu-id="8fd23-127">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="8fd23-128">1331</span><span class="sxs-lookup"><span data-stu-id="8fd23-128">1331</span></span> | <span data-ttu-id="8fd23-129">Не удалось правильно скопировать \[ 2 \] файл: Ошибка CRC.</span><span class="sxs-lookup"><span data-stu-id="8fd23-129">Failed to correctly copy \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="8fd23-130">Обратите внимание, что перемещаются только несжатые файлы.</span><span class="sxs-lookup"><span data-stu-id="8fd23-130">Note that only uncompressed files are moved.</span></span> <span data-ttu-id="8fd23-131">Если проверка завершается сбоем после перемещения несжатого файла, установщик отображает следующую ошибку.</span><span class="sxs-lookup"><span data-stu-id="8fd23-131">If the check fails after an uncompressed file is moved, the installer displays the following error.</span></span> <span data-ttu-id="8fd23-132">Если файл имеет атрибут **мсидбфилеаттрибутесвитал** , файл считается жизненно важным для установки, и установка завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="8fd23-132">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="8fd23-133">Если файл помечен как некритический в столбце Attributes [таблицы File](file-table.md), пользователь получает возможность отменить или пропустить ошибку и продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="8fd23-133">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="8fd23-134">Код</span><span class="sxs-lookup"><span data-stu-id="8fd23-134">Code</span></span> | <span data-ttu-id="8fd23-135">Сообщение</span><span class="sxs-lookup"><span data-stu-id="8fd23-135">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="8fd23-136">1332</span><span class="sxs-lookup"><span data-stu-id="8fd23-136">1332</span></span> | <span data-ttu-id="8fd23-137">Не удалось правильно переместить \[ 2 \] файл: Ошибка CRC.</span><span class="sxs-lookup"><span data-stu-id="8fd23-137">Failed to correctly move \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="8fd23-138">Если проверка завершается сбоем после исправления несжатого файла, установщик отображает следующую ошибку.</span><span class="sxs-lookup"><span data-stu-id="8fd23-138">If the check fails after an uncompressed file is patched, the installer displays the following error.</span></span> <span data-ttu-id="8fd23-139">Если файл имеет атрибут **мсидбфилеаттрибутесвитал** , файл считается жизненно важным для установки, и установка завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="8fd23-139">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="8fd23-140">Если файл помечен как некритический в столбце Attributes [таблицы File](file-table.md), пользователь получает возможность отменить или пропустить ошибку и продолжить установку.</span><span class="sxs-lookup"><span data-stu-id="8fd23-140">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="8fd23-141">Код</span><span class="sxs-lookup"><span data-stu-id="8fd23-141">Code</span></span> | <span data-ttu-id="8fd23-142">Сообщение</span><span class="sxs-lookup"><span data-stu-id="8fd23-142">Message</span></span>                                          |
|------|--------------------------------------------------|
| <span data-ttu-id="8fd23-143">1333</span><span class="sxs-lookup"><span data-stu-id="8fd23-143">1333</span></span> | <span data-ttu-id="8fd23-144">Не удалось правильно обновить \[ файл исправления 2 \] : Ошибка CRC.</span><span class="sxs-lookup"><span data-stu-id="8fd23-144">Failed to correctly patch \[2\] file: CRC error.</span></span> |



 

 

 



