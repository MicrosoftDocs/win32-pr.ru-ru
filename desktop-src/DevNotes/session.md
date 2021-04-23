---
description: Структура сеанса содержит сведения о текущем сеансе.
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: Структура сеанса
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e1f356020df681e00f43c7a47ac16048764c0ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806904"
---
# <a name="session-structure"></a><span data-ttu-id="c77f0-103">Структура сеанса</span><span class="sxs-lookup"><span data-stu-id="c77f0-103">SESSION structure</span></span>

<span data-ttu-id="c77f0-104">\[Эта структура содержит сведения, необходимые только при использовании функций **делетикстрактедфилес** и **Extract** , которые не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c77f0-104">\[This structure contains information required only when using the **DeleteExtractedFiles** and **Extract** functions, which are not supported.</span></span> <span data-ttu-id="c77f0-105">Эта документация предоставляется только в ознакомительных целях.\]</span><span class="sxs-lookup"><span data-stu-id="c77f0-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="c77f0-106">Структура **сеанса** содержит сведения о текущем сеансе.</span><span class="sxs-lookup"><span data-stu-id="c77f0-106">The **SESSION** structure contains information about the current session.</span></span>

## <a name="syntax"></a><span data-ttu-id="c77f0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c77f0-107">Syntax</span></span>


```C++
typedef struct {
  ACTION    act;
  HFILELIST hflist;
  BOOL      fAllCabinets;
  BOOL      fOverwrite;
  BOOL      fNoLineFeed;
  BOOL      fSelfExtract;
  long      cbSelfExtractSize;
  long      cbSelfExtractSize;
  int       ahfSelf[cMAX_CAB_FILE_OPEN];
  int       cErrors;
  HFDI      hfdi;
  ERF       erf;
  long      cFiles;
  long      cbTotalBytes;
  PERROR    perr;
  SPILLERR  se;
  long      cbSpill;
  char      achSelf[cbFILE_NAME_MAX];
  char      achMsg[cbMAX_LINE*2];
  char      achLine;
  char      achLocation;
  char      achFile;
  char      achDest;
  char      achCabPath;
  BOOL      fContinuationCabinet;
  BOOL      fShowReserveInfo;
  BOOL      fNextCabCalled;
  CABINET   acab[2];
  char      achZap[cbFILE_NAME_MAX];
  char      achCabinetFile[cbFILE_NAME_MAX];
  int       cArgv;
  char      **pArgv;
  int       fDestructive;
  USHORT    iCurrentFolder;
} SESSION, *PSESSION;
```



## <a name="members"></a><span data-ttu-id="c77f0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c77f0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c77f0-109">**ACT**</span><span class="sxs-lookup"><span data-stu-id="c77f0-109">**act**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-110">действие для выполнения.</span><span class="sxs-lookup"><span data-stu-id="c77f0-110">The action to perform.</span></span> <span data-ttu-id="c77f0-111">Этот элемент может быть одним из значений следующего перечислимого типа.</span><span class="sxs-lookup"><span data-stu-id="c77f0-111">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    actBAD,         // Invalid action
    actHELP,        // Show help
    actDEFAULT,     // Perform default action based on command line arguments
    actDIRECTORY,   // Force display of cabinet directory
    actEXTRACT,     // Force file extraction
    actCOPY,        // Do single file-to-file copy
} ACTION;  
```

</dd> <dt>

<span data-ttu-id="c77f0-112">**хфлист**</span><span class="sxs-lookup"><span data-stu-id="c77f0-112">**hflist**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-113">Маркер для списка файлов, указанных в командной строке.</span><span class="sxs-lookup"><span data-stu-id="c77f0-113">The handle to a list of files specified on the command line.</span></span> <span data-ttu-id="c77f0-114">Этот тип данных объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c77f0-114">This datatype is declared as follows:</span></span>

`typedef void *HFILELIST;`

</dd> <dt>

<span data-ttu-id="c77f0-115">**фаллкабинетс**</span><span class="sxs-lookup"><span data-stu-id="c77f0-115">**fAllCabinets**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-116">Флаг, указывающий, следует ли обрабатывать более одного CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="c77f0-116">A flag that indicates whether more than one cabinet file should be processed.</span></span> <span data-ttu-id="c77f0-117">Если это значение равно **true**, ящики продолжения обрабатываются.</span><span class="sxs-lookup"><span data-stu-id="c77f0-117">If this value is **TRUE**, continuation cabinets are processed.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-118">**фоверврите**</span><span class="sxs-lookup"><span data-stu-id="c77f0-118">**fOverwrite**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-119">Флаг, указывающий, следует ли перезаписывать существующие файлы.</span><span class="sxs-lookup"><span data-stu-id="c77f0-119">A flag that indicates whether existing files should be overwritten.</span></span> <span data-ttu-id="c77f0-120">Если это значение равно **true**, существующие файлы будут перезаписаны.</span><span class="sxs-lookup"><span data-stu-id="c77f0-120">If this value is **TRUE**, existing files are overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-121">**фнолинефид**</span><span class="sxs-lookup"><span data-stu-id="c77f0-121">**fNoLineFeed**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-122">Флаг, указывающий, содержит ли последний `printf` вызов символы новой строки ( `\n` ).</span><span class="sxs-lookup"><span data-stu-id="c77f0-122">A flag that indicates whether the last `printf` call has the newline (`\n`) characters.</span></span> <span data-ttu-id="c77f0-123">Если это значение равно **true**, последний `printf` вызов не включал символы новой строки.</span><span class="sxs-lookup"><span data-stu-id="c77f0-123">If this value is **TRUE**, the last `printf` call did not include the newline characters.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-124">**фселфекстракт**</span><span class="sxs-lookup"><span data-stu-id="c77f0-124">**fSelfExtract**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-125">Флаг, указывающий, является ли CAB-файл самораскрывающимся.</span><span class="sxs-lookup"><span data-stu-id="c77f0-125">A flag that indicates whether a cabinet is self extracting.</span></span> <span data-ttu-id="c77f0-126">Если это значение равно **true**, CAB-файл самоизвлекается.</span><span class="sxs-lookup"><span data-stu-id="c77f0-126">If this value is **TRUE**, the cabinet is self extracting.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-127">**кбселфекстрактсизе**</span><span class="sxs-lookup"><span data-stu-id="c77f0-127">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-128">Длина исполняемого фрагмента (exe) самораспаковывающегося CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="c77f0-128">The length of the executable (.exe) portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-129">**кбселфекстрактсизе**</span><span class="sxs-lookup"><span data-stu-id="c77f0-129">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-130">Длина части CAB-файла самораспаковывающегося архива.</span><span class="sxs-lookup"><span data-stu-id="c77f0-130">The length of the CAB portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-131">**ахфселф**</span><span class="sxs-lookup"><span data-stu-id="c77f0-131">**ahfSelf**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-132">Файлы дескрипторов CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="c77f0-132">The file handles to the cabinet.</span></span>

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

<span data-ttu-id="c77f0-133">**церрорс**</span><span class="sxs-lookup"><span data-stu-id="c77f0-133">**cErrors**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-134">Число ошибок, возникших во время сеанса извлечения.</span><span class="sxs-lookup"><span data-stu-id="c77f0-134">The count of errors encountered during the extraction session.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-135">**хфди**</span><span class="sxs-lookup"><span data-stu-id="c77f0-135">**hfdi**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-136">Маркер контекста FDI.</span><span class="sxs-lookup"><span data-stu-id="c77f0-136">A handle to the FDI context.</span></span> <span data-ttu-id="c77f0-137">Этот тип данных объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c77f0-137">This datatype is declared as follows:</span></span>

`typedef void FAR *HFDI; `

</dd> <dt>

<span data-ttu-id="c77f0-138">**erf**</span><span class="sxs-lookup"><span data-stu-id="c77f0-138">**erf**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-139">Структура ошибок FDI.</span><span class="sxs-lookup"><span data-stu-id="c77f0-139">The FDI error structure.</span></span> <span data-ttu-id="c77f0-140">См. раздел [**Фош**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span><span class="sxs-lookup"><span data-stu-id="c77f0-140">See [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-141">**кфилес**</span><span class="sxs-lookup"><span data-stu-id="c77f0-141">**cFiles**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-142">Число обработанных файлов.</span><span class="sxs-lookup"><span data-stu-id="c77f0-142">The count of files processed.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-143">**кбтоталбитес**</span><span class="sxs-lookup"><span data-stu-id="c77f0-143">**cbTotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-144">Общее число извлеченных байтов.</span><span class="sxs-lookup"><span data-stu-id="c77f0-144">The total number of bytes extracted.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-145">**PERR**</span><span class="sxs-lookup"><span data-stu-id="c77f0-145">**perr**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-146">Пройдите через FDI.</span><span class="sxs-lookup"><span data-stu-id="c77f0-146">The pass through FDI.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-147">**&**</span><span class="sxs-lookup"><span data-stu-id="c77f0-147">**se**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-148">Ошибка при сбросе файла.</span><span class="sxs-lookup"><span data-stu-id="c77f0-148">The spill file error.</span></span> <span data-ttu-id="c77f0-149">Этот элемент может быть одним из значений следующего перечислимого типа.</span><span class="sxs-lookup"><span data-stu-id="c77f0-149">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

<span data-ttu-id="c77f0-150">**кбспилл**</span><span class="sxs-lookup"><span data-stu-id="c77f0-150">**cbSpill**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-151">Размер запрошенного файла сброса.</span><span class="sxs-lookup"><span data-stu-id="c77f0-151">The size of the spill file requested.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-152">**ачселф**</span><span class="sxs-lookup"><span data-stu-id="c77f0-152">**achSelf**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-153">Имя исполняемого файла (exe).</span><span class="sxs-lookup"><span data-stu-id="c77f0-153">The name of the executable (.exe) file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="c77f0-154">**ачмсг**</span><span class="sxs-lookup"><span data-stu-id="c77f0-154">**achMsg**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-155">Буфер форматирования сообщения.</span><span class="sxs-lookup"><span data-stu-id="c77f0-155">The message formatting buffer.</span></span>

`#define cbMAX_LINE          256`

