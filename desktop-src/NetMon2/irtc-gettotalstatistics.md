---
description: Метод Жеттоталстатистикс извлекает общую статистику для текущей записи.
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'Метод ИРТК:: Жеттоталстатистикс (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 27128048b4326aae14ae6a2e2e6c0540b1105538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673557"
---
# <a name="irtcgettotalstatistics-method"></a><span data-ttu-id="7b632-103">Метод ИРТК:: Жеттоталстатистикс</span><span class="sxs-lookup"><span data-stu-id="7b632-103">IRTC::GetTotalStatistics method</span></span>

<span data-ttu-id="7b632-104">Метод **жеттоталстатистикс** извлекает [*общую статистику*](t.md) для текущей [*записи*](c.md).</span><span class="sxs-lookup"><span data-stu-id="7b632-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b632-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b632-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="7b632-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b632-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b632-107">*лпстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7b632-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b632-108">Указатель на структуру [статистики](statistics.md) , которая предоставляет общую статистику для записи.</span><span class="sxs-lookup"><span data-stu-id="7b632-108">Pointer to a [STATISTICS](statistics.md) structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="7b632-109">Вызывающие объекты отвечают за выделение и освобождение памяти, используемой структурой **статистики** .</span><span class="sxs-lookup"><span data-stu-id="7b632-109">It is the callers responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b632-110">*фклеарафтерреадинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b632-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b632-111">Флаг, указывающий, сетевой монитор как управлять внутренним хранилищем общей статистики.</span><span class="sxs-lookup"><span data-stu-id="7b632-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="7b632-112">Значение **true** указывает сетевой монитор очищать внутреннее хранилище общей статистики после получения текущей информации.</span><span class="sxs-lookup"><span data-stu-id="7b632-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b632-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b632-113">Return value</span></span>

<span data-ttu-id="7b632-114">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="7b632-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7b632-115">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="7b632-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="7b632-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7b632-116">Return code</span></span>                                                                                          | <span data-ttu-id="7b632-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7b632-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b632-118"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="7b632-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7b632-119">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="7b632-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="7b632-120">Вызовите [ИРТК:: Connect](irtc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="7b632-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="7b632-121"><dt>**НМЕРР \_ не в \_ реальном времени**</dt></span><span class="sxs-lookup"><span data-stu-id="7b632-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="7b632-122">НПП подключается к сети, но не с методом [ИРТК:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="7b632-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |
| <dl> <span data-ttu-id="7b632-123"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="7b632-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="7b632-124">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="7b632-124">The NPP is not capturing data.</span></span> <span data-ttu-id="7b632-125">Вызовите [ИРТК:: Start](irtc-start.md) , чтобы начать сбор данных.</span><span class="sxs-lookup"><span data-stu-id="7b632-125">Call [IRTC::Start](irtc-start.md) to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="7b632-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b632-126">Remarks</span></span>

<span data-ttu-id="7b632-127">Этот метод возвращает данные только во время выполнения записи, включая время приостановки записи.</span><span class="sxs-lookup"><span data-stu-id="7b632-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="7b632-128">Сетевой монитор также хранит [*статистику диалога*](c.md).</span><span class="sxs-lookup"><span data-stu-id="7b632-128">Network Monitor also stores [*conversation statistics*](c.md).</span></span> <span data-ttu-id="7b632-129">Чтобы получить статистику диалога, вызовите метод [ИРТК:: жетконверсатионстатистикс](irtc-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="7b632-129">To retrieve conversation statistics, call the [IRTC::GetConversationStatistics](irtc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b632-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7b632-130">Requirements</span></span>



| <span data-ttu-id="7b632-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7b632-131">Requirement</span></span> | <span data-ttu-id="7b632-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7b632-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b632-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b632-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7b632-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b632-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="7b632-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b632-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7b632-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7b632-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="7b632-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7b632-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b632-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b632-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="7b632-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7b632-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b632-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b632-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b632-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b632-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b632-142">иртк</span><span class="sxs-lookup"><span data-stu-id="7b632-142">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="7b632-143">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="7b632-143">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="7b632-144">ИРТК:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="7b632-144">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="7b632-145">ИРТК:: Start</span><span class="sxs-lookup"><span data-stu-id="7b632-145">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="7b632-146">СТАТИСТИЧЕСКИ</span><span class="sxs-lookup"><span data-stu-id="7b632-146">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




