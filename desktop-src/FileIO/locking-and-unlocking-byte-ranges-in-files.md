---
description: Пример кода, который показывает блокировку диапазона байтов и разблокировку с помощью функций Локкфиликс и Унлоккфиликс.
ms.assetid: 9d54fe11-b1ad-4723-a42a-00bc6dc64072
title: Блокировка и разблокировка диапазонов байтов в файлах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7789c56cea100d00168494fac97bdb46e036953c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348535"
---
# <a name="locking-and-unlocking-byte-ranges-in-files"></a><span data-ttu-id="6b1fb-103">Блокировка и разблокировка диапазонов байтов в файлах</span><span class="sxs-lookup"><span data-stu-id="6b1fb-103">Locking and Unlocking Byte Ranges in Files</span></span>

<span data-ttu-id="6b1fb-104">Несмотря на то, что система позволяет нескольким приложениям открывать файл и выполнять запись в него, приложения не должны записывать данные друг за друга.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-104">Although the system allows more than one application to open a file and write to it, applications must not write over each other's work.</span></span> <span data-ttu-id="6b1fb-105">Приложение может предотвратить эту проблему, временно заключив диапазон байтов в файле.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-105">An application can prevent this problem by temporarily locking a byte range in a file.</span></span>

<span data-ttu-id="6b1fb-106">Функции [**локкфиле**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) и [**локкфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) блокируют указанный диапазон байтов в файле.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-106">The [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile) and [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) functions lock a specified range of bytes in a file.</span></span> <span data-ttu-id="6b1fb-107">Диапазон может находиться за пределами текущего конца файла.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-107">The range may extend beyond the current end of the file.</span></span> <span data-ttu-id="6b1fb-108">Блокировка части файла предоставляет потокам блокировки монопольный доступ к указанному диапазону байтов с помощью указанного маркера файла.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-108">Locking part of a file gives the threads of the locking processes exclusive access to the specified byte range by using the specified file handle.</span></span> <span data-ttu-id="6b1fb-109">Попытки доступа к диапазону байтов, заблокированному другим процессом, всегда завершаются ошибкой.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-109">Attempts to access a byte range that is locked by another process always fail.</span></span> <span data-ttu-id="6b1fb-110">Если процесс блокировки пытается получить доступ к заблокированному диапазону байтов с помощью второго маркера файла, попытка будет неудачной.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-110">If the locking process attempts to access a locked byte range through a second file handle, the attempt fails.</span></span>

> [!Note]  
> <span data-ttu-id="6b1fb-111">Размещенные в памяти файлы не поддерживаются с блокировками диапазона байтов.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-111">Memory mapped files are not supported with byte range locks.</span></span>

 

<span data-ttu-id="6b1fb-112">Функция [**локкфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) позволяет приложению указать один из двух типов блокировок.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-112">The [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) function allows an application to specify one of two types of locks.</span></span> <span data-ttu-id="6b1fb-113">*Монопольная блокировка* запрещает всем остальным процессам доступ для чтения и записи к указанному диапазону байтов файла.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-113">An *exclusive lock* denies all other processes both read and write access to the specified byte range of a file.</span></span> <span data-ttu-id="6b1fb-114">*Общая блокировка* запрещает всем процессам доступ на запись к указанному диапазону байтов файла, включая процесс, который сначала блокирует диапазон байтов.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-114">A *shared lock* denies all processes write access to the specified byte range of a file, including the process that first locks the byte range.</span></span> <span data-ttu-id="6b1fb-115">Это можно использовать для создания в файле диапазона байтов, доступного только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-115">This can be used to create a read-only byte range in a file.</span></span>

<span data-ttu-id="6b1fb-116">Приложение разблокирует диапазон байтов с помощью функции [**унлоккфиле**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) или [**унлоккфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfileex) и должен разблокировать все заблокированные области перед закрытием файла.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-116">An application unlocks the byte range by using the [**UnlockFile**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfile) or [**UnlockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfileex) function and should unlock all locked areas before closing a file.</span></span>

<span data-ttu-id="6b1fb-117">Пример использования [**локкфиле**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile)см. [в разделе Добавление одного файла в другой файл](appending-one-file-to-another-file.md).</span><span class="sxs-lookup"><span data-stu-id="6b1fb-117">For an example of using [**LockFile**](/windows/desktop/api/FileAPI/nf-fileapi-lockfile), see [Appending One File to Another File](appending-one-file-to-another-file.md).</span></span>

<span data-ttu-id="6b1fb-118">В следующих примерах показано, как использовать [**локкфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex).</span><span class="sxs-lookup"><span data-stu-id="6b1fb-118">The following examples show how to use [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex).</span></span> <span data-ttu-id="6b1fb-119">Первый пример представляет собой простую демонстрацию для создания файла, записи в него данных, а затем блокировки раздела в середине.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-119">The first example is a simple demonstration to create a file, write some data to it, and then lock a section in the middle.</span></span>

<span data-ttu-id="6b1fb-120">**Примечание**  .  В этом примере данные после блокировки файла не изменяются.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-120">**Note**  This example does not change the data after the file is locked.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>

#define NUMWRITES 10
#define TESTSTRLEN 11