</dd> <dt>

<span data-ttu-id="c77f0-156">**ачлине**</span><span class="sxs-lookup"><span data-stu-id="c77f0-156">**achLine**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-157">Буфер форматирования строки.</span><span class="sxs-lookup"><span data-stu-id="c77f0-157">The line formatting buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-158">**ачлокатион**</span><span class="sxs-lookup"><span data-stu-id="c77f0-158">**achLocation**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-159">выходной каталог.</span><span class="sxs-lookup"><span data-stu-id="c77f0-159">The output directory.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-160">**ачфиле**</span><span class="sxs-lookup"><span data-stu-id="c77f0-160">**achFile**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-161">Имя текущего файла, которое извлекается.</span><span class="sxs-lookup"><span data-stu-id="c77f0-161">The current file name being extracted.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-162">**ачдест**</span><span class="sxs-lookup"><span data-stu-id="c77f0-162">**achDest**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-163">Имя файла принудительного назначения.</span><span class="sxs-lookup"><span data-stu-id="c77f0-163">The forced destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-164">**ачкабпас**</span><span class="sxs-lookup"><span data-stu-id="c77f0-164">**achCabPath**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-165">Путь для просмотра CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="c77f0-165">The path to look at for a cabinet file.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-166">**фконтинуатионкабинет**</span><span class="sxs-lookup"><span data-stu-id="c77f0-166">**fContinuationCabinet**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-167">Флаг, указывающий, является ли текущий CAB-файл первым обработанным.</span><span class="sxs-lookup"><span data-stu-id="c77f0-167">A flag that indicates whether the current cabinet is the first one processed.</span></span> <span data-ttu-id="c77f0-168">Если задано значение **true**, то это не первый обработанный CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="c77f0-168">If set to **TRUE**, it is not the first cabinet processed.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-169">**фшовресервеинфо**</span><span class="sxs-lookup"><span data-stu-id="c77f0-169">**fShowReserveInfo**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-170">Флаг, указывающий, следует ли предоставлять сведения о резервировании.</span><span class="sxs-lookup"><span data-stu-id="c77f0-170">A flag that indicates whether reserve information should be provided.</span></span> <span data-ttu-id="c77f0-171">Если задано значение **true**, сведения становятся доступными.</span><span class="sxs-lookup"><span data-stu-id="c77f0-171">If set to **TRUE**, the information is made available.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-172">**фнексткабкаллед**</span><span class="sxs-lookup"><span data-stu-id="c77f0-172">**fNextCabCalled**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-173">Этот член позволяет определить, какие из записей **Акаб** будут использоваться, если обрабатываются все файлы в наборе CAB-файлов (**Фаллкабинет** имеет значение **true**).</span><span class="sxs-lookup"><span data-stu-id="c77f0-173">This member provides a way to determine which of the **acab** entries to use if we are processing all files in a cabinet set (**fAllCabinet** is set to **TRUE**).</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-174">**акаб**</span><span class="sxs-lookup"><span data-stu-id="c77f0-174">**acab**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-175">Последние две записи в наборе CAB-файлов.</span><span class="sxs-lookup"><span data-stu-id="c77f0-175">The last two entries in the cabinet set.</span></span> <span data-ttu-id="c77f0-176">Эта структура определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c77f0-176">This structure is defined as follows:</span></span>

