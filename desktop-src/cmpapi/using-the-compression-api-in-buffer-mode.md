---
description: В следующих примерах демонстрируется использование API сжатия в режиме буфера.
ms.assetid: 0A062E5D-E5FA-4098-B76E-E136FC74D853
title: Использование API сжатия в режиме буфера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676a5bea1ea4fa673bbf9a8fc2caf9fe84d9bc1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692034"
---
# <a name="using-the-compression-api-in-buffer-mode"></a><span data-ttu-id="4d1ac-103">Использование API сжатия в режиме буфера</span><span class="sxs-lookup"><span data-stu-id="4d1ac-103">Using the Compression API in buffer mode</span></span>

<span data-ttu-id="4d1ac-104">В следующих примерах демонстрируется использование API сжатия в режиме буфера.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-104">The following samples demonstrate using the Compression API in buffer mode.</span></span> <span data-ttu-id="4d1ac-105">Режим буфера был разработан для простоты использования и автоматически разбивает входной буфер на блоки размера, подходящего для выбранного алгоритма сжатия.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-105">Buffer mode was developed for ease of use and automatically splits up the input buffer into blocks of a size that is appropriate for the selected compression algorithm.</span></span> <span data-ttu-id="4d1ac-106">Режим буфера автоматически форматирует и сохраняет несжатый размер буфера в сжатом буфере, где он доступен для декомпрессора.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-106">Buffer mode automatically formats and stores the uncompressed buffer size in the compressed buffer where it is available to the decompressor.</span></span> <span data-ttu-id="4d1ac-107">Размер сжатого буфера не сохраняется автоматически, и приложению необходимо сохранить его для распаковки.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-107">The size of the compressed buffer is not automatically saved, and the application needs to save this for decompression.</span></span> <span data-ttu-id="4d1ac-108">Не включайте флаг **сжатия \_ RAW** при вызове [**креатекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) или [**КРЕАТЕДЕКОМПРЕССОР**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) , если вы хотите использовать API сжатия в режиме буфера.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-108">Do not include the **COMPRESS\_RAW** flag when calling [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) or [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) if you want to use the Compression API in buffer mode.</span></span>

<span data-ttu-id="4d1ac-109">В большинстве случаев рекомендуется использовать режим буфера.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-109">Buffer mode is recommended for most cases.</span></span> <span data-ttu-id="4d1ac-110">Дополнительные сведения об использовании блочного режима см. в разделе [Использование API сжатия в блочном режиме](using-the-compression-api-in-block-mode.md) .</span><span class="sxs-lookup"><span data-stu-id="4d1ac-110">For more information about how to use block mode, see [Using the Compression API in block mode](using-the-compression-api-in-block-mode.md)</span></span>

