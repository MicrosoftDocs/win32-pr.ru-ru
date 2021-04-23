---
description: '\_ \_ Структура распознавания файловой системы \_ , определяемая внутри Windows и используемая службой "распознавание файловой системы" (FRS), содержит значение контрольной суммы, которое должно быть правильно вычислено для правильной работы службы FRS с указанной нераспознанной файловой системой.'
ms.assetid: 8f76784f-7d03-4874-ae7f-e8bdc42638c3
title: Вычисление контрольной суммы распознавания файловой системы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cac3975d4e1845dd1ff4aa218526e942fda152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999694"
---
# <a name="computing-a-file-system-recognition-checksum"></a><span data-ttu-id="4492e-103">Вычисление контрольной суммы распознавания файловой системы</span><span class="sxs-lookup"><span data-stu-id="4492e-103">Computing a File System Recognition Checksum</span></span>

<span data-ttu-id="4492e-104">Структура [**\_ распознавания файловой \_ \_ системы**](file-system-recognition-structure.md) , определяемая внутри Windows и используемая службой " [Распознавание файловой системы](file-system-recognition.md) " (FRS), содержит значение контрольной суммы, которое должно быть правильно вычислено для правильной работы службы FRS с указанной нераспознанной файловой системой.</span><span class="sxs-lookup"><span data-stu-id="4492e-104">The [**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**](file-system-recognition-structure.md) structure, defined internally by Windows and used by [file system recognition](file-system-recognition.md) (FRS), contains a checksum value that must be properly computed for FRS to work properly with a specified unrecognized file system.</span></span> <span data-ttu-id="4492e-105">В следующем примере выполняются эти вычисления.</span><span class="sxs-lookup"><span data-stu-id="4492e-105">The following example accomplishes this computation.</span></span>


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE, *PFILE_SYSTEM_RECOGNITION_STRUCTURE;

USHORT ComputeFileSystemInformationChecksum (
    __in PFILE_SYSTEM_RECOGNITION_STRUCTURE Fsrs
    )

/*++

Routine Description:

    This routine computes the file record checksum.

Arguments:

    Fsrs - Pointer to the record.

Return Value:

    The checksum result.

--*/

{
    USHORT Checksum = 0;
    USHORT i;
    PUCHAR Buffer = (PUCHAR)Fsrs;
    USHORT StartOffset;

    //
    //  Skip the jump instruction
    //

    StartOffset = FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, FsName);
    
    for (i = StartOffset; i < Fsrs->Length; i++) {

        //
        //  Skip the checksum field itself, which is a USHORT.
        //

        if ((i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)) ||
            (i == FIELD_OFFSET(FILE_SYSTEM_RECOGNITION_STRUCTURE, Checksum)+1)) {

            continue;
        }

        Checksum = ((Checksum & 1) ? 0x8000 : 0) + (Checksum >> 1) + Buffer[i];
    }

    return Checksum;
}
```



## <a name="related-topics"></a><span data-ttu-id="4492e-106">См. также</span><span class="sxs-lookup"><span data-stu-id="4492e-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4492e-107">Распознавание файловой системы</span><span class="sxs-lookup"><span data-stu-id="4492e-107">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="4492e-108">**\_ \_ Структура распознавания файловой \_ системы**</span><span class="sxs-lookup"><span data-stu-id="4492e-108">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> </dl>

 

 



