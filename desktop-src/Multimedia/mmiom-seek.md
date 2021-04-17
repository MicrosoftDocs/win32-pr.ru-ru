---
title: Сообщение MMIOM_SEEK (Ммсистем. h)
description: Сообщение ММИОМ \_ Seek отправляется в процедуру ввода-вывода функцией ммиосик, чтобы запросить перемещение текущего расположения файла.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682102"
---
# <a name="mmiom_seek-message"></a><span data-ttu-id="d8d1d-104">\_Сообщение ммиом Seek</span><span class="sxs-lookup"><span data-stu-id="d8d1d-104">MMIOM\_SEEK message</span></span>

<span data-ttu-id="d8d1d-105">Сообщение **ммиом \_ Seek** отправляется в процедуру ввода-вывода функцией [**ммиосик**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) , чтобы запросить перемещение текущего расположения файла.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-105">The **MMIOM\_SEEK** message is sent to an I/O procedure by the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function to request that the current file position be moved.</span></span>


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a><span data-ttu-id="d8d1d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8d1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8d1d-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*лневфилепос*</span><span class="sxs-lookup"><span data-stu-id="d8d1d-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="d8d1d-108">Новое расположение файла.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-108">New file position.</span></span> <span data-ttu-id="d8d1d-109">Значение этого параметра зависит от флага, указанного в **лчанжефлаг**.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-109">The meaning of this value is dependent on the flag specified in **lChangeFlag**.</span></span>

</dd> <dt>

<span data-ttu-id="d8d1d-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*лчанжефлаг*</span><span class="sxs-lookup"><span data-stu-id="d8d1d-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span></span>
</dt> <dd>

<span data-ttu-id="d8d1d-111">Флаг, указывающий, как изменяется расположение файла.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-111">Flag specifying how the file position is changed.</span></span> <span data-ttu-id="d8d1d-112">Определены следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d8d1d-112">The following values are defined:</span></span>



| <span data-ttu-id="d8d1d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="d8d1d-113">Requirement</span></span> | <span data-ttu-id="d8d1d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d8d1d-114">Value</span></span> |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d1d-115">Поиск \_ вал.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-115">SEEK\_CUR</span></span> | <span data-ttu-id="d8d1d-116">Переместить расположение файла, чтобы *лневфилепос* байты из текущей положения.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-116">Move the file position to be *lNewFilePos* bytes from the current position.</span></span> <span data-ttu-id="d8d1d-117">*лневфилепос* может быть положительным или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-117">*lNewFilePos* can be positive or negative.</span></span> |
| <span data-ttu-id="d8d1d-118">\_конец поиска</span><span class="sxs-lookup"><span data-stu-id="d8d1d-118">SEEK\_END</span></span> | <span data-ttu-id="d8d1d-119">Переместите положение файла в *лневфилепос* байт с конца файла.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-119">Move the file position to be *lNewFilePos* bytes from the end of the file.</span></span>                                             |
| <span data-ttu-id="d8d1d-120">Поиск \_ набора</span><span class="sxs-lookup"><span data-stu-id="d8d1d-120">SEEK\_SET</span></span> | <span data-ttu-id="d8d1d-121">Переместите положение файла в *лневфилепос* байт с начала файла.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-121">Move the file position to be *lNewFilePos* bytes from the beginning of the file.</span></span>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8d1d-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8d1d-122">Return Value</span></span>

<span data-ttu-id="d8d1d-123">Возвращает новое расположение файла.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-123">Returns the new file position.</span></span> <span data-ttu-id="d8d1d-124">Если возникает ошибка, возвращается значение 1.</span><span class="sxs-lookup"><span data-stu-id="d8d1d-124">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8d1d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8d1d-125">Remarks</span></span>

<span data-ttu-id="d8d1d-126">Процедура ввода-вывода отвечает за поддержание текущего расположения файла в элементе **лдискоффсет** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d8d1d-126">The I/O procedure is responsible for maintaining the current file position in the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8d1d-127">Требования</span><span class="sxs-lookup"><span data-stu-id="d8d1d-127">Requirements</span></span>



| <span data-ttu-id="d8d1d-128">Требование</span><span class="sxs-lookup"><span data-stu-id="d8d1d-128">Requirement</span></span> | <span data-ttu-id="d8d1d-129">Значение</span><span class="sxs-lookup"><span data-stu-id="d8d1d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d1d-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8d1d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d8d1d-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d8d1d-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d8d1d-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8d1d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d8d1d-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d8d1d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d8d1d-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d8d1d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8d1d-135"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8d1d-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

