---
description: Разрешает доступ к указанному диапазону байтов в буферном объекте.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'Метод Ибитебуффер:: LockRegion (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272040"
---
# <a name="ibytebufferlockregion-method"></a><span data-ttu-id="a0b71-103">Метод Ибитебуффер:: LockRegion</span><span class="sxs-lookup"><span data-stu-id="a0b71-103">IByteBuffer::LockRegion method</span></span>

<span data-ttu-id="a0b71-104">\[Метод **LockRegion** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="a0b71-104">\[The **LockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a0b71-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a0b71-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a0b71-106">Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="a0b71-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="a0b71-107">Метод **LockRegion** предоставляет доступ к указанному диапазону байтов в буферном объекте.</span><span class="sxs-lookup"><span data-stu-id="a0b71-107">The **LockRegion** method restricts access to a specified range of bytes in the buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b71-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0b71-108">Syntax</span></span>


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="a0b71-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0b71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0b71-110">*либоффсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0b71-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0b71-111">Целое число, задающее смещение в байтах для начала диапазона.</span><span class="sxs-lookup"><span data-stu-id="a0b71-111">Integer that specifies the byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="a0b71-112">*CB* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0b71-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0b71-113">Целое число, указывающее длину диапазона в байтах, поддающийся ограничению.</span><span class="sxs-lookup"><span data-stu-id="a0b71-113">Integer that specifies the length of the range, in bytes, to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="a0b71-114">*двлокктипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0b71-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0b71-115">Указывает ограничения, запрашиваемые при доступе к диапазону.</span><span class="sxs-lookup"><span data-stu-id="a0b71-115">Specifies the restrictions being requested on accessing the range.</span></span> <span data-ttu-id="a0b71-116">Это может быть одно из значений, приведенных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a0b71-116">This can be one of the values in the following table.</span></span>



| <span data-ttu-id="a0b71-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a0b71-117">Value</span></span>                                                                                                                                                            | <span data-ttu-id="a0b71-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a0b71-118">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <span data-ttu-id="a0b71-119"><dt>**Блокировка \_ записи**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b71-119"><dt>**LOCK\_WRITE**</dt></span></span> </dl>             | <span data-ttu-id="a0b71-120">Указанный диапазон байтов можно открыть и прочитать любое количество раз, но запись в заблокированный диапазон запрещена, кроме владельца, которому была предоставлена эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="a0b71-120">The specified range of bytes can be opened and read any number of times, but writing to the locked range is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <span data-ttu-id="a0b71-121"><dt>**\_монопольная блокировка**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b71-121"><dt>**LOCK\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="a0b71-122">Запись в указанный диапазон байтов запрещена, кроме владельца, которому была предоставлена эта блокировка.</span><span class="sxs-lookup"><span data-stu-id="a0b71-122">Writing to the specified range of bytes is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <span data-ttu-id="a0b71-123"><dt>**ЗАБЛОКИРОВАТЬ \_ онлйонце**</dt></span><span class="sxs-lookup"><span data-stu-id="a0b71-123"><dt>**LOCK\_ONLYONCE**</dt></span></span> </dl>    | <span data-ttu-id="a0b71-124">Если эта блокировка предоставлена, \_ в диапазоне нельзя получить другие блокировки блокировки онлйонце.</span><span class="sxs-lookup"><span data-stu-id="a0b71-124">If this lock is granted, no other LOCK\_ONLYONCE lock can be obtained on the range.</span></span> <span data-ttu-id="a0b71-125">Обычно этот тип блокировки является псевдонимом для другого типа блокировки.</span><span class="sxs-lookup"><span data-stu-id="a0b71-125">Usually this lock type is an alias for some other lock type.</span></span> <span data-ttu-id="a0b71-126">Таким образом, определенные реализации могут иметь дополнительное поведение, связанное с этим типом блокировки.</span><span class="sxs-lookup"><span data-stu-id="a0b71-126">Thus, specific implementations can have additional behavior associated with this lock type.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0b71-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0b71-127">Return value</span></span>

<span data-ttu-id="a0b71-128">Возвращаемое значение является значением **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a0b71-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="a0b71-129">Значение S \_ ОК указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="a0b71-129">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b71-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0b71-130">Remarks</span></span>

<span data-ttu-id="a0b71-131">Диапазон байтов может находиться за пределами текущего конца потока.</span><span class="sxs-lookup"><span data-stu-id="a0b71-131">The byte range can extend past the current end of the stream.</span></span> <span data-ttu-id="a0b71-132">Блокировка за пределами конца потока полезна в качестве метода связи между разными экземплярами потока без изменения данных, которые фактически являются частью потока.</span><span class="sxs-lookup"><span data-stu-id="a0b71-132">Locking beyond the end of a stream is useful as a method of communication between different instances of the stream without changing data that is actually part of the stream.</span></span>

<span data-ttu-id="a0b71-133">Поддерживается три типа блокировки: блокировка для исключения других модулей записи, блокировка для исключения других модулей чтения или записи и блокировка, которая позволяет только одному инициатору запроса получить блокировку в заданном диапазоне, что обычно является псевдонимом для одного из двух других типов блокировки.</span><span class="sxs-lookup"><span data-stu-id="a0b71-133">Three types of locking can be supported: locking to exclude other writers, locking to exclude other readers or writers, and locking that allows only one requester to obtain a lock on the given range, which is usually an alias for one of the other two lock types.</span></span> <span data-ttu-id="a0b71-134">Данный экземпляр потока может поддерживать один из двух первых типов или оба.</span><span class="sxs-lookup"><span data-stu-id="a0b71-134">A given stream instance might support either of the first two types, or both.</span></span> <span data-ttu-id="a0b71-135">Тип блокировки задается параметром *двлокктипе*, используя значение из перечисления [**LockType**](/windows/win32/api/objidl/ne-objidl-locktype) .</span><span class="sxs-lookup"><span data-stu-id="a0b71-135">The lock type is specified by *dwLockType*, using a value from the [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) enumeration.</span></span>

<span data-ttu-id="a0b71-136">После этого любой регион, заблокированный с помощью **LockRegion** , должен быть явно разблокирован вызовом [**Ибитебуффер:: UnlockRegion**](ibytebuffer-unlockregion.md) с теми же значениями *параметров либоффсет*, *CB* и *двлокктипе* .</span><span class="sxs-lookup"><span data-stu-id="a0b71-136">Any region locked with **LockRegion** must later be explicitly unlocked by calling [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="a0b71-137">Перед освобождением потока необходимо разблокировать регион.</span><span class="sxs-lookup"><span data-stu-id="a0b71-137">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="a0b71-138">Два смежных региона не могут быть заблокированы отдельно, а затем разблокированы с помощью одного вызова Unlock.</span><span class="sxs-lookup"><span data-stu-id="a0b71-138">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="a0b71-139">Примеры</span><span class="sxs-lookup"><span data-stu-id="a0b71-139">Examples</span></span>

<span data-ttu-id="a0b71-140">В следующем примере показано, как ограничивать доступ к диапазону байтов.</span><span class="sxs-lookup"><span data-stu-id="a0b71-140">The following example shows restricting access to a range of bytes.</span></span>


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="a0b71-141">Требования</span><span class="sxs-lookup"><span data-stu-id="a0b71-141">Requirements</span></span>



| <span data-ttu-id="a0b71-142">Требование</span><span class="sxs-lookup"><span data-stu-id="a0b71-142">Requirement</span></span> | <span data-ttu-id="a0b71-143">Значение</span><span class="sxs-lookup"><span data-stu-id="a0b71-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b71-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a0b71-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b71-145">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0b71-145">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a0b71-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a0b71-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b71-147">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0b71-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a0b71-148">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a0b71-148">End of client support</span></span><br/>    | <span data-ttu-id="a0b71-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0b71-149">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="a0b71-150">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a0b71-150">End of server support</span></span><br/>    | <span data-ttu-id="a0b71-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a0b71-151">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="a0b71-152">Header</span><span class="sxs-lookup"><span data-stu-id="a0b71-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0b71-153"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0b71-153"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0b71-154">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a0b71-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0b71-155"><dt>Скардссп. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a0b71-155"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a0b71-156">DLL</span><span class="sxs-lookup"><span data-stu-id="a0b71-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0b71-157"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0b71-157"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0b71-158">IID</span><span class="sxs-lookup"><span data-stu-id="a0b71-158">IID</span></span><br/>                      | <span data-ttu-id="a0b71-159">IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="a0b71-159">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

