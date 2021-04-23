---
description: В следующем примере демонстрируется использование API сжатия в блочном режиме.
ms.assetid: 7483BCE4-3B85-4659-98E3-670D2F7EE52D
title: Использование API сжатия в блочном режиме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddd1ecaec03d332262ffb24462e73a9fcb789d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142634"
---
# <a name="using-the-compression-api-in-block-mode"></a><span data-ttu-id="935ca-103">Использование API сжатия в блочном режиме</span><span class="sxs-lookup"><span data-stu-id="935ca-103">Using the Compression API in block mode</span></span>

<span data-ttu-id="935ca-104">В следующем примере демонстрируется использование API сжатия в блочном режиме.</span><span class="sxs-lookup"><span data-stu-id="935ca-104">The following example demonstrates using the Compression API in block mode.</span></span> <span data-ttu-id="935ca-105">Для создания программы сжатия или распаковки в режиме блокировки приложение должно включать флаг **сжатия \_ RAW** при вызове [**креатекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) или [**креатедекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span><span class="sxs-lookup"><span data-stu-id="935ca-105">To generate a compressor or decompressor using block mode, your application must include the **COMPRESS\_RAW** flag when it calls [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) or [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span></span> <span data-ttu-id="935ca-106">Режим блокировки позволяет разработчику управлять размером блока, но требует больше работы, чем приложение.</span><span class="sxs-lookup"><span data-stu-id="935ca-106">Block mode enables the developer to control the block size, but requires more work be done by the application.</span></span>

<span data-ttu-id="935ca-107">Режим блокировки завершится ошибкой, если размер входного буфера превышает размер внутреннего блока алгоритма сжатия.</span><span class="sxs-lookup"><span data-stu-id="935ca-107">The block mode will fail if the size of the input buffer is greater than the internal block size of the compression algorithm.</span></span> <span data-ttu-id="935ca-108">Внутренний размер блока — 32 КБ для MSZIP и 1 ГБ для алгоритмов сжатия XPRESS.</span><span class="sxs-lookup"><span data-stu-id="935ca-108">The internal block size is 32KB for the MSZIP and 1GB for the XPRESS compression algorithms.</span></span> <span data-ttu-id="935ca-109">Внутренний размер блока для ЛЗМС можно настроить до 64 ГБ с соответствующим увеличением использования памяти.</span><span class="sxs-lookup"><span data-stu-id="935ca-109">The internal block size for LZMS is configurable up to 64GB with a corresponding increase in memory use.</span></span> <span data-ttu-id="935ca-110">Значение параметра *ункомпресседбуфферсизе* для [**распаковки**](/windows/desktop/api/compressapi/nf-compressapi-decompress) должно быть в точности равно исходному размеру несжатых данных, а не только размеру выходного буфера.</span><span class="sxs-lookup"><span data-stu-id="935ca-110">The value of *UncompressedBufferSize* parameter of [**Decompress**](/windows/desktop/api/compressapi/nf-compressapi-decompress) must be exactly equal to the original size of the uncompressed data and not just the size of the output buffer.</span></span> <span data-ttu-id="935ca-111">Это означает, что приложению потребуется указать размер блока и сохранить точный исходный размер несжатых данных для использования декомпрессором.</span><span class="sxs-lookup"><span data-stu-id="935ca-111">This means your application will need to specify the block size and save the exact original size of the uncompressed data for use by the decompressor.</span></span> <span data-ttu-id="935ca-112">Размер сжатого буфера не сохраняется автоматически, и приложение также должно сохранить его для распаковки.</span><span class="sxs-lookup"><span data-stu-id="935ca-112">The size of the compressed buffer is not automatically saved, and the application also needs to save this for decompression.</span></span>

<span data-ttu-id="935ca-113">Режим буфера рекомендуется в большинстве случаев, поскольку он автоматически разделяет входной буфер на блоки размера, подходящие для выбранного алгоритма сжатия, сохраняет размер несжатого буфера в сжатом буфере.</span><span class="sxs-lookup"><span data-stu-id="935ca-113">The buffer mode is recommended in most cases because it automatically splits up the input buffer into blocks of a size that is appropriate for the selected compression algorithm stores the uncompressed buffer size in the compressed buffer.</span></span> <span data-ttu-id="935ca-114">Сведения о том, как использовать режим буфера, см. [в разделе Использование API сжатия в режиме буфера](using-the-compression-api-in-buffer-mode.md).</span><span class="sxs-lookup"><span data-stu-id="935ca-114">For information on how to use buffer mode, see [Using the Compression API in buffer mode](using-the-compression-api-in-buffer-mode.md).</span></span>

<span data-ttu-id="935ca-115">Приложения, использующие буфер или режим блокировки, имеют возможность указать настраиваемую подпрограмму выделения памяти при вызове [**креатекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) или [**креатедекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span><span class="sxs-lookup"><span data-stu-id="935ca-115">Applications using buffer or block mode have the option to specify a custom memory allocation routine in its call to [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) or [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span></span>

<span data-ttu-id="935ca-116">**Windows 8 и Windows Server 2012:** Чтобы использовать следующий пример кода, необходимо работать под Windows 8 или Windows Server 2012 и иметь "компрессапи. h" и "cabinet.dll" и ссылаться на "Cabinet. lib".</span><span class="sxs-lookup"><span data-stu-id="935ca-116">**Windows 8 and Windows Server 2012:** To use the following example code, you must be running Windows 8 or Windows Server 2012 and have "compressapi.h" and "cabinet.dll" and link to the "Cabinet.lib".</span></span>

<span data-ttu-id="935ca-117">Ниже показано использование API сжатия в блочном режиме для сжатия файла с помощью алгоритма сжатия ЛЗМС и настраиваемой подпрограммы выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="935ca-117">The following demonstrates using the Compression API in block mode to compress a file using the LZMS compression algorithm and a customized memory allocation routine.</span></span> <span data-ttu-id="935ca-118">Приложение должно включать флаг **сжатия \_ RAW** , чтобы использовать API сжатия в блочном режиме.</span><span class="sxs-lookup"><span data-stu-id="935ca-118">Your application must include the **COMPRESS\_RAW** flag to use the Compression API in block mode.</span></span> <span data-ttu-id="935ca-119">Сначала приложение вызывает [**креатекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) с **\_ алгоритмом сжатия \_ лзмс** \| **Сжатие \_ RAW** , чтобы создать программу сжатия.</span><span class="sxs-lookup"><span data-stu-id="935ca-119">First the application calls [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) with **COMPRESS\_ALGORITHM\_LZMS**\|**COMPRESS\_RAW** to generate the compressor.</span></span> <span data-ttu-id="935ca-120">Параметр *аллокатионраутинес* указывает подпрограммы выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="935ca-120">The *AllocationRoutines* parameter specifies the memory allocation routine.</span></span> <span data-ttu-id="935ca-121">Затем приложение задает размер блока для сжатия с помощью [**сеткомпрессоринформатион**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation).</span><span class="sxs-lookup"><span data-stu-id="935ca-121">The application then sets the block size for the compressor using [**SetCompressorInformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation).</span></span>

<span data-ttu-id="935ca-122">Приложение выполняет повторяющиеся вызовы для [**сжатия, чтобы сжать**](/windows/desktop/api/compressapi/nf-compressapi-compress) блок данных по блоку.</span><span class="sxs-lookup"><span data-stu-id="935ca-122">The application makes repeated calls to [**Compress**](/windows/desktop/api/compressapi/nf-compressapi-compress) to compress the data block by block.</span></span> <span data-ttu-id="935ca-123">Приложение записывает размер несжатого блока, сжатый размер блока и сжатые данные в выходной буфер.</span><span class="sxs-lookup"><span data-stu-id="935ca-123">The application writes the uncompressed block size, compressed block size, and compressed data into the output buffer.</span></span>


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

#define META_DATA_SIZE (2 * sizeof(ULONG))
#define BLOCK_SIZE (1 * 1024 * 1024)                //  Block size is 1MB

PVOID SimpleAlloc(PVOID Context, SIZE_T Size)
{
    UNREFERENCED_PARAMETER(Context);
    return malloc(Size);
}

VOID SimpleFree(PVOID Context, PVOID Memory)
{
    UNREFERENCED_PARAMETER(Context);
    if (Memory != NULL)
    {
        free(Memory);
    }
    return;
}

BOOL BlockModeCompress(
    _In_ PBYTE InputData, 
    _In_ DWORD InputSize, 
    _Deref_out_opt_ PBYTE *OutputData, 
    _Out_ DWORD *CompressedSize
    )
{
    COMPRESSOR_HANDLE Compressor    = NULL;
    DWORD ProcessedSoFar            = 0;
    SIZE_T OutputSoFar              = 0;
    DWORD CurrentBlockSize          = 0;
    SIZE_T CompressedDataSize       = 0;
    SIZE_T CompressedBlockSize      = 0;
    SIZE_T OutputDataSize           = 0;  
    BOOL Success                    = FALSE;

    //  Set maximum input block size for compressor.
    DWORD BlockSize                    = BLOCK_SIZE;

    COMPRESS_ALLOCATION_ROUTINES AllocationRoutines;

    //  Init. allocation routines
    AllocationRoutines.Allocate = SimpleAlloc;
    AllocationRoutines.Free = SimpleFree;
    AllocationRoutines.UserContext = NULL;

    *CompressedSize = 0;
    *OutputData = NULL;

    //  Create a LZMS compressor and set to Block mode.
    Success = CreateCompressor(
        COMPRESS_ALGORITHM_LZMS|COMPRESS_RAW,   //  Compression algorithm is LZMS
        &AllocationRoutines,                    //  Optional Memory allocation routines
        &Compressor);                           //  Handle

    if (!Success)
    {
        wprintf(L"Cannot create compressor handle: %d\n", GetLastError());
        goto done;
    }

    Success = SetCompressorInformation(
        Compressor,
        COMPRESS_INFORMATION_CLASS_BLOCK_SIZE,  //  Set block size for LZMS compressor
        &BlockSize,                             //  Block size information
        sizeof(DWORD));                         //  Information size

    if (!Success)
    {
        wprintf(L"Set compressor information error: %d\n", GetLastError());
        goto done;
    }     

    //  Query max. possible compressed block size.
    Success = Compress(
        Compressor,                 //  Compressor Handle
        NULL,                       //  Input buffer, Uncompressed data
        BlockSize,                  //  Uncompressed block size
        NULL,                       //  Compressed Buffer
        0,                          //  Compressed Buffer size
        &CompressedBlockSize);      //  Compressed Data size

    if (!Success)
    {
        DWORD ErrorCode = GetLastError();
        if (ErrorCode != ERROR_INSUFFICIENT_BUFFER)
        {
            wprintf(L"Query compressed block size error: %d\n", GetLastError());
            goto done;
        }
    }

    //  Get max. possible size for compressed data for given input data    
    OutputDataSize = (InputSize % BLOCK_SIZE == 0) ? 0 : 1;
    OutputDataSize += InputSize / BLOCK_SIZE;
    OutputDataSize = OutputDataSize * (META_DATA_SIZE + CompressedBlockSize) + sizeof(ULONG);

    *OutputData = (PBYTE)malloc(OutputDataSize);
    if (!*OutputData)
    {
        wprintf(L"Cannot allocate memory for compressed buffer.\n");
        Success = FALSE;
        goto done;       
    }

    //  Write uncompressed size to beginning of the buffer
    *((ULONG UNALIGNED *)*OutputData) = InputSize;
    OutputSoFar = sizeof(ULONG);

    //  Compress data block by block.
    while (ProcessedSoFar < InputSize)
    {
        if (OutputSoFar + META_DATA_SIZE >= OutputDataSize) 
        {
            Success = FALSE;
            wprintf(L"Compression fails.\n");
            goto done;
        }                      

        CurrentBlockSize = 
            (InputSize - ProcessedSoFar < BlockSize) ?
            (InputSize - ProcessedSoFar) : BlockSize;

        //  Compress a block.
        Success = Compress(
            Compressor,                                     //  Compressor Handle
            InputData + ProcessedSoFar,                     //  Uncompressed data
            CurrentBlockSize,                               //  Uncompressed data size
            *OutputData + OutputSoFar + META_DATA_SIZE,     //  Start of compressed buffer
            OutputDataSize - OutputSoFar - META_DATA_SIZE,  //  Compressed block size
            &CompressedDataSize);                           //  Compressed data size

        if (!Success) 
        {
            wprintf(L"Compression fails: %d\n", GetLastError());
            goto done;
        }

        //  Write block information to output data.
        *((ULONG UNALIGNED *)(*OutputData + OutputSoFar)) = (ULONG)CompressedDataSize;
        OutputSoFar += sizeof(ULONG);
        *((ULONG UNALIGNED *)(*OutputData + OutputSoFar)) = (ULONG)CurrentBlockSize;
        OutputSoFar += sizeof(ULONG);
        OutputSoFar += CompressedDataSize;

        ProcessedSoFar += CurrentBlockSize;
    }    
    
    
    if (OutputSoFar > UINT32_MAX)
    {
        *CompressedSize = 0;
        Success = FALSE;
    }
    else
    {
        *CompressedSize = static_cast<DWORD>(OutputSoFar);
    }

done:
    if (Compressor != NULL)
    {
        CloseCompressor(Compressor);
    }
    return Success;
}

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{
    PBYTE CompressedBuffer          = NULL;
    PBYTE InputBuffer               = NULL;
    HANDLE InputFile                = INVALID_HANDLE_VALUE;
    HANDLE CompressedFile           = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile           = TRUE;
    BOOL Success;
    SIZE_T CompressedDataSize;
    DWORD InputFileSize, ByteRead, ByteWritten;
    LARGE_INTEGER FileSize;    
    ULONGLONG StartTime, EndTime;
    double TimeDuration;

    if (argc != 3)
    {
        wprintf(L"Usage:\n\t%s <input_file_name> <compressd_file_name>\n", argv[0]);
        return;
    }

    //  Open input file for reading, existing file only.
    InputFile = CreateFile(
        argv[1],                  //  Input file name
        GENERIC_READ,             //  Open for reading
        FILE_SHARE_READ,          //  Share for read
        NULL,                     //  Default security
        OPEN_EXISTING,            //  Existing file only
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No attr. template

    if (InputFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot open \t%s\n", argv[1]);
        goto done;
    }

    //  Get input file size.
    Success = GetFileSizeEx(InputFile, &FileSize);
    if ((!Success)||(FileSize.QuadPart > 0xFFFFFFFF))
    {
        wprintf(L"Cannot get input file size or file is larger than 4GB.\n");        
        goto done;
    }
    InputFileSize = FileSize.LowPart;

    //  Allocate memory for file content.
    InputBuffer = (PBYTE)malloc(InputFileSize);
    if (!InputBuffer)
    {
        wprintf(L"Cannot allocate memory for input buffer.\n");
        goto done;
    }                              

    //  Read input file.
    Success = ReadFile(InputFile, InputBuffer, InputFileSize, &ByteRead, NULL);
    if ((!Success)||(ByteRead != InputFileSize))
    {
        wprintf(L"Cannot read from \t%s\n", argv[1]);
        goto done;
    }

    //  Open an empty file for writing, if exist, overwrite it.
    CompressedFile = CreateFile(
        argv[2],                  //  Compressed file name
        GENERIC_WRITE|DELETE,     //  Open for writing; delete if cannot compress
        0,                        //  Do not share
        NULL,                     //  Default security
        CREATE_ALWAYS,            //  Create a new file; if exist, overwrite it
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No template

    if (CompressedFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot create file \t%s\n", argv[2]);
        goto done;
    }

    StartTime = GetTickCount64();

    //  Call BlockModeCompress() again to do compression.    
    Success = BlockModeCompress(        
        InputBuffer,            //  Input buffer, Uncompressed data
        InputFileSize,          //  Uncompressed data size
        &CompressedBuffer,      //  Compressed Buffer
        &CompressedDataSize);   //  Compressed Data size

    if (!Success)
    {
        goto done;
    }

    EndTime = GetTickCount64();

    //  Get compression time.
    TimeDuration = (EndTime - StartTime)/1000.0;

    //  Write compressed data to output file.
    Success = WriteFile(
        CompressedFile,     //  File handle
        CompressedBuffer,   //  Start of data to write
        CompressedDataSize, //  Number of byte to write
        &ByteWritten,       //  Number of byte written
        NULL);              //  No overlapping structure

    if ((ByteWritten != CompressedDataSize) || (!Success))
    {
        wprintf(L"Cannot write compressed data to file: %d\n", GetLastError());
        goto done;
    }

    wprintf(
        L"Input file size: %d; Compressed Size: %d\n", 
        InputFileSize, 
        CompressedDataSize);
    wprintf(L"Compression Time(Exclude I/O): %.2f seconds\n", TimeDuration);
    wprintf(L"File Compressed.\n");

    DeleteTargetFile = FALSE;

done:

    if (CompressedBuffer) 
    {
        free(CompressedBuffer);
    }

    if (InputBuffer)
    {
        free(InputBuffer);
    }

    if (InputFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(InputFile);
    }

    if (CompressedFile != INVALID_HANDLE_VALUE)
    {
        //  Compression fails, delete the compressed file.
        if (DeleteTargetFile)
        {
            FILE_DISPOSITION_INFO fdi;
            fdi.DeleteFile = TRUE;      //  Marking for deletion
            Success = SetFileInformationByHandle(
                CompressedFile,
                FileDispositionInfo,
                &fdi,
                sizeof(FILE_DISPOSITION_INFO));    
            if (!Success) {
                wprintf(L"Cannot delete corrupted compressed file.\n");
            }
        }
        CloseHandle(CompressedFile);
    }
}
```



<span data-ttu-id="935ca-124">Ниже показано распаковка файлов с помощью API сжатия в блочном режиме.</span><span class="sxs-lookup"><span data-stu-id="935ca-124">The following demonstrates file decompression using the Compression API in block mode.</span></span>


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

#define META_DATA_SIZE (2 * sizeof(ULONG))

PVOID SimpleAlloc(PVOID Context, SIZE_T Size)
{
    UNREFERENCED_PARAMETER(Context);
    return malloc(Size);
}

VOID SimpleFree(PVOID Context, PVOID Memory)
{
    UNREFERENCED_PARAMETER(Context);
    if (Memory != NULL)
    {
        free(Memory);
    }
    return;
}

BOOL BlockModeDecompress(
    _In_ PBYTE InputData, 
    _In_ DWORD InputSize, 
    _Deref_out_opt_ PBYTE *OutputData, 
    _Out_ DWORD *DecompressedSize
    )
{
    DECOMPRESSOR_HANDLE Decompressor    = NULL;
    DWORD ProcessedSoFar                = 0;    
    DWORD CompressedBlockSize           = 0;
    DWORD UncompressedBlockSize         = 0;
    DWORD DecompressedSoFar             = 0;
    DWORD OutputDataSize                = 0;
    BOOL Success                        = FALSE;

    COMPRESS_ALLOCATION_ROUTINES AllocationRoutines;

    //  Init. allocation routines
    AllocationRoutines.Allocate = SimpleAlloc;
    AllocationRoutines.Free = SimpleFree;
    AllocationRoutines.UserContext = NULL;

    *DecompressedSize = 0;
    *OutputData = NULL;

    //  Create a LZMS decompressor and set to Block mode.
    Success = CreateDecompressor(
        COMPRESS_ALGORITHM_LZMS|COMPRESS_RAW,   //  Compression algorithm is LZMS
        &AllocationRoutines,                    //  Memory allocation routines
        &Decompressor);                         //  handle

    if (!Success)
    {
        wprintf(L"Cannot create decompressor handle: %d\n", GetLastError());
        goto done;
    }

    //  Read uncompressed size
    ProcessedSoFar = 0;
    OutputDataSize = *((ULONG UNALIGNED *)(InputData + ProcessedSoFar));
    ProcessedSoFar += sizeof(ULONG);

    *OutputData = (PBYTE)malloc(OutputDataSize);
    if (!*OutputData)
    {
        wprintf(L"Cannot allocate memory for uncompressed buffer.\n");
        Success = FALSE;
        goto done;
    }  

    //  Decompress data block by block.
    while (ProcessedSoFar < InputSize)
    {
        if (ProcessedSoFar + META_DATA_SIZE > InputSize)
        {
            Success = FALSE;
            wprintf(L"Data corrupt.\n");
            goto done;     
        }

        //  Read block information.
        CompressedBlockSize = *((ULONG UNALIGNED *)(InputData + ProcessedSoFar));
        ProcessedSoFar += sizeof(ULONG);
        UncompressedBlockSize = *((ULONG UNALIGNED *)(InputData + ProcessedSoFar));
        ProcessedSoFar += sizeof(ULONG);

        if (ProcessedSoFar + CompressedBlockSize > InputSize)
        {
            Success = FALSE;
            wprintf(L"Data corrupt.\n");
            goto done;     
        }

        if (DecompressedSoFar + UncompressedBlockSize > OutputDataSize)
        {
            Success = FALSE;
            wprintf(L"Output buffer not enough to hold decompressed data.\n");
            goto done;     
        }

        //  Decompress a block
        Success = Decompress(
            Decompressor,                   //  Decompressor Handle
            InputData + ProcessedSoFar,     //  Compressed data
            CompressedBlockSize,            //  compressed data size
            *OutputData + DecompressedSoFar, //  Start of decompressed buffer
            UncompressedBlockSize,          //  Uncompressed block size
            NULL);                          //  Decompressed data size
        if (!Success) 
        {
            wprintf(L"Decompression failure: %d\n", GetLastError());
            goto done;
        }
        ProcessedSoFar += CompressedBlockSize;
        DecompressedSoFar += UncompressedBlockSize;
    }

    *DecompressedSize = DecompressedSoFar;

done:
    if (Decompressor != NULL)
    {
        CloseDecompressor(Decompressor);
    }
    return Success;
}

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{       
    PBYTE CompressedBuffer              = NULL;
    PBYTE DecompressedBuffer            = NULL;
    HANDLE InputFile                    = INVALID_HANDLE_VALUE;
    HANDLE DecompressedFile             = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile               = TRUE;    
    BOOL Success;
    DWORD DecompressedDataSize;
    DWORD InputFileSize, ByteRead, ByteWritten;
    ULONGLONG StartTime, EndTime;
    LARGE_INTEGER FileSize;    
    double TimeDuration;

    if (argc != 3) 
    {
        wprintf(L"Usage:\n\t%s <compressed_file_name> <decompressed_file_name>\n", argv[0]);
        return;
    }

    //  Open input file for reading, existing file only.
    InputFile = CreateFile(
        argv[1],                  //  Input file name, compressed file
        GENERIC_READ,             //  Open for reading
        FILE_SHARE_READ,          //  Share for read
        NULL,                     //  Default security
        OPEN_EXISTING,            //  Existing file only
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No template

    if (InputFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot open \t%s\n", argv[1]);
        goto done;
    }

    //  Get compressed file size.
    Success = GetFileSizeEx(InputFile, &FileSize);
    if ((!Success)||(FileSize.QuadPart > 0xFFFFFFFF))
    {
        wprintf(L"Cannot get input file size or file is larger than 4GB.\n");        
        goto done;
    }
    InputFileSize = FileSize.LowPart;

    //  Allocate memory for compressed content.
    CompressedBuffer = (PBYTE)malloc(InputFileSize);
    if (!CompressedBuffer)
    {
        wprintf(L"Cannot allocate memory for compressed buffer.\n");
        goto done;
    }

    //  Read compressed content into buffer.
    Success = ReadFile(InputFile, CompressedBuffer, InputFileSize, &ByteRead, NULL);
    if ((!Success) || (ByteRead != InputFileSize))
    {
        wprintf(L"Cannot read from \t%s\n", argv[1]);
        goto done;
    }

    //  Open an empty file for writing, if exist, destroy it.
    DecompressedFile = CreateFile(
        argv[2],                  //  Decompressed file name
        GENERIC_WRITE|DELETE,     //  Open for writing
        0,                        //  Do not share
        NULL,                     //  Default security
        CREATE_ALWAYS,            //  Create a new file, if exists, overwrite it.
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No template

    if (DecompressedFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot create file \t%s\n", argv[2]);
        goto done;
    }                             
            
    StartTime = GetTickCount64();

    //  Decompress data and write data to DecompressedBuffer.
    Success = BlockModeDecompress(        
        CompressedBuffer,           //  Compressed data
        InputFileSize,              //  Compressed data size
        &DecompressedBuffer,        //  Decompressed buffer        
        &DecompressedDataSize);     //  Decompressed data size

    if (!Success)
    {
        goto done;
    }

    EndTime = GetTickCount64();

    //  Get decompression time.
    TimeDuration = (EndTime - StartTime)/1000.0;

    //  Write decompressed data to output file.
    Success = WriteFile(
        DecompressedFile,       //  File handle
        DecompressedBuffer,     //  Start of data to write
        DecompressedDataSize,   //  Number of byte to write
        &ByteWritten,           //  Number of byte written
        NULL);                  //  No overlapping structure
    if ((ByteWritten != DecompressedDataSize) || (!Success))
    {
        wprintf(L"Cannot write decompressed data to file.\n");
        goto done;
    }
    
    wprintf(
        L"Compressed size: %d; Decompressed Size: %d\n",
        InputFileSize,
        DecompressedDataSize);
    wprintf(L"Decompression Time(Exclude I/O): %.2f seconds\n", TimeDuration);
    wprintf(L"File decompressed.\n");

    DeleteTargetFile = FALSE;

done:
    if (CompressedBuffer) 
    {
        free(CompressedBuffer);
    }

    if (DecompressedBuffer)
    {
        free(DecompressedBuffer);
    }

    if (InputFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(InputFile);
    }

    if (DecompressedFile != INVALID_HANDLE_VALUE)
    {
        //  Compression fails, delete the compressed file.
        if (DeleteTargetFile)
        {
            FILE_DISPOSITION_INFO fdi;
            fdi.DeleteFile = TRUE;      //  Marking for deletion
            Success = SetFileInformationByHandle(
                DecompressedFile,
                FileDispositionInfo,
                &fdi,
                sizeof(FILE_DISPOSITION_INFO));    
            if (!Success) {
                wprintf(L"Cannot delete corrupted decompressed file.\n");
            }
        }
        CloseHandle(DecompressedFile); 
    }
}
```



<span data-ttu-id="935ca-125">Приложение, использующее буфер или режим блокировки, имеет возможность настроить выделение памяти, используемое API сжатия при вызове [**креатекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) или [**креатедекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span><span class="sxs-lookup"><span data-stu-id="935ca-125">An application using buffer or block mode has the option to customize the memory allocation used by the Compression API when it calls [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) or [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span></span> <span data-ttu-id="935ca-126">В режиме блокировки приложение должно обрабатывать сведения блока сжатия, такие как размер сжатых данных и размер несжатых данных. в противном случае [**распаковка**](/windows/desktop/api/compressapi/nf-compressapi-decompress) не сможет распаковать данные.</span><span class="sxs-lookup"><span data-stu-id="935ca-126">In block mode, the application must handle compression block information, such as compressed data size and uncompressed data size, otherwise [**Decompress**](/windows/desktop/api/compressapi/nf-compressapi-decompress) will be unable to decompress the information.</span></span>

<span data-ttu-id="935ca-127">В следующем фрагменте кода показана простая настраиваемая подпрограмма выделения.</span><span class="sxs-lookup"><span data-stu-id="935ca-127">The following snippet shows a simple customized allocation routine.</span></span>


```C++
PVOID SimpleAlloc(PVOID Context, SIZE_T Size)
{
return malloc(Size);
}

VOID SimpleFree(PVOID Context, PVOID Memory)
{
if (Memory != NULL)
{
        free(Memory);
}
return;
}

//  Init. allocation routines
AllocationRoutines.Allocate = SimpleAlloc;
AllocationRoutines.Free = SimpleFree;
AllocationRoutines.UserContext = NULL;
```



 

 



