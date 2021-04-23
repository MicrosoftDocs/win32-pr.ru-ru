---
title: Функция Мпманажерстатускуерекс (Мпклиент. h)
description: Возвращает сведения о состоянии различных компонентов диспетчера защиты от вредоносных программ. | Функция Мпманажерстатускуерекс (Мпклиент. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Функции Мпманажерстатускуерекс устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684972"
---
# <a name="mpmanagerstatusqueryex-function"></a><span data-ttu-id="8190a-105">Функция Мпманажерстатускуерекс</span><span class="sxs-lookup"><span data-stu-id="8190a-105">MpManagerStatusQueryEx function</span></span>

<span data-ttu-id="8190a-106">Возвращает сведения о состоянии различных компонентов диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="8190a-106">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="8190a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8190a-107">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8190a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8190a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8190a-109">*хмфандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8190a-109">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8190a-110">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="8190a-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="8190a-111">Обработчик для интерфейса диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="8190a-111">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="8190a-112">Этот маркер возвращается функцией [**мпманажеропен**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="8190a-112">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="8190a-113">*dwFlag* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8190a-113">*dwFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8190a-114">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8190a-114">Type: **DWORD**</span></span>

<span data-ttu-id="8190a-115">Определяет, какие сведения о запросах возвращаются.</span><span class="sxs-lookup"><span data-stu-id="8190a-115">Controls which query information is returned.</span></span> <span data-ttu-id="8190a-116">Некоторые сведения являются дорогостоящими и могут не потребоваться.</span><span class="sxs-lookup"><span data-stu-id="8190a-116">Some information is expensive and may not be needed.</span></span>



| <span data-ttu-id="8190a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8190a-117">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="8190a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8190a-118">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <span data-ttu-id="8190a-119"><dt>**\_ \_ флаги запроса состояния пакета управления \_ \_ нет**</dt></span><span class="sxs-lookup"><span data-stu-id="8190a-119"><dt>**MP\_STATUS\_QUERY\_FLAGS\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="8190a-120">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8190a-120">Default.</span></span><br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <span data-ttu-id="8190a-121"><dt>**\_флаг запроса состояния пакета управления " \_ \_ \_ несостояние"**</dt></span><span class="sxs-lookup"><span data-stu-id="8190a-121"><dt>**MP\_STATUS\_QUERY\_FLAG\_NOSTATE**</dt></span></span> </dl> | <span data-ttu-id="8190a-122">Не запрашивать сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="8190a-122">Do not query for state information.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8190a-123">*пстатусинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8190a-123">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8190a-124">Тип: **пмпстатус \_ info** .</span><span class="sxs-lookup"><span data-stu-id="8190a-124">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="8190a-125">Указатель на структуру, которая возвращает сведения о состоянии для последних просмотров, активных угроз и состояния различных компонентов.</span><span class="sxs-lookup"><span data-stu-id="8190a-125">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="8190a-126">См [**. \_ сведения о мпстатус**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="8190a-126">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8190a-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8190a-127">Return value</span></span>

<span data-ttu-id="8190a-128">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8190a-128">Type: **HRESULT**</span></span>

<span data-ttu-id="8190a-129">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="8190a-129">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="8190a-130">Вызов этой функции гарантированно будет выполнен, даже если служба защиты от вредоносных программ не запущена.</span><span class="sxs-lookup"><span data-stu-id="8190a-130">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="8190a-131">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8190a-131">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="8190a-132">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8190a-132">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8190a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="8190a-133">Requirements</span></span>



| <span data-ttu-id="8190a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="8190a-134">Requirement</span></span> | <span data-ttu-id="8190a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8190a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8190a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8190a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8190a-137">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8190a-137">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8190a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8190a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8190a-139">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8190a-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8190a-140">Header</span><span class="sxs-lookup"><span data-stu-id="8190a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8190a-141"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="8190a-141"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="8190a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8190a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8190a-143"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8190a-143"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8190a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8190a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8190a-145">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="8190a-145">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="8190a-146">**мпманажеропен**</span><span class="sxs-lookup"><span data-stu-id="8190a-146">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="8190a-147">**\_сведения о мпстатус**</span><span class="sxs-lookup"><span data-stu-id="8190a-147">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





