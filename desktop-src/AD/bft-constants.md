---
title: Константы БФТ (Нтдсбкли. h)
description: Константы БФТ используются в качестве битовых флагов для обнаружения различных типов файлов в резервной копии служб домен Active Directory Services.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988499"
---
# <a name="bft-constants"></a><span data-ttu-id="68297-103">Константы БФТ</span><span class="sxs-lookup"><span data-stu-id="68297-103">BFT Constants</span></span>

<span data-ttu-id="68297-104">Константы БФТ используются в качестве битовых флагов для обнаружения различных типов файлов в резервной копии служб домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="68297-104">The BFT constants are used as bit flags to identify different file types in an Active Directory Domain Services backup.</span></span>

<dl> <dt>

<span data-ttu-id="68297-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**\_Каталог журналов \_ БФТ**</span><span class="sxs-lookup"><span data-stu-id="68297-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**BFT\_LOG\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68297-106">0x20</span><span class="sxs-lookup"><span data-stu-id="68297-106">0x20</span></span>
</dt> <dt>



<span data-ttu-id="68297-107">Файл принадлежит каталогу журнала.</span><span class="sxs-lookup"><span data-stu-id="68297-107">The file belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68297-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**\_Каталог базы данных БФТ \_**</span><span class="sxs-lookup"><span data-stu-id="68297-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**BFT\_DATABASE\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68297-109">0x40</span><span class="sxs-lookup"><span data-stu-id="68297-109">0x40</span></span>
</dt> <dt>



<span data-ttu-id="68297-110">Файл принадлежит каталогу базы данных.</span><span class="sxs-lookup"><span data-stu-id="68297-110">The file belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68297-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**\_Каталог БФТ**</span><span class="sxs-lookup"><span data-stu-id="68297-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68297-112">0x80</span><span class="sxs-lookup"><span data-stu-id="68297-112">0x80</span></span>
</dt> <dt>



<span data-ttu-id="68297-113">Указанный путь является каталогом, а не именем файла.</span><span class="sxs-lookup"><span data-stu-id="68297-113">The path specified is a directory and not a file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68297-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**\_Журнал БФТ**</span><span class="sxs-lookup"><span data-stu-id="68297-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68297-115">0x21</span><span class="sxs-lookup"><span data-stu-id="68297-115">0x21</span></span>
</dt> <dt>



<span data-ttu-id="68297-116">Указывает файл журнала, который принадлежит каталогу журнала.</span><span class="sxs-lookup"><span data-stu-id="68297-116">Specifies a log file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68297-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**БФТ \_ log \_ dir**</span><span class="sxs-lookup"><span data-stu-id="68297-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68297-118">0x22</span><span class="sxs-lookup"><span data-stu-id="68297-118">0x22</span></span>
</dt> <dt>



<span data-ttu-id="68297-119">Файл — это путь к каталогу журнала.</span><span class="sxs-lookup"><span data-stu-id="68297-119">The file is the path of the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68297-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**\_dir Checkpoint \_ БФТ**</span><span class="sxs-lookup"><span data-stu-id="68297-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68297-121">0x23</span><span class="sxs-lookup"><span data-stu-id="68297-121">0x23</span></span>
</dt> <dt>



<span data-ttu-id="68297-122">Файл — это путь к каталогу контрольных точек.</span><span class="sxs-lookup"><span data-stu-id="68297-122">The file is the path of the checkpoint directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68297-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_ \_ база данных NTDS БФТ**</span><span class="sxs-lookup"><span data-stu-id="68297-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68297-124">0x44</span><span class="sxs-lookup"><span data-stu-id="68297-124">0x44</span></span>
</dt> <dt>



<span data-ttu-id="68297-125">Этот файл является базой данных службы каталогов, которая принадлежит каталогу базы данных.</span><span class="sxs-lookup"><span data-stu-id="68297-125">The file is a directory service database that belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68297-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_файл исправления \_ БФТ**</span><span class="sxs-lookup"><span data-stu-id="68297-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68297-127">0x25</span><span class="sxs-lookup"><span data-stu-id="68297-127">0x25</span></span>
</dt> <dt>



<span data-ttu-id="68297-128">Файл является файлом исправления, который принадлежит каталогу журнала.</span><span class="sxs-lookup"><span data-stu-id="68297-128">The file is a patch file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="68297-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**БФТ \_ неизвестный**</span><span class="sxs-lookup"><span data-stu-id="68297-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68297-130">0x0F</span><span class="sxs-lookup"><span data-stu-id="68297-130">0x0F</span></span>
</dt> <dt>



<span data-ttu-id="68297-131">Не удается распознать файл.</span><span class="sxs-lookup"><span data-stu-id="68297-131">The file cannot be recognized.</span></span> <span data-ttu-id="68297-132">Файл не совпадает с известными именами файлов и типами файлов.</span><span class="sxs-lookup"><span data-stu-id="68297-132">The file does not coincide with the known file names and file types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68297-133">Требования</span><span class="sxs-lookup"><span data-stu-id="68297-133">Requirements</span></span>



| <span data-ttu-id="68297-134">Требование</span><span class="sxs-lookup"><span data-stu-id="68297-134">Requirement</span></span> | <span data-ttu-id="68297-135">Значение</span><span class="sxs-lookup"><span data-stu-id="68297-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68297-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68297-136">Minimum supported client</span></span><br/> | <span data-ttu-id="68297-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68297-137">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="68297-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68297-138">Minimum supported server</span></span><br/> | <span data-ttu-id="68297-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68297-139">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="68297-140">Header</span><span class="sxs-lookup"><span data-stu-id="68297-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="68297-141"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="68297-141"><dt>Ntdsbcli.h</dt></span></span> </dl> |



 

 





