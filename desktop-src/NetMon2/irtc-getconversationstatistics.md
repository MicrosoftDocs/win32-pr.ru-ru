---
description: Метод Жетконверсатионстатистикс извлекает сведения о сеансе и станции о текущей записи.
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
ms.openlocfilehash: 758488cb3c3f65922bbf6aac4f39774a5430fc92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898838"
---
# <a name="irtcgetconversationstatistics-method"></a><span data-ttu-id="8b32d-103">Метод ИРТК:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="8b32d-103">IRTC::GetConversationStatistics method</span></span>

<span data-ttu-id="8b32d-104">Метод **жетконверсатионстатистикс** извлекает сведения о [*сеансе*](s.md) и [*станции*](s.md) о текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8b32d-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b32d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b32d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="8b32d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8b32d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b32d-107">*нсессионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8b32d-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b32d-108">Указатель на DWORD, содержащий количество [*сеансов*](s.md) , записанных для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8b32d-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="8b32d-109">*лпсессионстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8b32d-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b32d-110">Указатель на структуру [сессионстатс](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="8b32d-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b32d-111">*нстатионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8b32d-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b32d-112">Указатель на DWORD, содержащий число [*станций*](s.md) , записанных для текущего захвата.</span><span class="sxs-lookup"><span data-stu-id="8b32d-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="8b32d-113">*лпстатионстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8b32d-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b32d-114">Указатель на структуру [статионстатс](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="8b32d-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8b32d-115">*фклеарафтерреадинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8b32d-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b32d-116">Флаг, который указывает сетевой монитор очищать внутреннее хранилище структур [сессионстатс](sessionstats.md) и [статионстатс](stationstats.md) после получения текущих данных.</span><span class="sxs-lookup"><span data-stu-id="8b32d-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b32d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8b32d-117">Return value</span></span>

<span data-ttu-id="8b32d-118">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="8b32d-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8b32d-119">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="8b32d-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="8b32d-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8b32d-120">Return code</span></span>                                                                                                   | <span data-ttu-id="8b32d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="8b32d-121">Description</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b32d-122"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="8b32d-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="8b32d-123">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="8b32d-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="8b32d-124">Вызовите [ИРТК:: Connect](irtc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="8b32d-124">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="8b32d-125"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="8b32d-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="8b32d-126">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="8b32d-126">The NPP is not capturing data.</span></span> <span data-ttu-id="8b32d-127">Вызовите [ИРТК:: Start](irtc-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="8b32d-127">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="8b32d-128"><dt>**НМЕРР \_ не в \_ реальном времени**</dt></span><span class="sxs-lookup"><span data-stu-id="8b32d-128"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>           | <span data-ttu-id="8b32d-129">НПП подключается к сети, но не с методом [ИРТК:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="8b32d-129">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                                                                                                          |
| <dl> <span data-ttu-id="8b32d-130"><dt>**НМЕРР \_ без \_ \_ статистики**</dt></span><span class="sxs-lookup"><span data-stu-id="8b32d-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="8b32d-131">Для конфигурации этого соединения задано значение не сохранять статистику диалога.</span><span class="sxs-lookup"><span data-stu-id="8b32d-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="8b32d-132">Чтобы сохранить статистику диалога, закройте запись, задайте Ноконверсатионстатс = YES в большом двоичном объекте конфигурации, а затем перезапустите запись.</span><span class="sxs-lookup"><span data-stu-id="8b32d-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8b32d-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b32d-133">Remarks</span></span>

<span data-ttu-id="8b32d-134">Этот метод может вызываться только во время записи данных. Если вызвать этот метод во время приостановки текущей записи, метод не будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="8b32d-134">This method can only be called while you are capturing data; if you call this method while the current capture is paused, the method will not succeed.</span></span> <span data-ttu-id="8b32d-135">Чтобы начать запись, вызовите метод [ИРТК:: Start](irtc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="8b32d-135">To start a capture, call the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="8b32d-136">Чтобы получить другие типы статистики, вызовите метод [ИРТК:: жеттоталстатистикс](irtc-gettotalstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="8b32d-136">To retrieve other types of statistics, call the [IRTC::GetTotalStatistics](irtc-gettotalstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b32d-137">Требования</span><span class="sxs-lookup"><span data-stu-id="8b32d-137">Requirements</span></span>



| <span data-ttu-id="8b32d-138">Требование</span><span class="sxs-lookup"><span data-stu-id="8b32d-138">Requirement</span></span> | <span data-ttu-id="8b32d-139">Значение</span><span class="sxs-lookup"><span data-stu-id="8b32d-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b32d-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b32d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8b32d-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b32d-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="8b32d-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b32d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8b32d-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8b32d-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="8b32d-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8b32d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b32d-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b32d-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="8b32d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8b32d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b32d-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b32d-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b32d-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b32d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b32d-149">иртк</span><span class="sxs-lookup"><span data-stu-id="8b32d-149">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="8b32d-150">ИРТК:: Connect</span><span class="sxs-lookup"><span data-stu-id="8b32d-150">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="8b32d-151">ИРТК:: Жеттоталстатистикс</span><span class="sxs-lookup"><span data-stu-id="8b32d-151">IRTC::GetTotalStatistics</span></span>](irtc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="8b32d-152">ИРТК:: Start</span><span class="sxs-lookup"><span data-stu-id="8b32d-152">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="8b32d-153">сессионстатс</span><span class="sxs-lookup"><span data-stu-id="8b32d-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="8b32d-154">статионстатс</span><span class="sxs-lookup"><span data-stu-id="8b32d-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




