---
title: Сообщение MMIOM_WRITE (Ммсистем. h)
description: Сообщение ММИОМ \_ Write отправляется в процедуру ввода-вывода с помощью функции ммиоврите, чтобы запросить запись данных в открытый файл.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- MMIOM_WRITE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989272"
---
# <a name="mmiom_write-message"></a><span data-ttu-id="9bcfa-104">\_Сообщение записи ммиом</span><span class="sxs-lookup"><span data-stu-id="9bcfa-104">MMIOM\_WRITE message</span></span>

<span data-ttu-id="9bcfa-105">Сообщение **ммиом \_ Write** отправляется в процедуру ввода-вывода с помощью функции [**ммиоврите**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) , чтобы запросить запись данных в открытый файл.</span><span class="sxs-lookup"><span data-stu-id="9bcfa-105">The **MMIOM\_WRITE** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file.</span></span>


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="9bcfa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bcfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bcfa-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*лпбуффер*</span><span class="sxs-lookup"><span data-stu-id="9bcfa-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="9bcfa-108">Указатель на буфер, содержащий данные для записи в файл.</span><span class="sxs-lookup"><span data-stu-id="9bcfa-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="9bcfa-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*кбврите*</span><span class="sxs-lookup"><span data-stu-id="9bcfa-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="9bcfa-110">Число байтов для записи в файл.</span><span class="sxs-lookup"><span data-stu-id="9bcfa-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bcfa-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bcfa-111">Return Value</span></span>

<span data-ttu-id="9bcfa-112">Возвращает число байтов, фактически записанных в файл.</span><span class="sxs-lookup"><span data-stu-id="9bcfa-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="9bcfa-113">Если возникает ошибка, возвращается значение 1.</span><span class="sxs-lookup"><span data-stu-id="9bcfa-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bcfa-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bcfa-114">Remarks</span></span>

<span data-ttu-id="9bcfa-115">Процедура ввода-вывода отвечает за обновление элемента **лдискоффсет** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) для отражения нового расположения файла после операции записи.</span><span class="sxs-lookup"><span data-stu-id="9bcfa-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bcfa-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9bcfa-116">Requirements</span></span>



| <span data-ttu-id="9bcfa-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9bcfa-117">Requirement</span></span> | <span data-ttu-id="9bcfa-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9bcfa-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcfa-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bcfa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9bcfa-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9bcfa-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9bcfa-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bcfa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9bcfa-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9bcfa-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9bcfa-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9bcfa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bcfa-124"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bcfa-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