const char TestData[NUMWRITES][TESTSTRLEN] = 
{ 
    "TestData0\n",
    "TestData1\n",
    "TestData2\n",
    "TestData3\n",
    "TestData4\n",
    "TestData5\n",
    "TestData6\n",
    "TestData7\n",
    "TestData8\n",
    "TestData9\n"
};

int main(int argc, char *argv[])
{
    BOOL fSuccess = FALSE;

    // Create the file, open for both read and write.
    HANDLE hFile = CreateFile(TEXT("datafile.txt"),
                       GENERIC_READ | GENERIC_WRITE,
                       0,          // open with exclusive access
                       NULL,       // no security attributes
                       CREATE_NEW, // creating a new temp file
                       0,          // not overlapped index/O
                       NULL);
    
    if (hFile == INVALID_HANDLE_VALUE) 
    {
        // Handle the error.
        printf("CreateFile failed (%d)\n", GetLastError());
        return (1);
    }

    // Write some data to the file.
    DWORD dwNumBytesWritten = 0;

    for (int i=0; i<NUMWRITES; i++)
    {
        fSuccess = WriteFile(hFile,
                             TestData[i],
                             TESTSTRLEN,
                             &dwNumBytesWritten,
                             NULL);  // sync operation.
        if (!fSuccess) 
        {
           // Handle the error.
           printf("WriteFile failed (%d)\n", GetLastError());
           return (2);
        }
    } 

    FlushFileBuffers(hFile);

    // Lock the 4th write-section.  
    // First, set up the Overlapped structure with the file offset 
    // required by LockFileEx, three lines in to the file.
    OVERLAPPED sOverlapped;
    sOverlapped.Offset = TESTSTRLEN * 3;
    sOverlapped.OffsetHigh = 0;

    // Actually lock the file.  Specify exclusive access, and fail 
    // immediately if the lock cannot be obtained.
    fSuccess = LockFileEx(hFile,         // exclusive access, 
                          LOCKFILE_EXCLUSIVE_LOCK | 
                          LOCKFILE_FAIL_IMMEDIATELY,
                          0,             // reserved, must be zero
                          TESTSTRLEN,    // number of bytes to lock
                          0,
                          &sOverlapped); // contains the file offset
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("LockFileEx failed (%d)\n", GetLastError());
       return (3);
    }
    else printf("LockFileEx succeeded\n");

    /////////////////////////////////////////////////////////////////
    // Add code that does something interesting to locked section,  /
    // which should be line 4                                       /
    /////////////////////////////////////////////////////////////////

    // Unlock the file.
    fSuccess = UnlockFileEx(hFile, 
                            0,             // reserved, must be zero
                            TESTSTRLEN,    // num. of bytes to unlock
                            0,
                            &sOverlapped); // contains the file offset
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("UnlockFileEx failed (%d)\n", GetLastError());
       return (4);
    }
    else printf("UnlockFileEx succeeded\n");

    // Clean up handles, memory, and the created file.
    fSuccess = CloseHandle(hFile);
    if (!fSuccess) 
    {
       // Handle the error.
       printf ("CloseHandle failed (%d)\n", GetLastError());
       return (5);
    }

    fSuccess = DeleteFile(TEXT("datafile.txt"));
    if (!fSuccess) 
    {
        // Handle the error.
       printf ("DeleteFile failed (%d)\n", GetLastError());
       return (6);
    }
    return (0);
}
```



<span data-ttu-id="6b1fb-121">Следующий пример представляет собой расширенную демонстрацию блокировки диапазона байтов с использованием нескольких потоков и простой базы данных, выполняющей случайные операции с одним файлом данных.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-121">The following example is an advanced demonstration of byte range locking, using multiple threads and a simple database performing random operations on a single data file.</span></span> <span data-ttu-id="6b1fb-122">Дополнительные сведения см. в комментариях к внедренному коду и в разделе, следующем за образцом кода.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-122">For more information, see the embedded code comments and the section following the sample code.</span></span>


```C++
// THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF
// ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO
// THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A
// PARTICULAR PURPOSE.
//
// Copyright (C) Microsoft. All rights reserved

#define UNICODE
#define _CRT_RAND_S
#include <stdlib.h>
#include <windows.h>

#include <stdio.h>

#include <malloc.h>
#include <conio.h>
#include <process.h>
#include <winioctl.h>

#define RECORD_SIZE 0x300
#define NUM_RECORDS 0x1000
#define NUM_THREADS 8

#define NUM_FILEOPS 500

#define BITMAP_SIZE ((NUM_RECORDS) / 8)
#define DATA_SIZE   ((RECORD_SIZE) - sizeof(RECORD_HEADER))

#define MSG_PRINTF(S,...) wprintf(L"[THREAD_ID %d] " S, \
    GetCurrentThreadId(), \
    __VA_ARGS__)

#if defined BRLS_DEBUG

#define DBG_PRINTF(S,...) wprintf(L"[THREAD_ID %d] " S, \
    GetCurrentThreadId(), \
    __VA_ARGS__)

#else

#define DBG_PRINTF(...)
#define PrintBitmap(...)

#endif


#define MASTER_RECORD_TYPE_CODE 'rtsM'
#define DATA_RECORD_TYPE_CODE   'ataD'


