---
description: 'Метод ИРТК:: Жетконверсатионстатистикс — метод Жетконверсатионстатистикс извлекает сведения о сеансе и станции о текущей записи.'
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'Метод ИРТК:: Жетконверсатионстатистикс (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4d2476f4eb33d7e74d0de8363fa88d5e688a2e73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110702"
---
# <a name="irtcgetconversationstatistics-method"></a><span data-ttu-id="8ee46-103">Метод ИРТК:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="8ee46-103">IRTC::GetConversationStatistics method</span></span>

<span data-ttu-id="8ee46-104">Метод **жетконверсатионстатистикс** извлекает сведения о [*сеансе*](s.md) и [*станции*](s.md) о текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8ee46-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee46-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ee46-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="8ee46-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ee46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee46-107">*нсессионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8ee46-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee46-108">Указатель на DWORD, содержащий количество [*сеансов*](s.md) , записанных для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8ee46-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="8ee46-109">*лпсессионстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8ee46-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee46-110">Указатель на структуру [сессионстатс](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="8ee46-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8ee46-111">*нстатионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8ee46-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee46-112">Указатель на DWORD, содержащий число [*станций*](s.md) , записанных для текущего захвата.</span><span class="sxs-lookup"><span data-stu-id="8ee46-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="8ee46-113">*лпстатионстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8ee46-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee46-114">Указатель на структуру [статионстатс](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="8ee46-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8ee46-115">*фклеарафтерреадинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ee46-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee46-116">Флаг, который указывает сетевой монитор очищать внутреннее хранилище структур [сессионстатс](sessionstats.md) и [статионстатс](stationstats.md) после получения текущих данных.</span><span class="sxs-lookup"><span data-stu-id="8ee46-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee46-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ee46-117">Return value</span></span>

<span data-ttu-id="8ee46-118">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8ee46-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8ee46-119">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="8ee46-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="8ee46-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8ee46-120">Return code</span></span>                                                                                                   | <span data-ttu-id="8ee46-121">Описание</span><span class="sxs-lookup"><span data-stu-id="8ee46-121">Description</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ee46-122"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="8ee46-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="8ee46-123">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="8ee46-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="8ee46-124">Вызовите [ИРТК:: Connect](irtc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="8ee46-124">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="8ee46-125"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="8ee46-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="8ee46-126">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="8ee46-126">The NPP is not capturing data.</span></span> <span data-ttu-id="8ee46-127">Вызовите [ИРТК:: Start](irtc-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="8ee46-127">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="8ee46-128"><dt>**НМЕРР \_ не в \_ реальном времени**</dt></span><span class="sxs-lookup"><span data-stu-id="8ee46-128"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>           | <span data-ttu-id="8ee46-129">НПП подключается к сети, но не с методом [ИРТК:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="8ee46-129">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                                                                                                          |
| <dl> <span data-ttu-id="8ee46-130"><dt>**НМЕРР \_ без \_ \_ статистики**</dt></span><span class="sxs-lookup"><span data-stu-id="8ee46-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="8ee46-131">Для конфигурации этого соединения задано значение не сохранять статистику диалога.</span><span class="sxs-lookup"><span data-stu-id="8ee46-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="8ee46-132">Чтобы сохранить статистику диалога, закройте запись, задайте Ноконверсатионстатс = YES в большом двоичном объекте конфигурации, а затем перезапустите запись.</span><span class="sxs-lookup"><span data-stu-id="8ee46-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ee46-133">Remarks</span><span class="sxs-lookup"><span data-stu-id="8ee46-133">Remarks</span></span>

<span data-ttu-id="8ee46-134">Этот метод может вызываться только во время записи данных. Если вызвать этот метод во время приостановки текущей записи, метод не будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="8ee46-134">This method can only be called while you are capturing data; if you call this method while the current capture is paused, the method will not succeed.</span></span> <span data-ttu-id="8ee46-135">Чтобы начать запись, вызовите метод [ИРТК:: Start](irtc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="8ee46-135">To start a capture, call the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="8ee46-136">Чтобы получить другие типы статистики, вызовите метод [ИРТК:: жеттоталстатистикс](irtc-gettotalstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="8ee46-136">To retrieve other types of statistics, call the [IRTC::GetTotalStatistics](irtc-gettotalstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee46-137">Требования</span><span class="sxs-lookup"><span data-stu-id="8ee46-137">Requirements</span></span>



| <span data-ttu-id="8ee46-138">Требование</span><span class="sxs-lookup"><span data-stu-id="8ee46-138">Requirement</span></span> | <span data-ttu-id="8ee46-139">Значение</span><span class="sxs-lookup"><span data-stu-id="8ee46-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee46-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ee46-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8ee46-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ee46-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="8ee46-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ee46-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8ee46-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8ee46-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="8ee46-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8ee46-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ee46-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee46-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="8ee46-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8ee46-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ee46-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ee46-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee46-148">См. также</span><span class="sxs-lookup"><span data-stu-id="8ee46-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee46-149">иртк</span><span class="sxs-lookup"><span data-stu-id="8ee46-149">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="8ee46-150">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="8ee46-150">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="8ee46-151">ИРТК:: Жеттоталстатистикс</span><span class="sxs-lookup"><span data-stu-id="8ee46-151">IRTC::GetTotalStatistics</span></span>](irtc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="8ee46-152">ИРТК:: Start</span><span class="sxs-lookup"><span data-stu-id="8ee46-152">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="8ee46-153">сессионстатс</span><span class="sxs-lookup"><span data-stu-id="8ee46-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="8ee46-154">статионстатс</span><span class="sxs-lookup"><span data-stu-id="8ee46-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




