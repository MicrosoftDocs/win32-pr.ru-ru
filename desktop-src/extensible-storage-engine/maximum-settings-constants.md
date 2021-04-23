---
description: Дополнительные сведения о параметрах максимальной константы параметров
title: Максимальные константы параметров
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897658"
---
# <a name="maximum-settings-constants"></a><span data-ttu-id="1b2db-103">Максимальные константы параметров</span><span class="sxs-lookup"><span data-stu-id="1b2db-103">Maximum Settings Constants</span></span>


<span data-ttu-id="1b2db-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="1b2db-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="maximum-settings-constants"></a><span data-ttu-id="1b2db-105">Максимальные константы параметров</span><span class="sxs-lookup"><span data-stu-id="1b2db-105">Maximum Settings Constants</span></span>

<span data-ttu-id="1b2db-106">Эти константы предоставляют максимальные параметры, разрешенные для элементов в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="1b2db-106">These constants provide the maximum settings that are allowed on items in an ESE database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b2db-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="1b2db-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="1b2db-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1b2db-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-109">JET_BASE_NAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="1b2db-109">JET_BASE_NAME_LENGTH</span></span><br />
<span data-ttu-id="1b2db-110">3</span><span class="sxs-lookup"><span data-stu-id="1b2db-110">3</span></span></p></td>
<td><p><span data-ttu-id="1b2db-111">Задает длину префикса, используемого для имен файлов, используемых ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="1b2db-111">Sets the length for the prefix used to name files that are used by the database engine.</span></span> <span data-ttu-id="1b2db-112">Эта длина применима к имени, заданному для параметра системы <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</span><span class="sxs-lookup"><span data-stu-id="1b2db-112">This length is applicable to the name set for the <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> system parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-113">JET_MAX_COMPUTERNAME_LENGTH</span><span class="sxs-lookup"><span data-stu-id="1b2db-113">JET_MAX_COMPUTERNAME_LENGTH</span></span><br />
<span data-ttu-id="1b2db-114">15</span><span class="sxs-lookup"><span data-stu-id="1b2db-114">15</span></span></p></td>
<td><p><span data-ttu-id="1b2db-115">Задает максимальную длину для <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span><span class="sxs-lookup"><span data-stu-id="1b2db-115">Sets the maximum length for <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-116">JET_cbBookmarkMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-116">JET_cbBookmarkMost</span></span><br />
<span data-ttu-id="1b2db-117">256</span><span class="sxs-lookup"><span data-stu-id="1b2db-117">256</span></span></p></td>
<td><p><span data-ttu-id="1b2db-118">Максимальный размер закладки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1b2db-118">The default maximum size of a bookmark.</span></span> <span data-ttu-id="1b2db-119">Это допустимо, если размер ключа остался равным значению по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1b2db-119">This is valid when the key size is left at its default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-120">JET_cbBookmarkMostMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-120">JET_cbBookmarkMostMost</span></span><br />
<span data-ttu-id="1b2db-121">2000</span><span class="sxs-lookup"><span data-stu-id="1b2db-121">2000</span></span></p></td>
<td><p><span data-ttu-id="1b2db-122">Максимальный размер закладки, если для ESENT настроено максимально возможное количество ключей.</span><span class="sxs-lookup"><span data-stu-id="1b2db-122">The maximum size of a bookmark when esent is configured to have the largest keys possible.</span></span></p>
<p><span data-ttu-id="1b2db-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost введен в Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1b2db-123"><strong>Windows 7:</strong> JET_cbBookmarkMostMost is introduced in Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-124">JET_cbNameMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-124">JET_cbNameMost</span></span><br />
<span data-ttu-id="1b2db-125">64</span><span class="sxs-lookup"><span data-stu-id="1b2db-125">64</span></span></p></td>
<td><p><span data-ttu-id="1b2db-126">Максимальная длина имени объекта, столбца, индекса или свойства.</span><span class="sxs-lookup"><span data-stu-id="1b2db-126">The maximum length of a object, column, index, or property name.</span></span></p>
<p><span data-ttu-id="1b2db-127"><strong>Примечание</strong>  .  Если Unicode, значение равно 128.</span><span class="sxs-lookup"><span data-stu-id="1b2db-127"><strong>Note</strong>  If Unicode, the value is 128.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-128">JET_cbFullNameMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-128">JET_cbFullNameMost</span></span><br />
<span data-ttu-id="1b2db-129">255</span><span class="sxs-lookup"><span data-stu-id="1b2db-129">255</span></span></p></td>
<td><p><span data-ttu-id="1b2db-130">Максимальная длина &quot; конструкции Name.Name.Name... &quot;</span><span class="sxs-lookup"><span data-stu-id="1b2db-130">The maximum length of a &quot;name.name.name...&quot; construct.</span></span></p>
<p><span data-ttu-id="1b2db-131"><strong>Примечание</strong>  .  Если Unicode, значение равно 510.</span><span class="sxs-lookup"><span data-stu-id="1b2db-131"><strong>Note</strong>  If Unicode, the value is 510.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-132">JET_cbColumnLVPageOverhead</span><span class="sxs-lookup"><span data-stu-id="1b2db-132">JET_cbColumnLVPageOverhead</span></span><br />
<span data-ttu-id="1b2db-133">82</span><span class="sxs-lookup"><span data-stu-id="1b2db-133">82</span></span></p></td>
<td><p><span data-ttu-id="1b2db-134">Этот номер можно использовать для расчета максимального объема большого двоичного объекта, который может храниться ядром СУБД на одной странице базы данных.</span><span class="sxs-lookup"><span data-stu-id="1b2db-134">This number can be used to compute the maximum amount of a BLOB that can be stored by the database engine on a single database page.</span></span> <span data-ttu-id="1b2db-135">Формула имеет максимальный размер = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</span><span class="sxs-lookup"><span data-stu-id="1b2db-135">The formula is max size = JET_paramDatabasePageSize–JET_cbColumnLVPageOverhead.</span></span></p>
<p><span data-ttu-id="1b2db-136">Теперь это значение устарело.</span><span class="sxs-lookup"><span data-stu-id="1b2db-136">This value is now obsolete.</span></span> <span data-ttu-id="1b2db-137">Размер фрагмента данных с длинным значением должен быть получен с помощью параметра JET_paramLVChunkSizeMost.</span><span class="sxs-lookup"><span data-stu-id="1b2db-137">The long-value chunk size should be retrieved with the JET_paramLVChunkSizeMost parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-138">JET_cbColumnMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-138">JET_cbColumnMost</span></span><br />
<span data-ttu-id="1b2db-139">255</span><span class="sxs-lookup"><span data-stu-id="1b2db-139">255</span></span></p></td>
<td><p><span data-ttu-id="1b2db-140">Максимальный размер данных в столбцах, не являющихся значениями типа long.</span><span class="sxs-lookup"><span data-stu-id="1b2db-140">The maximum size of non-long-value column data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-141">JET_cbLVDefaultValueMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-141">JET_cbLVDefaultValueMost</span></span><br />
<span data-ttu-id="1b2db-142">255</span><span class="sxs-lookup"><span data-stu-id="1b2db-142">255</span></span></p></td>
<td><p><span data-ttu-id="1b2db-143">Максимальный размер значения по умолчанию для столбца длинных значений (Лонгбинари или LongText).</span><span class="sxs-lookup"><span data-stu-id="1b2db-143">The maximum size of a long-value (LongBinary or LongText) column default value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-144">JET_cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-144">JET_cbKeyMost</span></span><br />
<span data-ttu-id="1b2db-145">255</span><span class="sxs-lookup"><span data-stu-id="1b2db-145">255</span></span></p></td>
<td><p><span data-ttu-id="1b2db-146">Максимальный размер ключа сортировки или индекса по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1b2db-146">The default maximum size of a sort or index key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-147">JET_cbKeyMostMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-147">JET_cbKeyMostMost</span></span><br />
<span data-ttu-id="1b2db-148">2000</span><span class="sxs-lookup"><span data-stu-id="1b2db-148">2000</span></span></p></td>
<td><p><span data-ttu-id="1b2db-149">Максимальный настраиваемый размер ключа сортировки или индекса для любого размера страницы.</span><span class="sxs-lookup"><span data-stu-id="1b2db-149">The maximum configurable size of a sort or index key for any page size.</span></span> <span data-ttu-id="1b2db-150">(См. JET_INDEXCREATE2. Кбкэймост)</span><span class="sxs-lookup"><span data-stu-id="1b2db-150">(See JET_INDEXCREATE2.cbKeyMost)</span></span></p>
<p><span data-ttu-id="1b2db-151"><strong>Windows 7:</strong> JET_cbKeyMostMost введены в операционной системе Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1b2db-151"><strong>Windows 7:</strong> JET_cbKeyMostMost is introduced in the Windows 7 operating system.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-152">JET_cbKeyMost2KBytePage</span><span class="sxs-lookup"><span data-stu-id="1b2db-152">JET_cbKeyMost2KBytePage</span></span><br />
<span data-ttu-id="1b2db-153">500</span><span class="sxs-lookup"><span data-stu-id="1b2db-153">500</span></span></p></td>
<td><p><span data-ttu-id="1b2db-154">Максимально допустимый максимальный настраиваемый размер ключа индекса в базе данных с 2048 байт.</span><span class="sxs-lookup"><span data-stu-id="1b2db-154">The maximum allowable maximum configurable size for an index key in a database using 2048 byte pages.</span></span> <span data-ttu-id="1b2db-155">Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="1b2db-155">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="1b2db-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage представлен в операционной системе Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1b2db-156"><strong>Windows Vista:</strong> JET_cbKeyMost2KBytePage is introduced in the Windows Vista operating system.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-157">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="1b2db-157">JET_cbKeyMost4KBytePage</span></span><br />
<span data-ttu-id="1b2db-158">1000</span><span class="sxs-lookup"><span data-stu-id="1b2db-158">1000</span></span></p></td>
<td><p><span data-ttu-id="1b2db-159">Максимально допустимый максимальный настраиваемый размер ключа индекса в базе данных с 4096 байт.</span><span class="sxs-lookup"><span data-stu-id="1b2db-159">The maximum allowable maximum configurable size for an index key in a database using 4096 byte pages.</span></span> <span data-ttu-id="1b2db-160">Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="1b2db-160">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="1b2db-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage введен в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1b2db-161"><strong>Windows Vista:</strong> JET_cbKeyMost4KBytePage is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-162">JET_cbKeyMost8KBytePage</span><span class="sxs-lookup"><span data-stu-id="1b2db-162">JET_cbKeyMost8KBytePage</span></span><br />
<span data-ttu-id="1b2db-163">2000</span><span class="sxs-lookup"><span data-stu-id="1b2db-163">2000</span></span></p></td>
<td><p><span data-ttu-id="1b2db-164">Максимально допустимый максимальный настраиваемый размер ключа индекса в базе данных с 8192 байт.</span><span class="sxs-lookup"><span data-stu-id="1b2db-164">The maximum allowable maximum configurable size for an index key in a database using 8192 byte pages.</span></span> <span data-ttu-id="1b2db-165">Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="1b2db-165">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="1b2db-166"><strong>Windows Vista:  </strong> JET_cbKeyMost8KBytePage появился в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1b2db-166"><strong>Windows Vista:  </strong>JET_cbKeyMost8KBytePage is introduced in Windows Vista</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-167">JET_cbKeyMostMin</span><span class="sxs-lookup"><span data-stu-id="1b2db-167">JET_cbKeyMostMin</span></span><br />
<span data-ttu-id="1b2db-168">255</span><span class="sxs-lookup"><span data-stu-id="1b2db-168">255</span></span></p></td>
<td><p><span data-ttu-id="1b2db-169">Минимальный допустимый максимальный размер ключа индекса.</span><span class="sxs-lookup"><span data-stu-id="1b2db-169">The minimum allowable maximum size for an index key.</span></span> <span data-ttu-id="1b2db-170">Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</span><span class="sxs-lookup"><span data-stu-id="1b2db-170">See <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> for more information.</span></span></p>
<p><span data-ttu-id="1b2db-171"><strong>Windows Vista:  </strong> JET_cbKeyMostMin введен в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1b2db-171"><strong>Windows Vista:  </strong>JET_cbKeyMostMin is introduced in Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-172">JET_cbLimitKeyMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-172">JET_cbLimitKeyMost</span></span><br />
<span data-ttu-id="1b2db-173">256</span><span class="sxs-lookup"><span data-stu-id="1b2db-173">256</span></span></p></td>
<td><p><span data-ttu-id="1b2db-174">Максимальный размер ключа при формировании ключа с помощью ограничения <em>грбит</em>, например JET_bitStrLimit, которое используется в функции <a href="gg269329(v=exchg.10).md">жетмакекэй</a> .</span><span class="sxs-lookup"><span data-stu-id="1b2db-174">The maximum key size when the key is formed by using a limit <em>grbit</em>, such as JET_bitStrLimit, which is used in the <a href="gg269329(v=exchg.10).md">JetMakeKey</a> function.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-175">JET_cbPrimaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-175">JET_cbPrimaryKeyMost</span></span><br />
<span data-ttu-id="1b2db-176">255</span><span class="sxs-lookup"><span data-stu-id="1b2db-176">255</span></span></p></td>
<td><p><span data-ttu-id="1b2db-177">Максимальный размер первичного индекса.</span><span class="sxs-lookup"><span data-stu-id="1b2db-177">The maximum size of the primary index.</span></span> <span data-ttu-id="1b2db-178">Эта возможность устарела.</span><span class="sxs-lookup"><span data-stu-id="1b2db-178">This is now obsolete.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-179">JET_cbSecondaryKeyMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-179">JET_cbSecondaryKeyMost</span></span><br />
<span data-ttu-id="1b2db-180">255</span><span class="sxs-lookup"><span data-stu-id="1b2db-180">255</span></span></p></td>
<td><p><span data-ttu-id="1b2db-181">Максимальный размер вторичного индекса.</span><span class="sxs-lookup"><span data-stu-id="1b2db-181">The maximum size of the secondary index.</span></span> <span data-ttu-id="1b2db-182">Эта возможность устарела.</span><span class="sxs-lookup"><span data-stu-id="1b2db-182">This is now obsolete.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-183">JET_ccolKeyMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-183">JET_ccolKeyMost</span></span><br />
<span data-ttu-id="1b2db-184">12</span><span class="sxs-lookup"><span data-stu-id="1b2db-184">12</span></span></p></td>
<td><p><span data-ttu-id="1b2db-185">Максимальное число компонентов в ключе сортировки или индекса.</span><span class="sxs-lookup"><span data-stu-id="1b2db-185">The maximum number of components in a sort or index key.</span></span></p>
<p><span data-ttu-id="1b2db-186"><strong>Windows Vista:  </strong> В Windows Vista и более поздних версиях Windows значение равно 16.</span><span class="sxs-lookup"><span data-stu-id="1b2db-186"><strong>Windows Vista:  </strong>In Windows Vista and later versions of Windows the value is 16.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-187">JET_ccolMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-187">JET_ccolMost</span></span><br />
<span data-ttu-id="1b2db-188">0x0000fee0</span><span class="sxs-lookup"><span data-stu-id="1b2db-188">0x0000fee0</span></span></p></td>
<td><p><span data-ttu-id="1b2db-189">Максимально допустимое число столбцов в таблице.</span><span class="sxs-lookup"><span data-stu-id="1b2db-189">The maximum number of columns allowed in a table.</span></span></p>
<p><span data-ttu-id="1b2db-190"><strong>Windows XP:  </strong> Значение 0x0000fee0 используется в Windows XP и более поздних версий и более поздних версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="1b2db-190"><strong>Windows XP:  </strong>The value 0x0000fee0 is used in Windows XP and later and later versions of Windows</span></span></p>
<p><span data-ttu-id="1b2db-191"><strong>Windows 2000:  </strong> Значение 0x00007ffe используется в Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1b2db-191"><strong>Windows 2000:  </strong>The value 0x00007ffe is used in Windows 2000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-192">JET_ccolFixedMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-192">JET_ccolFixedMost</span></span><br />
<span data-ttu-id="1b2db-193">0x0000007F</span><span class="sxs-lookup"><span data-stu-id="1b2db-193">0x0000007f</span></span></p></td>
<td><p><span data-ttu-id="1b2db-194">Максимальное число фиксированных столбцов, разрешенное в таблице, в настоящее время 127.</span><span class="sxs-lookup"><span data-stu-id="1b2db-194">The maximum number of fixed columns allowed in a table, currently 127.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-195">JET_ccolVarMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-195">JET_ccolVarMost</span></span><br />
<span data-ttu-id="1b2db-196">0x00000080</span><span class="sxs-lookup"><span data-stu-id="1b2db-196">0x00000080</span></span></p></td>
<td><p><span data-ttu-id="1b2db-197">Максимальное число столбцов переменной длины, которые могут содержаться в таблице, в настоящее время 128.</span><span class="sxs-lookup"><span data-stu-id="1b2db-197">The maximum number of variable-length columns that can be contained in a table, currently 128.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-198">JET_ccolTaggedMost</span><span class="sxs-lookup"><span data-stu-id="1b2db-198">JET_ccolTaggedMost</span></span><br />
<span data-ttu-id="1b2db-199">(JET_ccolMost-0x000000ff)</span><span class="sxs-lookup"><span data-stu-id="1b2db-199">( JET_ccolMost - 0x000000ff )</span></span></p></td>
<td><p><span data-ttu-id="1b2db-200">Максимальное число столбцов с тегами, которые могут содержаться в таблице, в настоящее время 64993.</span><span class="sxs-lookup"><span data-stu-id="1b2db-200">The maximum number of tagged columns that can be contained in a table, currently 64993.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="1b2db-201">Требования</span><span class="sxs-lookup"><span data-stu-id="1b2db-201">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-202"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="1b2db-202"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="1b2db-203">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="1b2db-203">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b2db-204"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="1b2db-204"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="1b2db-205">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="1b2db-205">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b2db-206"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="1b2db-206"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="1b2db-207">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="1b2db-207">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