//
//  Record type definitions.
//
typedef struct _RECORD_HEADER {
    ULONG TypeCode;     // Either MASTER_RECORD_TYPE_CODE or DATA_RECORD_TYPE_CODE.
    ULONG SeqNumber;    // Starts at 1 and is incremented every time contents are modified.
} RECORD_HEADER;

typedef struct _MASTER_RECORD {
    RECORD_HEADER Header;
    BYTE Bitmap[BITMAP_SIZE];  // A bitmap indicating which records are allocated.
} MASTER_RECORD;

typedef struct _DATA_RECORD {
    RECORD_HEADER Header;
    BYTE Data[DATA_SIZE];       // Record raw data.
} DATA_RECORD;


//
//  Types of I/O for IoRecord.
//
typedef enum {
    IoRead,
    IoWrite,
    IoLock,
    IoUnlock
} IO_TYPE;


//
//  Types of operations for OperateOnRecord.
//
typedef enum {
    CreateRecord = 0,
    DeleteRecord,
    ModifyRecord,
    MaxOprRecord
} OPERATION;


//
//  Parameter block for I/Os passed to IoRecord.
//
typedef struct _IO_PARAM {
    IO_TYPE Type;
    union _IO_PARAM_PARAMS {
        struct {
            PVOID Data;
            ULONG RecSize;
        } IoInfo;
        struct {
            BOOL Exclusive;
        } LockInfo ;
    } Params;
} IO_PARAM, *PIO_PARAM;

void ErrorExitThread()
//
//  This function is called immediately after an unrecoverable error is logged.
//
{
    MSG_PRINTF(L"An error has been logged, calling ExitThread.\n");
    ExitThread(1);
}