<span data-ttu-id="4d1ac-111">Приложения, использующие буфер или режим блокировки, имеют возможность указать настраиваемую подпрограмму выделения памяти при вызове [**креатекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) или [**креатедекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span><span class="sxs-lookup"><span data-stu-id="4d1ac-111">Applications using buffer or block mode have the option to specify a custom memory allocation routine when calling [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) or [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span></span> <span data-ttu-id="4d1ac-112">Пример простой настраиваемой подпрограммы выделения см. в разделе [Использование API сжатия в режиме блокировки](using-the-compression-api-in-block-mode.md) .</span><span class="sxs-lookup"><span data-stu-id="4d1ac-112">See the [Using the Compression API in block mode](using-the-compression-api-in-block-mode.md) section for an example of a simple customized allocation routine.</span></span>

<span data-ttu-id="4d1ac-113">**Windows 8 и Windows Server 2012:** Чтобы использовать следующий пример кода, необходимо работать под Windows 8 или Windows Server 2012 и иметь "компрессапи. h" и "cabinet.dll" и ссылаться на "Cabinet. lib".</span><span class="sxs-lookup"><span data-stu-id="4d1ac-113">**Windows 8 and Windows Server 2012:** To use the following example code, you must be running Windows 8 or Windows Server 2012 and have "compressapi.h" and "cabinet.dll" and link to the "Cabinet.lib".</span></span>

<span data-ttu-id="4d1ac-114">В следующем фрагменте кода демонстрируется сжатие файлов с помощью алгоритма сжатия XPRESS и кодировка Хаффмана с использованием API сжатия в режиме буфера.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-114">The following code snippet demonstrates file compression with the XPRESS compression algorithm and Huffman encoding using the Compression API in buffer mode.</span></span> <span data-ttu-id="4d1ac-115">Приложение принимает файл, сжимает его содержимое и создает сжатый файл.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-115">The application accepts a file, compresses its contents and generates a compressed file.</span></span> <span data-ttu-id="4d1ac-116">Сначала приложение вызывает [**креатекомпрессор**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) с **\_ алгоритмом сжатия \_ Xpress \_ Хаффа** , чтобы создать компрессор.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-116">First the application calls [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) with **COMPRESS\_ALGORITHM\_XPRESS\_HUFF** to generate a compressor.</span></span> <span data-ttu-id="4d1ac-117">Затем вызывается [**Сжатие**](/windows/desktop/api/compressapi/nf-compressapi-compress)с параметром *компресседбуфферсизе* , равным 0, для запроса требуемого размера сжатого буфера.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-117">Then it calls [**Compress**](/windows/desktop/api/compressapi/nf-compressapi-compress), with *CompressedBufferSize* set to 0, to query for the required size of the compressed buffer.</span></span> <span data-ttu-id="4d1ac-118">Он выделяет выходной буфер для значения *компресседбуфферсизе* .</span><span class="sxs-lookup"><span data-stu-id="4d1ac-118">It allocates an output buffer to the *CompressedBufferSize* value.</span></span> <span data-ttu-id="4d1ac-119">Приложение вызывает **Сжатие** второй раз для выполнения фактического сжатия.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-119">The application calls **Compress** a second time to perform the actual compression.</span></span> <span data-ttu-id="4d1ac-120">Наконец, приложение записывает сжатые данные в выходной файл.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-120">Finally, the application writes the compressed data to the output file.</span></span>


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{
    COMPRESSOR_HANDLE Compressor    = NULL;
    PBYTE CompressedBuffer          = NULL;
    PBYTE InputBuffer               = NULL;
    HANDLE InputFile                = INVALID_HANDLE_VALUE;
    HANDLE CompressedFile           = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile           = TRUE;
    BOOL Success;
    SIZE_T CompressedDataSize, CompressedBufferSize;
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
        wprintf(L"Cannot allocate memory for uncompressed buffer.\n");
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

    //  Create an XpressHuff compressor.
    Success = CreateCompressor(
        COMPRESS_ALGORITHM_XPRESS_HUFF, //  Compression Algorithm
        NULL,                           //  Optional allocation routine
        &Compressor);                   //  Handle

    if (!Success)
    {
        wprintf(L"Cannot create a compressor %d.\n", GetLastError());
        goto done;
    }

    //  Query compressed buffer size.
    Success = Compress(
        Compressor,                  //  Compressor Handle
        InputBuffer,                 //  Input buffer, Uncompressed data
        InputFileSize,               //  Uncompressed data size
        NULL,                        //  Compressed Buffer
        0,                           //  Compressed Buffer size
        &CompressedBufferSize);      //  Compressed Data size

    //  Allocate memory for compressed buffer.
    if (!Success)
    {
        DWORD ErrorCode = GetLastError();

        if (ErrorCode != ERROR_INSUFFICIENT_BUFFER)
        {
            wprintf(L"Cannot compress data: %d.\n", ErrorCode);
            goto done;
        }
            
        CompressedBuffer = (PBYTE)malloc(CompressedBufferSize);
        if (!CompressedBuffer)
        {
            wprintf(L"Cannot allocate memory for compressed buffer.\n");
            goto done;
        }
    }

    StartTime = GetTickCount64();

    //  Call Compress() again to do real compression and output the compressed
    //  data to CompressedBuffer.
    Success = Compress(
        Compressor,             //  Compressor Handle
        InputBuffer,            //  Input buffer, Uncompressed data
        InputFileSize,          //  Uncompressed data size
        CompressedBuffer,       //  Compressed Buffer
        CompressedBufferSize,   //  Compressed Buffer size
        &CompressedDataSize);   //  Compressed Data size

    if (!Success)
    {
        wprintf(L"Cannot compress data: %d\n", GetLastError());
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
        wprintf(L"Cannot write compressed data to file: %d.\n", GetLastError());
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
    if (Compressor != NULL)
    {
        CloseCompressor(Compressor);
    }

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



<span data-ttu-id="4d1ac-121">В следующем фрагменте кода демонстрируется распаковка файлов с помощью API сжатия в режиме буфера.</span><span class="sxs-lookup"><span data-stu-id="4d1ac-121">The following code snippet demonstrates file decompression using the Compression API in buffer mode.</span></span>


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{
    DECOMPRESSOR_HANDLE Decompressor    = NULL;
    PBYTE CompressedBuffer              = NULL;
    PBYTE DecompressedBuffer            = NULL;
    HANDLE InputFile                    = INVALID_HANDLE_VALUE;
    HANDLE DecompressedFile             = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile               = TRUE;    
    BOOL Success;
    SIZE_T DecompressedBufferSize, DecompressedDataSize;
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

    //  Allocation memory for compressed content.
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

    //  Create an XpressHuff decompressor.
    Success = CreateDecompressor(
        COMPRESS_ALGORITHM_XPRESS_HUFF, //  Compression Algorithm
        NULL,                           //  Optional allocation routine
        &Decompressor);                 //  Handle

    if (!Success)
    {
        wprintf(L"Cannot create a decompressor: %d.\n", GetLastError());
        goto done;
    }

    //  Query decompressed buffer size.
    Success = Decompress(
        Decompressor,                //  Compressor Handle
        CompressedBuffer,            //  Compressed data
        InputFileSize,               //  Compressed data size
        NULL,                        //  Buffer set to NULL
        0,                           //  Buffer size set to 0
        &DecompressedBufferSize);    //  Decompressed Data size

    //  Allocate memory for decompressed buffer.
    if (!Success)
    {
        DWORD ErrorCode = GetLastError();

        // Note that the original size returned by the function is extracted 
        // from the buffer itself and should be treated as untrusted and tested
        // against reasonable limits.
        if (ErrorCode != ERROR_INSUFFICIENT_BUFFER) 
        {
            wprintf(L"Cannot decompress data: %d.\n",ErrorCode);
            goto done;
        }

        DecompressedBuffer = (PBYTE)malloc(DecompressedBufferSize);
        if (!DecompressedBuffer)
        {
            wprintf(L"Cannot allocate memory for decompressed buffer.\n");
            goto done;
        }           
    }
        
    StartTime = GetTickCount64();

    //  Decompress data and write data to DecompressedBuffer.
    Success = Decompress(
        Decompressor,               //  Decompressor handle
        CompressedBuffer,           //  Compressed data
        InputFileSize,              //  Compressed data size
        DecompressedBuffer,         //  Decompressed buffer
        DecompressedBufferSize,     //  Decompressed buffer size
        &DecompressedDataSize);     //  Decompressed data size

    if (!Success)
    {
        wprintf(L"Cannot decompress data: %d.\n", GetLastError());
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
    if (Decompressor != NULL)
    {
        CloseDecompressor(Decompressor);
    }

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



 

 



