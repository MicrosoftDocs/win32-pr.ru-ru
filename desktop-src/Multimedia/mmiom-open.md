---
title: Сообщение MMIOM_OPEN (Ммсистем. h)
description: Сообщение ММИОМ \_ Open отправляется в процедуру ввода-вывода с помощью функции ммиупен, чтобы запросить открытие или удаление файла.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- MMIOM_OPEN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650402"
---
# <a name="mmiom_open-message"></a><span data-ttu-id="7468a-104">ММИОМ \_ открытое сообщение</span><span class="sxs-lookup"><span data-stu-id="7468a-104">MMIOM\_OPEN message</span></span>

<span data-ttu-id="7468a-105">Сообщение **ммиом \_ Open** отправляется в процедуру ввода-вывода с помощью функции [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) , чтобы запросить открытие или удаление файла.</span><span class="sxs-lookup"><span data-stu-id="7468a-105">The **MMIOM\_OPEN** message is sent to an I/O procedure by the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to request that a file be opened or deleted.</span></span>


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="7468a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7468a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7468a-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*лпсзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="7468a-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span></span>
</dt> <dd>

<span data-ttu-id="7468a-108">Строка, заканчивающаяся нулем и содержащая имя открываемого файла.</span><span class="sxs-lookup"><span data-stu-id="7468a-108">Null-terminated string containing the name of the file to open.</span></span>

</dd> <dt>

<span data-ttu-id="7468a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7468a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7468a-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="7468a-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7468a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7468a-111">Return Value</span></span>

<span data-ttu-id="7468a-112">Возвращает ММСИСЕРР \_ в случае успеха или ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7468a-112">Returns MMSYSERR\_NOERROR if successful or an error otherwise.</span></span> <span data-ttu-id="7468a-113">Возможные значения ошибок включают следующее.</span><span class="sxs-lookup"><span data-stu-id="7468a-113">Possible error values include the following:</span></span>



| <span data-ttu-id="7468a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="7468a-114">Requirement</span></span> | <span data-ttu-id="7468a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7468a-115">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="7468a-116">ММИОМ \_ каннотопен</span><span class="sxs-lookup"><span data-stu-id="7468a-116">MMIOM\_CANNOTOPEN</span></span>  | <span data-ttu-id="7468a-117">Не удалось открыть файл.</span><span class="sxs-lookup"><span data-stu-id="7468a-117">The file could not be opened.</span></span>               |
| <span data-ttu-id="7468a-118">ММИОМ \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="7468a-118">MMIOM\_OUTOFMEMORY</span></span> | <span data-ttu-id="7468a-119">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="7468a-119">Not enough memory to perform the operation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7468a-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7468a-120">Remarks</span></span>

<span data-ttu-id="7468a-121">Элемент **dwFlags** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) содержит флаги, передаваемые функции [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="7468a-121">The **dwFlags** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure contains flags passed to the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span>

<span data-ttu-id="7468a-122">Элемент **лдискоффсет** структуры [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) инициализируется нулевым значением.</span><span class="sxs-lookup"><span data-stu-id="7468a-122">The **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure is initialized to zero.</span></span> <span data-ttu-id="7468a-123">Если это значение неверно, процедура ввода-вывода должна исправить ее.</span><span class="sxs-lookup"><span data-stu-id="7468a-123">If this value is incorrect, the I/O procedure must correct it.</span></span>

<span data-ttu-id="7468a-124">Если приложение передавало структуру [**ммиоинфо**](/previous-versions//dd757322(v=vs.85)) в [**ммиупен**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), возвращаемое значение возвращается в элементе **верроррет** .</span><span class="sxs-lookup"><span data-stu-id="7468a-124">If the application passed an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), the return value is returned in the **wErrorRet** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="7468a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7468a-125">Requirements</span></span>



| <span data-ttu-id="7468a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7468a-126">Requirement</span></span> | <span data-ttu-id="7468a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7468a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7468a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7468a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7468a-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7468a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7468a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7468a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7468a-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7468a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7468a-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7468a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7468a-133"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7468a-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

