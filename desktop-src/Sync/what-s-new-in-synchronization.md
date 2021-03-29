---
description: Windows содержит следующие новые программные элементы для синхронизации.
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: Новые возможности синхронизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264666"
---
# <a name="whats-new-in-synchronization"></a><span data-ttu-id="85952-103">Новые возможности синхронизации</span><span class="sxs-lookup"><span data-stu-id="85952-103">What's New in Synchronization</span></span>

<span data-ttu-id="85952-104">Windows содержит следующие новые программные элементы для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="85952-104">Windows includes the following new programming elements for synchronization.</span></span>

## <a name="windows-8"></a><span data-ttu-id="85952-105">Windows 8</span><span class="sxs-lookup"><span data-stu-id="85952-105">Windows 8</span></span>

### <a name="new-functions"></a><span data-ttu-id="85952-106">Новые функции</span><span class="sxs-lookup"><span data-stu-id="85952-106">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="85952-107">**делетесинчронизатионбарриер**</span><span class="sxs-lookup"><span data-stu-id="85952-107">**DeleteSynchronizationBarrier**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="85952-108">Удаляет барьер синхронизации.</span><span class="sxs-lookup"><span data-stu-id="85952-108">Deletes a synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-109">**ентерсинчронизатионбарриер**</span><span class="sxs-lookup"><span data-stu-id="85952-109">**EnterSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="85952-110">Заставляет вызывающий поток ждать в барьере синхронизации до тех пор, пока не будет введено максимальное число потоков.</span><span class="sxs-lookup"><span data-stu-id="85952-110">Causes the calling thread to wait at a synchronization barrier until the maximum number of threads have entered the barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-111">**жетоверлаппедресултекс**</span><span class="sxs-lookup"><span data-stu-id="85952-111">**GetOverlappedResultEx**</span></span>](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

<span data-ttu-id="85952-112">Возвращает результаты операции перекрытия для указанного файла, именованного канала или коммуникационного устройства в течение заданного интервала времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="85952-112">Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the specified time-out interval.</span></span> <span data-ttu-id="85952-113">Вызывающий поток может выполнить предупреждение.</span><span class="sxs-lookup"><span data-stu-id="85952-113">The calling thread can perform an alertable wait.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-114">**инитиализесинчронизатионбарриер**</span><span class="sxs-lookup"><span data-stu-id="85952-114">**InitializeSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="85952-115">Указывает максимальное число потоков и число счетчиков для нового барьера синхронизации.</span><span class="sxs-lookup"><span data-stu-id="85952-115">Specifies the maximum number of threads and spin count for a new synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-116">**ваитонаддресс**</span><span class="sxs-lookup"><span data-stu-id="85952-116">**WaitOnAddress**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

<span data-ttu-id="85952-117">Ожидает изменения значения по указанному адресу.</span><span class="sxs-lookup"><span data-stu-id="85952-117">Waits for the value at the specified address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-118">**вакебяддрессалл**</span><span class="sxs-lookup"><span data-stu-id="85952-118">**WakeByAddressAll**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

<span data-ttu-id="85952-119">Пробуждение всех потоков, ожидающих изменения значения адреса.</span><span class="sxs-lookup"><span data-stu-id="85952-119">Wakes all threads that are waiting for the value of an address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-120">**вакебяддресссингле**</span><span class="sxs-lookup"><span data-stu-id="85952-120">**WakeByAddressSingle**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

<span data-ttu-id="85952-121">Пробуждение одного потока, ожидающего изменения значения адреса.</span><span class="sxs-lookup"><span data-stu-id="85952-121">Wakes one thread that is waiting for the value of an address to change.</span></span>

</dd> </dl>

### <a name="new-interlocked-functions"></a><span data-ttu-id="85952-122">Новые функции с блокировкой</span><span class="sxs-lookup"><span data-stu-id="85952-122">New Interlocked Functions</span></span>

<dl> <dt>

