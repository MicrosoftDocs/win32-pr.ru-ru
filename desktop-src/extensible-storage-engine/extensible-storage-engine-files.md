---
description: 'Дополнительные сведения: расширяемые файлы подсистемы хранилища'
title: Расширяемые файлы подсистемы хранилища
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713359"
---
# <a name="extensible-storage-engine-files"></a><span data-ttu-id="56227-103">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="56227-103">Extensible Storage Engine Files</span></span>


<span data-ttu-id="56227-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="56227-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-files"></a><span data-ttu-id="56227-105">Расширяемые файлы подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="56227-105">Extensible Storage Engine Files</span></span>

<span data-ttu-id="56227-106">Расширяемая подсистема хранилища использует следующие типы файлов:</span><span class="sxs-lookup"><span data-stu-id="56227-106">The Extensible Storage Engine uses the following types of files:</span></span>

- [<span data-ttu-id="56227-107">Файлы журнала транзакций</span><span class="sxs-lookup"><span data-stu-id="56227-107">Transaction Log Files</span></span>](#transaction-log-files)

- [<span data-ttu-id="56227-108">Временные файлы журналов транзакций</span><span class="sxs-lookup"><span data-stu-id="56227-108">Temporary Transaction Log Files</span></span>](#temporary-transaction-log-files)

- [<span data-ttu-id="56227-109">Зарезервированные файлы журнала транзакций</span><span class="sxs-lookup"><span data-stu-id="56227-109">Reserved Transaction Log Files</span></span>](#reserved-transaction-log-files)

- [<span data-ttu-id="56227-110">Файлы контрольных точек</span><span class="sxs-lookup"><span data-stu-id="56227-110">Checkpoint Files</span></span>](#checkpoint-files)

- [<span data-ttu-id="56227-111">Файлы базы данных</span><span class="sxs-lookup"><span data-stu-id="56227-111">Database Files</span></span>](#database-files)

- [<span data-ttu-id="56227-112">Временные базы данных</span><span class="sxs-lookup"><span data-stu-id="56227-112">Temporary Databases</span></span>](#temporary-databases)

- [<span data-ttu-id="56227-113">Очистить файлы карт</span><span class="sxs-lookup"><span data-stu-id="56227-113">Flush Map Files</span></span>](#flush-map-files)

<span data-ttu-id="56227-114">В этой таблице содержится обзор имен файлов данных, управляемых ESE.</span><span class="sxs-lookup"><span data-stu-id="56227-114">This table contains an overview of the data file names that are managed by ESE.</span></span> <span data-ttu-id="56227-115">Для Windows Vista и более поздних версий параметр JET_paramLegacyNames влияет на используемые имена файлов.</span><span class="sxs-lookup"><span data-stu-id="56227-115">For Windows Vista and later, the JET_paramLegacyNames setting impacts the file names that are used.</span></span>

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p><span data-ttu-id="56227-116">Операционная система</span><span class="sxs-lookup"><span data-stu-id="56227-116">Operating System</span></span></p>
    </th>
    <th>
      <p><span data-ttu-id="56227-117">Windows Server 2003 и более ранние версии</span><span class="sxs-lookup"><span data-stu-id="56227-117">Windows Server 2003 and earlier</span></span><br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p><span data-ttu-id="56227-118">Windows Vista и более поздние версии (клиент)</span><span class="sxs-lookup"><span data-stu-id="56227-118">Windows Vista and later (client)</span></span> <br />
<span data-ttu-id="56227-119">Windows Server 2008 и более поздние версии (сервер)</span><span class="sxs-lookup"><span data-stu-id="56227-119">Windows Server 2008 and later (server)</span></span>
</p>
    </th>
    <th>
      <p><span data-ttu-id="56227-120">Юбилейное обновление Windows 10 и более поздние версии (клиент)</span><span class="sxs-lookup"><span data-stu-id="56227-120">Windows 10 Anniversary Update and later (client)</span></span> <br />
<span data-ttu-id="56227-121">Windows Server 2016 и более поздние версии (сервер)</span><span class="sxs-lookup"><span data-stu-id="56227-121">Windows Server 2016 and later (server)</span></span>
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="56227-122">
        <strong>Параметр JET_paramLegacyNames</strong>
      </span><span class="sxs-lookup"><span data-stu-id="56227-122">
        <strong>JET_paramLegacyNames setting</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-123">
        <strong>Н/Д</strong>
      </span><span class="sxs-lookup"><span data-stu-id="56227-123">
        <strong>N/A</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-124">
        <strong>None</strong>
      </span><span class="sxs-lookup"><span data-stu-id="56227-124">
        <strong>None</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-125">
        <strong>JET_bitESE98FileNames</strong>
      </span><span class="sxs-lookup"><span data-stu-id="56227-125">
        <strong>JET_bitESE98FileNames</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-126">
        <strong>То же, что и Windows Vista/Server 2008</strong>
      </span><span class="sxs-lookup"><span data-stu-id="56227-126">
        <strong>Same as Windows Vista/Server 2008</strong>
      </span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="56227-127">Текущий журнал</span><span class="sxs-lookup"><span data-stu-id="56227-127">Current Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-128">&lt;inst &gt; . log</span><span class="sxs-lookup"><span data-stu-id="56227-128">&lt;inst&gt;.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-129">&lt;inst &gt; . жткс</span><span class="sxs-lookup"><span data-stu-id="56227-129">&lt;inst&gt;.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-130">&lt;inst &gt; . log</span><span class="sxs-lookup"><span data-stu-id="56227-130">&lt;inst&gt;.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="56227-131">Журнал предварительной инициализации</span><span class="sxs-lookup"><span data-stu-id="56227-131">Pre-Init Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-132">&lt;inst &gt; tmp. log</span><span class="sxs-lookup"><span data-stu-id="56227-132">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-133">&lt;inst &gt; tmp. жткс</span><span class="sxs-lookup"><span data-stu-id="56227-133">&lt;inst&gt;tmp.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-134">&lt;inst &gt; tmp. log</span><span class="sxs-lookup"><span data-stu-id="56227-134">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="56227-135">Повернутые журналы</span><span class="sxs-lookup"><span data-stu-id="56227-135">Rotated Logs</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-136">&lt;inst &gt; XXXXX. log</span><span class="sxs-lookup"><span data-stu-id="56227-136">&lt;inst&gt;XXXXX.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-137">&lt;inst &gt; XXXXX. жткс после FFFFF переключается на &lt; inst &gt; XXXXXXXX. жткс</span><span class="sxs-lookup"><span data-stu-id="56227-137">&lt;inst&gt;XXXXX.jtx after FFFFF switch to &lt;inst&gt;XXXXXXXX.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-138">&lt;inst &gt; XXXXX. log после переключения FFFFF в &lt; inst &gt; XXXXXXXX. log.</span><span class="sxs-lookup"><span data-stu-id="56227-138">&lt;inst&gt;XXXXX.log after FFFFF switch to &lt;inst&gt;XXXXXXXX.log.</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="56227-139">
        <a href="gg294069(v=exchg.10).md">Файлы контрольных точек</a>
      </span><span class="sxs-lookup"><span data-stu-id="56227-139">
        <a href="gg294069(v=exchg.10).md">Checkpoint Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-140">&lt;inst &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="56227-140">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-141">&lt;inst &gt; . жкп</span><span class="sxs-lookup"><span data-stu-id="56227-141">&lt;inst&gt;.jcp</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-142">&lt;inst &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="56227-142">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="56227-143">
        <a href="gg294069(v=exchg.10).md">Временные базы данных</a>
      </span><span class="sxs-lookup"><span data-stu-id="56227-143">
        <a href="gg294069(v=exchg.10).md">Temporary Databases</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-144">&lt;имя файла временной базы данных &gt; по умолчанию: TMP. edb</span><span class="sxs-lookup"><span data-stu-id="56227-144">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-145">&lt;имя файла временной базы данных &gt; по умолчанию: TMP. edb</span><span class="sxs-lookup"><span data-stu-id="56227-145">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-146">&lt;имя файла временной базы данных &gt; по умолчанию: TMP. edb</span><span class="sxs-lookup"><span data-stu-id="56227-146">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="56227-147">
        <a href="gg294069(v=exchg.10).md">Зарезервированные файлы журнала транзакций</a>
      </span><span class="sxs-lookup"><span data-stu-id="56227-147">
        <a href="gg294069(v=exchg.10).md">Reserved Transaction Log Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-148">Res1. log &amp; Res2. log</span><span class="sxs-lookup"><span data-stu-id="56227-148">res1.log &amp; res2.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-149">&lt;inst &gt; рескскскскскс. ЖРС</span><span class="sxs-lookup"><span data-stu-id="56227-149">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
    <td colspan="2">
      <p><span data-ttu-id="56227-150">&lt;inst &gt; рескскскскскс. ЖРС</span><span class="sxs-lookup"><span data-stu-id="56227-150">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="56227-151">
        <a href="gg294069(v=exchg.10).md">Файлы базы данных</a>
      </span><span class="sxs-lookup"><span data-stu-id="56227-151">
        <a href="gg294069(v=exchg.10).md">Database Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-152">&lt;имя файла базы данных&gt;</span><span class="sxs-lookup"><span data-stu-id="56227-152">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-153">&lt;имя файла базы данных&gt;</span><span class="sxs-lookup"><span data-stu-id="56227-153">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-154">&lt;имя файла базы данных&gt;</span><span class="sxs-lookup"><span data-stu-id="56227-154">&lt;db file name&gt;</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="56227-155">
        <a href="gg294069(v=exchg.10).md">Очистить файлы карт</a>
      </span><span class="sxs-lookup"><span data-stu-id="56227-155">
        <a href="gg294069(v=exchg.10).md">Flush Map Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-156">Н/Д</span><span class="sxs-lookup"><span data-stu-id="56227-156">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-157">Н/Д</span><span class="sxs-lookup"><span data-stu-id="56227-157">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-158">Н/Д</span><span class="sxs-lookup"><span data-stu-id="56227-158">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="56227-159">&lt;имя файла базы данных без расширения &gt; . жфм</span><span class="sxs-lookup"><span data-stu-id="56227-159">&lt;db file name without extension&gt;.jfm</span></span></p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a><span data-ttu-id="56227-160">Файлы журнала транзакций</span><span class="sxs-lookup"><span data-stu-id="56227-160">Transaction Log Files</span></span>

<span data-ttu-id="56227-161">Файлы журнала транзакций содержат операции с файлами базы данных.</span><span class="sxs-lookup"><span data-stu-id="56227-161">Transaction log files contain operations on database files.</span></span> <span data-ttu-id="56227-162">Они содержат достаточно информации для перевода базы данных в логически целостное состояние после непредвиденного завершения процесса или завершения работы системы.</span><span class="sxs-lookup"><span data-stu-id="56227-162">They contain enough information to bring a database to a logically consistent state after an unexpected process termination or system shutdown.</span></span>

<span data-ttu-id="56227-163">Имена файлов журнала зависят от имени из трех букв, которое можно задать с помощью [JET_paramBaseName](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="56227-163">The names of the log files are dependent on a three-letter base name, which can be set with [JET_paramBaseName](./transaction-log-parameters.md).</span></span> <span data-ttu-id="56227-164">В приведенных ниже примерах используется базовое имя EDB, так как это базовое имя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="56227-164">The examples below use a base name of "edb", because that is the default base name.</span></span> <span data-ttu-id="56227-165">Расширение для файлов журнала транзакций будет иметь тип. log или. жткс в зависимости от того, задан ли JET_bitESE98FileNames в параметре JET_paramLegacyFileNames.</span><span class="sxs-lookup"><span data-stu-id="56227-165">The extension for the transaction log files will be either .log or .jtx depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter.</span></span> <span data-ttu-id="56227-166">Дополнительные сведения см. в разделе [Расширенные параметры подсистемы хранилища](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="56227-166">For more information, see [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="56227-167">Файлы журнала транзакций имеют имя \<base\> \<generation-number\> . log, начинающееся с 1.</span><span class="sxs-lookup"><span data-stu-id="56227-167">Transaction log files are named \<base\>\<generation-number\>.log, beginning with 1.</span></span> <span data-ttu-id="56227-168">Номер создания журнала имеет шестнадцатеричный формат.</span><span class="sxs-lookup"><span data-stu-id="56227-168">The log generation number is in hexadecimal format.</span></span> <span data-ttu-id="56227-169">Например, Edb00001. log — это первый журнал, а edb000ff. log — журнал 255th.</span><span class="sxs-lookup"><span data-stu-id="56227-169">For example, edb00001.log is the first log, and edb000ff.log is the 255th log.</span></span> <span data-ttu-id="56227-170">Файлы журнала содержат пять шестнадцатеричных цифр в имени файла журнала, пока не будет создан файл журнала 1048576th, после чего файлы журнала начинают называться в формате 11,3 (например, edb00100000. log).</span><span class="sxs-lookup"><span data-stu-id="56227-170">The log files have five hexadecimal digits in the log file name, until the 1048576th log file, at which point the log files start being named in an 11.3 format (for example, edb00100000.log).</span></span> <span data-ttu-id="56227-171">\<base\>. log всегда является файлом журнала, который используется в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="56227-171">\<base\>.log is always the log file that is currently being used.</span></span> <span data-ttu-id="56227-172">Если ядро СУБД неактивно, можно определить поколение EDB. log с помощью следующей команды: **esentutl.exe-ML EDB. log**.</span><span class="sxs-lookup"><span data-stu-id="56227-172">If the database engine is not active, the generation of edb.log can be identified using the following command: **esentutl.exe -ml edb.log**.</span></span>

<span data-ttu-id="56227-173">Хотя файлы журнала транзакций имеют. Расширение журнала, обычно связанное с текстовыми файлами, файлы журнала транзакций имеют двоичный формат и никогда не должны редактироваться пользователем. Операции с базой данных записываются в журнал первыми.</span><span class="sxs-lookup"><span data-stu-id="56227-173">Although transaction log files have the .LOG extension commonly associated with text files, transaction log files are in a binary format and should never be edited by a user.Database operations are written to the log first.</span></span> <span data-ttu-id="56227-174">Данные могут быть записаны в файл базы данных позднее; возможно, немедленно, возможно, будет намного позже.</span><span class="sxs-lookup"><span data-stu-id="56227-174">The data can be written to the database file later; possibly immediately, potentially much later.</span></span> <span data-ttu-id="56227-175">В случае непредвиденного завершения процесса или прекращения работы системы операции по-прежнему находятся в файлах журнала, и можно выполнить откат незавершенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="56227-175">In the event of unexpected process or system termination, the operations are still present in the log files, and incomplete transactions can be rolled back.</span></span> <span data-ttu-id="56227-176">Процесс воспроизведения файлов журнала транзакций называется *мягким восстановлением* и выполняется автоматически при вызове [жетинит](./jetinit-function.md) или [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="56227-176">The act of replaying transaction log files is called *soft recovery*, and it is done automatically when [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md) is called.</span></span> <span data-ttu-id="56227-177">Мягкое восстановление также можно выполнить вручную с помощью параметра "-r" программы Esentutl.exe.</span><span class="sxs-lookup"><span data-stu-id="56227-177">Soft recovery can also be performed manually with the "-r" option of the Esentutl.exe program.</span></span> <span data-ttu-id="56227-178">Процесс воспроизведения файлов журнала транзакций в базе данных, восстановленной из резервной копии, называется *жесткое восстановление*.</span><span class="sxs-lookup"><span data-stu-id="56227-178">The act of replaying transaction log files on a database that is restored from a backup is called *hard recovery*.</span></span>

<span data-ttu-id="56227-179">Файлы журнала имеют фиксированный размер, настраиваемый с помощью [JET_paramLogFileSize](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="56227-179">Log files are of a fixed size, customizable with [JET_paramLogFileSize](./transaction-log-parameters.md).</span></span> <span data-ttu-id="56227-180">Когда текущий файл журнала (EDB. log) заполняется, он переименовывается в \<base\> \<generation-number\> . log, а новый файл журнала транзакций необходим в потоке журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="56227-180">When the current log file (that is, edb.log) gets filled, it gets renamed to \<base\>\<generation-number\>.log, and a new transaction log file is needed in the transaction log stream.</span></span>

<span data-ttu-id="56227-181">С каждым экземпляром базы данных связана одна последовательность файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="56227-181">Each database instance has a single log file sequence associated with it.</span></span> <span data-ttu-id="56227-182">В Windows XP появился [жеткреатеинстанце](./jetcreateinstance-function.md), что позволяет одному процессу использовать несколько последовательностей файлов журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="56227-182">Windows XP introduced [JetCreateInstance](./jetcreateinstance-function.md), allowing multiple transaction log file sequences to be used by a single process.</span></span> <span data-ttu-id="56227-183">Однако несколько последовательностей файлов журнала транзакций не могут существовать в одном каталоге.</span><span class="sxs-lookup"><span data-stu-id="56227-183">Multiple transaction log file sequences cannot exist in the same directory, however.</span></span>

<span data-ttu-id="56227-184">Файлы журнала транзакций не следует менять, переименовывать, перемещать или удалять вручную, так как это может привести к повреждению данных.</span><span class="sxs-lookup"><span data-stu-id="56227-184">Transaction log files should almost never be manually manipulated, renamed, moved, or deleted because data corruption can result.</span></span>

<span data-ttu-id="56227-185">Файлы журнала транзакций будут удалены ядром СУБД во время полной архивации (см. раздел [жетбаккуп](./jetbackup-function.md), [жеттрункателог](./jettruncatelog-function.md), [жеттрункателогинстанце](./jettruncateloginstance-function.md)) или во время нормальной работы, если циклическое ведение журнала включено.</span><span class="sxs-lookup"><span data-stu-id="56227-185">Transaction log files will be deleted by the database engine during a full backup (see [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)), or during normal operations, if circular logging is enabled.</span></span>

<span data-ttu-id="56227-186">После заполнения файла журнала транзакций ядру СУБД необходимо создать новый файл журнала.</span><span class="sxs-lookup"><span data-stu-id="56227-186">After a transaction log file is filled up, the database engine needs to create a new log file.</span></span> <span data-ttu-id="56227-187">Циклическое ведение журнала — это способ, с помощью которого ядро СУБД может автоматически очищать файлы журналов, если они больше не требуются для восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="56227-187">Circular logging is a means by which log files can be automatically cleaned up by the database engine when they are no longer required for crash recovery.</span></span> <span data-ttu-id="56227-188">Этот процесс является альтернативой удалению файлов журнала в ходе выполнения резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="56227-188">This process is an alternative to removing log files as a by-product of performing a backup.</span></span> <span data-ttu-id="56227-189">Циклическое ведение журнала можно контролировать с помощью системного параметра [JET_paramCircularLog](./transaction-log-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="56227-189">Circular logging can be controlled with the [JET_paramCircularLog](./transaction-log-parameters.md) system parameter.</span></span> <span data-ttu-id="56227-190">Файлы журнала транзакций не следует удалять с помощью любого другого метода.</span><span class="sxs-lookup"><span data-stu-id="56227-190">Transaction log files should not be deleted using any other method.</span></span>

### <a name="temporary-transaction-log-files"></a><span data-ttu-id="56227-191">Временные файлы журналов транзакций</span><span class="sxs-lookup"><span data-stu-id="56227-191">Temporary Transaction Log Files</span></span>

<span data-ttu-id="56227-192">Когда EDB. log заполняется, ESE необходимо создать новый файл.</span><span class="sxs-lookup"><span data-stu-id="56227-192">When edb.log fills up, ESE needs to create a new file.</span></span> <span data-ttu-id="56227-193">Новый файл транзакций журнала называется временным файлом журнала транзакций до его использования ESE.</span><span class="sxs-lookup"><span data-stu-id="56227-193">The new log transaction file is known as a temporary transaction log file prior to its use by ESE.</span></span>

<span data-ttu-id="56227-194">Во время создания нового файла журнала и его размера он будет называться \<base\> tmp. log.</span><span class="sxs-lookup"><span data-stu-id="56227-194">While a new log file is created and its size extended, it will be called \<base\>tmp.log.</span></span> <span data-ttu-id="56227-195">Создание нового файла может быть потенциально дорогостоящей операцией, поэтому ESE создаст следующий файл журнала в режиме «в фоновом задании».</span><span class="sxs-lookup"><span data-stu-id="56227-195">Creating a new file can be a potentially costly operation, so ESE will create the next log file proactively as a background task.</span></span>

<span data-ttu-id="56227-196">Поскольку временный файл журнала транзакций создается с учетом необходимости создания нового файла журнала транзакций, он не содержит никаких полезных сведений.</span><span class="sxs-lookup"><span data-stu-id="56227-196">Because the temporary transaction log file is created in anticipation of need for a new transaction log file, it does not contain any useful information.</span></span>

### <a name="reserved-transaction-log-files"></a><span data-ttu-id="56227-197">Зарезервированные файлы журнала транзакций</span><span class="sxs-lookup"><span data-stu-id="56227-197">Reserved Transaction Log Files</span></span>

<span data-ttu-id="56227-198">Зарезервированные файлы журнала транзакций создаются, когда подсистема начинает регистрировать важные операции, чтобы получить чистое завершение работы.</span><span class="sxs-lookup"><span data-stu-id="56227-198">The reserved transaction log files are created when the engine starts to allow important operations to be logged to get a clean shutdown.</span></span>

<span data-ttu-id="56227-199">**Windows Vista:** В Windows Vista и более поздних версиях зарезервированные файлы журнала транзакций имеют имя \<base\> рескскскскскс. ЖРС.</span><span class="sxs-lookup"><span data-stu-id="56227-199">**Windows Vista:** In Windows Vista and later, the Reserved Transaction Log Files are named \<base\>RESXXXXX.jrs.</span></span>

<span data-ttu-id="56227-200">**Windows Server 2003:** В Windows Server 2003 и более ранних версиях зарезервированные файлы журнала транзакций имеют имена Res1. log и Res2. log.</span><span class="sxs-lookup"><span data-stu-id="56227-200">**Windows Server 2003:** In Windows Server 2003 and earlier, The Reserved Transaction Log Files are named res1.log and res2.log.</span></span>

<span data-ttu-id="56227-201">В случае нехватки места на диске для ядра СУБД невозможно создать новый файл журнала.</span><span class="sxs-lookup"><span data-stu-id="56227-201">When the database engine runs out of disk space it cannot create a new log file.</span></span> <span data-ttu-id="56227-202">Самый надежный способ — завершить работу аккуратно, но некоторые операции (например, операции отката) все еще должны быть зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="56227-202">The safest thing to do is to shut down cleanly, but some operations (such as rollback operations) must still be logged.</span></span> <span data-ttu-id="56227-203">На этом этапе большинство операций с базами данных завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="56227-203">Most database operations will fail during this stage.</span></span>

<span data-ttu-id="56227-204">Поскольку зарезервированные файлы журнала транзакций создаются с учетом необходимости использования файлов журнала транзакций в сценарии нехватки дискового пространства, они не содержат полезных сведений.</span><span class="sxs-lookup"><span data-stu-id="56227-204">Because the reserved transaction log files are created in anticipation of need for transaction log files in an out-of-disk scenario, they do not contain any useful information.</span></span>

### <a name="checkpoint-files"></a><span data-ttu-id="56227-205">файлы контрольных точек</span><span class="sxs-lookup"><span data-stu-id="56227-205">Checkpoint Files</span></span>

<span data-ttu-id="56227-206">Файл контрольных точек хранит контрольную точку для определенной последовательности файлов журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="56227-206">The checkpoint file stores the checkpoint for a particular transaction log file sequence.</span></span> <span data-ttu-id="56227-207">Файл контрольных точек называется \<base\> CHK или \<base\> жкп, в зависимости от того, задан ли JET_bitESE98FileNames в параметре JET_paramLegacyFileNames, а его расположение задается [JET_paramSystemPath](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="56227-207">The checkpoint file is named \<base\>.chk or \<base\>.jcp, depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter, and its location is given by [JET_paramSystemPath](./transaction-log-parameters.md).</span></span>

<span data-ttu-id="56227-208">Операции базы данных сначала записываются в файлы журнала, а затем кэшируются в памяти.</span><span class="sxs-lookup"><span data-stu-id="56227-208">Database operations are first written to the log files and then cached in memory.</span></span> <span data-ttu-id="56227-209">В более поздней точке операции записываются в файл базы данных, но по соображениям производительности порядок записи операций в файл базы данных может отличаться от порядка, в котором они были изначально зарегистрированы.</span><span class="sxs-lookup"><span data-stu-id="56227-209">At some later point, the operations get written to the database file, but for performance reasons, the order in which operations are written to the database file might not match the order in which they were originally logged.</span></span> <span data-ttu-id="56227-210">Операции, записанные в файл журнала транзакций, будут находиться в одном из двух состояний:</span><span class="sxs-lookup"><span data-stu-id="56227-210">Operations written to the transaction log file will be in one of two states:</span></span>

  - <span data-ttu-id="56227-211">Записывается в файл журнала транзакций и в файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="56227-211">Written to the transaction log file and the database file.</span></span>

  - <span data-ttu-id="56227-212">Записывается в файл журнала транзакций и еще не записывается в файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="56227-212">Written to the transaction log file and not yet written to the database file.</span></span>

<span data-ttu-id="56227-213">Многие операции с базами данных могут храниться в одном файле журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="56227-213">Many database operations can be stored in a single transaction log file.</span></span> <span data-ttu-id="56227-214">Данный файл журнала может состоять из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="56227-214">A given log file can consist of the following items:</span></span>

  - <span data-ttu-id="56227-215">Все операции, записанные в файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="56227-215">All operations written to the database file.</span></span>

  - <span data-ttu-id="56227-216">Нет операций, записанных в файл базы данных</span><span class="sxs-lookup"><span data-stu-id="56227-216">No operations written to the database file</span></span>

  - <span data-ttu-id="56227-217">Сочетание операций, записанных в файл базы данных, и операций, которые еще не записаны в файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="56227-217">A mix of operations written to the database file and operations not yet written to the database file.</span></span>

<span data-ttu-id="56227-218">Контрольная точка относится к моменту времени в потоке журнала транзакций, где все операции до контрольной точки записываются в файл базы данных.</span><span class="sxs-lookup"><span data-stu-id="56227-218">The checkpoint refers to the point in time in the transaction log stream where all operations prior to the checkpoint have been written to the database file.</span></span> <span data-ttu-id="56227-219">Нет никакой гарантии на операции, выполняемые после создания контрольной точки. Некоторые могут быть в памяти, а некоторые могут быть записаны в базу данных.</span><span class="sxs-lookup"><span data-stu-id="56227-219">There is no guarantee about the operations that occur after the checkpoint; some might be in memory, and some might be written to the database.</span></span>

<span data-ttu-id="56227-220">Так как все операции в файлах журнала до контрольной точки представлены в файле базы данных, для мягкого восстановления требуется только файлы журнала транзакций после контрольной точки, чтобы перевести определенную базу данных в чистое состояние.</span><span class="sxs-lookup"><span data-stu-id="56227-220">Since all the operations in the log files prior to the checkpoint are represented in the database file, only the transaction log files after the checkpoint are needed for soft recovery to bring a particular database into a clean state.</span></span>

### <a name="database-files"></a><span data-ttu-id="56227-221">Файлы базы данных</span><span class="sxs-lookup"><span data-stu-id="56227-221">Database Files</span></span>

<span data-ttu-id="56227-222">Файл базы данных содержит схему для всех таблиц в базе данных, записи для всех таблиц в базе данных и индексы по таблицам.</span><span class="sxs-lookup"><span data-stu-id="56227-222">The database file contains the schema for all of the tables in the database, the records for all of the tables in the database, and the indexes over the tables.</span></span> <span data-ttu-id="56227-223">Его расположение задается с помощью [жеткреатедатабасе](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [жетаттачдатабасе](./jetattachdatabase-function.md)или [JetAttachDatabase2](./jetattachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="56227-223">Its location is given using [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md), or [JetAttachDatabase2](./jetattachdatabase2-function.md).</span></span>

<span data-ttu-id="56227-224">После успешного вызова [жеттерм](./jetterm-function.md) или [JetTerm2](./jetterm2-function.md)база данных завершает работу в чистом виде.</span><span class="sxs-lookup"><span data-stu-id="56227-224">A database is cleanly shut down only after a successful call to [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="56227-225">Программа Esentutl.exe может определить, завершается ли работа базы данных с помощью параметра "-MH".</span><span class="sxs-lookup"><span data-stu-id="56227-225">The Esentutl.exe program can detect whether a database is shut down cleanly with the "-mh" option.</span></span> <span data-ttu-id="56227-226">Например, "esentutl.exe-MH Sample. edb" будет считывать заголовок базы данных с именем Sample. edb и выводить сведения о состоянии Sample. edb.</span><span class="sxs-lookup"><span data-stu-id="56227-226">For example, "esentutl.exe -mh sample.edb" will read the database header of a database named sample.edb, and print out the state of sample.edb.</span></span> <span data-ttu-id="56227-227">Он может вывести на печать состояние: чистое завершение работы или состояние: "грязное" завершение работы.</span><span class="sxs-lookup"><span data-stu-id="56227-227">It may print out "State: Clean Shutdown" or "State: Dirty Shutdown".</span></span>

<span data-ttu-id="56227-228">База данных, которая не была завершена аккуратно, находится в состоянии "неправильное завершение работы".</span><span class="sxs-lookup"><span data-stu-id="56227-228">A database that has not been cleanly shut down is in a dirty shutdown state.</span></span> <span data-ttu-id="56227-229">До выхода Windows XP это состояние было вызвано *несоответствующим*.</span><span class="sxs-lookup"><span data-stu-id="56227-229">Prior to Windows XP, this state was called *inconsistent*.</span></span> <span data-ttu-id="56227-230">"Грязную" (ненепротиворечивую) базу данных можно вернуть в исходное состояние с мягким восстановлением.</span><span class="sxs-lookup"><span data-stu-id="56227-230">A dirty (inconsistent) database can be brought to a clean state with soft recovery.</span></span> <span data-ttu-id="56227-231">Поврежденная база данных не совпадает с «грязной» («непротиворечивой») базой данных.</span><span class="sxs-lookup"><span data-stu-id="56227-231">A corrupt database is not the same as a dirty ("inconsistent") database.</span></span>

<span data-ttu-id="56227-232">Поврежденная база данных относится к физическому или логическому повреждению и не может быть исправлена с помощью мягкого восстановления.</span><span class="sxs-lookup"><span data-stu-id="56227-232">A corrupt database refers to a physical or logical corruption, and cannot be fixed with soft recovery.</span></span> <span data-ttu-id="56227-233">Физические повреждения могут быть отражены в битах, что часто будет перехватываться контрольными суммами на страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="56227-233">Physical corruptions can be bit flips, which will frequently be caught by the checksums on the database pages.</span></span> <span data-ttu-id="56227-234">Неудачная контрольная сумма в файле базы данных сама по себе является JET_errReadVerifyFailure ошибкой.</span><span class="sxs-lookup"><span data-stu-id="56227-234">A failed checksum in a database file manifests itself as a JET_errReadVerifyFailure error.</span></span>

<span data-ttu-id="56227-235">Только аккуратное завершение работы баз данных может быть безопасно перемещено или переименовано.</span><span class="sxs-lookup"><span data-stu-id="56227-235">Only cleanly shut down databases can be safely moved around or renamed.</span></span> <span data-ttu-id="56227-236">Если база данных не была корректно завершена, она не может быть автоматически перемещена или переименована.</span><span class="sxs-lookup"><span data-stu-id="56227-236">If a database was not cleanly shut down, it cannot be automatically safely moved or renamed.</span></span>

<span data-ttu-id="56227-237">Несколько баз данных могут быть связаны с одной последовательностью файлов журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="56227-237">Multiple databases can be associated with a single transaction log file sequence.</span></span>

### <a name="temporary-databases"></a><span data-ttu-id="56227-238">Временные базы данных</span><span class="sxs-lookup"><span data-stu-id="56227-238">Temporary Databases</span></span>

<span data-ttu-id="56227-239">Временная база данных используется в качестве резервного хранилища для темптаблес, а также используется при создании индексов.</span><span class="sxs-lookup"><span data-stu-id="56227-239">The temporary database is used as a backing store for temptables and it is also used when creating indices.</span></span>

<span data-ttu-id="56227-240">Имя и расположение настраиваются с помощью [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="56227-240">The name and location is configured with [JET_paramTempPath](./temporary-database-parameters.md).</span></span>

<span data-ttu-id="56227-241">Темптаблес создаются с помощью [жетопентемптабле](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [жетопентемпораритабле](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="56227-241">Temptables are created with [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span> <span data-ttu-id="56227-242">Они также создаются некоторыми вызовами API и используются для возврата сведений о схеме (например, [жетжетиндексинфо](./jetgetindexinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="56227-242">They are also created by some API calls and used to return schema information (such as [JetGetIndexInfo](./jetgetindexinfo-function.md)).</span></span>

## <a name="flush-map-files"></a><span data-ttu-id="56227-243">Очистить файлы карт</span><span class="sxs-lookup"><span data-stu-id="56227-243">Flush Map Files</span></span>

<span data-ttu-id="56227-244">Начиная с юбилея Windows 10 юбилейное обновление (клиент) и Windows Server 2016 (сервер), подсистема ESE добавила дополнительный уровень защиты от потерянных операций записи (или потерянных сбросов) 1, что позволяет ей обнаруживать такие события, initialization2 перекрестной обработки.</span><span class="sxs-lookup"><span data-stu-id="56227-244">Starting with the Windows 10 Anniversary Update (client) and Windows Server 2016 (server), ESE added an additional level of protection against lost writes (or lost flushes) 1, allowing it to detect such events cross-process re-initialization2.</span></span> <span data-ttu-id="56227-245">Эта функция требует сохранения метаданных в отдельном файле, который называется "дисковой картой".</span><span class="sxs-lookup"><span data-stu-id="56227-245">This feature requires persisting metadata to a separate file called a "flush map" file.</span></span>

<span data-ttu-id="56227-246">Для каждого файла базы данных создается один файл для записи на диск, который находится в том же каталоге.</span><span class="sxs-lookup"><span data-stu-id="56227-246">One flush map file is created for each database file, and is located in the same directory.</span></span> <span data-ttu-id="56227-247">Имя файла аналогично имени файла базы данных, но с другим расширением.</span><span class="sxs-lookup"><span data-stu-id="56227-247">The file is named similarly to the database file, but with a different extension.</span></span> <span data-ttu-id="56227-248">Например, если клиентское приложение создает базу данных с полным путем C: \\ MyDirectory \\ мидабатасе. edb, соответствующий файл записи на диск с файлом отображения имеет значение C: \\ MyDirectory \\ мидабатасе. жфм.</span><span class="sxs-lookup"><span data-stu-id="56227-248">For example, if the client application creates a database with the full path C:\\MyDirectory\\MyDabatase.edb, its corresponding flush map file is C:\\MyDirectory\\MyDabatase.jfm.</span></span>

<span data-ttu-id="56227-249">В этом усовершенствовании представлены два требования к именам файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="56227-249">This enhancement introduces two requirements for how database files must be named:</span></span>

  - <span data-ttu-id="56227-250">Две базы данных в одном каталоге не должны иметь одинаковые имена файлов с разными расширениями.</span><span class="sxs-lookup"><span data-stu-id="56227-250">Two databases in the same directory must not have the same filename with different extensions.</span></span> <span data-ttu-id="56227-251">Например: C: \\ MyDirectory \\ мидабатасе. DB1 и C: \\ MyDirectory \\ мидабатасе. DB2.</span><span class="sxs-lookup"><span data-stu-id="56227-251">For example: C:\\MyDirectory\\MyDabatase.db1 and C:\\MyDirectory\\MyDabatase.db2.</span></span>

  - <span data-ttu-id="56227-252">2\.</span><span class="sxs-lookup"><span data-stu-id="56227-252">2\.</span></span> <span data-ttu-id="56227-253">База данных не должна иметь расширение жфм.</span><span class="sxs-lookup"><span data-stu-id="56227-253">A database must not have a .jfm extension.</span></span>

<span data-ttu-id="56227-254">При копировании или перемещении файла базы данных вручную соответствующий файл с картой на диск должен быть также скопирован или перемещен в тот же целевой каталог.</span><span class="sxs-lookup"><span data-stu-id="56227-254">When you manually copy or move a database file, its corresponding flush map file should also be, respectively, copied or moved to the same destination directory.</span></span> <span data-ttu-id="56227-255">Если файл с картой записи на диск отсутствует во время нового вложения базы данных (через [жетаттачдатабасе](./jetattachdatabase-function.md), новый экземпляр будет создан и повторно заполнен по запросу по мере считывания страниц из базы данных.</span><span class="sxs-lookup"><span data-stu-id="56227-255">If a flush map file is not present at the time of a new database attachment (via [JetAttachDatabase](./jetattachdatabase-function.md), a new one will be created and re-populated on-demand as pages are read in from the database.</span></span> <span data-ttu-id="56227-256">При смешивании несовпадающих файлов базы данных и файла сопоставлений дисковых карт подсистема ESE выполняет принудительное удаление и повторное создание несовпадающей схемы записи на диск с нуля.</span><span class="sxs-lookup"><span data-stu-id="56227-256">Mixing mismatching database and flush map files is handled by ESE, and forces the mismatched flush map to be deleted and re-created from scratch.</span></span>

<span data-ttu-id="56227-257">Размер файла на карте записи прямо пропорционален размеру связанного файла базы данных и приблизительно равен (все размеры в байтах, результат должен округляться до следующего числа, кратного 8 192):</span><span class="sxs-lookup"><span data-stu-id="56227-257">The size of a flush map file is directly proportional to its associated database file and approximately equal to (all sizes in bytes, result must be rounded up to the next multiple of 8,192):</span></span>

`8,192 + ((<database file size> / <database page size>) / 4)`

<span data-ttu-id="56227-258">Например: для базы данных размером 1,5 ГБ, использующей размер страницы 32 КБ, приблизительный размер схемы записи на диск составляет 24 576 байт (или 24KB).</span><span class="sxs-lookup"><span data-stu-id="56227-258">For example: for a 1.5GB database using a 32KB page size, the approximate size of the flush map is 24,576 bytes (or 24KB).</span></span>

<span data-ttu-id="56227-259">Файл отображения на диск должен быть обновлен, так как страницы базы данных сбрасываются.</span><span class="sxs-lookup"><span data-stu-id="56227-259">The flush map file needs to be refreshed as database pages are flushed.</span></span> <span data-ttu-id="56227-260">Если включено ведение журнала транзакций (например, [JET_paramRecovery](./transaction-log-parameters.md) задано значение "on", значение по умолчанию), обновление схемы очистки выполняется по мере внесения изменений в базу данных клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="56227-260">If transactional logging is enabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "on", the default), refreshing the flush map is performed as the client application makes modifications to the database.</span></span> <span data-ttu-id="56227-261">В среднем вся схема очистки записывается на носитель с энергонезависимым по одному разу для каждых 20% [JET_paramCheckpointDepthMax](./database-cache-parameters.md) (в байтах) создаваемых журналов транзакций.</span><span class="sxs-lookup"><span data-stu-id="56227-261">On average, the entire flush map is written to the non-volatile media once for every 20% of [JET_paramCheckpointDepthMax](./database-cache-parameters.md) -worth (in bytes) of transactional logs generated.</span></span> <span data-ttu-id="56227-262">Количество операций записи зависит от того, насколько распределены изменения в пределах базы данных.</span><span class="sxs-lookup"><span data-stu-id="56227-262">The number of write operations depends on how distributed throughout the database the modifications are.</span></span> <span data-ttu-id="56227-263">Но в большинстве случаев приблизительно (все размеры в байтах):</span><span class="sxs-lookup"><span data-stu-id="56227-263">But it is at most, approximately (all sizes in bytes):</span></span>

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

<span data-ttu-id="56227-264">Если ведение журнала транзакций отключено (например, [JET_paramRecovery](./transaction-log-parameters.md) установлен в значение OFF), то схема записи на диск обновляется только один раз, когда база данных явно отсоединяется явным образом (через [жетдетачдатабасе](./jetdetachdatabase-function.md)или неявно отключается в явном виде путем завершения связанного экземпляра ESE (через любую функцию [жеттерм](./jetterm-function.md) , если [JET_bitTermDirty](./jetterm2-function.md) не передается).</span><span class="sxs-lookup"><span data-stu-id="56227-264">If transactional logging is disabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "off"), the flush map gets refreshed only once when the database is explicitly detached cleanly (via [JetDetachDatabase](./jetdetachdatabase-function.md), or implicitly detached cleanly by terminating its associated ESE instance (via any of the [JetTerm](./jetterm-function.md) functions, as long as [JET_bitTermDirty](./jetterm2-function.md) is not passed).</span></span>

<span data-ttu-id="56227-265">1 потерянная запись (или потерянная очистка) определяется как операция записи, которая успешно возвращает данные из операционной системы в ядро базы данных ESE, но фактических данных они никогда не сохраняются в файле базы данных на носителе с энергонезависимым.</span><span class="sxs-lookup"><span data-stu-id="56227-265">1 A lost write (or lost flush) is defined as a write operation that returns successfully from the operating system to the ESE database engine but the actual data never gets persisted to the database file in the non-volatile media.</span></span> <span data-ttu-id="56227-266">Обычно это вызвано неправильной или неправильно настроенным стеком хранилища (программное обеспечение или оборудование).</span><span class="sxs-lookup"><span data-stu-id="56227-266">It is usually caused by a malfunctioning or misconfigured storage stack (software or hardware).</span></span> <span data-ttu-id="56227-267">Клиентские приложения могут получить ошибку [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) от функций ESE, требующих считывание данных из базы данных, если данные находятся в регионе, в котором произошло потеря события записи.</span><span class="sxs-lookup"><span data-stu-id="56227-267">Client applications may receive a [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) error from ESE functions that require reading data from the database if the data is located in a region that underwent a lost write event.</span></span>

<span data-ttu-id="56227-268">2 возможность обнаружения потерянных операций записи в течение всего времени существования процесса существует с момента выпуска Windows 8 (Client) и Windows Server 2012 (сервер).</span><span class="sxs-lookup"><span data-stu-id="56227-268">2 The ability to detect lost writes within a process's lifetime has been present since Windows 8 (client) and Windows Server 2012 (server).</span></span>