BOOL IoRecord(HANDLE hFile, ULONG RecNumber, PIO_PARAM pIoParam)
//
//  This function performs I/O (read, write, lock or unlock) in a record, according
//  to the parameters passed in the IO_PARAM block.
//
//  Arguments:
//      hFile       - Handle to the file containing the records.
//      RecNumber   - Number of the record to be operated on.
//      pIoParam    - Pointer to IO_PARAM structure.
//
//  Return value:
//      TRUE if the I/O succeeded, FALSE if not.
//
{
    OVERLAPPED Overlapped;
    BOOL Result;
    ULARGE_INTEGER RecOffset;
    DWORD NumBytes;

    //  Initialize Overlapped.
    SecureZeroMemory(&Overlapped, sizeof(OVERLAPPED));
    Overlapped.hEvent = CreateEvent(NULL,
        FALSE,
        FALSE,
        NULL);

    if (NULL == Overlapped.hEvent) 
    {
        MSG_PRINTF(L"CreateEvent for Overlapped.hEvent failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Calculate record position.
    RecOffset.QuadPart = RecNumber * RECORD_SIZE;

    Overlapped.Offset     = RecOffset.LowPart;
    Overlapped.OffsetHigh = RecOffset.HighPart;

    //  Issue the operation.
    switch (pIoParam->Type) 
    {
    case IoLock:
        Result = LockFileEx(hFile,
            pIoParam->Params.LockInfo.Exclusive ? LOCKFILE_EXCLUSIVE_LOCK : 0,
            0,
            RECORD_SIZE,
            0,
            &Overlapped);
        break;
    case IoUnlock:
        Result = UnlockFileEx(hFile,
            0,
            RECORD_SIZE,
            0,
            &Overlapped);
        break;
    case IoRead:
        Result = ReadFile(hFile,
            pIoParam->Params.IoInfo.Data,
            pIoParam->Params.IoInfo.RecSize,
            NULL,
            &Overlapped);
        break;
    case IoWrite:
        Result = WriteFile(hFile,
            pIoParam->Params.IoInfo.Data,
            pIoParam->Params.IoInfo.RecSize,
            NULL,
            &Overlapped);
        break;
    default:
        Result = FALSE;
        break;
    }

    if (!Result) 
    {
        if (GetLastError() == ERROR_IO_PENDING) 
        {
            //  Wait until the operation finishes.
            if (GetOverlappedResult(hFile,
                &Overlapped,
                &NumBytes,
                TRUE) == FALSE) 
            {
                MSG_PRINTF(L"GetOverlappedResult for Overlapped.hEvent failed with error 0x%08x.\n", 
                    GetLastError());
                ErrorExitThread();
            }
            Result = TRUE;
        } else {
            MSG_PRINTF(L"IoRecord failed with error 0x%08x. Failure passed to caller.\n", 
                GetLastError());
        }
    }
    CloseHandle(Overlapped.hEvent);
    return Result;
}


//
//  The following functions are wrappers around IoRecord, they just set the correct
//  parameters in the IO_PARAM block to correspond to the requested operation and
//  pass that to IoRecord.
//
BOOL ReadRecord(HANDLE hFile, ULONG RecNumber, PVOID Record, ULONG RecSize)
{
    IO_PARAM IoParam;

    IoParam.Type                  = IoRead;
    IoParam.Params.IoInfo.Data    = Record;
    IoParam.Params.IoInfo.RecSize = RecSize;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL WriteRecord(HANDLE hFile, ULONG RecNumber, PVOID Record, ULONG RecSize)
{
    IO_PARAM IoParam;

    IoParam.Type                  = IoWrite;
    IoParam.Params.IoInfo.Data    = Record;
    IoParam.Params.IoInfo.RecSize = RecSize;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL LockRecord(HANDLE hFile, ULONG RecNumber, BOOL Exclusive)
{
    IO_PARAM IoParam;

    IoParam.Type                      = IoLock;
    IoParam.Params.LockInfo.Exclusive = Exclusive;

    return IoRecord(hFile, RecNumber, &IoParam);
}


BOOL UnlockRecord(HANDLE hFile, ULONG RecNumber)
{
    IO_PARAM IoParam;

    IoParam.Type = IoUnlock;

    return IoRecord(hFile, RecNumber, &IoParam);
}


ULONG ReserveFirstFreeRecord(BYTE* Bitmap)
//
//  This function iterates through the bitmap and reserves the first free record
//  it can find in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//
//  Return value:
//      Either zero, if there are no free records, or the position of the record
//      that was just reserved.
//          
{
    int i;
    BYTE Bit = 1;

    for (i = 0; i < NUM_RECORDS; i++) 
    {
        if (Bitmap[i / 8] & Bit) 
        {
            Bit <<= 1;
            if (Bit == 0) { Bit = 1; }
        } else {
            Bitmap[i / 8] |= Bit;
            return i;
        }
    }

    return 0;
}


BOOL TestBit(BYTE* Bitmap, ULONG Bit)
//
//  This function tests if a given bit is set in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//      Bit     - Position of the bit in the bitmap.
//
//  Return value:
//      TRUE if the bit is set, FALSE otherwise.
//
{
    ULONG Byte = Bit / 8;

    Bit = Bit % 8;

    return (BOOL)(Bitmap[Byte] & (1 << Bit));
}


void ClearBit(BYTE* Bitmap, ULONG Bit)
//
//  This function clears a given bit in the bitmap.
//
//  Arguments:
//      Bitmap  - Pointer to the bitmap.
//      Bit     - Position of the bit in the bitmap.
//
{
    ULONG Byte = Bit / 8;

    Bit = Bit % 8;

    Bitmap[Byte] &= ~(1 << Bit);
}


#ifdef BRLS_DEBUG
void PrintBitmap(BYTE* Bitmap)
//
//   This function prints the whole bitmap, for debugging purposes.
//
//   Arguments:
//      Bitmap  - Pointer to the bitmap.
//
{
    int i;

    for (i = 0; i < BITMAP_SIZE; i++) 
    {
        wprintf(L"%1x", Bitmap[i]);
    }

    wprintf(L"\n");
}
#endif


void InitRecord(RECORD_HEADER* Record, BOOL Master, ULONG SeqNumber)
//
//  This function initializes a in-memory record structure with the correct
//  type code and sequence number. In case of the Master Record, the bitmap
//  is initialized too.
//
//  Arguments:
//      Record      - Pointer to the record structure.
//      Master      - TRUE if this is a Master Record, FALSE otherwise.
//      SeqNumber   - Initial sequence number.
//
{
    ULONG RecSize   = Master ? sizeof(MASTER_RECORD)   : sizeof(DATA_RECORD);
    ULONG TypeCode  = Master ? MASTER_RECORD_TYPE_CODE : DATA_RECORD_TYPE_CODE;

    SecureZeroMemory(Record, RecSize);

    Record->TypeCode  = TypeCode;
    Record->SeqNumber = Master ? 0 : SeqNumber;

    if (Master) 
    {
        ((MASTER_RECORD*)Record)->Bitmap[0] = 1;
    }
}


DATA_RECORD* PrepareRecord(ULONG SeqNumber)
//
//  This function allocates a new in-memory record structure and initializes it
//  as a brand new data record.
//
//  Arguments:
//      SeqNumber   - Sequence number with which to initialize the record.
//
//  Return value:
//      Pointer to the record structure.
//
{
    DATA_RECORD* Record = NULL;

    Record = (DATA_RECORD*) malloc(sizeof(DATA_RECORD));

    if (Record == NULL) 
    {
        MSG_PRINTF(L"Critical error: malloc for CreateRecord failed.\n");
        ErrorExitThread();
    }

    InitRecord((RECORD_HEADER*)Record, FALSE, SeqNumber);

    return Record;
}


void WriteData(DATA_RECORD* Record)
//
//  This function fills a in-memory data record structure with random data.
//  Errors do not interrupt execution.
//
//  Arguments:
//      Record  - Pointer to the record structure.
//
{
    PUINT iData;
    int i;
    errno_t err;

    iData = (PUINT)Record->Data;

    for (i = 0; i < DATA_SIZE; i += sizeof(ULONG), iData++) 
    {
        err = rand_s(iData);
        if (err != 0) 
        {
            MSG_PRINTF(L"rand_s for WriteData failed with error 0x%08x, continuing execution.\n", 
                err);
        }
    }
}


BOOL OperateOnRecord(HANDLE hFile, PULONG RecNumber, OPERATION Operation)
//
//  This function executes a high-level operation in a record (create, modify or delete).
//
//  Arguments:
//      hFile       - Handle to the file containing the record to be operated on.
//      RecNumber   - Pointer to a ULONG that either will receive the number of the
//                    record created by this operation or just contains the number
//                    of the record that will be modified or deleted.
//      Operation   - Operation to be performed (CreateRecord, ModifyRecord or
//                    DeleteRecord).
//
//  Return value:
//      TRUE if the operation succeeded, FALSE otherwise.
//
{
    BOOL Result;
    BOOL Exists;
    BOOL ExclusiveLock;
    MASTER_RECORD MasterRecord;
    DATA_RECORD*  Record;

    //  Fail operations on Master Record.
    if ((Operation != CreateRecord) && (*RecNumber == 0)) 
    {
        MSG_PRINTF(L"Cannot operate on Master Record.\n");
        return FALSE;
    }

    //  Lock Master Record. If we're just modifying a record, we can get a
    //  shared lock.
    ExclusiveLock = (Operation != ModifyRecord);

    Result = LockRecord(hFile, 0, ExclusiveLock);
    if (!Result) 
    {
        MSG_PRINTF(L"LockRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Read in Master Record.
    Result = ReadRecord(hFile, 0, (PVOID)&MasterRecord, sizeof(MASTER_RECORD));
    if (!Result) 
    {
        MSG_PRINTF(L"ReadRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    if (MasterRecord.Header.TypeCode != MASTER_RECORD_TYPE_CODE) 
    {
        MSG_PRINTF(L"Master Record corruption error: wrong typecode!\n");
        ErrorExitThread();
    }

    DBG_PRINTF(L"MasterRecord bitmap (before): ");
    PrintBitmap(MasterRecord.Bitmap);

    if (Operation != CreateRecord) 
    {
        //  Test the bit in the bitmap corresponding to this record.
        Exists = TestBit(MasterRecord.Bitmap, *RecNumber);

        //  Clear the bit if we are deleting the record.
        if ((Operation == DeleteRecord) && Exists) 
        {
            ClearBit(MasterRecord.Bitmap, *RecNumber);
        }

    } else {

        //  Reserve the first free record.
        *RecNumber = ReserveFirstFreeRecord(MasterRecord.Bitmap);

        if (*RecNumber != 0) 
        {
            Exists = TRUE;
        } else {
            Exists = FALSE;
            MSG_PRINTF(L"File is full!\n");
        }
    }

    DBG_PRINTF(L"MasterRecord bitmap (after): ");
    PrintBitmap(MasterRecord.Bitmap);

    if ((Operation != ModifyRecord) && Exists) 
    {
        //  Update the Master Record's sequence number.
        MasterRecord.Header.SeqNumber++;

        //  Write Master Record down.
        Result = WriteRecord(hFile, 0, (PVOID)&MasterRecord, sizeof(MASTER_RECORD));
        if (!Result) 
        {
            MSG_PRINTF(L"WriteRecord (MasterRecord) for CreateRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }
    }

    //  Unlock Master Record.
    Result = UnlockRecord(hFile, 0);
    if (!Result) 
    {
        MSG_PRINTF(L"UnlockRecord (MasterRecord) for OperateOnRecord failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    if (!Exists) 
    {
        if (*RecNumber != 0) 
        {
            MSG_PRINTF(L"Record %d not present!\n", *RecNumber);
        }
        return FALSE;
    }

    //  For record deletion, processing is done and skip to write.
    //  Otherwise, there is more to do.
    if (Operation != DeleteRecord) 
    {
        //  Prepare a new record in memory.
        Record = PrepareRecord(1);

        //  Lock the record exclusively.
        Result = LockRecord(hFile, *RecNumber, TRUE);
        if (!Result) 
        {
            MSG_PRINTF(L"LockRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        if (Operation == ModifyRecord) 
        {
            //  Read the record in from the file if we're modifying it.
            Result = ReadRecord(hFile, *RecNumber, Record, RECORD_SIZE);
            if (!Result) 
            {
                MSG_PRINTF(L"ReadRecord for ModifyRecord failed with error 0x%08x.\n", 
                    GetLastError());
                ErrorExitThread();
            }

            //  Update record sequence number.
            Record->Header.SeqNumber++;
        }

        //  Write to the in-memory record.
        WriteData(Record);

        //  Write the record to the file.
        Result = WriteRecord(hFile, *RecNumber, Record, RECORD_SIZE);
        if (!Result) 
        {
            MSG_PRINTF(L"WriteRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        //  Unlock the record.
        Result = UnlockRecord(hFile, *RecNumber);
        if (!Result) 
        {
            MSG_PRINTF(L"UnlockRecord for ModifyRecord failed with error 0x%08x.\n", 
                GetLastError());
            ErrorExitThread();
        }

        //  Free the record structure.
        free(Record);
    }

    return TRUE;
}


ULONG RandomOption(ULONG NumOpts)
//
//  This function returns a random number between 0 and (NumOpts - 1).
//  It basically is a random option select.
//
//  Arguments:
//      NumOpts - Number of options to choose from.
//
//  Return value:
//      A random option (random ULONG x | 0 <= x < NumOpts).
//
{
    UINT Random;
    errno_t err;

    err = rand_s(&Random);
    if (err != 0) 
    {
        MSG_PRINTF(L"rand_s for RandomOption failed with error 0x%08x\n", 
            err);
    }

    return Random % NumOpts;
}


DWORD WINAPI WorkerThread(PVOID data)
//
//  This is the tight loop executed by each of the threads operating in the file.
//  Each thread has its own handle to the same file. After obtaining that handle,
//  they go into a tight loop in which a record number and a record operation are
//  chosen at random and that operation is then performed in that record.
//
//  Arguments:
//      Data    - PVOID to a string containing the file name (so it can be opened).
//
//  Return value:
//      It should not return.
//
{
    HANDLE hFile;
    LPCWSTR FileName = (LPCWSTR)data;
    ULONG RecNumber;
    OPERATION Operation;
    BOOL Result;

    UINT i;

    hFile = CreateFile(FileName,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        FILE_ATTRIBUTE_NORMAL | FILE_FLAG_OVERLAPPED,
        NULL);

    if (hFile == INVALID_HANDLE_VALUE) 
    {
        MSG_PRINTF(L"CreateFile failed with error 0x%08x.\n", 
            GetLastError());
        ErrorExitThread();
    }

    //  Main loop for doing the random operations.
    for (i = 0; i < NUM_FILEOPS; i++) 
    {
        RecNumber = RandomOption(NUM_RECORDS);
        Operation = (OPERATION)RandomOption(MaxOprRecord);

        //  Output message as to what action is being attempted.
        switch (Operation) 
        {
        case CreateRecord:
            MSG_PRINTF(L"attempting record creation.\n");
            break;
        case ModifyRecord:
            MSG_PRINTF(L"attempting modification of record %d.\n", RecNumber);
            break;
        case DeleteRecord:
            MSG_PRINTF(L"attempting deletion of record %d.\n", RecNumber);
            break;
        }

        //  Perform the actual operation and handle the result, 
        //  then loop again until done.
        Result = OperateOnRecord(hFile, &RecNumber, Operation);

        if (Result) 
        {
            switch (Operation) 
            {
            case CreateRecord:
                MSG_PRINTF(L"created record %d.\n", RecNumber);
                break;

            case ModifyRecord:
                MSG_PRINTF(L"modified record %d.\n", RecNumber);
                break;

            case DeleteRecord:
                MSG_PRINTF(L"deleted record %d.\n", RecNumber);
                break;
            }
        }
    }

    CloseHandle(hFile);
    MSG_PRINTF(L"%d file operations complete. Exiting thread.\n", i);

    return 0;
}


BOOL InitNewFile(LPCWSTR FileName)
//
//  This function initializes a file with records. If the file already exists, it
//  just returns, assuming it has a valid Master Record on it. If it does not 
//  exist, a brand new file is created and initialized with a clean Master Record.
//
//  Arguments:
//      FileName    - Name of the file to be initialized.
//
//  Return value:
//      TRUE if the initialization succeeded, FALSE otherwise.
//      
{
    HANDLE hFile;
    MASTER_RECORD MasterRecord;
    DWORD BytesWritten;
    DWORD Result;

    //
    //  Create the file or open existing.
    //
    hFile = CreateFile(FileName,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_ALWAYS,
        FILE_ATTRIBUTE_NORMAL,
        NULL);

    if (INVALID_HANDLE_VALUE == hFile) 
    {
        MSG_PRINTF(L"CreateFile failed with error 0x%08x.\n", 
            GetLastError());
        return FALSE;
    } 
    else if (ERROR_ALREADY_EXISTS == GetLastError()) 
    {
        //  This is ok, simply assume it's a valid file.
        //  Note that this does not actually test that the file
        //  is valid for this application. That error is caught later.
        CloseHandle(hFile);
        return TRUE;
    } //  The implied "else" is that the handle is a good one.


    InitRecord((RECORD_HEADER*)&MasterRecord, TRUE, 0);

    Result = WriteFile(hFile,
        &MasterRecord,
        sizeof(MASTER_RECORD),
        &BytesWritten,
        NULL);

    if (!Result) 
    {
        MSG_PRINTF(L"WriteFile failed with error 0x%08x.\n", 
            GetLastError());
    }

    CloseHandle(hFile);

    return Result;
}


int __cdecl wmain(int argc, LPCWSTR argv[])
//
//  Main function. Reads file name from command line argument, initializes the file
//  and starts the worker threads, waiting for them to return.
//
{
    HANDLE gThread[NUM_THREADS];

    DWORD IdThread;
    DWORD ResultCode;
    LPCWSTR FileName = NULL;

    if (argc != 2) {
        wprintf(L"Invalid number of arguments!\n");
        wprintf(L"Usage: %ws file_name\n", argv[0]);
        return -1;
    }

    FileName = argv[1];

    if (!InitNewFile(FileName))
    {
        wprintf(L"Unable to initialize the data file %ws.\n", FileName);
    }

    wprintf(L"Main thread creating %d worker threads for processing.\n", 
        NUM_THREADS);
    for (int i = 0; i < NUM_THREADS; i++) 
    {
        gThread[i] = CreateThread(NULL,
            0,
            (LPTHREAD_START_ROUTINE)WorkerThread,
            (PVOID)FileName,
            0,
            &IdThread);
    }

    wprintf(L"Main thread waiting for worker threads to exit...\n");

    ResultCode = WaitForMultipleObjects(
        NUM_THREADS,
        gThread,
        TRUE,
        INFINITE);

    wprintf(L"WaitForMultipleObjects returned 0x%08x, execution complete.\n",
        ResultCode);

    // Do some clean-up.
    for (int i = 0; i < NUM_THREADS; i++) 
    {
        CloseHandle(gThread[i]);
    }

    return 0;
}
```



<span data-ttu-id="6b1fb-123">Этот пример представляет собой консольное приложение Windows, которое выполняет несколько одновременных обращений к файлу, с учетом блокировок диапазона байтов с помощью простой базы данных, состоящей из нескольких записей фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-123">This sample is a Windows console application that executes multiple concurrent accesses to a file, all coordinated by byte range locks using a simple database, composed of several records of a fixed size.</span></span> <span data-ttu-id="6b1fb-124">Обратите внимание, что значение true конкурренце зависит от того, сколько ядер процессора существует в главной системе.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-124">Note that true concurrence depends on how many processor cores exist on the host system.</span></span>

<span data-ttu-id="6b1fb-125">Все записи имеют первые два общих поля: код типа и порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-125">All records have the first two fields in common: a type code and a sequence number.</span></span> <span data-ttu-id="6b1fb-126">Код типа — это один из двух кодов: код "МСТР" относится к типу **главной \_ записи** , а код "данные" ссылается на тип **\_ записи данных** .</span><span class="sxs-lookup"><span data-stu-id="6b1fb-126">The type code is one of two codes: The "Mstr" code refers to the **MASTER\_RECORD** type, and the "Data" code refers to a **DATA\_RECORD** type.</span></span> <span data-ttu-id="6b1fb-127">Может существовать только одна **Главная \_ запись** и ноль или более **\_ записей данных**.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-127">There can be only one **MASTER\_RECORD** and zero or more **DATA\_RECORD** s.</span></span> <span data-ttu-id="6b1fb-128">В этом примере данные, содержащиеся в записях данных, создаются случайным образом.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-128">For this example, data contained in the data records is randomly generated.</span></span> <span data-ttu-id="6b1fb-129">Второе поле, порядковый номер, увеличивается при каждом изменении записи.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-129">The second field, the sequence number, is incremented every time a record is modified.</span></span>

<span data-ttu-id="6b1fb-130">После начала выполнения, если файл данных еще не существует, он создается и инициализируется функцией **инитневфиле** .</span><span class="sxs-lookup"><span data-stu-id="6b1fb-130">When execution begins, if the data file does not already exist, it is created and initialized by the **InitNewFile** function.</span></span> <span data-ttu-id="6b1fb-131">Функция **инитневфиле** записывает запись типа Master с пустым битовым изображением в начале.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-131">The **InitNewFile** function writes a record of type Master with an empty bitmap at the beginning.</span></span> <span data-ttu-id="6b1fb-132">Если файл уже существует, он открывается; Предполагается наличие допустимой главной записи в начале.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-132">If the file already exists, it is opened; it is assumed to have a valid Master record at the beginning.</span></span>

<span data-ttu-id="6b1fb-133">После того как файл успешно создан или успешно открыт, запущено несколько рабочих потоков, и все они выполняют цикл, в котором операция и запись выбираются случайным образом, а затем выполняется попытка выполнить эту операцию над этой записью.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-133">After the file is either successfully created or successfully opened, multiple worker threads are started, and all of them run a loop in which an operation and a record are chosen at random and then that operation is attempted on that record.</span></span> <span data-ttu-id="6b1fb-134">Так как эти операции являются случайными, не все из них выполняются, но не обязательно являются ошибками.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-134">Because these operations are random, not all of them succeed, but are not necessarily errors.</span></span> <span data-ttu-id="6b1fb-135">Соответствующие сведения о состоянии записываются в консоль.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-135">Appropriate status information is logged to the console.</span></span>

<span data-ttu-id="6b1fb-136">Возможны следующие операции: создание новой записи, изменение существующей записи или удаление существующей записи.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-136">The possible operations are as follows: creation of a new record, modification of an existing record, or deletion of an existing record.</span></span> <span data-ttu-id="6b1fb-137">Операция создания просматривает точечный рисунок, чтобы найти первую свободную запись и выделить эту запись в качестве новой записи.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-137">The creation operation looks at the bitmap to find the first free record and allocates that record as the new record.</span></span> <span data-ttu-id="6b1fb-138">Операция изменения считывает битовую карту, чтобы проверить факт существования этой записи, и, если это так, изменяет эту запись.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-138">The modification operation reads the bitmap to see whether that record actually exists and, if so, modifies that record.</span></span> <span data-ttu-id="6b1fb-139">Операция удаления очищает бит в битовой карте, соответствующей записи, освобождая пространство, занимаемое записью для будущего выделения.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-139">The deletion operation clears the bit in the bitmap corresponding to the record, freeing the space that record occupied for future allocation.</span></span> <span data-ttu-id="6b1fb-140">Кроме того, эти операции делятся на две части: доступ к Мастеррекорд, где хранятся метаданные, и доступ к самой записи данных.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-140">Further, these operations are split in two parts: access to the MasterRecord, where the metadata is stored, and access to the data record itself.</span></span>

<span data-ttu-id="6b1fb-141">Поскольку они записывают данные в записи данных, операции создания записей и изменения записей являются единственными, требующими доступа к записи данных.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-141">Because they write data to the data records, the record creation and record modification operations are the only ones that require data record access.</span></span> <span data-ttu-id="6b1fb-142">По этой причине область, охваченная записью, блокируется исключительно до выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-142">For that reason, the region covered by the record is locked exclusively prior to the operation being performed.</span></span> <span data-ttu-id="6b1fb-143">Операции создания и удаления изменяют точечный рисунок, поэтому им нужно заблокировать только главную запись.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-143">The creation and deletion operations modify the bitmap, so they need to lock the Master record exclusively.</span></span> <span data-ttu-id="6b1fb-144">Однако операциям изменения записи требуется только чтение точечного рисунка, а не запись в него, чтобы проверить, существует ли файл.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-144">However, record modification operations only need to read the bitmap, not write to it, in order to verify whether the file exists.</span></span> <span data-ttu-id="6b1fb-145">Для этой операции главной записи требуется только блокировка общего диапазона байтов.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-145">For that operation, the Master record needs only a shared byte range lock.</span></span>

<span data-ttu-id="6b1fb-146">Монопольные блокировки диапазона байтов предотвращают доступ к файлу для чтения и записи из всех других дескрипторов, и именно поэтому они используются при записи в запись.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-146">Exclusive byte range locks prevent both read and write access from all other handles to the file, and that's the reason why they are used when writing to a record.</span></span> <span data-ttu-id="6b1fb-147">С другой стороны, блокировка общего диапазона байтов предотвращает доступ на запись из всех дескрипторов, включая дескриптор, который владеет блокировкой, но разрешает доступ для чтения из всех.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-147">On the other hand, a shared byte range lock prevents write access from all handles, including the handle owning the lock, but allows read access from all of them.</span></span>

<span data-ttu-id="6b1fb-148">Чтобы продемонстрировать использование блокировок диапазона байтов с файлом, все операции ввода-вывода в этом примере, за исключением создания инициализации файла, выполняются с помощью асинхронного маркера файла.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-148">To demonstrate the use of byte range locks with the file, all I/O in this sample, other than new file initialization, is done via an asynchronous file handle.</span></span> <span data-ttu-id="6b1fb-149">Это можно увидеть в функции **иорекорд** в вариантах **иолокк** и **иаунлокк** в операторе switch.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-149">This can be seen in the **IoRecord** function in the **IoLock** and **IoUnlock** cases within the switch statement.</span></span> <span data-ttu-id="6b1fb-150">Функции [**локкфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) и [**унлоккфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfileex) используются с перекрывающейся моделью ввода-вывода путем передачи [**перекрывающейся**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) структуры на них со смещением для начала заблокированного диапазона и события, которое будет сигнальным после предоставления блокировки на этот диапазон, если только функция не возвращает значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-150">The [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex) and [**UnlockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-unlockfileex) functions are used with the overlapped I/O model by passing an [**OVERLAPPED**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) structure to them with the offset for the start of the locked range, and an event that will be signaled after the lock over that range is granted unless the function returns immediately.</span></span>

<span data-ttu-id="6b1fb-151">После выполнения асинхронного запроса ввода-вывода следующая операция в функции **иорекорд** будет ожидать выполнения операции в строке.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-151">After issuing the asynchronous I/O request, the next operation in the **IoRecord** function is to wait for the operation in-line.</span></span> <span data-ttu-id="6b1fb-152">Это часто является неоптимальным сценарием, если требуется максимальная производительность, и используется для простоты.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-152">This is often a sub-optimal scenario when maximum performance is desired, and is used here for the sake of simplicity.</span></span> <span data-ttu-id="6b1fb-153">В рабочих приложениях предпочтительнее использовать [порты завершения ввода-вывода](i-o-completion-ports.md) или аналогичные механизмы, так как они выпускают потоки для выполнения других операций обработки в то время, когда операция ввода-вывода завершается.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-153">In production applications, the use of [I/O completion ports](i-o-completion-ports.md) or similar mechanisms is preferred because it releases threads to do other processing while the I/O completes.</span></span>

<span data-ttu-id="6b1fb-154">Пример заканчивается после выполнения случайных операций **NUM \_ филеопс** .</span><span class="sxs-lookup"><span data-stu-id="6b1fb-154">The sample ends after executing **NUM\_FILEOPS** random operations.</span></span> <span data-ttu-id="6b1fb-155">Каждый поток будет регистрировать свое состояние завершения как условие ошибки или нормальное завершение.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-155">Each thread will log its termination status as either an error condition or normal termination.</span></span> <span data-ttu-id="6b1fb-156">Обратите внимание, что не все потоки будут завершаться в одно и то же время в зависимости от количества ядер процессора в системе размещения и скорости подсистемы ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="6b1fb-156">Note that not all threads will end at the same time, depending on how many processor cores the host system has and the speed of the I/O subsystem.</span></span>

 

 



