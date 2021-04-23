---
title: Функция Мпманажеропен (Мпклиент. h)
description: Устанавливает подключение к диспетчеру защиты от вредоносных программ на локальном компьютере.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Функции Мпманажеропен устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803538"
---
# <a name="mpmanageropen-function"></a><span data-ttu-id="1e796-104">Функция Мпманажеропен</span><span class="sxs-lookup"><span data-stu-id="1e796-104">MpManagerOpen function</span></span>

<span data-ttu-id="1e796-105">Устанавливает подключение к диспетчеру защиты от вредоносных программ на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="1e796-105">Establishes a connection to the malware protection manager on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e796-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e796-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="1e796-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e796-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e796-108">*двресервед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e796-108">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e796-109">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="1e796-109">Type: **DWORD**</span></span>

<span data-ttu-id="1e796-110">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="1e796-110">Reserved for future use.</span></span> <span data-ttu-id="1e796-111">Должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="1e796-111">Must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1e796-112">*фмфандле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1e796-112">*phMpHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e796-113">Тип: **пмфандле**</span><span class="sxs-lookup"><span data-stu-id="1e796-113">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="1e796-114">Обработчик для интерфейса диспетчера защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="1e796-114">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="1e796-115">Этот обработчик должен быть закрыт функцией [**мфандлеклосе**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="1e796-115">This handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e796-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e796-116">Return value</span></span>

<span data-ttu-id="1e796-117">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1e796-117">Type: **HRESULT**</span></span>

<span data-ttu-id="1e796-118">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="1e796-118">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="1e796-119">Вызов этой функции гарантированно будет выполнен, даже если служба защиты от вредоносных программ не запущена.</span><span class="sxs-lookup"><span data-stu-id="1e796-119">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="1e796-120">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e796-120">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="1e796-121">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="1e796-121">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e796-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1e796-122">Requirements</span></span>



| <span data-ttu-id="1e796-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1e796-123">Requirement</span></span> | <span data-ttu-id="1e796-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1e796-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e796-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e796-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1e796-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1e796-126">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1e796-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e796-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1e796-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1e796-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e796-129">Header</span><span class="sxs-lookup"><span data-stu-id="1e796-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e796-130"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e796-130"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e796-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1e796-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e796-132"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e796-132"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e796-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e796-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e796-134">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="1e796-134">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="1e796-135">**мфандлеклосе**</span><span class="sxs-lookup"><span data-stu-id="1e796-135">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> </dl>

 

 





