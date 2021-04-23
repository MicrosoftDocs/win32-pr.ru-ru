---
description: Извлекает сведения о сеансе и станции о текущем захвате.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'Метод Истатс:: Жетконверсатионстатистикс (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674483"
---
# <a name="istatsgetconversationstatistics-method"></a><span data-ttu-id="6881d-103">Метод Истатс:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="6881d-103">IStats::GetConversationStatistics method</span></span>

<span data-ttu-id="6881d-104">Метод **жетконверсатионстатистикс** извлекает сведения о сеансе и станции о текущей записи.</span><span class="sxs-lookup"><span data-stu-id="6881d-104">The **GetConversationStatistics** method retrieves session and station information about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6881d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6881d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="6881d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6881d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6881d-107">*нсессионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6881d-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6881d-108">Указатель на DWORD, содержащий количество [*сеансов*](s.md) , записанных для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="6881d-108">A pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="6881d-109">*лпсессионстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6881d-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6881d-110">Указатель на структуру [**сессионстатс**](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="6881d-110">A pointer to a [**SESSIONSTATS**](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6881d-111">*нстатионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6881d-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6881d-112">Указатель на DWORD, содержащий число [*станций*](s.md) , записанных для текущего захвата.</span><span class="sxs-lookup"><span data-stu-id="6881d-112">A pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="6881d-113">*лпстатионстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6881d-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6881d-114">Указатель на структуру [**статионстатс**](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="6881d-114">A pointer to a [**STATIONSTATS**](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6881d-115">*фклеарафтерреадинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6881d-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6881d-116">Флаг, используемый для указания сетевой монитор очистить внутреннее хранилище структур [**сессионстатс**](sessionstats.md) и [**статионстатс**](stationstats.md) после получения текущих данных.</span><span class="sxs-lookup"><span data-stu-id="6881d-116">Flag used to instruct Network Monitor to clear the internal storage of the [**SESSIONSTATS**](sessionstats.md) and [**STATIONSTATS**](stationstats.md) structures after the current data is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6881d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6881d-117">Return value</span></span>

<span data-ttu-id="6881d-118">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6881d-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6881d-119">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="6881d-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="6881d-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6881d-120">Return code</span></span>                                                                                                   | <span data-ttu-id="6881d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="6881d-121">Description</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6881d-122"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="6881d-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="6881d-123">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="6881d-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="6881d-124">Вызовите [**истатс:: Connect**](istats-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="6881d-124">Call [**IStats::Connect**](istats-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="6881d-125"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="6881d-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="6881d-126">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="6881d-126">The NPP is not capturing data.</span></span> <span data-ttu-id="6881d-127">Вызовите [**истатс:: Start**](istats-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="6881d-127">Call [**IStats::Start**](istats-start.md) to start the capture.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="6881d-128"><dt>**НМЕРР \_ не \_ \_ только статистика**</dt></span><span class="sxs-lookup"><span data-stu-id="6881d-128"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>        | <span data-ttu-id="6881d-129">НПП подключается к сети, но не с методом [**истатс:: Connect**](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="6881d-129">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="6881d-130"><dt>**НМЕРР \_ без \_ \_ статистики**</dt></span><span class="sxs-lookup"><span data-stu-id="6881d-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="6881d-131">Для конфигурации этого соединения задано значение не сохранять статистику диалога.</span><span class="sxs-lookup"><span data-stu-id="6881d-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="6881d-132">Чтобы сохранить статистику диалога, закройте запись, задайте **ноконверсатионстатс = Yes** в большом двоичном объекте конфигурации, а затем перезапустите запись.</span><span class="sxs-lookup"><span data-stu-id="6881d-132">To save conversation statistics, stop the capture, set **NoConversationStats = YES** in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6881d-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6881d-133">Remarks</span></span>

<span data-ttu-id="6881d-134">Этот метод можно вызывать только во время сбора данных. Если текущая запись приостановлена, вызов этого метода не будет выполнен.</span><span class="sxs-lookup"><span data-stu-id="6881d-134">This method can be called only while data capture is in progress; when the current capture is paused, a call to this method will not succeed.</span></span>

<span data-ttu-id="6881d-135">Чтобы начать запись, вызовите метод [**истатс:: Start**](istats-start.md) .</span><span class="sxs-lookup"><span data-stu-id="6881d-135">To start a capture, call the [**IStats::Start**](istats-start.md) method.</span></span> <span data-ttu-id="6881d-136">Чтобы получить другие типы статистики, вызовите метод [**истатс:: жеттоталстатистикс**](istats-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="6881d-136">To retrieve other types of statistics, call [**IStats::GetTotalStatistics**](istats-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6881d-137">Требования</span><span class="sxs-lookup"><span data-stu-id="6881d-137">Requirements</span></span>



| <span data-ttu-id="6881d-138">Требование</span><span class="sxs-lookup"><span data-stu-id="6881d-138">Requirement</span></span> | <span data-ttu-id="6881d-139">Значение</span><span class="sxs-lookup"><span data-stu-id="6881d-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6881d-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6881d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="6881d-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6881d-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6881d-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6881d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="6881d-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6881d-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6881d-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6881d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="6881d-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6881d-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6881d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6881d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6881d-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6881d-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6881d-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6881d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6881d-149">**истатс**</span><span class="sxs-lookup"><span data-stu-id="6881d-149">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="6881d-150">**Истатс:: Жеттоталстатистикс**</span><span class="sxs-lookup"><span data-stu-id="6881d-150">**IStats::GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="6881d-151">**Истатс:: Start**</span><span class="sxs-lookup"><span data-stu-id="6881d-151">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="6881d-152">**Истатс:: Connect**</span><span class="sxs-lookup"><span data-stu-id="6881d-152">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="6881d-153">**сессионстатс**</span><span class="sxs-lookup"><span data-stu-id="6881d-153">**SESSIONSTATS**</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="6881d-154">**статионстатс**</span><span class="sxs-lookup"><span data-stu-id="6881d-154">**STATIONSTATS**</span></span>](stationstats.md)
</dt> </dl>

 

 




