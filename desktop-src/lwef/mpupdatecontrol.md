---
title: Функция Мпупдатеконтрол (Мпклиент. h)
description: Позволяет управлять операцией обновления сигнатур, которая была асинхронно инициирована через Мпупдатестарт.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Функции Мпупдатеконтрол устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491547"
---
# <a name="mpupdatecontrol-function"></a><span data-ttu-id="de486-104">Функция Мпупдатеконтрол</span><span class="sxs-lookup"><span data-stu-id="de486-104">MpUpdateControl function</span></span>

<span data-ttu-id="de486-105">Позволяет управлять операцией обновления сигнатур, которая была асинхронно инициирована через [**мпупдатестарт**](mpupdatestart.md).</span><span class="sxs-lookup"><span data-stu-id="de486-105">Allows the control of a signature update operation that was asynchronously initiated via [**MpUpdateStart**](mpupdatestart.md).</span></span> <span data-ttu-id="de486-106">Для вызова этой функции требуются права администратора, так как она допускает отмену обновления сигнатур на уровне системы.</span><span class="sxs-lookup"><span data-stu-id="de486-106">Calling this function requires administrator privilege as it allows the cancellation of a system-wide signature update.</span></span>

## <a name="syntax"></a><span data-ttu-id="de486-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de486-107">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a><span data-ttu-id="de486-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="de486-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de486-109">*хупдатехандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de486-109">*hUpdateHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de486-110">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="de486-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="de486-111">Обработчик асинхронной операции обновления сигнатур.</span><span class="sxs-lookup"><span data-stu-id="de486-111">Handle to an asynchronous signature update operation.</span></span> <span data-ttu-id="de486-112">Этот маркер возвращается функцией [**мпсканстарт**](mpscanstart.md) .</span><span class="sxs-lookup"><span data-stu-id="de486-112">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="de486-113">*Упдатеконтрол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de486-113">*UpdateControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de486-114">Тип: **файл mpcontrol**</span><span class="sxs-lookup"><span data-stu-id="de486-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="de486-115">Задает параметр управления обновлением сигнатур.</span><span class="sxs-lookup"><span data-stu-id="de486-115">Specifies the signature update control option.</span></span> <span data-ttu-id="de486-116">Это должно быть следующее значение:</span><span class="sxs-lookup"><span data-stu-id="de486-116">It must be the following value:</span></span>



| <span data-ttu-id="de486-117">Значение</span><span class="sxs-lookup"><span data-stu-id="de486-117">Value</span></span>                                                                                                                                                               | <span data-ttu-id="de486-118">Значение</span><span class="sxs-lookup"><span data-stu-id="de486-118">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="de486-119"><dt>**прервать файл MPCONTROL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de486-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="de486-120">Прервать операцию обновления сигнатур.</span><span class="sxs-lookup"><span data-stu-id="de486-120">Abort the signature update operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de486-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de486-121">Return value</span></span>

<span data-ttu-id="de486-122">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="de486-122">Type: **HRESULT**</span></span>

<span data-ttu-id="de486-123">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="de486-123">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="de486-124">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de486-124">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="de486-125">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="de486-125">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="de486-126">Требования</span><span class="sxs-lookup"><span data-stu-id="de486-126">Requirements</span></span>



| <span data-ttu-id="de486-127">Требование</span><span class="sxs-lookup"><span data-stu-id="de486-127">Requirement</span></span> | <span data-ttu-id="de486-128">Значение</span><span class="sxs-lookup"><span data-stu-id="de486-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de486-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de486-129">Minimum supported client</span></span><br/> | <span data-ttu-id="de486-130">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="de486-130">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="de486-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de486-131">Minimum supported server</span></span><br/> | <span data-ttu-id="de486-132">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="de486-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de486-133">Header</span><span class="sxs-lookup"><span data-stu-id="de486-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="de486-134"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="de486-134"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="de486-135">DLL</span><span class="sxs-lookup"><span data-stu-id="de486-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de486-136"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de486-136"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de486-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de486-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de486-138">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="de486-138">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="de486-139">**мпсканстарт**</span><span class="sxs-lookup"><span data-stu-id="de486-139">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





