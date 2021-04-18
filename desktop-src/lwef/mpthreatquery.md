---
title: Функция Мпсреаткуери (Мпклиент. h)
description: Используется для запроса статических (таких как серьезность и категория) или локализованных сведений о конкретной угрозе (например, описание категории и рекомендации).
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Функции Мпсреаткуери устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661869"
---
# <a name="mpthreatquery-function"></a><span data-ttu-id="8c1d0-104">Функция Мпсреаткуери</span><span class="sxs-lookup"><span data-stu-id="8c1d0-104">MpThreatQuery function</span></span>

<span data-ttu-id="8c1d0-105">Используется для запроса статических (таких как серьезность и категория) или локализованных сведений о конкретной угрозе (например, описание категории и рекомендации).</span><span class="sxs-lookup"><span data-stu-id="8c1d0-105">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c1d0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c1d0-106">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8c1d0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c1d0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c1d0-108">*хмфандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c1d0-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c1d0-109">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="8c1d0-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="8c1d0-110">Обработчик для интерфейса диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="8c1d0-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="8c1d0-111">Этот маркер возвращается функцией [**мпманажеропен**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="8c1d0-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8c1d0-112">*Среатид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8c1d0-112">*ThreatID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c1d0-113">Тип: **мпсреат \_ ID**</span><span class="sxs-lookup"><span data-stu-id="8c1d0-113">Type: **MPTHREAT\_ID**</span></span>

<span data-ttu-id="8c1d0-114">Идентификатор угрозы, для которого запрашиваются сведения.</span><span class="sxs-lookup"><span data-stu-id="8c1d0-114">Threat identifier for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="8c1d0-115">*ппсреатинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8c1d0-115">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c1d0-116">Введите: \**пмпсреат \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="8c1d0-116">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="8c1d0-117">Возвращает указатель на структуру сведений об угрозе, [_ *мпсреат \_ info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="8c1d0-117">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="8c1d0-118">Структура содержит такие сведения, как идентификатор угрозы, имя и серьезность.</span><span class="sxs-lookup"><span data-stu-id="8c1d0-118">The structure contains information such as threat id, name, and severity.</span></span>

</dd> <dt>

<span data-ttu-id="8c1d0-119">*ппсреатлокализединфо* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="8c1d0-119">*ppThreatLocalizedInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c1d0-120">Тип: \**пмпсреат \_ локализованная \_ информация \** _</span><span class="sxs-lookup"><span data-stu-id="8c1d0-120">Type: \**PMPTHREAT\_LOCALIZED\_INFO\** _</span></span>

<span data-ttu-id="8c1d0-121">Возвращает указатель на структуру, содержащую локализованные сведения о угрозе.</span><span class="sxs-lookup"><span data-stu-id="8c1d0-121">Returns a pointer to a structure containing localized information about the threat.</span></span> <span data-ttu-id="8c1d0-122">Если вы не заинтересованы в локализованной информации об угрозе, можно передать \*значение _ NULL\*\*.</span><span class="sxs-lookup"><span data-stu-id="8c1d0-122">You can pass _ *NULL*\* if you are not interested in localized information about the threat.</span></span> <span data-ttu-id="8c1d0-123">См [**. \_ \_ сведения о локализованных данных мпсреат**](mpthreat-localized-info.md).</span><span class="sxs-lookup"><span data-stu-id="8c1d0-123">See [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c1d0-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c1d0-124">Return value</span></span>

<span data-ttu-id="8c1d0-125">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8c1d0-125">Type: **HRESULT**</span></span>

<span data-ttu-id="8c1d0-126">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="8c1d0-126">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="8c1d0-127">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c1d0-127">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="8c1d0-128">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8c1d0-128">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c1d0-129">Требования</span><span class="sxs-lookup"><span data-stu-id="8c1d0-129">Requirements</span></span>



| <span data-ttu-id="8c1d0-130">Требование</span><span class="sxs-lookup"><span data-stu-id="8c1d0-130">Requirement</span></span> | <span data-ttu-id="8c1d0-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8c1d0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c1d0-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c1d0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8c1d0-133">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8c1d0-133">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8c1d0-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c1d0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8c1d0-135">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8c1d0-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8c1d0-136">Header</span><span class="sxs-lookup"><span data-stu-id="8c1d0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c1d0-137"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c1d0-137"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="8c1d0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8c1d0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c1d0-139"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c1d0-139"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c1d0-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c1d0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c1d0-141">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="8c1d0-141">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="8c1d0-142">**мпманажеропен**</span><span class="sxs-lookup"><span data-stu-id="8c1d0-142">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="8c1d0-143">**\_сведения о мпсреат**</span><span class="sxs-lookup"><span data-stu-id="8c1d0-143">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="8c1d0-144">**\_локализованные \_ сведения мпсреат**</span><span class="sxs-lookup"><span data-stu-id="8c1d0-144">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





