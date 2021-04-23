---
description: Представляет атрибут имени файла. Файл имеет один атрибут имени файла для каждого каталога, в котором он указан.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: Структура FILE_NAME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072345"
---
# <a name="file_name-structure"></a><span data-ttu-id="8f342-104">\_Структура имени файла</span><span class="sxs-lookup"><span data-stu-id="8f342-104">FILE\_NAME structure</span></span>

<span data-ttu-id="8f342-105">\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="8f342-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="8f342-106">Представляет атрибут имени файла.</span><span class="sxs-lookup"><span data-stu-id="8f342-106">Represents a file name attribute.</span></span> <span data-ttu-id="8f342-107">Файл имеет один атрибут имени файла для каждого каталога, в котором он указан.</span><span class="sxs-lookup"><span data-stu-id="8f342-107">A file has one file name attribute for every directory it is entered into.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f342-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f342-108">Syntax</span></span>


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a><span data-ttu-id="8f342-109">Члены</span><span class="sxs-lookup"><span data-stu-id="8f342-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="8f342-110">**парентдиректори**</span><span class="sxs-lookup"><span data-stu-id="8f342-110">**ParentDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="8f342-111">Ссылка на файл каталога, который индексируется по этому имени.</span><span class="sxs-lookup"><span data-stu-id="8f342-111">A file reference to the directory that indexes to this name.</span></span> <span data-ttu-id="8f342-112">См [**. \_ \_ Справочник по сегментам MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8f342-112">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f342-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="8f342-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="8f342-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="8f342-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="8f342-115">**филенамеленгс**</span><span class="sxs-lookup"><span data-stu-id="8f342-115">**FileNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="8f342-116">Длина имени файла в символах Юникода.</span><span class="sxs-lookup"><span data-stu-id="8f342-116">The length of the file name, in Unicode characters.</span></span>

</dd> <dt>

<span data-ttu-id="8f342-117">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="8f342-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="8f342-118">Флаги имени файла.</span><span class="sxs-lookup"><span data-stu-id="8f342-118">The file name flags.</span></span>

<dl> <dt>

<span data-ttu-id="8f342-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**Файл \_ ИМЯ \_ NTFS** (0x01)</span><span class="sxs-lookup"><span data-stu-id="8f342-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**FILE\_NAME\_NTFS** (0x01)</span></span>
</dt> <dt>

<span data-ttu-id="8f342-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**Файл \_ ИМЯ \_ DOS** (0x02)</span><span class="sxs-lookup"><span data-stu-id="8f342-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**FILE\_NAME\_DOS** (0x02)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="8f342-121">**FileName**</span><span class="sxs-lookup"><span data-stu-id="8f342-121">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="8f342-122">Первый символ имени файла.</span><span class="sxs-lookup"><span data-stu-id="8f342-122">The first character of the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f342-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8f342-123">Remarks</span></span>

<span data-ttu-id="8f342-124">Обратите внимание, что для этой структуры нет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="8f342-124">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="8f342-125">Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="8f342-125">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="8f342-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f342-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f342-127">Основная таблица файлов</span><span class="sxs-lookup"><span data-stu-id="8f342-127">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
