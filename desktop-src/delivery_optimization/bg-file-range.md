---
title: Структура BG_FILE_RANGE (Deliveryoptimization. h)
description: Структура BG_FILE_RANGE определяет диапазон байтов для загрузки из файла.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- Структура BG_FILE_RANGE
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415968"
---
# <a name="bg_file_range-structure"></a><span data-ttu-id="f29ac-104">Структура BG_FILE_RANGE</span><span class="sxs-lookup"><span data-stu-id="f29ac-104">BG_FILE_RANGE structure</span></span>

<span data-ttu-id="f29ac-105">Структура **BG_FILE_RANGE** определяет диапазон байтов для загрузки из файла.</span><span class="sxs-lookup"><span data-stu-id="f29ac-105">The **BG_FILE_RANGE** structure identifies a range of bytes to download from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f29ac-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f29ac-106">Syntax</span></span>


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a><span data-ttu-id="f29ac-107">Члены</span><span class="sxs-lookup"><span data-stu-id="f29ac-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f29ac-108">**инитиалоффсет**</span><span class="sxs-lookup"><span data-stu-id="f29ac-108">**InitialOffset**</span></span>
</dt> <dd>

<span data-ttu-id="f29ac-109">Смещение от нуля до начала диапазона байтов для скачивания из файла.</span><span class="sxs-lookup"><span data-stu-id="f29ac-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

</dd> <dt>

<span data-ttu-id="f29ac-110">**Длина**</span><span class="sxs-lookup"><span data-stu-id="f29ac-110">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="f29ac-111">Длина диапазона в байтах.</span><span class="sxs-lookup"><span data-stu-id="f29ac-111">The length of the range, in bytes.</span></span> <span data-ttu-id="f29ac-112">Не указывайте нулевую длину байта.</span><span class="sxs-lookup"><span data-stu-id="f29ac-112">Do not specify a zero byte length.</span></span> <span data-ttu-id="f29ac-113">Чтобы указать, что диапазон расширяется до конца файла, укажите **BG_LENGTH_TO_EOF**.</span><span class="sxs-lookup"><span data-stu-id="f29ac-113">To indicate that the range extends to the end of the file, specify **BG_LENGTH_TO_EOF**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f29ac-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f29ac-114">Remarks</span></span>

<span data-ttu-id="f29ac-115">Диапазон должен существовать в файле или выдает ошибку **DO_E_INVALID_RANGE** .</span><span class="sxs-lookup"><span data-stu-id="f29ac-115">The range must exist in the file or DO generates an **DO_E_INVALID_RANGE** error.</span></span>

## <a name="requirements"></a><span data-ttu-id="f29ac-116">Требования</span><span class="sxs-lookup"><span data-stu-id="f29ac-116">Requirements</span></span>



| <span data-ttu-id="f29ac-117">Требование</span><span class="sxs-lookup"><span data-stu-id="f29ac-117">Requirement</span></span> | <span data-ttu-id="f29ac-118">Значение</span><span class="sxs-lookup"><span data-stu-id="f29ac-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f29ac-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f29ac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f29ac-120">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="f29ac-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f29ac-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f29ac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f29ac-122">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="f29ac-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f29ac-123">Header</span><span class="sxs-lookup"><span data-stu-id="f29ac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f29ac-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="f29ac-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f29ac-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f29ac-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29ac-126">**IBackgroundCopyFile2:: Жетфилеранжес**</span><span class="sxs-lookup"><span data-stu-id="f29ac-126">**IBackgroundCopyFile2::GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





