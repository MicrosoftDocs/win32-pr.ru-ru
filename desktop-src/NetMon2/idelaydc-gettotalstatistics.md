---
description: 'Метод Иделайдк:: Жеттоталстатистикс — метод Жеттоталстатистикс извлекает общую статистику для текущей записи.'
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'Метод Иделайдк:: Жеттоталстатистикс (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b3a0ce4f230236e276fede528a5e778ecafd51fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113532"
---
# <a name="idelaydcgettotalstatistics-method"></a><span data-ttu-id="e98dd-103">Метод Иделайдк:: Жеттоталстатистикс</span><span class="sxs-lookup"><span data-stu-id="e98dd-103">IDelaydC::GetTotalStatistics method</span></span>

<span data-ttu-id="e98dd-104">Метод **жеттоталстатистикс** извлекает [*общую статистику*](t.md) для текущей [*записи*](c.md).</span><span class="sxs-lookup"><span data-stu-id="e98dd-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e98dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e98dd-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="e98dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e98dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e98dd-107">*лпстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e98dd-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e98dd-108">Указатель на структуру [статистики](statistics.md), которая предоставляет общую статистику для записи.</span><span class="sxs-lookup"><span data-stu-id="e98dd-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="e98dd-109">Ответственность за выделение и освобождение памяти, используемой структурой **статистики** , несет вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="e98dd-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="e98dd-110">*фклеарафтерреадинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e98dd-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e98dd-111">Флаг, указывающий, сетевой монитор как управлять внутренним хранилищем общей статистики.</span><span class="sxs-lookup"><span data-stu-id="e98dd-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="e98dd-112">Значение **true** указывает сетевой монитор очищать внутреннее хранилище общей статистики после получения текущей информации.</span><span class="sxs-lookup"><span data-stu-id="e98dd-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e98dd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e98dd-113">Return value</span></span>

<span data-ttu-id="e98dd-114">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e98dd-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e98dd-115">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="e98dd-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e98dd-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e98dd-116">Return code</span></span>                                                                                          | <span data-ttu-id="e98dd-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e98dd-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e98dd-118"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="e98dd-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e98dd-119">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="e98dd-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="e98dd-120">Вызовите [иделайдк:: Connect](idelaydc-connect.md) , чтобы подключиться к сети.</span><span class="sxs-lookup"><span data-stu-id="e98dd-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="e98dd-121"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="e98dd-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="e98dd-122">НПП подключается к сети, но не с методом [иделайдк:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="e98dd-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="e98dd-123"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="e98dd-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="e98dd-124">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="e98dd-124">The NPP is not capturing data.</span></span> <span data-ttu-id="e98dd-125">Вызовите [иделайдк:: Start](idelaydc-start.md) , чтобы начать сбор данных.</span><span class="sxs-lookup"><span data-stu-id="e98dd-125">Call [IDelaydC::Start](idelaydc-start.md) to start capturing data.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="e98dd-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="e98dd-126">Remarks</span></span>

<span data-ttu-id="e98dd-127">Этот метод возвращает данные только во время выполнения записи; При приостановке записи вызовы этого метода не будут выполнены.</span><span class="sxs-lookup"><span data-stu-id="e98dd-127">This method returns data only while a capture is in progress; when the capture is paused, calls to this method will not succeed.</span></span>

<span data-ttu-id="e98dd-128">Сетевой монитор также хранит [*статистику диалога*](c.md), которую можно получить, вызвав метод [Иделайдк:: жетконверсатионстатистикс](idelaydc-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="e98dd-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e98dd-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e98dd-129">Requirements</span></span>



| <span data-ttu-id="e98dd-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e98dd-130">Requirement</span></span> | <span data-ttu-id="e98dd-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e98dd-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e98dd-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e98dd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e98dd-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e98dd-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e98dd-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e98dd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e98dd-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e98dd-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e98dd-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e98dd-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e98dd-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e98dd-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e98dd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e98dd-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e98dd-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e98dd-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e98dd-140">См. также</span><span class="sxs-lookup"><span data-stu-id="e98dd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e98dd-141">иделайдк</span><span class="sxs-lookup"><span data-stu-id="e98dd-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="e98dd-142">Иделайдк:: Connect</span><span class="sxs-lookup"><span data-stu-id="e98dd-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="e98dd-143">Иделайдк:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="e98dd-143">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="e98dd-144">Иделайдк:: Start</span><span class="sxs-lookup"><span data-stu-id="e98dd-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="e98dd-145">СТАТИСТИЧЕСКИ</span><span class="sxs-lookup"><span data-stu-id="e98dd-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




