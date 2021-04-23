---
description: Функция Жетфрамесркаддрессоффсет возвращает смещение исходного адреса кадров.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Функция Жетфрамесркаддрессоффсет (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265652"
---
# <a name="getframesrcaddressoffset-function"></a><span data-ttu-id="087bc-103">Функция Жетфрамесркаддрессоффсет</span><span class="sxs-lookup"><span data-stu-id="087bc-103">GetFrameSrcAddressOffset function</span></span>

<span data-ttu-id="087bc-104">Функция **жетфрамесркаддрессоффсет** возвращает смещение исходного адреса кадра.</span><span class="sxs-lookup"><span data-stu-id="087bc-104">The **GetFrameSrcAddressOffset** function returns the offset of the frame's source address.</span></span>

## <a name="syntax"></a><span data-ttu-id="087bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="087bc-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="087bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="087bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="087bc-107">*хфраме*</span><span class="sxs-lookup"><span data-stu-id="087bc-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="087bc-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="087bc-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="087bc-109">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="087bc-109">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="087bc-110">Тип исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="087bc-110">Source address type.</span></span> <span data-ttu-id="087bc-111">Значение параметра может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="087bc-111">The parameter value can be one of the following:</span></span>

-   <span data-ttu-id="087bc-112">\_тип адреса \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="087bc-112">ADDRESS\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="087bc-113">\_IP-адрес типа адреса \_</span><span class="sxs-lookup"><span data-stu-id="087bc-113">ADDRESS\_TYPE\_IP</span></span>
-   <span data-ttu-id="087bc-114">\_тип адреса \_ IPX</span><span class="sxs-lookup"><span data-stu-id="087bc-114">ADDRESS\_TYPE\_IPX</span></span>
-   <span data-ttu-id="087bc-115">\_тип адреса \_ токенринг</span><span class="sxs-lookup"><span data-stu-id="087bc-115">ADDRESS\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="087bc-116">\_тип адреса \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="087bc-116">ADDRESS\_TYPE\_FDDI</span></span>
-   <span data-ttu-id="087bc-117">\_тип адреса \_ КСНС</span><span class="sxs-lookup"><span data-stu-id="087bc-117">ADDRESS\_TYPE\_XNS</span></span>
-   <span data-ttu-id="087bc-118">тип адреса " \_ \_ IP-адрес Vines" \_</span><span class="sxs-lookup"><span data-stu-id="087bc-118">ADDRESS\_TYPE\_VINES\_IP</span></span>
-   <span data-ttu-id="087bc-119">\_тип адреса \_ ATM</span><span class="sxs-lookup"><span data-stu-id="087bc-119">ADDRESS\_TYPE\_ATM</span></span>

</dd> <dt>

<span data-ttu-id="087bc-120">*аддрессленгс*</span><span class="sxs-lookup"><span data-stu-id="087bc-120">*AddressLength*</span></span> 
</dt> <dd>

<span data-ttu-id="087bc-121">Указатель на возвращаемый **параметр типа DWORD** содержит длину адреса в байтах.</span><span class="sxs-lookup"><span data-stu-id="087bc-121">Pointer to a **DWORD**, which on return, contains the length of the address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="087bc-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="087bc-122">Return value</span></span>

<span data-ttu-id="087bc-123">Если функция выполнена успешно, возвращаемое значение является смещением к исходному адресу.</span><span class="sxs-lookup"><span data-stu-id="087bc-123">If the function is successful, the return value is the offset to the source address.</span></span>

<span data-ttu-id="087bc-124">Если функция завершилась неудачно, возвращаемое значение равно минус единице (-1).</span><span class="sxs-lookup"><span data-stu-id="087bc-124">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="requirements"></a><span data-ttu-id="087bc-125">Требования</span><span class="sxs-lookup"><span data-stu-id="087bc-125">Requirements</span></span>



| <span data-ttu-id="087bc-126">Требование</span><span class="sxs-lookup"><span data-stu-id="087bc-126">Requirement</span></span> | <span data-ttu-id="087bc-127">Значение</span><span class="sxs-lookup"><span data-stu-id="087bc-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="087bc-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="087bc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="087bc-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="087bc-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="087bc-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="087bc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="087bc-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="087bc-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="087bc-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="087bc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="087bc-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="087bc-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="087bc-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="087bc-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="087bc-135"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="087bc-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="087bc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="087bc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="087bc-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="087bc-137"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




