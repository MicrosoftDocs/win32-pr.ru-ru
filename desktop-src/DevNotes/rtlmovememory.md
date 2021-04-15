---
description: Копирует содержимое блока памяти источника в целевой блок памяти и поддерживает перекрывающиеся блоки памяти источника и назначения.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Функция Ртлмовемемори (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662082"
---
# <a name="rtlmovememory-function"></a><span data-ttu-id="7451a-103">Функция Ртлмовемемори</span><span class="sxs-lookup"><span data-stu-id="7451a-103">RtlMoveMemory function</span></span>

<span data-ttu-id="7451a-104">Копирует содержимое блока памяти источника в целевой блок памяти и поддерживает перекрывающиеся блоки памяти источника и назначения.</span><span class="sxs-lookup"><span data-stu-id="7451a-104">Copies the contents of a source memory block to a destination memory block, and supports overlapping source and destination memory blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="7451a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7451a-105">Syntax</span></span>


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a><span data-ttu-id="7451a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7451a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7451a-107">*Назначение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7451a-107">*Destination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7451a-108">Указатель на блок памяти назначения, в который копируются байты.</span><span class="sxs-lookup"><span data-stu-id="7451a-108">A pointer to the destination memory block to copy the bytes to.</span></span>

</dd> <dt>

<span data-ttu-id="7451a-109">*Исходный код* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7451a-109">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7451a-110">Указатель на блок памяти источника, из которого копируются байты.</span><span class="sxs-lookup"><span data-stu-id="7451a-110">A pointer to the source memory block to copy the bytes from.</span></span>

</dd> <dt>

<span data-ttu-id="7451a-111">*Длина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7451a-111">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7451a-112">Число байтов для копирования из источника в место назначения.</span><span class="sxs-lookup"><span data-stu-id="7451a-112">The number of bytes to copy from the source to the destination.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7451a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7451a-113">Return value</span></span>

<span data-ttu-id="7451a-114">None</span><span class="sxs-lookup"><span data-stu-id="7451a-114">None</span></span>

## <a name="remarks"></a><span data-ttu-id="7451a-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="7451a-115">Remarks</span></span>

<span data-ttu-id="7451a-116">Блок памяти источника, определяемый *исходным* и *длинным*, может пересекаться с целевым блоком памяти, который определяется *назначением* и *длиной*.</span><span class="sxs-lookup"><span data-stu-id="7451a-116">The source memory block, which is defined by *Source* and *Length*, can overlap the destination memory block, which is defined by *Destination* and *Length*.</span></span>

<span data-ttu-id="7451a-117">Подпрограммы [**ртлкопимемори**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) выполняются быстрее, чем **Ртлмовемемори**, но **ртлкопимемори** требует, чтобы исходный и целевой блоки памяти не перекрывалися.</span><span class="sxs-lookup"><span data-stu-id="7451a-117">The [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) routine runs faster than **RtlMoveMemory**, but **RtlCopyMemory** requires that the source and destination memory blocks do not overlap.</span></span>

<span data-ttu-id="7451a-118">Вызывающие объекты **ртлмовемемори** могут выполняться на любом уровне IRQL, если блоки памяти источника и назначения находятся в нестраничной системной памяти.</span><span class="sxs-lookup"><span data-stu-id="7451a-118">Callers of **RtlMoveMemory** can be running at any IRQL if the source and destination memory blocks are in nonpaged system memory.</span></span> <span data-ttu-id="7451a-119">В противном случае вызывающий объект должен работать на уровне IRQL <= APC \_ .</span><span class="sxs-lookup"><span data-stu-id="7451a-119">Otherwise, the caller must be running at IRQL <= APC\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7451a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="7451a-120">Requirements</span></span>



| <span data-ttu-id="7451a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="7451a-121">Requirement</span></span> | <span data-ttu-id="7451a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="7451a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7451a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7451a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="7451a-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7451a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="7451a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7451a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="7451a-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7451a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="7451a-127">Целевая платформа</span><span class="sxs-lookup"><span data-stu-id="7451a-127">Target platform</span></span><br/>          | <dl> <span data-ttu-id="7451a-128"><dt>[Универсальной](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="7451a-128"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="7451a-129">Header</span><span class="sxs-lookup"><span data-stu-id="7451a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7451a-130"><dt>WDM. h (включает WDM. h, Нтддк. h или Нтифс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7451a-130"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="7451a-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7451a-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="7451a-132"><dt>NTDLL. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7451a-132"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7451a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7451a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7451a-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7451a-134"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="7451a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7451a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7451a-136">**ртлкопимемори**</span><span class="sxs-lookup"><span data-stu-id="7451a-136">**RtlCopyMemory**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
