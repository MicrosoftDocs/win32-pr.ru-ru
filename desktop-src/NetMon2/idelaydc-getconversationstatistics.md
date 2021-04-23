---
description: Метод Жетконверсатионстатистикс извлекает сведения о сеансе и станции о текущей записи.
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: 'Метод Иделайдк:: Жетконверсатионстатистикс (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: aaba5ccfbab48639f53395519f001f5f8e85e483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682473"
---
# <a name="idelaydcgetconversationstatistics-method"></a><span data-ttu-id="1e41d-103">Метод Иделайдк:: Жетконверсатионстатистикс</span><span class="sxs-lookup"><span data-stu-id="1e41d-103">IDelaydC::GetConversationStatistics method</span></span>

<span data-ttu-id="1e41d-104">Метод **жетконверсатионстатистикс** извлекает сведения о [*сеансе*](s.md) и [*станции*](s.md) о текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1e41d-104">The **GetConversationStatistics** method retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e41d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e41d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="1e41d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e41d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e41d-107">*нсессионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e41d-107">*nSessions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e41d-108">Указатель на DWORD, содержащий количество [*сеансов*](s.md) , записанных для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1e41d-108">Pointer to a DWORD that contains the number of [*sessions*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="1e41d-109">*лпсессионстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e41d-109">*lpSessionStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e41d-110">Указатель на структуру [сессионстатс](sessionstats.md) .</span><span class="sxs-lookup"><span data-stu-id="1e41d-110">Pointer to a [SESSIONSTATS](sessionstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1e41d-111">*нстатионс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e41d-111">*nStations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e41d-112">Указатель на DWORD, содержащий число [*станций*](s.md) , записанных для текущего захвата.</span><span class="sxs-lookup"><span data-stu-id="1e41d-112">Pointer to a DWORD that contains the number of [*stations*](s.md) recorded for the current capture.</span></span>

</dd> <dt>

<span data-ttu-id="1e41d-113">*лпстатионстатс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e41d-113">*lpStationStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e41d-114">Указатель на структуру [статионстатс](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="1e41d-114">Pointer to a [STATIONSTATS](stationstats.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1e41d-115">*фклеарафтерреадинг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e41d-115">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e41d-116">Флаг, который указывает сетевой монитор очищать внутреннее хранилище структур [сессионстатс](sessionstats.md) и [статионстатс](stationstats.md) после получения текущих данных.</span><span class="sxs-lookup"><span data-stu-id="1e41d-116">Flag used to tell Network Monitor to clear out the internal storage of the [SESSIONSTATS](sessionstats.md) and [STATIONSTATS](stationstats.md) structures after it retrieves the current information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e41d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e41d-117">Return value</span></span>

<span data-ttu-id="1e41d-118">Если метод выполнен успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1e41d-118">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1e41d-119">Если метод завершается неудачно, возвращаемое значение является одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="1e41d-119">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="1e41d-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="1e41d-120">Return code</span></span>                                                                                                   | <span data-ttu-id="1e41d-121">Описание</span><span class="sxs-lookup"><span data-stu-id="1e41d-121">Description</span></span>                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e41d-122"><dt>**НМЕРР \_ не \_ подключен**</dt></span><span class="sxs-lookup"><span data-stu-id="1e41d-122"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="1e41d-123">НПП не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="1e41d-123">The NPP is not connected to the network.</span></span> <span data-ttu-id="1e41d-124">Вызовите [иделайдк:: Connect](idelaydc-connect.md) , чтобы подключить НПП к сети.</span><span class="sxs-lookup"><span data-stu-id="1e41d-124">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="1e41d-125"><dt>**НМЕРР \_ не \_ захватывается**</dt></span><span class="sxs-lookup"><span data-stu-id="1e41d-125"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>          | <span data-ttu-id="1e41d-126">НПП не захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="1e41d-126">The NPP is not capturing data.</span></span> <span data-ttu-id="1e41d-127">Вызовите [иделайдк:: Start](idelaydc-start.md) , чтобы начать запись.</span><span class="sxs-lookup"><span data-stu-id="1e41d-127">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="1e41d-128"><dt>**НМЕРР \_ не \_ отложена**</dt></span><span class="sxs-lookup"><span data-stu-id="1e41d-128"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>            | <span data-ttu-id="1e41d-129">НПП подключается к сети, но не с методом [иделайдк:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="1e41d-129">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="1e41d-130"><dt>**НМЕРР \_ без \_ \_ статистики**</dt></span><span class="sxs-lookup"><span data-stu-id="1e41d-130"><dt>**NMERR\_NO\_CONVERSATION\_STATS**</dt></span></span> </dl> | <span data-ttu-id="1e41d-131">Для конфигурации этого соединения задано значение не сохранять статистику диалога.</span><span class="sxs-lookup"><span data-stu-id="1e41d-131">The configuration for this connection is set to not save conversation statistics.</span></span> <span data-ttu-id="1e41d-132">Чтобы сохранить статистику диалога, закройте запись, задайте Ноконверсатионстатс = YES в большом двоичном объекте конфигурации, а затем перезапустите запись.</span><span class="sxs-lookup"><span data-stu-id="1e41d-132">To save conversation statistics, stop the capture, set NoConversationStats = YES in the configuration BLOB, and then restart the capture.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1e41d-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e41d-133">Remarks</span></span>

<span data-ttu-id="1e41d-134">Этот метод может вызываться только во время сбора данных. Если текущая запись приостановлена, вызовы этого метода не будут выполнены.</span><span class="sxs-lookup"><span data-stu-id="1e41d-134">This method can only be called only while data capture is in progress; when the current capture is paused, calls to this method will not succeed.</span></span> <span data-ttu-id="1e41d-135">Чтобы начать запись, вызовите метод [иделайдк:: Start](idelaydc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="1e41d-135">To start a capture, call the [IDelaydC::Start](idelaydc-start.md) method.</span></span>

<span data-ttu-id="1e41d-136">Чтобы получить другие типы статистики, вызовите метод [иделайдк:: жеттоталстатистикс](idelaydc-gettotalstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="1e41d-136">To retrieve other types of statistics, call [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e41d-137">Требования</span><span class="sxs-lookup"><span data-stu-id="1e41d-137">Requirements</span></span>



| <span data-ttu-id="1e41d-138">Требование</span><span class="sxs-lookup"><span data-stu-id="1e41d-138">Requirement</span></span> | <span data-ttu-id="1e41d-139">Значение</span><span class="sxs-lookup"><span data-stu-id="1e41d-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e41d-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e41d-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1e41d-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e41d-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="1e41d-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e41d-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1e41d-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e41d-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="1e41d-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1e41d-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e41d-145"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e41d-145"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="1e41d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1e41d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e41d-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e41d-147"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e41d-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e41d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e41d-149">иделайдк</span><span class="sxs-lookup"><span data-stu-id="1e41d-149">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="1e41d-150">Иделайдк:: Connect</span><span class="sxs-lookup"><span data-stu-id="1e41d-150">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="1e41d-151">Иделайдк:: Жеттоталстатистикс</span><span class="sxs-lookup"><span data-stu-id="1e41d-151">IDelaydC::GetTotalStatistics</span></span>](idelaydc-gettotalstatistics.md)
</dt> <dt>

[<span data-ttu-id="1e41d-152">Иделайдк:: Start</span><span class="sxs-lookup"><span data-stu-id="1e41d-152">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="1e41d-153">сессионстатс</span><span class="sxs-lookup"><span data-stu-id="1e41d-153">SESSIONSTATS</span></span>](sessionstats.md)
</dt> <dt>

[<span data-ttu-id="1e41d-154">статионстатс</span><span class="sxs-lookup"><span data-stu-id="1e41d-154">STATIONSTATS</span></span>](stationstats.md)
</dt> </dl>

 

 




