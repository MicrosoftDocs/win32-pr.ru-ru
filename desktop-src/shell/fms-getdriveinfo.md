---
description: Содержит сведения о диске, выбранном в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).
title: Структура FMS_GETDRIVEINFO (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: 107e12e1076a2fc928ecb9b578ab01d64898a83a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842235"
---
# <a name="fms_getdriveinfo-structure"></a><span data-ttu-id="1aeaf-103">\_Структура FMS жетдривеинфо</span><span class="sxs-lookup"><span data-stu-id="1aeaf-103">FMS\_GETDRIVEINFO structure</span></span>

<span data-ttu-id="1aeaf-104">Содержит сведения о диске, выбранном в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).</span><span class="sxs-lookup"><span data-stu-id="1aeaf-104">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="1aeaf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1aeaf-105">Syntax</span></span>


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a><span data-ttu-id="1aeaf-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1aeaf-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1aeaf-107">**двтоталспаце**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-107">**dwTotalSpace**</span></span>
</dt> <dd>

<span data-ttu-id="1aeaf-108">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1aeaf-109">Общий объем дискового пространства (в байтах) на диске, связанном с диском.</span><span class="sxs-lookup"><span data-stu-id="1aeaf-109">The total amount of storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="1aeaf-110">**двфриспаце**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-110">**dwFreeSpace**</span></span>
</dt> <dd>

<span data-ttu-id="1aeaf-111">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="1aeaf-112">Объем свободного дискового пространства (в байтах) на диске, связанном с диском.</span><span class="sxs-lookup"><span data-stu-id="1aeaf-112">The amount of free storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="1aeaf-113">**сзпас**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-113">**szPath**</span></span>
</dt> <dd>

<span data-ttu-id="1aeaf-114">Тип: **TCHAR \[ 260 \]**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-114">Type: **TCHAR\[260\]**</span></span>

</dd> <dd>

<span data-ttu-id="1aeaf-115">путь к текущему каталогу, заканчивающийся нулем.</span><span class="sxs-lookup"><span data-stu-id="1aeaf-115">the null-terminated path of the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="1aeaf-116">**сзволуме**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-116">**szVolume**</span></span>
</dt> <dd>

<span data-ttu-id="1aeaf-117">Тип: **TCHAR \[ 14 \]**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-117">Type: **TCHAR\[14\]**</span></span>

</dd> <dd>

<span data-ttu-id="1aeaf-118">Метка тома, завершающаяся нулем, для диска, связанного с диском.</span><span class="sxs-lookup"><span data-stu-id="1aeaf-118">The null-terminated volume label of the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="1aeaf-119">**сзшаре**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-119">**szShare**</span></span>
</dt> <dd>

<span data-ttu-id="1aeaf-120">Тип: **TCHAR \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-120">Type: **TCHAR\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="1aeaf-121">Имя сетевого ресурса, заканчивающееся нулем (если доступ к диску осуществляется по сети).</span><span class="sxs-lookup"><span data-stu-id="1aeaf-121">The null-terminated name of the network resource (if the drive is being accessed through a network).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1aeaf-122">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="1aeaf-122">Requirements</span></span>



| <span data-ttu-id="1aeaf-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1aeaf-123">Requirement</span></span> | <span data-ttu-id="1aeaf-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1aeaf-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1aeaf-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1aeaf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1aeaf-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1aeaf-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1aeaf-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1aeaf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1aeaf-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1aeaf-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1aeaf-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1aeaf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aeaf-130"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aeaf-130"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aeaf-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1aeaf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aeaf-132">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-132">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="1aeaf-133">**FM \_ жетдривеинфо**</span><span class="sxs-lookup"><span data-stu-id="1aeaf-133">**FM\_GETDRIVEINFO**</span></span>](fm-getdriveinfo.md)
</dt> </dl>

 

 




