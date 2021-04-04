---
description: 'Удаляет ограничение доступа для диапазона байтов, которые ранее были ограничены с помощью Ибитебуффер:: LockRegion.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'Метод Ибитебуффер:: UnlockRegion (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92e49ba000177326ad14d3b83002613a15e96e18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999303"
---
# <a name="ibytebufferunlockregion-method"></a><span data-ttu-id="f44f0-103">Метод Ибитебуффер:: UnlockRegion</span><span class="sxs-lookup"><span data-stu-id="f44f0-103">IByteBuffer::UnlockRegion method</span></span>

<span data-ttu-id="f44f0-104">\[Метод **UnlockRegion** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f44f0-104">\[The **UnlockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f44f0-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f44f0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f44f0-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="f44f0-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="f44f0-107">Метод **UnlockRegion** удаляет ограничение доступа для диапазона байтов, которые ранее были ограничены с помощью [**Ибитебуффер:: LockRegion**](ibytebuffer-lockregion.md).</span><span class="sxs-lookup"><span data-stu-id="f44f0-107">The **UnlockRegion** method removes the access restriction on a range of bytes previously restricted by using [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f44f0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f44f0-108">Syntax</span></span>


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="f44f0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f44f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f44f0-110">*либоффсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f44f0-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44f0-111">Смещение в байтах для начала диапазона.</span><span class="sxs-lookup"><span data-stu-id="f44f0-111">Byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="f44f0-112">*CB* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f44f0-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44f0-113">Длина (в байтах) диапазона, который должен быть ограничен.</span><span class="sxs-lookup"><span data-stu-id="f44f0-113">Length, in bytes, of the range to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="f44f0-114">*двлокктипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f44f0-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f44f0-115">Ограничения доступа, ранее помещенные в диапазон.</span><span class="sxs-lookup"><span data-stu-id="f44f0-115">Access restrictions previously placed on the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f44f0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f44f0-116">Return value</span></span>

<span data-ttu-id="f44f0-117">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f44f0-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="f44f0-118">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="f44f0-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f44f0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f44f0-119">Remarks</span></span>

<span data-ttu-id="f44f0-120">Метод **ибитебуффер:: UnlockRegion** разблокирует область, ранее заблокированную с помощью метода [**Ибитебуффер:: LockRegion**](ibytebuffer-lockregion.md) .</span><span class="sxs-lookup"><span data-stu-id="f44f0-120">The **IByteBuffer::UnlockRegion** method unlocks a region previously locked by using the [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md) method.</span></span> <span data-ttu-id="f44f0-121">Заблокированные регионы позже должны быть явным образом разблокированы путем вызова **ибитебуффер:: UnlockRegion** с теми же значениями параметров *либоффсет*, *CB* и *двлокктипе* .</span><span class="sxs-lookup"><span data-stu-id="f44f0-121">Locked regions must later be explicitly unlocked by calling **IByteBuffer::UnlockRegion** with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="f44f0-122">Перед освобождением потока необходимо разблокировать регион.</span><span class="sxs-lookup"><span data-stu-id="f44f0-122">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="f44f0-123">Два смежных региона не могут быть заблокированы отдельно, а затем разблокированы с помощью одного вызова Unlock.</span><span class="sxs-lookup"><span data-stu-id="f44f0-123">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="f44f0-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="f44f0-124">Examples</span></span>

<span data-ttu-id="f44f0-125">В следующем примере показано Разблокирование диапазона байтов.</span><span class="sxs-lookup"><span data-stu-id="f44f0-125">The following example shows unlocking a range of bytes.</span></span>


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="f44f0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f44f0-126">Requirements</span></span>



| <span data-ttu-id="f44f0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f44f0-127">Requirement</span></span> | <span data-ttu-id="f44f0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f44f0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f44f0-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f44f0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f44f0-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f44f0-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f44f0-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f44f0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f44f0-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f44f0-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f44f0-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f44f0-133">End of client support</span></span><br/>    | <span data-ttu-id="f44f0-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f44f0-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f44f0-135">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f44f0-135">End of server support</span></span><br/>    | <span data-ttu-id="f44f0-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f44f0-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f44f0-137">Header</span><span class="sxs-lookup"><span data-stu-id="f44f0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f44f0-138"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f44f0-138"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f44f0-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f44f0-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f44f0-140"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f44f0-140"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f44f0-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f44f0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f44f0-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f44f0-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f44f0-143">IID</span><span class="sxs-lookup"><span data-stu-id="f44f0-143">IID</span></span><br/>                      | <span data-ttu-id="f44f0-144">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="f44f0-144">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

