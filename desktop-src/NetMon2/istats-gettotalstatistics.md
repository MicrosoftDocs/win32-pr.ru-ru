---
description: 'Метод Истатс:: Жеттоталстатистикс — метод Жеттоталстатистикс извлекает общую статистику для текущей записи.'
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'Метод Истатс:: Жеттоталстатистикс (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6566a58212e8f20d0d999302f41ab97cb9f005e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098412"
---
# <a name="istatsgettotalstatistics-method"></a><span data-ttu-id="de06c-103">Метод Истатс:: Жеттоталстатистикс</span><span class="sxs-lookup"><span data-stu-id="de06c-103">IStats::GetTotalStatistics method</span></span>

<span data-ttu-id="de06c-104">Метод **жеттоталстатистикс** извлекает [*общую статистику*](t.md) для текущей [*записи*](c.md).</span><span class="sxs-lookup"><span data-stu-id="de06c-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="de06c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de06c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="de06c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de06c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de06c-107">*лпстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="de06c-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de06c-108">Указатель на структуру [статистики](statistics.md), которая предоставляет общую статистику для записи.</span><span class="sxs-lookup"><span data-stu-id="de06c-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="de06c-109">Ответственность за выделение и освобождение памяти, используемой структурой **статистики** , несет вызывающий объект.</span><span class="sxs-lookup"><span data-stu-id="de06c-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="de06c-110">*фклеарафтерреадинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de06c-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de06c-111">Флаг, указывающий, сетевой монитор как управлять внутренним хранилищем общей статистики.</span><span class="sxs-lookup"><span data-stu-id="de06c-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="de06c-112">Значение TRUE указывает сетевой монитор очищать внутреннее хранилище общей статистики после получения текущей информации.</span><span class="sxs-lookup"><span data-stu-id="de06c-112">A setting of TRUE tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de06c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de06c-113">Return value</span></span>

<span data-ttu-id="de06c-114">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="de06c-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="de06c-115">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="de06c-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="de06c-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="de06c-116">Return code</span></span>                                                                                            | <span data-ttu-id="de06c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="de06c-117">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de06c-118"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="de06c-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="de06c-119">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="de06c-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="de06c-120">Вызовите метод [истатс:: Connect](istats-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="de06c-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="de06c-121"><dt>**НМЕРР \_ не \_ \_ только статистика**</dt></span><span class="sxs-lookup"><span data-stu-id="de06c-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="de06c-122">НПП подключается к сети, но не с методом [истатс:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="de06c-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |
| <dl> <span data-ttu-id="de06c-123"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="de06c-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="de06c-124">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="de06c-124">The NPP is not capturing data.</span></span> <span data-ttu-id="de06c-125">Вызовите метод [истатс:: Start](istats-start.md) , чтобы начать запись данных.</span><span class="sxs-lookup"><span data-stu-id="de06c-125">Call the [IStats::Start](istats-start.md) method to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="de06c-126">Remarks</span><span class="sxs-lookup"><span data-stu-id="de06c-126">Remarks</span></span>

<span data-ttu-id="de06c-127">Этот метод возвращает данные только во время выполнения записи, включая время приостановки записи.</span><span class="sxs-lookup"><span data-stu-id="de06c-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="de06c-128">Сетевой монитор также хранит [*статистику диалога*](c.md), которую можно получить, вызвав метод [Истатс:: жетконверсатионстатистикс](istats-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="de06c-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IStats::GetConversationStatistics](istats-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="de06c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="de06c-129">Requirements</span></span>



| <span data-ttu-id="de06c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="de06c-130">Requirement</span></span> | <span data-ttu-id="de06c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="de06c-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de06c-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de06c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="de06c-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="de06c-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="de06c-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de06c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="de06c-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="de06c-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="de06c-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="de06c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="de06c-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="de06c-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="de06c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="de06c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de06c-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de06c-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de06c-140">См. также</span><span class="sxs-lookup"><span data-stu-id="de06c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de06c-141">истатс</span><span class="sxs-lookup"><span data-stu-id="de06c-141">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="de06c-142">Истатс:: Connect</span><span class="sxs-lookup"><span data-stu-id="de06c-142">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="de06c-143">Истатс:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="de06c-143">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="de06c-144">Истатс:: Start,</span><span class="sxs-lookup"><span data-stu-id="de06c-144">IStats::Start,</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="de06c-145">СТАТИСТИЧЕСКИ</span><span class="sxs-lookup"><span data-stu-id="de06c-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




