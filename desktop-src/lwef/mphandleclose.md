---
title: Функция Мфандлеклосе (Мпклиент. h)
description: Закрывает маркер, возвращенный Мпманажеропен, Мпсканстарт, Мпсреатопен или Мпупдатестарт.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Функции Мфандлеклосе устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535141"
---
# <a name="mphandleclose-function"></a><span data-ttu-id="9ce3a-104">Функция Мфандлеклосе</span><span class="sxs-lookup"><span data-stu-id="9ce3a-104">MpHandleClose function</span></span>

<span data-ttu-id="9ce3a-105">Закрывает маркер, возвращенный [**мпманажеропен**](mpmanageropen.md), [**мпсканстарт**](mpscanstart.md), [**мпсреатопен**](mpthreatopen.md)или [**мпупдатестарт**](mpupdatestart.md).</span><span class="sxs-lookup"><span data-stu-id="9ce3a-105">Closes the handle returned by [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md), or [**MpUpdateStart**](mpupdatestart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce3a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ce3a-106">Syntax</span></span>


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="9ce3a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9ce3a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ce3a-108">*хмфандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9ce3a-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ce3a-109">Тип: **мфандле**</span><span class="sxs-lookup"><span data-stu-id="9ce3a-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="9ce3a-110">Закрываемый обработчик.</span><span class="sxs-lookup"><span data-stu-id="9ce3a-110">Handle to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ce3a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9ce3a-111">Return value</span></span>

<span data-ttu-id="9ce3a-112">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9ce3a-112">Type: **HRESULT**</span></span>

<span data-ttu-id="9ce3a-113">Если функция выполнена успешно, возвращается значение **S \_**.</span><span class="sxs-lookup"><span data-stu-id="9ce3a-113">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="9ce3a-114">Если функция завершается ошибкой, возвращаемое значение является неудачным кодом **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9ce3a-114">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="9ce3a-115">Вызывающий объект может использовать функцию [**мперрормессажеформат**](mperrormessageformat.md) для получения общего описания сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="9ce3a-115">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

<span data-ttu-id="9ce3a-116">Функция может вернуть следующую конкретную ошибку:</span><span class="sxs-lookup"><span data-stu-id="9ce3a-116">The following specific error can be returned by the function:</span></span>

| <span data-ttu-id="9ce3a-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9ce3a-117">Return Code</span></span>             | <span data-ttu-id="9ce3a-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9ce3a-118">Description</span></span>                      |
|-------------------------|----------------------------------|
| <span data-ttu-id="9ce3a-119">\_ \_ Недопустимый маркер "E Win" \_</span><span class="sxs-lookup"><span data-stu-id="9ce3a-119">E\_WIN\_INVALID\_HANDLE</span></span> | <span data-ttu-id="9ce3a-120">Указан недопустимый маркер.</span><span class="sxs-lookup"><span data-stu-id="9ce3a-120">The specified handle is invalid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9ce3a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="9ce3a-121">Requirements</span></span>



| <span data-ttu-id="9ce3a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="9ce3a-122">Requirement</span></span> | <span data-ttu-id="9ce3a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="9ce3a-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce3a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ce3a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9ce3a-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9ce3a-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9ce3a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ce3a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9ce3a-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9ce3a-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ce3a-128">Header</span><span class="sxs-lookup"><span data-stu-id="9ce3a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ce3a-129"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ce3a-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9ce3a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9ce3a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ce3a-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ce3a-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce3a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ce3a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce3a-133">**мперрормессажеформат**</span><span class="sxs-lookup"><span data-stu-id="9ce3a-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="9ce3a-134">**мпманажеропен**</span><span class="sxs-lookup"><span data-stu-id="9ce3a-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="9ce3a-135">**мпсканстарт**</span><span class="sxs-lookup"><span data-stu-id="9ce3a-135">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="9ce3a-136">**мпсреатопен**</span><span class="sxs-lookup"><span data-stu-id="9ce3a-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> </dl>

 

 





