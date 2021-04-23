---
description: Освобождает блок памяти, выделенный из кучи с помощью Ртлаллокатехеап.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: Функция Ртлфрихеап (Нтифс. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538843"
---
# <a name="rtlfreeheap-function"></a><span data-ttu-id="a5873-103">Функция Ртлфрихеап</span><span class="sxs-lookup"><span data-stu-id="a5873-103">RtlFreeHeap function</span></span>

<span data-ttu-id="a5873-104">Освобождает блок памяти, выделенный из кучи с помощью [**ртлаллокатехеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span><span class="sxs-lookup"><span data-stu-id="a5873-104">Frees a memory block that was allocated from a heap by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5873-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5873-105">Syntax</span></span>


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a><span data-ttu-id="a5873-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5873-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5873-107">*Хеафандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5873-107">*HeapHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5873-108">Маркер для кучи, блок памяти которого должен быть освобожден.</span><span class="sxs-lookup"><span data-stu-id="a5873-108">A handle for the heap whose memory block is to be freed.</span></span> <span data-ttu-id="a5873-109">Этот параметр является маркером, возвращаемым функцией [**ртлкреатехеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span><span class="sxs-lookup"><span data-stu-id="a5873-109">This parameter is a handle returned by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>

</dd> <dt>

<span data-ttu-id="a5873-110">*Флаги* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a5873-110">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a5873-111">Набор флагов, управляющих аспектами освобождения блока памяти.</span><span class="sxs-lookup"><span data-stu-id="a5873-111">A set of flags that controls aspects of freeing a memory block.</span></span> <span data-ttu-id="a5873-112">Указание следующего значения переопределяет соответствующее значение, указанное в параметре *flags* , когда куча была создана с помощью [**ртлкреатехеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span><span class="sxs-lookup"><span data-stu-id="a5873-112">Specifying the following value overrides the corresponding value that was specified in the *Flags* parameter when the heap was created by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>



| <span data-ttu-id="a5873-113">Flag</span><span class="sxs-lookup"><span data-stu-id="a5873-113">Flag</span></span>                           | <span data-ttu-id="a5873-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a5873-114">Meaning</span></span>                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5873-115">КУЧА \_ без \_ сериализации</span><span class="sxs-lookup"><span data-stu-id="a5873-115">HEAP\_NO\_SERIALIZE</span></span><br/> | <span data-ttu-id="a5873-116">Взаимное исключение не будет использоваться, если **ртлфрихеап** обращается к куче.</span><span class="sxs-lookup"><span data-stu-id="a5873-116">Mutual exclusion will not be used when **RtlFreeHeap** is accessing the heap.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="a5873-117">*Хеапбасе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5873-117">*HeapBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5873-118">Указатель на блок памяти для освобождения.</span><span class="sxs-lookup"><span data-stu-id="a5873-118">A pointer to the memory block to free.</span></span> <span data-ttu-id="a5873-119">Этот указатель возвращается функцией [**ртлаллокатехеап**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span><span class="sxs-lookup"><span data-stu-id="a5873-119">This pointer is returned by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5873-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5873-120">Return value</span></span>

<span data-ttu-id="a5873-121">Возвращает **значение true** , если блок был успешно освобожден; В противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="a5873-121">Returns **TRUE** if the block was freed successfully; **FALSE** otherwise.</span></span>

> [!Note]  
> <span data-ttu-id="a5873-122">Начиная с Windows 8 возвращаемое значение типизировано как **логическое**, имеющее размер, отличный от **логического**.</span><span class="sxs-lookup"><span data-stu-id="a5873-122">Starting with Windows 8 the return value is typed as **LOGICAL**, which has a different size than **BOOLEAN**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a5873-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a5873-123">Requirements</span></span>



| <span data-ttu-id="a5873-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a5873-124">Requirement</span></span> | <span data-ttu-id="a5873-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a5873-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5873-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5873-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a5873-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5873-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="a5873-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5873-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a5873-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5873-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="a5873-130">Целевая платформа</span><span class="sxs-lookup"><span data-stu-id="a5873-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="a5873-131"><dt>[Универсальной](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="a5873-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="a5873-132">Header</span><span class="sxs-lookup"><span data-stu-id="a5873-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5873-133"><dt>Нтифс. h (включение Нтифс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5873-133"><dt>Ntifs.h (include Ntifs.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="a5873-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a5873-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5873-135"><dt>NTDLL. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5873-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a5873-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a5873-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5873-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5873-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="a5873-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5873-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5873-139">**ртлаллокатехеап**</span><span class="sxs-lookup"><span data-stu-id="a5873-139">**RtlAllocateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[<span data-ttu-id="a5873-140">**ртлкреатехеап**</span><span class="sxs-lookup"><span data-stu-id="a5873-140">**RtlCreateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[<span data-ttu-id="a5873-141">**ртлдестройхеап**</span><span class="sxs-lookup"><span data-stu-id="a5873-141">**RtlDestroyHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
