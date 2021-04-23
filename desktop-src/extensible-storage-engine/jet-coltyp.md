---
description: 'Дополнительные сведения: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912683"
---
# <a name="jet_coltyp"></a><span data-ttu-id="ca62f-103">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="ca62f-103">JET_COLTYP</span></span>


<span data-ttu-id="ca62f-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="ca62f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_coltyp"></a><span data-ttu-id="ca62f-105">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="ca62f-105">JET_COLTYP</span></span>

<span data-ttu-id="ca62f-106">**JET_COLTYP** группа констант описывает все возможные типы столбцов, которые можно найти в таблице.</span><span class="sxs-lookup"><span data-stu-id="ca62f-106">The **JET_COLTYP** group of constants describe all possible column types that can be found in a table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca62f-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="ca62f-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="ca62f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ca62f-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-109">JET_coltypNil</span><span class="sxs-lookup"><span data-stu-id="ca62f-109">JET_coltypNil</span></span><br />
<span data-ttu-id="ca62f-110">0</span><span class="sxs-lookup"><span data-stu-id="ca62f-110">0</span></span></p></td>
<td><p><span data-ttu-id="ca62f-111">Недопустимый тип столбца.</span><span class="sxs-lookup"><span data-stu-id="ca62f-111">An invalid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca62f-112">JET_coltypBit</span><span class="sxs-lookup"><span data-stu-id="ca62f-112">JET_coltypBit</span></span><br />
<span data-ttu-id="ca62f-113">1</span><span class="sxs-lookup"><span data-stu-id="ca62f-113">1</span></span></p></td>
<td><p><span data-ttu-id="ca62f-114">Тип столбца, допускающий три значения: <strong>true</strong>, <strong>false</strong>или <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca62f-114">A column type that allows three values: <strong>True</strong>, <strong>False</strong>, or <strong>NULL</strong>.</span></span> <span data-ttu-id="ca62f-115">Этот тип столбца имеет длину один байт и имеет фиксированный размер.</span><span class="sxs-lookup"><span data-stu-id="ca62f-115">This type of column is one byte in length and is a fixed size.</span></span> <span data-ttu-id="ca62f-116"><strong>Значение false</strong> сортирует до <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="ca62f-116"><strong>False</strong> sorts before <strong>True</strong>.</span></span> <span data-ttu-id="ca62f-117">Обратите внимание, что размер этого типа не соответствует размеру логического типа Variant.</span><span class="sxs-lookup"><span data-stu-id="ca62f-117">Note that the size of this type does not match the size of the variant Boolean type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-118">JET_coltypUnsignedByte</span><span class="sxs-lookup"><span data-stu-id="ca62f-118">JET_coltypUnsignedByte</span></span><br />
<span data-ttu-id="ca62f-119">2</span><span class="sxs-lookup"><span data-stu-id="ca62f-119">2</span></span></p></td>
<td><p><span data-ttu-id="ca62f-120">1-байтовое целое число без знака, которое может принимать значения от 0 (ноль) до 255.</span><span class="sxs-lookup"><span data-stu-id="ca62f-120">A 1-byte unsigned integer that can take on values between 0 (zero) and 255.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca62f-121">JET_coltypShort</span><span class="sxs-lookup"><span data-stu-id="ca62f-121">JET_coltypShort</span></span><br />
<span data-ttu-id="ca62f-122">3</span><span class="sxs-lookup"><span data-stu-id="ca62f-122">3</span></span></p></td>
<td><p><span data-ttu-id="ca62f-123">2-байтовое целое число со знаком, которое может принимать значения от-32768 до 32767.</span><span class="sxs-lookup"><span data-stu-id="ca62f-123">A 2-byte signed integer that can take on values between -32768 and 32767.</span></span> <span data-ttu-id="ca62f-124">Отрицательные значения сортируются перед положительными значениями.</span><span class="sxs-lookup"><span data-stu-id="ca62f-124">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-125">JET_coltypLong</span><span class="sxs-lookup"><span data-stu-id="ca62f-125">JET_coltypLong</span></span><br />
<span data-ttu-id="ca62f-126">4</span><span class="sxs-lookup"><span data-stu-id="ca62f-126">4</span></span></p></td>
<td><p><span data-ttu-id="ca62f-127">4-байтовое целое число со знаком, которое может принимать значения от-2147483648 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="ca62f-127">A 4-byte signed integer that can take on values between - 2147483648 and 2147483647.</span></span> <span data-ttu-id="ca62f-128">Отрицательные значения сортируются перед положительными значениями.</span><span class="sxs-lookup"><span data-stu-id="ca62f-128">Negative values sort before positive values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca62f-129">JET_coltypCurrency</span><span class="sxs-lookup"><span data-stu-id="ca62f-129">JET_coltypCurrency</span></span><br />
<span data-ttu-id="ca62f-130">5</span><span class="sxs-lookup"><span data-stu-id="ca62f-130">5</span></span></p></td>
<td><p><span data-ttu-id="ca62f-131">8-байтовое целое число со знаком, которое может принимать значения от-9223372036854775808 до 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="ca62f-131">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="ca62f-132">Отрицательные значения сортируются перед положительными значениями.</span><span class="sxs-lookup"><span data-stu-id="ca62f-132">Negative values sort before positive values.</span></span> <span data-ttu-id="ca62f-133">Этот тип столбца идентичен типу денежной единицы типа Variant.</span><span class="sxs-lookup"><span data-stu-id="ca62f-133">This column type is identical to the variant currency type.</span></span> <span data-ttu-id="ca62f-134">Этот тип столбца также может использоваться в качестве собственного 8-байтового целого числа со знаком.</span><span class="sxs-lookup"><span data-stu-id="ca62f-134">This column type can also be used as a native 8-byte signed integer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-135">JET_coltypIEEESingle</span><span class="sxs-lookup"><span data-stu-id="ca62f-135">JET_coltypIEEESingle</span></span><br />
<span data-ttu-id="ca62f-136">6</span><span class="sxs-lookup"><span data-stu-id="ca62f-136">6</span></span></p></td>
<td><p><span data-ttu-id="ca62f-137">Число с плавающей запятой одиночной точности (4 байта).</span><span class="sxs-lookup"><span data-stu-id="ca62f-137">A single-precision (4-byte) floating point number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca62f-138">JET_coltypIEEEDouble</span><span class="sxs-lookup"><span data-stu-id="ca62f-138">JET_coltypIEEEDouble</span></span><br />
<span data-ttu-id="ca62f-139">7</span><span class="sxs-lookup"><span data-stu-id="ca62f-139">7</span></span></p></td>
<td><p><span data-ttu-id="ca62f-140">Число с плавающей запятой двойной точности (8 байт).</span><span class="sxs-lookup"><span data-stu-id="ca62f-140">A double-precision (8-byte) floating point number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-141">JET_coltypDateTime</span><span class="sxs-lookup"><span data-stu-id="ca62f-141">JET_coltypDateTime</span></span><br />
<span data-ttu-id="ca62f-142">8</span><span class="sxs-lookup"><span data-stu-id="ca62f-142">8</span></span></p></td>
<td><p><span data-ttu-id="ca62f-143">Число с плавающей запятой двойной точности (8 байт), представляющее дату в дробных днях, начиная с 1900 года.</span><span class="sxs-lookup"><span data-stu-id="ca62f-143">A double-precision (8-byte) floating point number that represents a date in fractional days since the year 1900.</span></span> <span data-ttu-id="ca62f-144">Этот тип столбца идентичен типу Variant типа Date.</span><span class="sxs-lookup"><span data-stu-id="ca62f-144">This column type is identical to the variant date type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca62f-145">JET_coltypBinary</span><span class="sxs-lookup"><span data-stu-id="ca62f-145">JET_coltypBinary</span></span><br />
<span data-ttu-id="ca62f-146">9</span><span class="sxs-lookup"><span data-stu-id="ca62f-146">9</span></span></p></td>
<td><p><span data-ttu-id="ca62f-147">Двоичный столбец фиксированной или переменной длины, который может иметь длину до 255 байт.</span><span class="sxs-lookup"><span data-stu-id="ca62f-147">A fixed or variable length, raw binary column that can be up to 255 bytes in length.</span></span></p>
<p><span data-ttu-id="ca62f-148">Этот тип столбца можно использовать для реализации GUID, если он настроен в виде двоичного столбца фиксированной длины (16 байт).</span><span class="sxs-lookup"><span data-stu-id="ca62f-148">This column type can be used to implement a GUID if configured as a fixed length, 16-byte binary column.</span></span> <span data-ttu-id="ca62f-149">Единственное предостережение заключается в том, что относительный порядок значений в индексе по такому столбцу не будет совпадать с относительным порядком стандартного отображения строки реестра (т &quot; . е. {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot; ).</span><span class="sxs-lookup"><span data-stu-id="ca62f-149">The only caveat is that the relative ordering of values in an index over such a column will not match the relative ordering of the standard registry-string rendering of a GUID (that is &quot;{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-150">JET_coltypText</span><span class="sxs-lookup"><span data-stu-id="ca62f-150">JET_coltypText</span></span><br />
<span data-ttu-id="ca62f-151">10</span><span class="sxs-lookup"><span data-stu-id="ca62f-151">10</span></span></p></td>
<td><p><span data-ttu-id="ca62f-152">Фиксированный или переменный текстовый столбец длиной до 255 символов ASCII длиной или 127 символов Юникода в длину.</span><span class="sxs-lookup"><span data-stu-id="ca62f-152">A fixed or variable length text column that can be up to 255 ASCII characters in length or 127 Unicode characters in length.</span></span></p>
<p><span data-ttu-id="ca62f-153">Все строки хранятся в виде подсчитанного количества символов.</span><span class="sxs-lookup"><span data-stu-id="ca62f-153">All strings are stored as a counted number of characters.</span></span> <span data-ttu-id="ca62f-154">Строки не должны завершаться нулем.</span><span class="sxs-lookup"><span data-stu-id="ca62f-154">The strings need not be null terminated.</span></span> <span data-ttu-id="ca62f-155">Кроме того, для счетчика не нужно включать терминатор null.</span><span class="sxs-lookup"><span data-stu-id="ca62f-155">Further, it is not necessary for the count to include a null terminator.</span></span> <span data-ttu-id="ca62f-156">Наконец, можно хранить внедренные символы NULL.</span><span class="sxs-lookup"><span data-stu-id="ca62f-156">Finally, embedded null characters can be stored.</span></span></p>
<p><span data-ttu-id="ca62f-157">Строки ASCII всегда обрабатываются как нечувствительные к регистру в целях сортировки и поиска.</span><span class="sxs-lookup"><span data-stu-id="ca62f-157">ASCII strings are always treated as case insensitive for sorting and searching purposes.</span></span> <span data-ttu-id="ca62f-158">Кроме того, для сортировки и поиска учитываются только символы, предшествующие первому символу null (если таковые имеются).</span><span class="sxs-lookup"><span data-stu-id="ca62f-158">Further, only the characters preceding the first null character (if any) are considered for sorting and searching.</span></span></p>
<p><span data-ttu-id="ca62f-159">Строки в Юникоде используют API Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString завершилось ошибкой</a> для создания ключей сортировки, которые впоследствии используются для сортировки и поиска этих данных.</span><span class="sxs-lookup"><span data-stu-id="ca62f-159">Unicode strings use the Win32 API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> to create sort keys that are subsequently used for sorting and searching that data.</span></span> <span data-ttu-id="ca62f-160">По умолчанию строки Юникода считаются в языковом стандарте «Английский (США)» и сортируются и ищутся с помощью следующих флагов нормализации: NORM_IGNORECASE, NORM_IGNOREKANATYPE и NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="ca62f-160">By default, Unicode strings are considered to be in the U.S. English locale and are sorted and searched using the following normalization flags: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="ca62f-161">В Windows 2000 можно настроить эти флаги для каждого индекса, чтобы также включить NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="ca62f-161">In Windows 2000, it is possible to customize these flags per index to also include NORM_IGNORENONSPACE.</span></span> <span data-ttu-id="ca62f-162">В Windows XP и более поздних версиях можно запросить любое сочетание следующих флагов нормализации на индекс: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH и SORT_STRINGSORT.</span><span class="sxs-lookup"><span data-stu-id="ca62f-162">In Windows XP and later releases, it is possible to request any combination of the following normalization flags per index: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH, and SORT_STRINGSORT.</span></span></p>
<p><span data-ttu-id="ca62f-163">Во всех выпусках можно настроить языковой стандарт для каждого индекса.</span><span class="sxs-lookup"><span data-stu-id="ca62f-163">In all releases, it is possible to customize the locale per index.</span></span> <span data-ttu-id="ca62f-164">Любой языковой стандарт может использоваться при условии, что на компьютере установлен соответствующий языковой пакет.</span><span class="sxs-lookup"><span data-stu-id="ca62f-164">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="ca62f-165">Наконец, любые символы NULL, обнаруженные в строке Юникода, полностью игнорируются.</span><span class="sxs-lookup"><span data-stu-id="ca62f-165">Finally, any null characters encountered in a Unicode string are completely ignored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca62f-166">JET_coltypLongBinary</span><span class="sxs-lookup"><span data-stu-id="ca62f-166">JET_coltypLongBinary</span></span><br />
<span data-ttu-id="ca62f-167">11</span><span class="sxs-lookup"><span data-stu-id="ca62f-167">11</span></span></p></td>
<td><p><span data-ttu-id="ca62f-168">Двоичный столбец фиксированной или переменной длины, который может иметь длину до 2147483647 байт.</span><span class="sxs-lookup"><span data-stu-id="ca62f-168">A fixed or variable length, raw binary column that can be up to 2147483647 bytes in length.</span></span> <span data-ttu-id="ca62f-169">Этот тип считается длинным значением.</span><span class="sxs-lookup"><span data-stu-id="ca62f-169">This type is considered to be a Long Value.</span></span> <span data-ttu-id="ca62f-170">Значение типа long является специальным, так как оно может быть большим и доступно в виде потока.</span><span class="sxs-lookup"><span data-stu-id="ca62f-170">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="ca62f-171">В противном случае этот тип идентичен JET_coltypBinary.</span><span class="sxs-lookup"><span data-stu-id="ca62f-171">This type is otherwise identical to JET_coltypBinary.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-172">JET_coltypLongText</span><span class="sxs-lookup"><span data-stu-id="ca62f-172">JET_coltypLongText</span></span><br />
<span data-ttu-id="ca62f-173">12</span><span class="sxs-lookup"><span data-stu-id="ca62f-173">12</span></span></p></td>
<td><p><span data-ttu-id="ca62f-174">Столбец с фиксированной или переменной длиной, который может содержать до 2147483647 символов ASCII длиной или 1073741823 символов Юникода в длину.</span><span class="sxs-lookup"><span data-stu-id="ca62f-174">A fixed or variable length, text column that can be up to 2147483647 ASCII characters in length or 1073741823 Unicode characters in length.</span></span> <span data-ttu-id="ca62f-175">Этот тип считается длинным значением.</span><span class="sxs-lookup"><span data-stu-id="ca62f-175">This type is considered to be a Long Value.</span></span> <span data-ttu-id="ca62f-176">Значение типа long является специальным, так как оно может быть большим и доступно в виде потока.</span><span class="sxs-lookup"><span data-stu-id="ca62f-176">A Long Value is special because it can be large and because it can be accessed as a stream.</span></span> <span data-ttu-id="ca62f-177">В противном случае этот тип идентичен JET_coltypText.</span><span class="sxs-lookup"><span data-stu-id="ca62f-177">This type is otherwise identical to JET_coltypText.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca62f-178">JET_coltypSLV</span><span class="sxs-lookup"><span data-stu-id="ca62f-178">JET_coltypSLV</span></span><br />
<span data-ttu-id="ca62f-179">13</span><span class="sxs-lookup"><span data-stu-id="ca62f-179">13</span></span></p></td>
<td><p><span data-ttu-id="ca62f-180">Этот тип столбца устарел.</span><span class="sxs-lookup"><span data-stu-id="ca62f-180">This column type is obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-181">JET_coltypUnsignedLong</span><span class="sxs-lookup"><span data-stu-id="ca62f-181">JET_coltypUnsignedLong</span></span><br />
<span data-ttu-id="ca62f-182">14</span><span class="sxs-lookup"><span data-stu-id="ca62f-182">14</span></span></p></td>
<td><p><span data-ttu-id="ca62f-183">4-байтовое целое число без знака, которое может принимать значения от 0 (ноль) до 4294967295.</span><span class="sxs-lookup"><span data-stu-id="ca62f-183">A 4-byte unsigned integer that can take on values between 0 (zero) and 4294967295.</span></span></p>
<p><span data-ttu-id="ca62f-184"><strong>Windows Vista и Windows Server 2008:</strong>  Этот тип столбца поддерживается в Windows Vista, Windows Server 2008 и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="ca62f-184"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca62f-185">JET_coltypLongLong</span><span class="sxs-lookup"><span data-stu-id="ca62f-185">JET_coltypLongLong</span></span><br />
<span data-ttu-id="ca62f-186">15</span><span class="sxs-lookup"><span data-stu-id="ca62f-186">15</span></span></p></td>
<td><p><span data-ttu-id="ca62f-187">8-байтовое целое число со знаком, которое может принимать значения от-9223372036854775808 до 9223372036854775807.</span><span class="sxs-lookup"><span data-stu-id="ca62f-187">An 8-byte signed integer that can take on values between - 9223372036854775808 and 9223372036854775807.</span></span> <span data-ttu-id="ca62f-188">Отрицательные значения сортируются перед положительными значениями.</span><span class="sxs-lookup"><span data-stu-id="ca62f-188">Negative values sort before positive values.</span></span></p>
<p><span data-ttu-id="ca62f-189"><strong>Windows Vista и Windows Server 2008:</strong>  Этот тип столбца поддерживается в Windows Vista, Windows Server 2008 и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="ca62f-189"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-190">JET_coltypGUID</span><span class="sxs-lookup"><span data-stu-id="ca62f-190">JET_coltypGUID</span></span><br />
<span data-ttu-id="ca62f-191">16</span><span class="sxs-lookup"><span data-stu-id="ca62f-191">16</span></span></p></td>
<td><p><span data-ttu-id="ca62f-192">Двоичный столбец фиксированной длины длиной 16 байт, который изначально представляет тип данных GUID.</span><span class="sxs-lookup"><span data-stu-id="ca62f-192">A fixed length 16 byte binary column that natively represents the GUID data type.</span></span> <span data-ttu-id="ca62f-193">Значения столбца GUID сортируются так же, как строки в стандартной форме (например, {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span><span class="sxs-lookup"><span data-stu-id="ca62f-193">GUID column values sort in the same way that those values would sort as strings when in standard form (i.e. {4999b5c0-7657-42d9-bdc1-4b779784e013}).</span></span></p>
<p><span data-ttu-id="ca62f-194"><strong>Windows Vista и Windows Server 2008:</strong>  Этот тип столбца поддерживается в Windows Vista, Windows Server 2008 и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="ca62f-194"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca62f-195">JET_coltypUnsignedShort</span><span class="sxs-lookup"><span data-stu-id="ca62f-195">JET_coltypUnsignedShort</span></span><br />
<span data-ttu-id="ca62f-196">17</span><span class="sxs-lookup"><span data-stu-id="ca62f-196">17</span></span></p></td>
<td><p><span data-ttu-id="ca62f-197">2-байтовое целое число без знака, которое может принимать значения от 0 до 65535.</span><span class="sxs-lookup"><span data-stu-id="ca62f-197">A 2-byte unsigned integer that can take on values between 0 and 65535.</span></span></p>
<p><span data-ttu-id="ca62f-198"><strong>Windows Vista и Windows Server 2008:</strong>  Этот тип столбца поддерживается в Windows Vista, Windows Server 2008 и более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="ca62f-198"><strong>Windows Vista and Windows Server 2008:</strong>  This column type is supported on Windows Vista, Windows Server 2008 and later releases.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-199">JET_coltypMax</span><span class="sxs-lookup"><span data-stu-id="ca62f-199">JET_coltypMax</span></span><br />
<span data-ttu-id="ca62f-200">18</span><span class="sxs-lookup"><span data-stu-id="ca62f-200">18</span></span></p></td>
<td><p><span data-ttu-id="ca62f-201">Константа, описывающая максимальное значение (то есть одно из более наибольшего допустимого) типа столбца, поддерживаемого ядром.</span><span class="sxs-lookup"><span data-stu-id="ca62f-201">A constant describing the maximum (that is, one beyond the largest valid) column type supported by the engine.</span></span></p>
<p><span data-ttu-id="ca62f-202">Это значение следует использовать с осторожностью, так как оно меняется по мере поддержки новых типов столбцов.</span><span class="sxs-lookup"><span data-stu-id="ca62f-202">This value should be used with care because it will change as new column types are supported.</span></span> <span data-ttu-id="ca62f-203">Например, он имеет другое литеральное значение в Windows 2000, чем в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="ca62f-203">For example, it has a different literal value on Windows 2000 than it does on Windows XP and later releases.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="ca62f-204">Требования</span><span class="sxs-lookup"><span data-stu-id="ca62f-204">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-205"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="ca62f-205"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="ca62f-206">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="ca62f-206">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca62f-207"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="ca62f-207"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="ca62f-208">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="ca62f-208">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca62f-209"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="ca62f-209"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="ca62f-210">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="ca62f-210">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="ca62f-211">См. также:</span><span class="sxs-lookup"><span data-stu-id="ca62f-211">See Also</span></span>

[<span data-ttu-id="ca62f-212">жетаддколумн</span><span class="sxs-lookup"><span data-stu-id="ca62f-212">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="ca62f-213">жеткреатетаблеколумниндекс</span><span class="sxs-lookup"><span data-stu-id="ca62f-213">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)