<span data-ttu-id="85952-123">[**интерлоккедадднофенце**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-124">Выполняет атомарную операцию сложения с указанными **длинными** значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-124">Performs an atomic addition operation on the specified **LONG** values.</span></span> <span data-ttu-id="85952-125">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-125">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-127">Выполняет атомарную операцию сложения для указанных значений **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="85952-127">Performs an atomic addition operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="85952-128">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-128">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-129">[**интерлоккеданднофенце**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-130">Выполняет атомарную операцию и над указанными **длинными** значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-130">Performs an atomic AND operation on the specified **LONG** values.</span></span> <span data-ttu-id="85952-131">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-131">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-133">Выполняет атомарную операцию и над указанными значениями **char** .</span><span class="sxs-lookup"><span data-stu-id="85952-133">Performs an atomic AND operation on the specified **char** values.</span></span> <span data-ttu-id="85952-134">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-134">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-136">Выполняет атомарную операцию и над указанными **короткими** значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-136">Performs an atomic AND operation on the specified **SHORT** values.</span></span> <span data-ttu-id="85952-137">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-137">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-139">Выполняет атомарную операцию и над указанными значениями **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="85952-139">Performs an atomic AND operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="85952-140">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-140">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-142">Проверяет указанный бит указанного значения **LONG64** и дополняет его.</span><span class="sxs-lookup"><span data-stu-id="85952-142">Tests the specified bit of the specified **LONG64** value and complements it.</span></span> <span data-ttu-id="85952-143">Эта операция является атомарной.</span><span class="sxs-lookup"><span data-stu-id="85952-143">The operation is atomic.</span></span>

</dd> <dt>

<span data-ttu-id="85952-144">[**интерлоккедбиттестандресетаккуире**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-145">Проверяет указанный бит указанного **длинного** значения и присваивает ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="85952-145">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="85952-146">Операция является атомарной и выполняется с семантикой получения порядка памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-146">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-147">[**интерлоккедбиттестандресетрелеасе**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-148">Проверяет указанный бит указанного **длинного** значения и присваивает ему значение 0.</span><span class="sxs-lookup"><span data-stu-id="85952-148">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="85952-149">Операция является атомарной и выполняется с помощью семантики освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-149">The operation is atomic, and it is performed using memory release semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-150">[**интерлоккедбиттестандсетаккуире**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-151">Проверяет указанный бит указанного **длинного** значения и задает для него значение 1.</span><span class="sxs-lookup"><span data-stu-id="85952-151">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="85952-152">Операция является атомарной и выполняется с семантикой получения порядка памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-152">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-153">[**интерлоккедбиттестандсетрелеасе**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-154">Проверяет указанный бит указанного **длинного** значения и задает для него значение 1.</span><span class="sxs-lookup"><span data-stu-id="85952-154">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="85952-155">Операция является атомарной и выполняется с семантикой упорядочения памяти выпуска.</span><span class="sxs-lookup"><span data-stu-id="85952-155">The operation is atomic, and it is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-156">[**интерлоккедкомпариксчанженофенце**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-157">Выполняет атомарную операцию сравнения и обмена с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-157">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="85952-158">Функция сравнивает два заданных 32-битных значения и обмен с другим 32-битным значением на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="85952-158">The function compares two specified 32-bit values and exchanges with another 32-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="85952-159">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-159">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-160">**InterlockedCompareExchange16**</span><span class="sxs-lookup"><span data-stu-id="85952-160">**InterlockedCompareExchange16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

<span data-ttu-id="85952-161">Выполняет атомарную операцию сравнения и обмена с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-161">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="85952-162">Функция сравнивает два заданных 16-разрядных значения и обмена с другим 16-разрядным значением на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="85952-162">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="85952-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-164">Выполняет атомарную операцию сравнения и обмена с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-164">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="85952-165">Функция сравнивает два заданных 16-разрядных значения и обмена с другим 16-разрядным значением на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="85952-165">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="85952-166">Операция выполняется с семантикой получения порядка памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-166">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-168">Выполняет атомарную операцию сравнения и обмена с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-168">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="85952-169">Функция сравнивает два заданных 16-разрядных значения и обмена с другим 16-разрядным значением на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="85952-169">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="85952-170">Обмен выполняется с семантикой упорядочения памяти выпуска.</span><span class="sxs-lookup"><span data-stu-id="85952-170">The exchange is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-172">Выполняет атомарную операцию сравнения и обмена с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-172">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="85952-173">Функция сравнивает два заданных 16-разрядных значения и обмена с другим 16-разрядным значением на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="85952-173">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="85952-174">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-174">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-176">Выполняет атомарную операцию сравнения и обмена с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-176">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="85952-177">Функция сравнивает два заданных 64-битных значения и обмен с другим 64-битным значением на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="85952-177">The function compares two specified 64-bit values and exchanges with another 64-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="85952-178">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-178">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-179">**InterlockedCompareExchange128**</span><span class="sxs-lookup"><span data-stu-id="85952-179">**InterlockedCompareExchange128**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

<span data-ttu-id="85952-180">Выполняет атомарную операцию сравнения и обмена с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-180">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="85952-181">Функция сравнивает два заданных 128-битных значения и обмен с другим 128-битным значением на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="85952-181">The function compares two specified 128-bit values and exchanges with another 128-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="85952-182">[**интерлоккедкомпариксчанжепоинтернофенце**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-183">Выполняет атомарную операцию сравнения и обмена с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-183">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="85952-184">Функция сравнивает два указанных значения указателя и обмена с другим значением указателя на основе результата сравнения.</span><span class="sxs-lookup"><span data-stu-id="85952-184">The function compares two specified pointer values and exchanges with another pointer value based on the outcome of the comparison.</span></span> <span data-ttu-id="85952-185">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-185">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-186">[**интерлоккеддекрементнофенце**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-187">Уменьшение (уменьшение на единицу) значения указанной 32-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-187">Decrements (decreases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="85952-188">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-188">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-189">**InterlockedDecrement16**</span><span class="sxs-lookup"><span data-stu-id="85952-189">**InterlockedDecrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

<span data-ttu-id="85952-190">Уменьшение (уменьшение на единицу) значения указанной 16-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-190">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="85952-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-192">Уменьшение (уменьшение на единицу) значения указанной 16-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-192">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="85952-193">Операция выполняется с семантикой получения порядка памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-193">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-195">Уменьшение (уменьшение на единицу) значения указанной 16-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-195">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="85952-196">Эта операция выполняется с семантикой упорядочения памяти выпуска.</span><span class="sxs-lookup"><span data-stu-id="85952-196">The operation is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-198">Уменьшение (уменьшение на единицу) значения указанной 16-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-198">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="85952-199">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-199">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-201">Уменьшение (уменьшение на единицу) значения указанной 64-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-201">Decrements (decreases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="85952-202">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-202">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-203">[**интерлоккедексчанженофенце**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-204">Устанавливает 64-разрядную переменную в указанное значение как атомарную операцию.</span><span class="sxs-lookup"><span data-stu-id="85952-204">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="85952-205">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-205">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-206">**InterlockedExchange8**</span><span class="sxs-lookup"><span data-stu-id="85952-206">**InterlockedExchange8**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

<span data-ttu-id="85952-207">Задает для 8-битовой переменной указанное значение в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-207">Sets an 8-bit variable to the specified value as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="85952-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-209">Задает для 16-разрядной переменной указанное значение в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-209">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="85952-210">Операция выполняется с использованием семантики получения порядка памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-210">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-212">Задает для 16-разрядной переменной указанное значение в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-212">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="85952-213">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-213">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-215">Устанавливает 64-разрядную переменную в указанное значение как атомарную операцию.</span><span class="sxs-lookup"><span data-stu-id="85952-215">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="85952-216">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-216">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-217">[**интерлоккедексчанжепоинтернофенце**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-218">Атомарно обменивается парой адресов.</span><span class="sxs-lookup"><span data-stu-id="85952-218">Atomically exchanges a pair of addresses.</span></span> <span data-ttu-id="85952-219">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-219">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-220">[**интерлоккедексчанжеадднофенце**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-221">Выполняет атомарное сложение 2 32-разрядных значений.</span><span class="sxs-lookup"><span data-stu-id="85952-221">Performs an atomic addition of two 32-bit values.</span></span> <span data-ttu-id="85952-222">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-222">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-224">Выполняет атомарное сложение 2 64-разрядных значений.</span><span class="sxs-lookup"><span data-stu-id="85952-224">Performs an atomic addition of two 64-bit values.</span></span> <span data-ttu-id="85952-225">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-225">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-226">[**интерлоккединкрементнофенце**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-227">Приращение (увеличивается на единицу) значения указанной 32-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-227">Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="85952-228">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-228">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-229">**InterlockedIncrement16**</span><span class="sxs-lookup"><span data-stu-id="85952-229">**InterlockedIncrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

<span data-ttu-id="85952-230">Приращение (увеличивается на единицу) значения заданной 16-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-230">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="85952-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-232">Приращение (увеличивается на единицу) значения заданной 16-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-232">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="85952-233">Операция выполняется с использованием семантики получения порядка памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-233">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-235">Приращение (увеличивается на единицу) значения заданной 16-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-235">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="85952-236">Операция выполняется с использованием семантики порядка освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-236">The operation is performed using release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85952-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-238">Приращение (увеличивается на единицу) значения заданной 16-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-238">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="85952-239">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-239">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-241">Приращение (увеличивается на единицу) значения указанной 64-разрядной переменной в качестве атомарной операции.</span><span class="sxs-lookup"><span data-stu-id="85952-241">Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="85952-242">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-242">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-243">[**интерлоккедорнофенце**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-244">Выполняет атомарную операцию или над указанными **длинными** значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-244">Performs an atomic OR operation on the specified **LONG** values.</span></span> <span data-ttu-id="85952-245">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-245">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-247">Выполняет атомарную операцию OR с указанными значениями **char** .</span><span class="sxs-lookup"><span data-stu-id="85952-247">Performs an atomic OR operation on the specified **char** values.</span></span> <span data-ttu-id="85952-248">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-248">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-250">Выполняет атомарную операцию или над указанными **короткими** значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-250">Performs an atomic OR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="85952-251">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-251">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-253">Выполняет атомарную операцию или с указанными значениями **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="85952-253">Performs an atomic OR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="85952-254">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-254">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-255">**интерлоккедпушлистслистекс**</span><span class="sxs-lookup"><span data-stu-id="85952-255">**InterlockedPushListSListEx**</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

<span data-ttu-id="85952-256">Вставляет однонаправленный список в начале другого однонаправленного списка.</span><span class="sxs-lookup"><span data-stu-id="85952-256">Inserts a singly-linked list at the front of another singly linked list.</span></span> <span data-ttu-id="85952-257">Доступ к спискам синхронизируется в многопроцессорной системе.</span><span class="sxs-lookup"><span data-stu-id="85952-257">Access to the lists is synchronized on a multiprocessor system.</span></span> <span data-ttu-id="85952-258">В этой версии метода не используется соглашение о вызовах [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) .</span><span class="sxs-lookup"><span data-stu-id="85952-258">This version of the method does not use the [\_\_fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) calling convention.</span></span>

</dd> <dt>

<span data-ttu-id="85952-259">[**интерлоккедксорнофенце**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-260">Выполняет атомарную операцию XOR с указанными **длинными** значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-260">Performs an atomic XOR operation on the specified **LONG** values.</span></span> <span data-ttu-id="85952-261">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-261">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-263">Выполняет атомарную операцию XOR с указанными значениями **char** .</span><span class="sxs-lookup"><span data-stu-id="85952-263">Performs an atomic XOR operation on the specified **char** values.</span></span> <span data-ttu-id="85952-264">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-264">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-266">Выполняет атомарную операцию XOR с указанными **короткими** значениями.</span><span class="sxs-lookup"><span data-stu-id="85952-266">Performs an atomic XOR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="85952-267">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-267">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="85952-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="85952-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="85952-269">Выполняет атомарную операцию XOR с указанными значениями **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="85952-269">Performs an atomic XOR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="85952-270">Операция выполняется атомарно, но без использования барьеров памяти.</span><span class="sxs-lookup"><span data-stu-id="85952-270">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> </dl>

## <a name="windows-7"></a><span data-ttu-id="85952-271">Windows 7</span><span class="sxs-lookup"><span data-stu-id="85952-271">Windows 7</span></span>

### <a name="new-functions"></a><span data-ttu-id="85952-272">Новые функции</span><span class="sxs-lookup"><span data-stu-id="85952-272">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="85952-273">**сетваитаблетимерекс**</span><span class="sxs-lookup"><span data-stu-id="85952-273">**SetWaitableTimerEx**</span></span>](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

<span data-ttu-id="85952-274">Активирует указанный таймер ожидания и предоставляет сведения о контексте для таймера.</span><span class="sxs-lookup"><span data-stu-id="85952-274">Activates the specified waitable timer and provides context information for the timer.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-275">**тряккуиресрвлоккексклусиве**</span><span class="sxs-lookup"><span data-stu-id="85952-275">**TryAcquireSRWLockExclusive**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

<span data-ttu-id="85952-276">Пытается получить упрощенную блокировку чтения/записи (SRW) в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="85952-276">Attempts to acquire a slim reader/writer (SRW) lock in exclusive mode.</span></span> <span data-ttu-id="85952-277">Если вызов выполнен успешно, вызывающий поток принимает владение блокировкой.</span><span class="sxs-lookup"><span data-stu-id="85952-277">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> <dt>

[<span data-ttu-id="85952-278">**тряккуиресрвлоккшаред**</span><span class="sxs-lookup"><span data-stu-id="85952-278">**TryAcquireSRWLockShared**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

<span data-ttu-id="85952-279">Пытается получить блокировку упрощенного чтения/записи (SRW) в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="85952-279">Attempts to acquire a slim reader/writer (SRW) lock in shared mode.</span></span> <span data-ttu-id="85952-280">Если вызов выполнен успешно, вызывающий поток принимает владение блокировкой.</span><span class="sxs-lookup"><span data-stu-id="85952-280">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> </dl>

### <a name="new-structures"></a><span data-ttu-id="85952-281">Новые структуры</span><span class="sxs-lookup"><span data-stu-id="85952-281">New Structures</span></span>

<dl> <dt>

[<span data-ttu-id="85952-282">**\_контекст причины**</span><span class="sxs-lookup"><span data-stu-id="85952-282">**REASON\_CONTEXT**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

<span data-ttu-id="85952-283">Содержит сведения о контексте для таймера, активированного с помощью [**сетваитаблетимерекс**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span><span class="sxs-lookup"><span data-stu-id="85952-283">Contains context information for a timer activated with [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span></span>

</dd> </dl>

 

 
