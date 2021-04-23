---
description: Таблица Мсифилехаш используется для хранения 128-разрядного хэша исходного файла, предоставленного пакетом установщик Windows. Хэш разбивается на 4 32-разрядные значения и хранится в отдельных столбцах таблицы.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Таблица Мсифилехаш
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86acb299e5d7f099a8d49affc64810d128e88369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662371"
---
# <a name="msifilehash-table"></a><span data-ttu-id="96e24-104">Таблица Мсифилехаш</span><span class="sxs-lookup"><span data-stu-id="96e24-104">MsiFileHash Table</span></span>

<span data-ttu-id="96e24-105">Таблица **мсифилехаш** используется для хранения 128-разрядного хэша исходного файла, предоставленного пакетом установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="96e24-105">The **MsiFileHash** table is used to store a 128-bit hash of a source file provided by the Windows Installer package.</span></span> <span data-ttu-id="96e24-106">Хэш разбивается на 4 32-разрядные значения и хранится в отдельных столбцах таблицы.</span><span class="sxs-lookup"><span data-stu-id="96e24-106">The hash is split into four 32-bit values and stored in separate columns of the table.</span></span>

<span data-ttu-id="96e24-107">Установщик Windows может использовать хэширование файлов в качестве средства для обнаружения и устранения ненужного копирования файлов.</span><span class="sxs-lookup"><span data-stu-id="96e24-107">Windows Installer can use file hashing as a means to detect and eliminate unnecessary file copying.</span></span> <span data-ttu-id="96e24-108">Хэш файла, хранящийся в таблице **мсифилехаш** , может сравниваться с хэшем существующего файла на компьютере пользователя, полученного путем вызова [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span><span class="sxs-lookup"><span data-stu-id="96e24-108">A file hash stored in the **MsiFileHash** table may be compared to a hash of an existing file on the user's computer obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="96e24-109">Таблицу **мсифилехаш** можно использовать только с файлами без версий.</span><span class="sxs-lookup"><span data-stu-id="96e24-109">The **MsiFileHash** table can only be used with unversioned files.</span></span>

<span data-ttu-id="96e24-110">Таблица **мсифилехаш** содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="96e24-110">The **MsiFileHash** table has the following columns.</span></span>



| <span data-ttu-id="96e24-111">Столбец</span><span class="sxs-lookup"><span data-stu-id="96e24-111">Column</span></span>    | <span data-ttu-id="96e24-112">Type</span><span class="sxs-lookup"><span data-stu-id="96e24-112">Type</span></span>                               | <span data-ttu-id="96e24-113">Ключ</span><span class="sxs-lookup"><span data-stu-id="96e24-113">Key</span></span> | <span data-ttu-id="96e24-114">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="96e24-114">Nullable</span></span> |
|-----------|------------------------------------|-----|----------|
| <span data-ttu-id="96e24-115">Файл\_</span><span class="sxs-lookup"><span data-stu-id="96e24-115">File\_</span></span>    | [<span data-ttu-id="96e24-116">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="96e24-116">Identifier</span></span>](identifier.md)       | <span data-ttu-id="96e24-117">Да</span><span class="sxs-lookup"><span data-stu-id="96e24-117">Y</span></span>   | <span data-ttu-id="96e24-118">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-118">N</span></span>        |
| <span data-ttu-id="96e24-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="96e24-119">Options</span></span>   | [<span data-ttu-id="96e24-120">Integer</span><span class="sxs-lookup"><span data-stu-id="96e24-120">Integer</span></span>](integer.md)             | <span data-ttu-id="96e24-121">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-121">N</span></span>   | <span data-ttu-id="96e24-122">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-122">N</span></span>        |
| <span data-ttu-id="96e24-123">HashPart1</span><span class="sxs-lookup"><span data-stu-id="96e24-123">HashPart1</span></span> | [<span data-ttu-id="96e24-124">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="96e24-124">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="96e24-125">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-125">N</span></span>   | <span data-ttu-id="96e24-126">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-126">N</span></span>        |
| <span data-ttu-id="96e24-127">HashPart2</span><span class="sxs-lookup"><span data-stu-id="96e24-127">HashPart2</span></span> | [<span data-ttu-id="96e24-128">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="96e24-128">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="96e24-129">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-129">N</span></span>   | <span data-ttu-id="96e24-130">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-130">N</span></span>        |
| <span data-ttu-id="96e24-131">HashPart3</span><span class="sxs-lookup"><span data-stu-id="96e24-131">HashPart3</span></span> | [<span data-ttu-id="96e24-132">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="96e24-132">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="96e24-133">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-133">N</span></span>   | <span data-ttu-id="96e24-134">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-134">N</span></span>        |
| <span data-ttu-id="96e24-135">Hashpart4</span><span class="sxs-lookup"><span data-stu-id="96e24-135">Hashpart4</span></span> | [<span data-ttu-id="96e24-136">даублеинтежер</span><span class="sxs-lookup"><span data-stu-id="96e24-136">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="96e24-137">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-137">N</span></span>   | <span data-ttu-id="96e24-138">Нет</span><span class="sxs-lookup"><span data-stu-id="96e24-138">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="96e24-139">Столбцы</span><span class="sxs-lookup"><span data-stu-id="96e24-139">Columns</span></span>

<dl> <dt>

<span data-ttu-id="96e24-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span><span class="sxs-lookup"><span data-stu-id="96e24-140"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="96e24-141">Внешний ключ к [таблице файлов](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="96e24-141">Foreign key to [File table](file-table.md).</span></span> <span data-ttu-id="96e24-142">72 строка char.</span><span class="sxs-lookup"><span data-stu-id="96e24-142">72 char string.</span></span>

</dd> <dt>

<span data-ttu-id="96e24-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Параметры</span><span class="sxs-lookup"><span data-stu-id="96e24-143"><span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Options</span></span>
</dt> <dd>

<span data-ttu-id="96e24-144">Этот столбец должен быть равен 0 и зарезервирован для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="96e24-144">This column must be 0 and is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="96e24-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span><span class="sxs-lookup"><span data-stu-id="96e24-145"><span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1</span></span>
</dt> <dd>

<span data-ttu-id="96e24-146">Первые 32 бит хэша.</span><span class="sxs-lookup"><span data-stu-id="96e24-146">First 32 bits of hash.</span></span> <span data-ttu-id="96e24-147">Хэш файла, указанный в этом поле, должен быть получен путем вызова [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) или [**метода FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="96e24-147">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="96e24-148">Не используйте другие методы.</span><span class="sxs-lookup"><span data-stu-id="96e24-148">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="96e24-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span><span class="sxs-lookup"><span data-stu-id="96e24-149"><span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2</span></span>
</dt> <dd>

<span data-ttu-id="96e24-150">Второй 32 бит хэша.</span><span class="sxs-lookup"><span data-stu-id="96e24-150">Second 32 bits of hash.</span></span> <span data-ttu-id="96e24-151">Хэш файла, указанный в этом поле, должен быть получен путем вызова [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) или [**метода FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="96e24-151">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="96e24-152">Не используйте другие методы хэширования.</span><span class="sxs-lookup"><span data-stu-id="96e24-152">Do not use other hashing methods.</span></span>

</dd> <dt>

<span data-ttu-id="96e24-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span><span class="sxs-lookup"><span data-stu-id="96e24-153"><span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3</span></span>
</dt> <dd>

<span data-ttu-id="96e24-154">Третий 32 бит хэша.</span><span class="sxs-lookup"><span data-stu-id="96e24-154">Third 32 bits of hash.</span></span> <span data-ttu-id="96e24-155">Хэш файла, указанный в этом поле, должен быть получен путем вызова [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) или [**метода FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="96e24-155">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="96e24-156">Не используйте другие методы.</span><span class="sxs-lookup"><span data-stu-id="96e24-156">Do not use other methods.</span></span>

</dd> <dt>

<span data-ttu-id="96e24-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span><span class="sxs-lookup"><span data-stu-id="96e24-157"><span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4</span></span>
</dt> <dd>

<span data-ttu-id="96e24-158">Четвертый 32 бит хэша.</span><span class="sxs-lookup"><span data-stu-id="96e24-158">Fourth 32 bits of hash.</span></span> <span data-ttu-id="96e24-159">Хэш файла, указанный в этом поле, должен быть получен путем вызова [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) или [**метода FileHash**](installer-filehash.md).</span><span class="sxs-lookup"><span data-stu-id="96e24-159">The file hash entered in this field must be obtained by calling [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) or the [**FileHash method**](installer-filehash.md).</span></span> <span data-ttu-id="96e24-160">Не используйте другие методы.</span><span class="sxs-lookup"><span data-stu-id="96e24-160">Do not use other methods.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="96e24-161">Проверка</span><span class="sxs-lookup"><span data-stu-id="96e24-161">Validation</span></span>

<dl>

[<span data-ttu-id="96e24-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="96e24-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="96e24-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="96e24-163">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="96e24-164">ICE32</span><span class="sxs-lookup"><span data-stu-id="96e24-164">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="96e24-165">ICE60</span><span class="sxs-lookup"><span data-stu-id="96e24-165">ICE60</span></span>](ice60.md)  
[<span data-ttu-id="96e24-166">ICE66</span><span class="sxs-lookup"><span data-stu-id="96e24-166">ICE66</span></span>](ice66.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="96e24-167">См. также</span><span class="sxs-lookup"><span data-stu-id="96e24-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96e24-168">**мсижетфилехаш**</span><span class="sxs-lookup"><span data-stu-id="96e24-168">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[<span data-ttu-id="96e24-169">Управление версиями файлов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="96e24-169">Default File Versioning</span></span>](default-file-versioning.md)
</dt> </dl>

 

 



