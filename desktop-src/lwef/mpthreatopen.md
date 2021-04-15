---
title: Функция Мпсреатопен (Мпклиент. h)
description: Возвращает маркер перечисления, предназначенный для получения угроз.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Функции Мпсреатопен устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661905"
---
# <a name="mpthreatopen-function"></a><span data-ttu-id="7b4de-104">Функция Мпсреатопен</span><span class="sxs-lookup"><span data-stu-id="7b4de-104">MpThreatOpen function</span></span>

<span data-ttu-id="7b4de-105">Возвращает маркер перечисления, предназначенный для получения угроз.</span><span class="sxs-lookup"><span data-stu-id="7b4de-105">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="7b4de-106">Эта функция может использоваться для открытия угроз, обнаруженных конкретным сканированием, всех активных угроз в системе, истории заражения угроз или всех угроз, имеющихся в базе данных сигнатур.</span><span class="sxs-lookup"><span data-stu-id="7b4de-106">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4de-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b4de-107">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a><span data-ttu-id="7b4de-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7b4de-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b4de-109">*хсканхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b4de-109">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4de-110">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="7b4de-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="7b4de-111">Может быть обработкой завершенной операции просмотра, возвращаемой функцией [**мпсканстарт**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="7b4de-111">Can be a handle to a completed scan operation, returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="7b4de-112">Кроме того, для этого параметра можно задать маркер интерфейса диспетчера защиты от вредоносных программ, возвращаемый функцией [**мпманажеропен**](mpmanageropen.md) , чтобы перечислить все активные угрозы в системе, историю заражения угроз или угрозы из базы данных сигнатур.</span><span class="sxs-lookup"><span data-stu-id="7b4de-112">Alternately, this parameter can be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) to enumerate all active threats in the system, the history of threat disinfection, or threats from signature database.</span></span>

</dd> <dt>

<span data-ttu-id="7b4de-113">*Среатсаурце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b4de-113">*ThreatSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4de-114">Тип: **мпсреат \_ Source**</span><span class="sxs-lookup"><span data-stu-id="7b4de-114">Type: **MPTHREAT\_SOURCE**</span></span>

<span data-ttu-id="7b4de-115">Используется для управления источником перечисления угроз.</span><span class="sxs-lookup"><span data-stu-id="7b4de-115">Used to control the source of threat enumeration.</span></span> <span data-ttu-id="7b4de-116">Возможные значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="7b4de-116">The possible values for this parameter are:</span></span>



| <span data-ttu-id="7b4de-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7b4de-117">Value</span></span>                                                                                                                                                                                                 | <span data-ttu-id="7b4de-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7b4de-118">Meaning</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <span data-ttu-id="7b4de-119"><dt>**\_Проверка источника \_ мпсреат**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-119"><dt>**MPTHREAT\_SOURCE\_SCAN**</dt></span></span> </dl>                   | <span data-ttu-id="7b4de-120">Угрозы, связанные с конкретным обработчиком сканирования.</span><span class="sxs-lookup"><span data-stu-id="7b4de-120">Threats that are associated with the specific scan handle.</span></span><br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <span data-ttu-id="7b4de-121"><dt>**\_источник мпсреат \_ активен**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-121"><dt>**MPTHREAT\_SOURCE\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="7b4de-122">Угрозы, которые в настоящее время активны в системе.</span><span class="sxs-lookup"><span data-stu-id="7b4de-122">Threats that are currently active in the system.</span></span><br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <span data-ttu-id="7b4de-123"><dt>**\_журнал источника \_ мпсреат**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-123"><dt>**MPTHREAT\_SOURCE\_HISTORY**</dt></span></span> </dl>          | <span data-ttu-id="7b4de-124">Угрозы, обрабатываемые и сохраняемые в виде журнала.</span><span class="sxs-lookup"><span data-stu-id="7b4de-124">Threats that are acted upon and preserved as a history.</span></span><br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <span data-ttu-id="7b4de-125"><dt>**\_Карантин источника \_ мпсреат**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-125"><dt>**MPTHREAT\_SOURCE\_QUARANTINE**</dt></span></span> </dl> | <span data-ttu-id="7b4de-126">Угрозы, помещенные в карантин.</span><span class="sxs-lookup"><span data-stu-id="7b4de-126">Threats that are quarantined.</span></span><br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <span data-ttu-id="7b4de-127"><dt>**\_Исходная \_ подпись мпсреат**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-127"><dt>**MPTHREAT\_SOURCE\_SIGNATURE**</dt></span></span> </dl>    | <span data-ttu-id="7b4de-128">Угрозы, которые можно обнаружить с помощью текущей базы данных сигнатур.</span><span class="sxs-lookup"><span data-stu-id="7b4de-128">Threats that are possible to detect with the current signature database.</span></span><br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <span data-ttu-id="7b4de-129"><dt>**\_состояние источника \_ мпсреат**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-129"><dt>**MPTHREAT\_SOURCE\_STATE**</dt></span></span> </dl>                | <span data-ttu-id="7b4de-130">Угрозы, которые были выполнены недавно.</span><span class="sxs-lookup"><span data-stu-id="7b4de-130">Threats that have been acted upon recently.</span></span> <span data-ttu-id="7b4de-131">("Недавно" определяется настраиваемым внутренним параметром.)</span><span class="sxs-lookup"><span data-stu-id="7b4de-131">("Recently" is defined by a configurable internal setting.)</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7b4de-132">*Среаттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7b4de-132">*ThreatType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4de-133">Тип: **мпсреат \_ тип**</span><span class="sxs-lookup"><span data-stu-id="7b4de-133">Type: **MPTHREAT\_TYPE**</span></span>

