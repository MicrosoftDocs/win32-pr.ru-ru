---
description: Содержит сведения о размере устройства. Это возвращается с помощью \_ \_ управляющего кода для считывания емкости хранилища ioctl \_ .
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: Структура STORAGE_READ_CAPACITY (Нтддстор. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423258"
---
# <a name="storage_read_capacity-structure"></a><span data-ttu-id="34020-104">\_Структура емкости для чтения хранилища \_</span><span class="sxs-lookup"><span data-stu-id="34020-104">STORAGE\_READ\_CAPACITY structure</span></span>

<span data-ttu-id="34020-105">Содержит сведения о размере устройства.</span><span class="sxs-lookup"><span data-stu-id="34020-105">Contains information about the size of a device.</span></span> <span data-ttu-id="34020-106">Это возвращается с помощью управляющего кода для [**\_ \_ считывания \_ емкости хранилища ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) .</span><span class="sxs-lookup"><span data-stu-id="34020-106">This is returned from the [**IOCTL\_STORAGE\_READ\_CAPACITY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="34020-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34020-107">Syntax</span></span>


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a><span data-ttu-id="34020-108">Члены</span><span class="sxs-lookup"><span data-stu-id="34020-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="34020-109">**Version**</span><span class="sxs-lookup"><span data-stu-id="34020-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="34020-110">Версия этой структуры.</span><span class="sxs-lookup"><span data-stu-id="34020-110">The version of this structure.</span></span> <span data-ttu-id="34020-111">Вызывающий объект должен присвоить этому элементу значение `sizeof(STORAGE_READ_CAPACITY)` .</span><span class="sxs-lookup"><span data-stu-id="34020-111">The caller must set this member to `sizeof(STORAGE_READ_CAPACITY)`.</span></span>

</dd> <dt>

<span data-ttu-id="34020-112">**Размер**</span><span class="sxs-lookup"><span data-stu-id="34020-112">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="34020-113">Размер возвращаемых данных.</span><span class="sxs-lookup"><span data-stu-id="34020-113">The size of the data returned.</span></span>

</dd> <dt>

<span data-ttu-id="34020-114">**блоккленгс**</span><span class="sxs-lookup"><span data-stu-id="34020-114">**BlockLength**</span></span>
</dt> <dd>

<span data-ttu-id="34020-115">Число байтов на блок.</span><span class="sxs-lookup"><span data-stu-id="34020-115">The number of bytes per block.</span></span>

</dd> <dt>

<span data-ttu-id="34020-116">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="34020-116">**NumberOfBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="34020-117">Общее число блоков на диске.</span><span class="sxs-lookup"><span data-stu-id="34020-117">The total number of blocks on the disk.</span></span>

</dd> <dt>

<span data-ttu-id="34020-118">**дискленгс**</span><span class="sxs-lookup"><span data-stu-id="34020-118">**DiskLength**</span></span>
</dt> <dd>

<span data-ttu-id="34020-119">Размер диска в байтах.</span><span class="sxs-lookup"><span data-stu-id="34020-119">The disk size in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34020-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34020-120">Remarks</span></span>

<span data-ttu-id="34020-121">Файл заголовка Нтддстор. h доступен в комплекте драйверов Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="34020-121">The header file Ntddstor.h is available in the Windows Driver Kit (WDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="34020-122">Требования</span><span class="sxs-lookup"><span data-stu-id="34020-122">Requirements</span></span>



| <span data-ttu-id="34020-123">Требование</span><span class="sxs-lookup"><span data-stu-id="34020-123">Requirement</span></span> | <span data-ttu-id="34020-124">Значение</span><span class="sxs-lookup"><span data-stu-id="34020-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34020-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="34020-125">Minimum supported client</span></span><br/> | <span data-ttu-id="34020-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34020-126">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="34020-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="34020-127">Minimum supported server</span></span><br/> | <span data-ttu-id="34020-128">Windows Server 2008, Windows Server 2003 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="34020-128">Windows Server 2008, Windows Server 2003 with SP1</span></span><br/>                          |
| <span data-ttu-id="34020-129">Header</span><span class="sxs-lookup"><span data-stu-id="34020-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="34020-130"><dt>Нтддстор. h</dt></span><span class="sxs-lookup"><span data-stu-id="34020-130"><dt>Ntddstor.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34020-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34020-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34020-132">**\_Чтение данных \_ о \_ емкости хранилища ioctl**</span><span class="sxs-lookup"><span data-stu-id="34020-132">**IOCTL\_STORAGE\_READ\_CAPACITY**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




