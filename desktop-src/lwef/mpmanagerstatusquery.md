---
title: Функция Мпманажерстатускуери (Мпклиент. h)
description: Возвращает сведения о состоянии различных компонентов диспетчера защиты от вредоносных программ. | Функция Мпманажерстатускуери (Мпклиент. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Функции Мпманажерстатускуери устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352252"
---
# <a name="mpmanagerstatusquery-function"></a><span data-ttu-id="be19b-105">Функция Мпманажерстатускуери</span><span class="sxs-lookup"><span data-stu-id="be19b-105">MpManagerStatusQuery function</span></span>

<span data-ttu-id="be19b-106">\[**Мпманажерстатускуери** не поддерживается и может быть изменен или недоступен в будущем.</span><span class="sxs-lookup"><span data-stu-id="be19b-106">\[**MpManagerStatusQuery** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="be19b-107">Вместо этого используйте [**мпманажерстатускуерекс**](mpmanagerstatusqueryex.md).\]</span><span class="sxs-lookup"><span data-stu-id="be19b-107">Instead, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span></span>

<span data-ttu-id="be19b-108">Возвращает сведения о состоянии различных компонентов диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="be19b-108">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="be19b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be19b-109">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="be19b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="be19b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be19b-111">*хмфандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be19b-111">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be19b-112">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="be19b-112">Type: **MPHANDLE**</span></span>

<span data-ttu-id="be19b-113">Обработчик для интерфейса диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="be19b-113">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="be19b-114">Этот маркер возвращается функцией [**мпманажеропен**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="be19b-114">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="be19b-115">*пстатусинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="be19b-115">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be19b-116">Тип: **пмпстатус \_ info** .</span><span class="sxs-lookup"><span data-stu-id="be19b-116">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="be19b-117">Указатель на структуру, которая возвращает сведения о состоянии для последних просмотров, активных угроз и состояния различных компонентов.</span><span class="sxs-lookup"><span data-stu-id="be19b-117">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="be19b-118">См [**. \_ сведения о мпстатус**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="be19b-118">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be19b-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be19b-119">Return value</span></span>

<span data-ttu-id="be19b-120">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="be19b-120">Type: **HRESULT**</span></span>

<span data-ttu-id="be19b-121">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="be19b-121">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="be19b-122">Вызов этой функции гарантированно будет выполнен, даже если служба защиты от вредоносных программ не запущена.</span><span class="sxs-lookup"><span data-stu-id="be19b-122">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="be19b-123">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be19b-123">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="be19b-124">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="be19b-124">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="be19b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="be19b-125">Requirements</span></span>



| <span data-ttu-id="be19b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="be19b-126">Requirement</span></span> | <span data-ttu-id="be19b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="be19b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be19b-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be19b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="be19b-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="be19b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="be19b-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be19b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="be19b-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="be19b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="be19b-132">Header</span><span class="sxs-lookup"><span data-stu-id="be19b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="be19b-133"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="be19b-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="be19b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="be19b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be19b-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be19b-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be19b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be19b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be19b-137">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="be19b-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="be19b-138">**мпманажеропен**</span><span class="sxs-lookup"><span data-stu-id="be19b-138">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="be19b-139">**мпманажерстатускуерекс**</span><span class="sxs-lookup"><span data-stu-id="be19b-139">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="be19b-140">**\_сведения о мпстатус**</span><span class="sxs-lookup"><span data-stu-id="be19b-140">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





