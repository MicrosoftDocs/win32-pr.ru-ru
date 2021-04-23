---
title: Сообщение MMIOM_READ (Ммсистем. h)
description: Сообщение ММИОМ \_ readed отправляется в процедуру ввода-вывода с помощью функции ммиореад, чтобы запросить чтение указанного числа байтов из открытого файла.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- MMIOM_READ сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493266"
---
# <a name="mmiom_read-message"></a><span data-ttu-id="be05b-104">ММИОМ \_ Чтение сообщения</span><span class="sxs-lookup"><span data-stu-id="be05b-104">MMIOM\_READ message</span></span>

<span data-ttu-id="be05b-105">Сообщение **ммиом \_ readed** отправляется в процедуру ввода-вывода с помощью функции [**ммиореад**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) , чтобы запросить чтение указанного числа байтов из открытого файла.</span><span class="sxs-lookup"><span data-stu-id="be05b-105">The **MMIOM\_READ** message is sent to an I/O procedure by the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) function to request that a specified number of bytes be read from an open file.</span></span>


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a><span data-ttu-id="be05b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be05b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be05b-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*лбуффер*</span><span class="sxs-lookup"><span data-stu-id="be05b-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="be05b-108">Указатель на буфер, который должен быть заполнен данными, считанными из файла.</span><span class="sxs-lookup"><span data-stu-id="be05b-108">Pointer to the buffer to be filled with data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="be05b-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*кбреад*</span><span class="sxs-lookup"><span data-stu-id="be05b-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span></span>
</dt> <dd>

<span data-ttu-id="be05b-110">Число байтов для чтения из файла.</span><span class="sxs-lookup"><span data-stu-id="be05b-110">Number of bytes to read from file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be05b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be05b-111">Return Value</span></span>

<span data-ttu-id="be05b-112">Возвращает число байтов, фактически считанных из файла.</span><span class="sxs-lookup"><span data-stu-id="be05b-112">Returns the number of bytes actually read from the file.</span></span> <span data-ttu-id="be05b-113">Если не удается прочитать больше байтов, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="be05b-113">If no more bytes can be read, the return value is 0.</span></span> <span data-ttu-id="be05b-114">Если возникает ошибка, возвращается значение 1.</span><span class="sxs-lookup"><span data-stu-id="be05b-114">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="be05b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be05b-115">Remarks</span></span>

<span data-ttu-id="be05b-116">Процедура ввода-вывода отвечает за обновление элемента **лдискоффсет** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) для отражения нового расположения файла после операции чтения.</span><span class="sxs-lookup"><span data-stu-id="be05b-116">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the read operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="be05b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="be05b-117">Requirements</span></span>



| <span data-ttu-id="be05b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="be05b-118">Requirement</span></span> | <span data-ttu-id="be05b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="be05b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be05b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be05b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="be05b-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be05b-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be05b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be05b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="be05b-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be05b-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="be05b-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="be05b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="be05b-125"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be05b-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

