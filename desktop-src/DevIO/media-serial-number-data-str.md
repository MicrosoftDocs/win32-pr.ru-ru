---
description: Содержит серийный номер USB-устройства. Он используется в качестве \_ \_ контрольного кода для хранилища ioctl Get \_ Media \_ серийный \_ номер.
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: Структура MEDIA_SERIAL_NUMBER_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105647755"
---
# <a name="media_serial_number_data-structure"></a><span data-ttu-id="756e8-104">\_ \_ Структура данных серийного номера носителя \_</span><span class="sxs-lookup"><span data-stu-id="756e8-104">MEDIA\_SERIAL\_NUMBER\_DATA structure</span></span>

<span data-ttu-id="756e8-105">Содержит серийный номер USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="756e8-105">Contains the serial number of a USB device.</span></span> <span data-ttu-id="756e8-106">Он используется в качестве контрольного кода для [**\_ хранилища ioctl \_ Get \_ Media \_ серийный \_ номер**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) .</span><span class="sxs-lookup"><span data-stu-id="756e8-106">It is used by the [**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) control code.</span></span>

## <a name="syntax"></a><span data-ttu-id="756e8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="756e8-107">Syntax</span></span>


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a><span data-ttu-id="756e8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="756e8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="756e8-109">**сериалнумберленгс**</span><span class="sxs-lookup"><span data-stu-id="756e8-109">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="756e8-110">Размер строки **сериалнумбердата** в байтах.</span><span class="sxs-lookup"><span data-stu-id="756e8-110">The size of the **SerialNumberData** string, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="756e8-111">**Результат**</span><span class="sxs-lookup"><span data-stu-id="756e8-111">**Result**</span></span>
</dt> <dd>

<span data-ttu-id="756e8-112">Состояние запроса.</span><span class="sxs-lookup"><span data-stu-id="756e8-112">The status of the request.</span></span>

</dd> <dt>

<span data-ttu-id="756e8-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="756e8-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="756e8-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="756e8-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="756e8-115">**сериалнумбердата**</span><span class="sxs-lookup"><span data-stu-id="756e8-115">**SerialNumberData**</span></span>
</dt> <dd>

<span data-ttu-id="756e8-116">Серийный номер устройства.</span><span class="sxs-lookup"><span data-stu-id="756e8-116">The serial number of the device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="756e8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="756e8-117">Remarks</span></span>

<span data-ttu-id="756e8-118">Для структуры **\_ \_ \_ данных серийного номера носителя** не доступен файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="756e8-118">No header file is available for the **MEDIA\_SERIAL\_NUMBER\_DATA** structure.</span></span> <span data-ttu-id="756e8-119">Включите определение структуры в верхнюю часть этой страницы в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="756e8-119">Include the structure definition at the top of this page in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="756e8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="756e8-120">Requirements</span></span>



| <span data-ttu-id="756e8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="756e8-121">Requirement</span></span> | <span data-ttu-id="756e8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="756e8-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="756e8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="756e8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="756e8-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="756e8-124">Windows XP</span></span><br/>          |
| <span data-ttu-id="756e8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="756e8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="756e8-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="756e8-126">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="756e8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="756e8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="756e8-128">**IOCTL \_ хранилище \_ Получение \_ \_ серийного \_ номера носителя**</span><span class="sxs-lookup"><span data-stu-id="756e8-128">**IOCTL\_STORAGE\_GET\_MEDIA\_SERIAL\_NUMBER**</span></span>](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