<span data-ttu-id="7b4de-134">Используется для фильтрации перечисленных угроз на основе типа обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7b4de-134">Used to filter enumerated threats based on the detection type.</span></span> <span data-ttu-id="7b4de-135">Возможные значения для этого параметра:</span><span class="sxs-lookup"><span data-stu-id="7b4de-135">The possible values for this parameter are:</span></span>



| <span data-ttu-id="7b4de-136">Значение</span><span class="sxs-lookup"><span data-stu-id="7b4de-136">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="7b4de-137">Значение</span><span class="sxs-lookup"><span data-stu-id="7b4de-137">Meaning</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <span data-ttu-id="7b4de-138"><dt>**\_тип мпсреат \_ кновнбад**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-138"><dt>**MPTHREAT\_TYPE\_KNOWNBAD**</dt></span></span> </dl>       | <span data-ttu-id="7b4de-139">Обнаружение выполняется на основе определенной сигнатуры, эмуляции или другого метода обнаружения угроз.</span><span class="sxs-lookup"><span data-stu-id="7b4de-139">Detection is performed based on a specific signature, emulation, or other threat detection method.</span></span><br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <span data-ttu-id="7b4de-140"><dt>**\_тип мпсреат \_ подозрительный**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-140"><dt>**MPTHREAT\_TYPE\_SUSPICIOUS**</dt></span></span> </dl> | <span data-ttu-id="7b4de-141">Обнаружение выполняется на основе мониторинга поведения.</span><span class="sxs-lookup"><span data-stu-id="7b4de-141">Detection is performed based on behavior monitoring.</span></span><br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <span data-ttu-id="7b4de-142"><dt>**\_неизвестный тип мпсреат \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-142"><dt>**MPTHREAT\_TYPE\_UNKNOWN**</dt></span></span> </dl>          | <span data-ttu-id="7b4de-143">Обнаружение выполняется на основе неизвестных угроз (неклассифицированных).</span><span class="sxs-lookup"><span data-stu-id="7b4de-143">Detection is performed based on unknown threats (unclassified).</span></span><br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <span data-ttu-id="7b4de-144"><dt>**\_тип мпсреат \_ кновнгуд**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-144"><dt>**MPTHREAT\_TYPE\_KNOWNGOOD**</dt></span></span> </dl>    | <span data-ttu-id="7b4de-145">Обнаружение выполняется на основе известных угроз безопасности.</span><span class="sxs-lookup"><span data-stu-id="7b4de-145">Detection is performed based on known safe threats.</span></span><br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <span data-ttu-id="7b4de-146"><dt>**МПСРЕАТ \_ тип \_ NIS**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-146"><dt>**MPTHREAT\_TYPE\_NIS**</dt></span></span> </dl>                      | <span data-ttu-id="7b4de-147">Обнаружение выполняется на основе угроз NIS.</span><span class="sxs-lookup"><span data-stu-id="7b4de-147">Detection is performed based on NIS threats.</span></span><br/>                                                       |



 

</dd> <dt>

<span data-ttu-id="7b4de-148">*фсреатенумхандле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7b4de-148">*phThreatEnumHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4de-149">Тип: **пмфандле**</span><span class="sxs-lookup"><span data-stu-id="7b4de-149">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="7b4de-150">Возвращенный обработчик перечисления угроз, который идентифицирует контекст перечисления.</span><span class="sxs-lookup"><span data-stu-id="7b4de-150">Returned threat enumeration handle which identifies the enumeration context.</span></span> <span data-ttu-id="7b4de-151">Этот обработчик можно использовать для перечисления сведений об угрозах с помощью [**мпсреатенумерате**](mpthreatenumerate.md).</span><span class="sxs-lookup"><span data-stu-id="7b4de-151">This handle can be used to enumerate threat information using [**MpThreatEnumerate**](mpthreatenumerate.md).</span></span> <span data-ttu-id="7b4de-152">Этот маркер должен быть закрыт функцией [**мфандлеклосе**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="7b4de-152">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b4de-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7b4de-153">Return value</span></span>

<span data-ttu-id="7b4de-154">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7b4de-154">Type: **HRESULT**</span></span>

<span data-ttu-id="7b4de-155">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="7b4de-155">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="7b4de-156">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7b4de-156">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="7b4de-157">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7b4de-157">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4de-158">Требования</span><span class="sxs-lookup"><span data-stu-id="7b4de-158">Requirements</span></span>



| <span data-ttu-id="7b4de-159">Требование</span><span class="sxs-lookup"><span data-stu-id="7b4de-159">Requirement</span></span> | <span data-ttu-id="7b4de-160">Значение</span><span class="sxs-lookup"><span data-stu-id="7b4de-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4de-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b4de-161">Minimum supported client</span></span><br/> | <span data-ttu-id="7b4de-162">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7b4de-162">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="7b4de-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b4de-163">Minimum supported server</span></span><br/> | <span data-ttu-id="7b4de-164">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7b4de-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b4de-165">Header</span><span class="sxs-lookup"><span data-stu-id="7b4de-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b4de-166"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-166"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b4de-167">DLL</span><span class="sxs-lookup"><span data-stu-id="7b4de-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b4de-168"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b4de-168"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b4de-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b4de-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4de-170">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="7b4de-170">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="7b4de-171">**мфандлеклосе**</span><span class="sxs-lookup"><span data-stu-id="7b4de-171">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="7b4de-172">**мпманажеропен**</span><span class="sxs-lookup"><span data-stu-id="7b4de-172">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="7b4de-173">**мпсканстарт**</span><span class="sxs-lookup"><span data-stu-id="7b4de-173">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="7b4de-174">**мпсреатенумерате**</span><span class="sxs-lookup"><span data-stu-id="7b4de-174">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> </dl>

 

 





