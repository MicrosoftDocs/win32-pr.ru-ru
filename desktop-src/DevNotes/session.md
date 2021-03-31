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
# <a name="session-structure"></a>Структура сеанса

\[Эта структура содержит сведения, необходимые только при использовании функций **делетикстрактедфилес** и **Extract** , которые не поддерживаются. Эта документация предоставляется только в ознакомительных целях.\]

Структура **сеанса** содержит сведения о текущем сеансе.

## <a name="syntax"></a>Синтаксис


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



## <a name="members"></a>Члены

<dl> <dt>

**ACT**
</dt> <dd>

действие для выполнения. Этот элемент может быть одним из значений следующего перечислимого типа.

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

**хфлист**
</dt> <dd>

Маркер для списка файлов, указанных в командной строке. Этот тип данных объявляется следующим образом:

`typedef void *HFILELIST;`

</dd> <dt>

**фаллкабинетс**
</dt> <dd>

Флаг, указывающий, следует ли обрабатывать более одного CAB-файла. Если это значение равно **true**, ящики продолжения обрабатываются.

</dd> <dt>

**фоверврите**
</dt> <dd>

Флаг, указывающий, следует ли перезаписывать существующие файлы. Если это значение равно **true**, существующие файлы будут перезаписаны.

</dd> <dt>

**фнолинефид**
</dt> <dd>

Флаг, указывающий, содержит ли последний `printf` вызов символы новой строки ( `\n` ). Если это значение равно **true**, последний `printf` вызов не включал символы новой строки.

</dd> <dt>

**фселфекстракт**
</dt> <dd>

Флаг, указывающий, является ли CAB-файл самораскрывающимся. Если это значение равно **true**, CAB-файл самоизвлекается.

</dd> <dt>

**кбселфекстрактсизе**
</dt> <dd>

Длина исполняемого фрагмента (exe) самораспаковывающегося CAB-файла.

</dd> <dt>

**кбселфекстрактсизе**
</dt> <dd>

Длина части CAB-файла самораспаковывающегося архива.

</dd> <dt>

**ахфселф**
</dt> <dd>

Файлы дескрипторов CAB-файла.

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

**церрорс**
</dt> <dd>

Число ошибок, возникших во время сеанса извлечения.

</dd> <dt>

**хфди**
</dt> <dd>

Маркер контекста FDI. Этот тип данных объявляется следующим образом:

`typedef void FAR *HFDI; `

</dd> <dt>

**erf**
</dt> <dd>

Структура ошибок FDI. См. раздел [**Фош**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).

</dd> <dt>

**кфилес**
</dt> <dd>

Число обработанных файлов.

</dd> <dt>

**кбтоталбитес**
</dt> <dd>

Общее число извлеченных байтов.

</dd> <dt>

**PERR**
</dt> <dd>

Пройдите через FDI.

</dd> <dt>

**&**
</dt> <dd>

Ошибка при сбросе файла. Этот элемент может быть одним из значений следующего перечислимого типа.

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

**кбспилл**
</dt> <dd>

Размер запрошенного файла сброса.

</dd> <dt>

**ачселф**
</dt> <dd>

Имя исполняемого файла (exe).

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**ачмсг**
</dt> <dd>

Буфер форматирования сообщения.

`#define cbMAX_LINE          256`

</dd> <dt>

**ачлине**
</dt> <dd>

Буфер форматирования строки.

</dd> <dt>

**ачлокатион**
</dt> <dd>

выходной каталог.

</dd> <dt>

**ачфиле**
</dt> <dd>

Имя текущего файла, которое извлекается.

</dd> <dt>

**ачдест**
</dt> <dd>

Имя файла принудительного назначения.

</dd> <dt>

**ачкабпас**
</dt> <dd>

Путь для просмотра CAB-файла.

</dd> <dt>

**фконтинуатионкабинет**
</dt> <dd>

Флаг, указывающий, является ли текущий CAB-файл первым обработанным. Если задано значение **true**, то это не первый обработанный CAB-файл.

</dd> <dt>

**фшовресервеинфо**
</dt> <dd>

Флаг, указывающий, следует ли предоставлять сведения о резервировании. Если задано значение **true**, сведения становятся доступными.

</dd> <dt>

**фнексткабкаллед**
</dt> <dd>

Этот член позволяет определить, какие из записей **Акаб** будут использоваться, если обрабатываются все файлы в наборе CAB-файлов (**Фаллкабинет** имеет значение **true**).

</dd> <dt>

**акаб**
</dt> <dd>

Последние две записи в наборе CAB-файлов. Эта структура определяется следующим образом:

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

**ачзап**
</dt> <dd>

Префикс для удаления из имени файла.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**ачкабинетфиле**
</dt> <dd>

Текущий CAB-файл.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**каргв**
</dt> <dd>

Самораскрывающийся argc по умолчанию.

</dd> <dt>

**паргв**
</dt> <dd>

Указатель на указатель на самораскрывающийся argv по умолчанию \[ \] .

</dd> <dt>

**фдеструктиве**
</dt> <dd>

Флаг, который уменьшает необходимое место на диске, если установлено значение **true**.

</dd> <dt>

**икуррентфолдер**
</dt> <dd>

Если для **фдеструктиве** задано значение **true**, извлекаются только текущая папка.

</dd> </dl>

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**делетикстрактедфилес**](deleteextractedfiles.md)
</dt> <dt>

[**Распаковк**](extract.md)
</dt> </dl>

 

 