``` syntax
typedef struct {
    char    achCabPath[cbFILE_NAME_MAX];     // Cabinet file path
    char    achCabFilename[cbFILE_NAME_MAX]; // Cabinet file name.ext
    char    achDiskName[cbFILE_NAME_MAX];    // User readable disk label
    USHORT  setID;
    USHORT  iCabinet;
} CABINET;
typedef CABINET *PCABINET;
```

</dd> <dt>

<span data-ttu-id="c77f0-177">**ачзап**</span><span class="sxs-lookup"><span data-stu-id="c77f0-177">**achZap**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-178">Префикс для удаления из имени файла.</span><span class="sxs-lookup"><span data-stu-id="c77f0-178">The prefix to strip from the file name.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="c77f0-179">**ачкабинетфиле**</span><span class="sxs-lookup"><span data-stu-id="c77f0-179">**achCabinetFile**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-180">Текущий CAB-файл.</span><span class="sxs-lookup"><span data-stu-id="c77f0-180">The current cabinet file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="c77f0-181">**каргв**</span><span class="sxs-lookup"><span data-stu-id="c77f0-181">**cArgv**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-182">Самораскрывающийся argc по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c77f0-182">The default self-extracting argc.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-183">**паргв**</span><span class="sxs-lookup"><span data-stu-id="c77f0-183">**pArgv**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-184">Указатель на указатель на самораскрывающийся argv по умолчанию \[ \] .</span><span class="sxs-lookup"><span data-stu-id="c77f0-184">A pointer to a pointer to the default self-extracting argv\[\].</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-185">**фдеструктиве**</span><span class="sxs-lookup"><span data-stu-id="c77f0-185">**fDestructive**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-186">Флаг, который уменьшает необходимое место на диске, если установлено значение **true**.</span><span class="sxs-lookup"><span data-stu-id="c77f0-186">A flag that minimizes the disk space needed when set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="c77f0-187">**икуррентфолдер**</span><span class="sxs-lookup"><span data-stu-id="c77f0-187">**iCurrentFolder**</span></span>
</dt> <dd>

<span data-ttu-id="c77f0-188">Если для **фдеструктиве** задано значение **true**, извлекаются только текущая папка.</span><span class="sxs-lookup"><span data-stu-id="c77f0-188">If **fDestructive** is set to **TRUE**, extract only the current folder.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c77f0-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c77f0-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c77f0-190">**делетикстрактедфилес**</span><span class="sxs-lookup"><span data-stu-id="c77f0-190">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="c77f0-191">**Распаковк**</span><span class="sxs-lookup"><span data-stu-id="c77f0-191">**Extract**</span></span>](extract.md)
</dt> </dl>

 

 
