---
description: SymStore (symstore.exe) — это инструмент для создания хранилищ символов. Он включен в пакет средств отладки для Windows.
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: Использование SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141527"
---
# <a name="using-symstore"></a><span data-ttu-id="362c6-104">Использование SymStore</span><span class="sxs-lookup"><span data-stu-id="362c6-104">Using SymStore</span></span>

<span data-ttu-id="362c6-105">SymStore (symstore.exe) — это инструмент для создания хранилищ символов.</span><span class="sxs-lookup"><span data-stu-id="362c6-105">SymStore (symstore.exe) is a tool for creating symbol stores.</span></span> <span data-ttu-id="362c6-106">Он включен в пакет [средств отладки для Windows](https://www.microsoft.com/?ref=go) .</span><span class="sxs-lookup"><span data-stu-id="362c6-106">It is included in the [Debugging Tools for Windows](https://www.microsoft.com/?ref=go) package.</span></span>

<span data-ttu-id="362c6-107">SymStore хранит символы в формате, позволяющем отладчику искать символы на основе отметки времени и размера изображения (для файла. dbg или исполняемого), а также сигнатуры и возраста (для PDB-файла).</span><span class="sxs-lookup"><span data-stu-id="362c6-107">SymStore stores symbols in a format that enables the debugger to look up the symbols based on the time stamp and size of the image (for a .dbg or executable file), or signature and age (for a .pdb file).</span></span> <span data-ttu-id="362c6-108">Преимуществом хранилища символов в традиционном формате хранения символов является то, что все символы могут храниться или ссылаться на один и тот же сервер и извлекаться отладчиком без каких-либо предыдущих знаний о том, какой продукт содержит соответствующий символ.</span><span class="sxs-lookup"><span data-stu-id="362c6-108">The advantage of the symbol store over the traditional symbol storage format is that all symbols can be stored or referenced on the same server and retrieved by the debugger without any prior knowledge of which product contains the corresponding symbol.</span></span>

<span data-ttu-id="362c6-109">Обратите внимание, что несколько версий PDB-файлов символов (например, общедоступные и частные версии) не могут храниться на одном сервере, так как каждый из них содержит одинаковую подпись и возраст.</span><span class="sxs-lookup"><span data-stu-id="362c6-109">Note that multiple versions of .pdb symbol files (for example, public and private versions) cannot be stored on the same server, because they each contain the same signature and age.</span></span>

## <a name="symstore-transactions"></a><span data-ttu-id="362c6-110">SymStore транзакции</span><span class="sxs-lookup"><span data-stu-id="362c6-110">SymStore Transactions</span></span>

<span data-ttu-id="362c6-111">Каждый вызов SymStore записывается как транзакция.</span><span class="sxs-lookup"><span data-stu-id="362c6-111">Every call to SymStore is recorded as a transaction.</span></span> <span data-ttu-id="362c6-112">Существует два типа транзакций: Добавление и удаление.</span><span class="sxs-lookup"><span data-stu-id="362c6-112">There are two types of transactions: add and delete.</span></span>

<span data-ttu-id="362c6-113">При создании хранилища символов в корневом каталоге сервера создается каталог с именем «000admin».</span><span class="sxs-lookup"><span data-stu-id="362c6-113">When the symbol store is created, a directory, called "000admin", is created under the root of the server.</span></span> <span data-ttu-id="362c6-114">Каталог 000admin содержит по одному файлу для каждой транзакции, а также к файлам журналов Server.txt и History.txt.</span><span class="sxs-lookup"><span data-stu-id="362c6-114">The 000admin directory contains one file for each transaction, as well as the log files Server.txt and History.txt.</span></span> <span data-ttu-id="362c6-115">Файл Server.txt содержит список всех транзакций, которые в настоящее время находятся на сервере.</span><span class="sxs-lookup"><span data-stu-id="362c6-115">The Server.txt file contains a list of all transactions that are currently on the server.</span></span> <span data-ttu-id="362c6-116">Файл History.txt содержит хронологию всех транзакций.</span><span class="sxs-lookup"><span data-stu-id="362c6-116">The History.txt file contains a chronological history of all transactions.</span></span>

<span data-ttu-id="362c6-117">Каждый раз, когда SymStore сохраняет или удаляет файлы символов, создается новый номер транзакции.</span><span class="sxs-lookup"><span data-stu-id="362c6-117">Each time SymStore stores or removes symbol files, a new transaction number is created.</span></span> <span data-ttu-id="362c6-118">Затем файл с именем, равным этому номеру транзакции, создается в 000admin.</span><span class="sxs-lookup"><span data-stu-id="362c6-118">Then, a file, whose name is this transaction number, is created in 000admin.</span></span> <span data-ttu-id="362c6-119">Этот файл содержит список всех файлов или указателей, добавленных в хранилище символов во время этой транзакции.</span><span class="sxs-lookup"><span data-stu-id="362c6-119">This file contains a list of all the files or pointers that have been added to the symbol store during this transaction.</span></span> <span data-ttu-id="362c6-120">Если транзакция удалена, SymStore прочитает ее файл транзакций, чтобы определить, какие файлы и указатели следует удалить.</span><span class="sxs-lookup"><span data-stu-id="362c6-120">If a transaction is deleted, SymStore will read through its transaction file to determine which files and pointers it should delete.</span></span>

<span data-ttu-id="362c6-121">Параметры **Add** и **Del** указывают, следует ли выполнять транзакцию добавления или удаления.</span><span class="sxs-lookup"><span data-stu-id="362c6-121">The **add** and **del** options specify whether an add or delete transaction is to be performed.</span></span> <span data-ttu-id="362c6-122">Включение параметра **/p** с операцией Add указывает на необходимость добавления указателя; Пропуск параметра **/p** указывает, что будет добавлен фактический файл символов.</span><span class="sxs-lookup"><span data-stu-id="362c6-122">Including the **/p** option with an add operation specifies that a pointer is to be added; omitting the **/p** option specifies that the actual symbol file is to be added.</span></span>

<span data-ttu-id="362c6-123">Хранилище символов также можно создать на двух отдельных этапах.</span><span class="sxs-lookup"><span data-stu-id="362c6-123">It is also possible to create the symbol store in two separate stages.</span></span> <span data-ttu-id="362c6-124">На первом этапе для создания файла индекса используется SymStore с параметром **/x** .</span><span class="sxs-lookup"><span data-stu-id="362c6-124">In the first stage, you use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="362c6-125">На втором этапе используется SymStore с параметром **/y** для создания фактического хранилища файлов или указателей из данных в файле индекса.</span><span class="sxs-lookup"><span data-stu-id="362c6-125">In the second stage, you use SymStore with the **/y** option to create the actual store of files or pointers from the information in the index file.</span></span>

<span data-ttu-id="362c6-126">Это может быть полезной методикой по ряду причин.</span><span class="sxs-lookup"><span data-stu-id="362c6-126">This can be a useful technique for a variety of reasons.</span></span> <span data-ttu-id="362c6-127">Например, это позволяет легко воссоздать хранилище символов, если хранилище каким-либо образом теряется, пока файл индекса еще существует.</span><span class="sxs-lookup"><span data-stu-id="362c6-127">For instance, this allows the symbol store to be easily recreated if the store is somehow lost, as long as the index file still exists.</span></span> <span data-ttu-id="362c6-128">Или, возможно, компьютер, на котором находятся файлы символов, имеет низкую сетевую связь с компьютером, на котором будет создано хранилище символов.</span><span class="sxs-lookup"><span data-stu-id="362c6-128">Or perhaps the computer containing the symbol files has a slow network connection to the computer on which the symbol store will be created.</span></span> <span data-ttu-id="362c6-129">В этом случае можно создать файл индекса на том же компьютере, где находятся файлы символов, переместить файл индекса на второй компьютер, а затем создать хранилище на втором компьютере.</span><span class="sxs-lookup"><span data-stu-id="362c6-129">In this case, you can create the index file on the same machine as the symbol files, transfer the index file to the second machine, and then create the store on the second machine.</span></span>

<span data-ttu-id="362c6-130">Полный список всех параметров SymStore см. в разделе [параметры Command-Line SymStore](symstore-command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="362c6-130">For a full listing of all SymStore parameters, see [SymStore Command-Line Options](symstore-command-line-options.md).</span></span>

> [!Note]  
> <span data-ttu-id="362c6-131">SymStore не поддерживает одновременные транзакции от нескольких пользователей.</span><span class="sxs-lookup"><span data-stu-id="362c6-131">SymStore does not support simultaneous transactions from multiple users.</span></span> <span data-ttu-id="362c6-132">Рекомендуется, чтобы один пользователь был назначен администратором хранилища символов и отвечал всем транзакциям **добавления** и **Del** .</span><span class="sxs-lookup"><span data-stu-id="362c6-132">It is recommended that one user be designated "administrator" of the symbol store and be responsible for all **add** and **del** transactions.</span></span>

 

## <a name="transaction-examples"></a><span data-ttu-id="362c6-133">Примеры транзакций</span><span class="sxs-lookup"><span data-stu-id="362c6-133">Transaction Examples</span></span>

<span data-ttu-id="362c6-134">Ниже приведены два примера SymStore добавления указателей символов для сборки 3790 Windows Server 2003 в \\ \\ SampleDir \\ SymSrv:</span><span class="sxs-lookup"><span data-stu-id="362c6-134">Here are two examples of SymStore adding symbol pointers for build 3790 of Windows Server 2003 to \\\\sampledir\\symsrv:</span></span>

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

<span data-ttu-id="362c6-135">В следующем примере SymStore добавляет фактические файлы символов для проекта приложения в \\ \\ ларжеапп \\ выборе \\ ячеек в \\ \\ тестдир \\ SymSrv:</span><span class="sxs-lookup"><span data-stu-id="362c6-135">In the following example, SymStore adds the actual symbol files for an application project in \\\\largeapp\\appserver\\bins to \\\\testdir\\symsrv:</span></span>

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

<span data-ttu-id="362c6-136">Ниже приведен пример использования файла индекса.</span><span class="sxs-lookup"><span data-stu-id="362c6-136">Here is an example of how an index file is used.</span></span> <span data-ttu-id="362c6-137">Сначала SymStore создает файл индекса на основе коллекции файлов символов в \\ \\ \\ \\ ячейках ларжеапп выборе \\ .</span><span class="sxs-lookup"><span data-stu-id="362c6-137">First, SymStore creates an index file based on the collection of symbol files in \\\\largeapp\\appserver\\bins\\.</span></span> <span data-ttu-id="362c6-138">В этом случае файл индекса размещается на третьем компьютере, \\ \\ хубсервер \\ хубшаре.</span><span class="sxs-lookup"><span data-stu-id="362c6-138">In this case, the index file is placed on a third computer, \\\\hubserver\\hubshare.</span></span> <span data-ttu-id="362c6-139">Используйте параметр **/g** , чтобы указать, что префикс файла " \\ \\ ларжеапп \\ выборе" может измениться в будущем:</span><span class="sxs-lookup"><span data-stu-id="362c6-139">You use the **/g** option to specify that the file prefix "\\\\largeapp\\appserver" might change in the future:</span></span>

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

<span data-ttu-id="362c6-140">Теперь предположим, что вы перемещаете все файлы символов с компьютера \\ \\ ларжеапп \\ выборе и поместили их на \\ \\ мярчиве \\ выборе.</span><span class="sxs-lookup"><span data-stu-id="362c6-140">Now suppose you move all the symbol files off of the machine \\\\largeapp\\appserver and put them on \\\\myarchive\\appserver.</span></span> <span data-ttu-id="362c6-141">Затем можно создать хранилище символов из файла индекса \\ \\ хубсервер \\ хубшаре \\myindex.txt следующим образом:</span><span class="sxs-lookup"><span data-stu-id="362c6-141">You can then create the symbol store itself from the index file \\\\hubserver\\hubshare\\myindex.txt as follows:</span></span>

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

<span data-ttu-id="362c6-142">Наконец, ниже приведен пример SymStore удаления файла, добавленного предыдущей транзакцией.</span><span class="sxs-lookup"><span data-stu-id="362c6-142">Finally, here is an example of SymStore deleting a file added by a previous transaction.</span></span> <span data-ttu-id="362c6-143">Описание процесса определения идентификатора транзакции (в данном случае 0000000096) см. в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="362c6-143">See the following section for an explanation of how to determine the transaction ID (in this case, 0000000096).</span></span>

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a><span data-ttu-id="362c6-144">Сжатые файлы</span><span class="sxs-lookup"><span data-stu-id="362c6-144">Compressed Files</span></span>

<span data-ttu-id="362c6-145">SymStore можно использовать с сжатыми файлами двумя разными способами.</span><span class="sxs-lookup"><span data-stu-id="362c6-145">SymStore can be used with compressed files in two different ways.</span></span>

1.  <span data-ttu-id="362c6-146">Используйте SymStore с параметром **/p** для хранения указателей на файлы символов.</span><span class="sxs-lookup"><span data-stu-id="362c6-146">Use SymStore with the **/p** option to store pointers to the symbol files.</span></span> <span data-ttu-id="362c6-147">После завершения SymStore необходимо сжать файлы, на которые ссылаются указатели.</span><span class="sxs-lookup"><span data-stu-id="362c6-147">After SymStore finishes, compress the files that the pointers refer to.</span></span>
2.  <span data-ttu-id="362c6-148">Для создания файла индекса используйте SymStore с параметром **/x** .</span><span class="sxs-lookup"><span data-stu-id="362c6-148">Use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="362c6-149">После завершения SymStore необходимо сжать файлы, перечисленные в индексном файле.</span><span class="sxs-lookup"><span data-stu-id="362c6-149">After SymStore finishes, compress the files listed in the index file.</span></span> <span data-ttu-id="362c6-150">Затем используйте SymStore с параметром **/y** (и, если требуется, параметр **/p** ) для хранения файлов или указателей на файлы в хранилище символов.</span><span class="sxs-lookup"><span data-stu-id="362c6-150">Then use SymStore with the **/y** option (and, if you wish, the **/p** option) to store the files or pointers to the files in the symbol store.</span></span> <span data-ttu-id="362c6-151">(Для выполнения этой операции SymStore не потребуется распаковать файлы.)</span><span class="sxs-lookup"><span data-stu-id="362c6-151">(SymStore will not need to uncompress the files to perform this operation.)</span></span>

<span data-ttu-id="362c6-152">Сервер символов будет отвечать за распаковку файлов, когда они понадобятся.</span><span class="sxs-lookup"><span data-stu-id="362c6-152">Your symbol server will be responsible for uncompressing the files when they are needed.</span></span>

<span data-ttu-id="362c6-153">При использовании SymSrv в качестве сервера символов необходимо выполнить сжатие с помощью средства compress.exe, распространяемого вместе с пакетом средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="362c6-153">If you are using SymSrv as your symbol server, any compression should be done using the compress.exe tool that is distributed with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="362c6-154">Сжатые файлы должны содержать символ подчеркивания в качестве последнего символа в расширениях файлов (например, Module1. PD \_ или Module2. DB \_ ).</span><span class="sxs-lookup"><span data-stu-id="362c6-154">Compressed files should have an underscore as the last character in their file extensions (for example, module1.pd\_ or module2.db\_).</span></span> <span data-ttu-id="362c6-155">Дополнительные сведения см. [в разделе Использование SymSrv](using-symsrv.md).</span><span class="sxs-lookup"><span data-stu-id="362c6-155">For details, see [Using SymSrv](using-symsrv.md).</span></span>

## <a name="the-servertxt-and-historytxt-files"></a><span data-ttu-id="362c6-156">Файлы server.txt и history.txt</span><span class="sxs-lookup"><span data-stu-id="362c6-156">The server.txt and history.txt Files</span></span>

<span data-ttu-id="362c6-157">При добавлении транзакции в нее добавляются несколько элементов данных, server.txt и history.txt для будущего поиска.</span><span class="sxs-lookup"><span data-stu-id="362c6-157">When a transaction is added, several items of information are added to server.txt and history.txt for future lookup capability.</span></span> <span data-ttu-id="362c6-158">Ниже приведен пример строки в server.txt и history.txt для добавления транзакции.</span><span class="sxs-lookup"><span data-stu-id="362c6-158">The following is an example of a line in server.txt and history.txt for an add transaction:</span></span>

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

<span data-ttu-id="362c6-159">Это строка с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="362c6-159">This is a comma-separated line.</span></span> <span data-ttu-id="362c6-160">Поля определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="362c6-160">The fields are defined as follows.</span></span>



| <span data-ttu-id="362c6-161">Поле</span><span class="sxs-lookup"><span data-stu-id="362c6-161">Field</span></span>      | <span data-ttu-id="362c6-162">Описание</span><span class="sxs-lookup"><span data-stu-id="362c6-162">Description</span></span>                                                                         |
|------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="362c6-163">0000000096</span><span class="sxs-lookup"><span data-stu-id="362c6-163">0000000096</span></span> | <span data-ttu-id="362c6-164">ИДЕНТИФИКАЦИОНный номер транзакции, созданный SymStore.</span><span class="sxs-lookup"><span data-stu-id="362c6-164">Transaction ID number, as created by SymStore.</span></span>                                      |
| <span data-ttu-id="362c6-165">add</span><span class="sxs-lookup"><span data-stu-id="362c6-165">add</span></span>        | <span data-ttu-id="362c6-166">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="362c6-166">Type of transaction.</span></span> <span data-ttu-id="362c6-167">Это поле может быть либо " **Добавить** ", либо " **Del**".</span><span class="sxs-lookup"><span data-stu-id="362c6-167">This field can be either **add** or **del**.</span></span>                   |
| <span data-ttu-id="362c6-168">ptr</span><span class="sxs-lookup"><span data-stu-id="362c6-168">ptr</span></span>        | <span data-ttu-id="362c6-169">Указывает, были ли добавлены файлы или указатели.</span><span class="sxs-lookup"><span data-stu-id="362c6-169">Whether files or pointers were added.</span></span> <span data-ttu-id="362c6-170">Это поле может быть либо **File** , либо **ptr**.</span><span class="sxs-lookup"><span data-stu-id="362c6-170">This field can be either **file** or **ptr**.</span></span> |
| <span data-ttu-id="362c6-171">10/09/99</span><span class="sxs-lookup"><span data-stu-id="362c6-171">10/09/99</span></span>   | <span data-ttu-id="362c6-172">Дата возникновения транзакции.</span><span class="sxs-lookup"><span data-stu-id="362c6-172">Date when transaction occurred.</span></span>                                                     |
| <span data-ttu-id="362c6-173">00:08:32</span><span class="sxs-lookup"><span data-stu-id="362c6-173">00:08:32</span></span>   | <span data-ttu-id="362c6-174">Время начала транзакции.</span><span class="sxs-lookup"><span data-stu-id="362c6-174">Time when transaction started.</span></span>                                                      |
| <span data-ttu-id="362c6-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="362c6-175">Windows XP</span></span> | <span data-ttu-id="362c6-176">Продукт.</span><span class="sxs-lookup"><span data-stu-id="362c6-176">Product.</span></span>                                                                            |
| <span data-ttu-id="362c6-177">Фре x86</span><span class="sxs-lookup"><span data-stu-id="362c6-177">x86 fre</span></span>    | <span data-ttu-id="362c6-178">Версия (необязательно).</span><span class="sxs-lookup"><span data-stu-id="362c6-178">Version (optional).</span></span>                                                                 |
| <span data-ttu-id="362c6-179">Добавлено из</span><span class="sxs-lookup"><span data-stu-id="362c6-179">Added from</span></span> | <span data-ttu-id="362c6-180">Комментарий (необязательно)</span><span class="sxs-lookup"><span data-stu-id="362c6-180">Comment (optional)</span></span>                                                                  |
| <span data-ttu-id="362c6-181">Не используется</span><span class="sxs-lookup"><span data-stu-id="362c6-181">Unused</span></span>     | <span data-ttu-id="362c6-182">(Зарезервировано для последующего использования.)</span><span class="sxs-lookup"><span data-stu-id="362c6-182">(Reserved for later use.)</span></span>                                                           |



 

<span data-ttu-id="362c6-183">Ниже приведены примеры строк из файла транзакций 0000000096.</span><span class="sxs-lookup"><span data-stu-id="362c6-183">Here are some sample lines from the transaction file 0000000096.</span></span> <span data-ttu-id="362c6-184">Каждая строка записывает каталог и расположение файла или указателя, добавленного в каталог.</span><span class="sxs-lookup"><span data-stu-id="362c6-184">Each line records the directory and the location of the file or pointer that was added to the directory.</span></span>

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

<span data-ttu-id="362c6-185">Если для отмены исходных транзакций **добавления** используется транзакция **Del** , эти строки будут удалены из server.txt, а следующая строка будет добавлена в history.txt:</span><span class="sxs-lookup"><span data-stu-id="362c6-185">If you use a **del** transaction to undo the original **add** transactions, these lines will be removed from server.txt, and the following line will be added to history.txt:</span></span>

``` syntax
0000000105,del,0000000096
```

<span data-ttu-id="362c6-186">Поля для транзакции Delete определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="362c6-186">The fields for the delete transaction are defined as follows.</span></span>



| <span data-ttu-id="362c6-187">Поле</span><span class="sxs-lookup"><span data-stu-id="362c6-187">Field</span></span>      | <span data-ttu-id="362c6-188">Описание</span><span class="sxs-lookup"><span data-stu-id="362c6-188">Description</span></span>                                                       |
|------------|-------------------------------------------------------------------|
| <span data-ttu-id="362c6-189">0000000105</span><span class="sxs-lookup"><span data-stu-id="362c6-189">0000000105</span></span> | <span data-ttu-id="362c6-190">ИДЕНТИФИКАЦИОНный номер транзакции, созданный SymStore.</span><span class="sxs-lookup"><span data-stu-id="362c6-190">Transaction ID number, as created by SymStore.</span></span>                    |
| <span data-ttu-id="362c6-191">del</span><span class="sxs-lookup"><span data-stu-id="362c6-191">del</span></span>        | <span data-ttu-id="362c6-192">Тип транзакции.</span><span class="sxs-lookup"><span data-stu-id="362c6-192">Type of transaction.</span></span> <span data-ttu-id="362c6-193">Это поле может быть либо " **Добавить** ", либо " **Del**".</span><span class="sxs-lookup"><span data-stu-id="362c6-193">This field can be either **add** or **del**.</span></span> |
| <span data-ttu-id="362c6-194">0000000096</span><span class="sxs-lookup"><span data-stu-id="362c6-194">0000000096</span></span> | <span data-ttu-id="362c6-195">Транзакция, которая была удалена.</span><span class="sxs-lookup"><span data-stu-id="362c6-195">Transaction that was deleted.</span></span>                                     |



 

## <a name="symbol-storage-format"></a><span data-ttu-id="362c6-196">Формат хранения символов</span><span class="sxs-lookup"><span data-stu-id="362c6-196">Symbol Storage Format</span></span>

<span data-ttu-id="362c6-197">SymStore использует саму файловую систему в качестве базы данных.</span><span class="sxs-lookup"><span data-stu-id="362c6-197">SymStore uses the file system itself as a database.</span></span> <span data-ttu-id="362c6-198">Он создает большое дерево каталогов с именами каталогов, основанными на таких вещах, как отметки времени файла символов, подписи, возраст и другие данные.</span><span class="sxs-lookup"><span data-stu-id="362c6-198">It creates a large tree of directories, with directory names based on such things as the symbol file time stamps, signatures, age, and other data.</span></span>

<span data-ttu-id="362c6-199">Например, после добавления нескольких различных файлов ACPI. dbg на сервер каталоги могут выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="362c6-199">For example, after several different acpi.dbg files have been added to the server, the directories could look like this:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

<span data-ttu-id="362c6-200">В этом примере путь поиска для файла символов ACPI. dbg может выглядеть примерно так: \\ \\ мибуилдс \\ SymSrv \\ ACPI. dbg \\ 37cdb03962040.</span><span class="sxs-lookup"><span data-stu-id="362c6-200">In this example, the lookup path for the acpi.dbg symbol file might look something like this: \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040.</span></span>

<span data-ttu-id="362c6-201">В каталоге поиска могут находиться три файла:</span><span class="sxs-lookup"><span data-stu-id="362c6-201">Three files may exist inside the lookup directory:</span></span>

1.  <span data-ttu-id="362c6-202">Если файл был сохранен, в нем будет существовать ACPI. dbg.</span><span class="sxs-lookup"><span data-stu-id="362c6-202">If the file was stored, then acpi.dbg will exist there.</span></span>
2.  <span data-ttu-id="362c6-203">Если был сохранен указатель, то файл с именем file. PTR будет существовать и содержать путь к фактическому файлу символов.</span><span class="sxs-lookup"><span data-stu-id="362c6-203">If a pointer was stored, then a file called file.ptr will exist and contain the path to the actual symbol file.</span></span>
3.  <span data-ttu-id="362c6-204">Файл с именем ReFS. PTR, содержащий список всех текущих расположений для ACPI. dbg с этой меткой времени и размером образа, которые в данный момент добавляются в хранилище символов.</span><span class="sxs-lookup"><span data-stu-id="362c6-204">A file called refs.ptr, which contains a list of all the current locations for acpi.dbg with this timestamp and image size that are currently added to the symbol store.</span></span>

<span data-ttu-id="362c6-205">Отображение списка каталогов \\ \\ мибуилдс \\ SymSrv \\ ACPI. dbg \\ 37cdb03962040 предоставляет следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="362c6-205">Displaying the directory listing of \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040 gives the following:</span></span>

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

<span data-ttu-id="362c6-206">Файл File. PTR содержит текстовую строку " \\ \\ мибуилдс \\ SYMBOLS \\ x86 \\ 2128. chk \\ SYMBOLS \\ sys \\ ACPI. dbg".</span><span class="sxs-lookup"><span data-stu-id="362c6-206">The file file.ptr contains the text string "\\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg".</span></span> <span data-ttu-id="362c6-207">Так как в этом каталоге нет файла с именем ACPI. dbg, отладчик попытается найти файл в \\ \\ мибуилдс \\ SYMBOLS \\ x86 \\ 2128. chk \\ SYMBOLS \\ sys \\ ACPI. dbg.</span><span class="sxs-lookup"><span data-stu-id="362c6-207">Since there is no file called acpi.dbg in this directory, the debugger will try to find the file at \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg.</span></span>

<span data-ttu-id="362c6-208">Содержимое ReFS. PTR используется только SymStore, а не отладчиком.</span><span class="sxs-lookup"><span data-stu-id="362c6-208">The contents of refs.ptr are used only by SymStore, not the debugger.</span></span> <span data-ttu-id="362c6-209">Этот файл содержит записи всех транзакций, выполненных в этом каталоге.</span><span class="sxs-lookup"><span data-stu-id="362c6-209">This file contains a record of all transactions that have taken place in this directory.</span></span> <span data-ttu-id="362c6-210">Пример строки из ReFS. PTR может быть следующим:</span><span class="sxs-lookup"><span data-stu-id="362c6-210">A sample line from refs.ptr might be:</span></span>

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

<span data-ttu-id="362c6-211">Это показывает, что указатель на \\ \\ мибуилдс \\ символы \\ x86 \\ 2128. \\ символы CHK \\ sys \\ ACPI. dbg был добавлен с транзакцией «0000000026».</span><span class="sxs-lookup"><span data-stu-id="362c6-211">This shows that a pointer to \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg was added with transaction "0000000026".</span></span>

<span data-ttu-id="362c6-212">Некоторые файлы символов остаются постоянными с помощью различных продуктов или сборок или определенного продукта.</span><span class="sxs-lookup"><span data-stu-id="362c6-212">Some symbol files stay constant through various products or builds or a particular product.</span></span> <span data-ttu-id="362c6-213">Одним из примеров этого является файл msvcrt. pdb.</span><span class="sxs-lookup"><span data-stu-id="362c6-213">One example of this is the file msvcrt.pdb.</span></span> <span data-ttu-id="362c6-214">При выполнении каталога \\ \\ мибуилдс \\ SymSrv \\ msvcrt. pdb показано, что на сервер символов добавлены только две версии msvcrt. pdb:</span><span class="sxs-lookup"><span data-stu-id="362c6-214">Doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb shows that only two versions of msvcrt.pdb have been added to the symbols server:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

<span data-ttu-id="362c6-215">Однако при выполнении каталога \\ \\ мибуилдс \\ SymSrv \\ msvcrt. pdb \\ 37a8f40e2 показывает, что ReFS. PTR содержит несколько указателей.</span><span class="sxs-lookup"><span data-stu-id="362c6-215">However, doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2 shows that refs.ptr has several pointers in it.</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

<span data-ttu-id="362c6-216">Ниже приведены содержимое файла \\ \\ мибуилдс \\ SymSrv \\ msvcrt. pdb \\ 37a8f40e2 \\ ReFS. PTR:</span><span class="sxs-lookup"><span data-stu-id="362c6-216">The contents of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2\\refs.ptr are the following:</span></span>

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

<span data-ttu-id="362c6-217">Это показывает, что один и тот же файл msvcrt. pdb использовался для нескольких сборок символов, хранящихся в \\ \\ мибуилдс \\ SymSrv.</span><span class="sxs-lookup"><span data-stu-id="362c6-217">This shows that the same msvcrt.pdb was used for multiple builds of symbols stored on \\\\mybuilds\\symsrv.</span></span>

<span data-ttu-id="362c6-218">Ниже приведен пример каталога, который содержит сочетание дополнений к файлам и указателям.</span><span class="sxs-lookup"><span data-stu-id="362c6-218">Here is an example of a directory that contains a mixture of file and pointer additions:</span></span>

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

<span data-ttu-id="362c6-219">В этом случае ReFS. PTR имеет следующее содержимое:</span><span class="sxs-lookup"><span data-stu-id="362c6-219">In this case, refs.ptr has the following contents:</span></span>

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="362c6-220">Таким же транзакция 43, 44 и 45 добавила один и тот же файл на сервер, а транзакции 46 и 47 добавили указатели.</span><span class="sxs-lookup"><span data-stu-id="362c6-220">Thus, transactions 43, 44, and 45 added the same file to the server, and transactions 46 and 47 added pointers.</span></span> <span data-ttu-id="362c6-221">Если транзакции 43, 44 и 45 удаляются, файл dbghelp. dbg будет удален из каталога.</span><span class="sxs-lookup"><span data-stu-id="362c6-221">If transactions 43, 44, and 45 are deleted, then the file dbghelp.dbg will be deleted from the directory.</span></span> <span data-ttu-id="362c6-222">После этого каталог будет иметь следующее содержимое:</span><span class="sxs-lookup"><span data-stu-id="362c6-222">The directory will then have the following contents:</span></span>

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

<span data-ttu-id="362c6-223">Файл File. PTR содержит « \\ \\ sampledir2 \\ bin \\ Symbol \\ Retail \\ DLL \\ dbghelp. dbg», а ReFS. PTR содержит</span><span class="sxs-lookup"><span data-stu-id="362c6-223">Now file.ptr contains "\\\\sampledir2\\bin\\symbols\\retail\\dll\\dbghelp.dbg", and refs.ptr contains</span></span>

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="362c6-224">Когда последняя запись в ReFS. PTR является указателем, файловый файл. PTR будет существовать и содержать путь к связанному файлу.</span><span class="sxs-lookup"><span data-stu-id="362c6-224">Whenever the final entry in refs.ptr is a pointer, the file file.ptr will exist and contain the path to the associated file.</span></span> <span data-ttu-id="362c6-225">Когда последняя запись в ReFS. PTR является файлом, файл. PTR не будет существовать в этом каталоге.</span><span class="sxs-lookup"><span data-stu-id="362c6-225">Whenever the final entry in refs.ptr is a file, no file.ptr will exist in this directory.</span></span> <span data-ttu-id="362c6-226">Таким образом, любая операция удаления, которая удаляет последнюю запись в ReFS. PTR, может привести к созданию, удалению или изменению файла. PTR.</span><span class="sxs-lookup"><span data-stu-id="362c6-226">Therefore, any delete operation that removes the final entry in refs.ptr may result in file.ptr being created, deleted, or changed.</span></span>

 

 



