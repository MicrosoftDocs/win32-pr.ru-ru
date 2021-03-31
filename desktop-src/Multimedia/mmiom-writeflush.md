---
title: Сообщение MMIOM_WRITEFLUSH (Ммсистем. h)
description: Сообщение ММИОМ \_ вритефлуш отправляется в процедуру ввода-вывода с помощью функции ммиоврите, чтобы запросить запись данных в открытый файл и очистить все внутренние буферы, используемые процедурой ввода-вывода, на диск.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- MMIOM_WRITEFLUSH сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b294d4c461970a3304f09088cf63a6564acd50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803670"
---
# <a name="mmiom_writeflush-message"></a><span data-ttu-id="9b242-104">\_Сообщение ммиом вритефлуш</span><span class="sxs-lookup"><span data-stu-id="9b242-104">MMIOM\_WRITEFLUSH message</span></span>

<span data-ttu-id="9b242-105">Сообщение **ммиом \_ вритефлуш** отправляется в процедуру ввода-вывода с помощью функции [**ммиоврите**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) , чтобы запросить запись данных в открытый файл и очистить все внутренние буферы, используемые процедурой ввода-вывода, на диск.</span><span class="sxs-lookup"><span data-stu-id="9b242-105">The **MMIOM\_WRITEFLUSH** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file and that any internal buffers used by the I/O procedure be flushed to disk.</span></span>


```C++
MMIOM_WRITEFLUSH 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="9b242-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b242-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b242-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*лпбуффер*</span><span class="sxs-lookup"><span data-stu-id="9b242-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="9b242-108">Указатель на буфер, содержащий данные для записи в файл.</span><span class="sxs-lookup"><span data-stu-id="9b242-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="9b242-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*кбврите*</span><span class="sxs-lookup"><span data-stu-id="9b242-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="9b242-110">Число байтов для записи в файл.</span><span class="sxs-lookup"><span data-stu-id="9b242-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b242-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b242-111">Return Value</span></span>

<span data-ttu-id="9b242-112">Возвращает число байтов, фактически записанных в файл.</span><span class="sxs-lookup"><span data-stu-id="9b242-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="9b242-113">Если возникает ошибка, возвращается значение 1.</span><span class="sxs-lookup"><span data-stu-id="9b242-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b242-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b242-114">Remarks</span></span>

<span data-ttu-id="9b242-115">Процедура ввода-вывода отвечает за обновление элемента **лдискоффсет** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) для отражения нового расположения файла после операции записи.</span><span class="sxs-lookup"><span data-stu-id="9b242-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

<span data-ttu-id="9b242-116">Это сообщение эквивалентно сообщению [**\_ Write ммиом**](mmiom-write.md) , за исключением того, что он запрашивает, чтобы процедура ввода-вывода сбросила свои внутренние буферы, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="9b242-116">This message is equivalent to the [**MMIOM\_WRITE**](mmiom-write.md) message except that it requests that the I/O procedure flush its internal buffers, if any.</span></span> <span data-ttu-id="9b242-117">Если процедура ввода-вывода не выполняет внутреннюю буферизацию, это сообщение может обрабатываться точно так же, как сообщение **ммиом \_ Write** .</span><span class="sxs-lookup"><span data-stu-id="9b242-117">Unless an I/O procedure performs internal buffering, this message can be handled exactly like the **MMIOM\_WRITE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b242-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9b242-118">Requirements</span></span>



| <span data-ttu-id="9b242-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9b242-119">Requirement</span></span> | <span data-ttu-id="9b242-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9b242-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b242-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b242-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9b242-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9b242-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9b242-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b242-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9b242-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9b242-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9b242-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9b242-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b242-126"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b242-126"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

