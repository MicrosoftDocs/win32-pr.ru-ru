---
title: Функция Мпсканконтрол (Мпклиент. h)
description: Разрешает Управление сканированием, которое было асинхронно инициировано через Мпсканстарт.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Функции Мпсканконтрол устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490389"
---
# <a name="mpscancontrol-function"></a><span data-ttu-id="8fe28-104">Функция Мпсканконтрол</span><span class="sxs-lookup"><span data-stu-id="8fe28-104">MpScanControl function</span></span>

<span data-ttu-id="8fe28-105">Разрешает Управление сканированием, которое было асинхронно инициировано через [**мпсканстарт**](mpscanstart.md).</span><span class="sxs-lookup"><span data-stu-id="8fe28-105">Allows the control of a scan that was asynchronously initiated via [**MpScanStart**](mpscanstart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe28-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fe28-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a><span data-ttu-id="8fe28-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fe28-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe28-108">*хсканхандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8fe28-108">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe28-109">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="8fe28-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="8fe28-110">Обработчик операции асинхронной проверки.</span><span class="sxs-lookup"><span data-stu-id="8fe28-110">Handle to an asynchronous scan operation.</span></span> <span data-ttu-id="8fe28-111">Этот маркер возвращается функцией [**мпсканстарт**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="8fe28-111">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="8fe28-112">Этот параметр также можно задать в качестве маркера интерфейса диспетчера защиты от вредоносных программ, возвращаемого функцией [**мпманажеропен**](mpmanageropen.md) для управления инициированной системой проверки. в этом случае вызывающая сторона должна иметь права администратора.</span><span class="sxs-lookup"><span data-stu-id="8fe28-112">This parameter can also be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) function to control a system initiated scan, in which case the caller must have administrative privilege.</span></span>

</dd> <dt>

<span data-ttu-id="8fe28-113">*Сканконтрол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8fe28-113">*ScanControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe28-114">Тип: **файл mpcontrol**</span><span class="sxs-lookup"><span data-stu-id="8fe28-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="8fe28-115">Задает параметр контроля проверки.</span><span class="sxs-lookup"><span data-stu-id="8fe28-115">Specifies a scan control option.</span></span> <span data-ttu-id="8fe28-116">Этот параметр должен быть одним из следующих параметров управления:</span><span class="sxs-lookup"><span data-stu-id="8fe28-116">This parameter must be one of the following control options:</span></span>



| <span data-ttu-id="8fe28-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8fe28-117">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="8fe28-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8fe28-118">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="8fe28-119"><dt>**прервать файл MPCONTROL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fe28-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl>    | <span data-ttu-id="8fe28-120">Прервать операцию сканирования.</span><span class="sxs-lookup"><span data-stu-id="8fe28-120">Abort the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <span data-ttu-id="8fe28-121"><dt>**Приостановка файл MPCONTROL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fe28-121"><dt>**MPCONTROL\_PAUSE**</dt></span></span> </dl>    | <span data-ttu-id="8fe28-122">Приостановка операции сканирования.</span><span class="sxs-lookup"><span data-stu-id="8fe28-122">Pause the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <span data-ttu-id="8fe28-123"><dt>**возобновление файл MPCONTROL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8fe28-123"><dt>**MPCONTROL\_RESUME**</dt></span></span> </dl> | <span data-ttu-id="8fe28-124">Возобновить приостановленную операцию просмотра.</span><span class="sxs-lookup"><span data-stu-id="8fe28-124">Resume the paused scan operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe28-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fe28-125">Return value</span></span>

<span data-ttu-id="8fe28-126">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8fe28-126">Type: **HRESULT**</span></span>

<span data-ttu-id="8fe28-127">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="8fe28-127">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="8fe28-128">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8fe28-128">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="8fe28-129">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8fe28-129">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe28-130">Требования</span><span class="sxs-lookup"><span data-stu-id="8fe28-130">Requirements</span></span>



| <span data-ttu-id="8fe28-131">Требование</span><span class="sxs-lookup"><span data-stu-id="8fe28-131">Requirement</span></span> | <span data-ttu-id="8fe28-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8fe28-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe28-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fe28-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe28-134">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8fe28-134">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8fe28-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fe28-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe28-136">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8fe28-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8fe28-137">Header</span><span class="sxs-lookup"><span data-stu-id="8fe28-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe28-138"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fe28-138"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="8fe28-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8fe28-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fe28-140"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fe28-140"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe28-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fe28-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe28-142">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="8fe28-142">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="8fe28-143">**мпманажеропен**</span><span class="sxs-lookup"><span data-stu-id="8fe28-143">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="8fe28-144">**мпсканстарт**</span><span class="sxs-lookup"><span data-stu-id="8fe28-144">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





