---
description: Функция Жетфрамедстаддрессоффсет возвращает смещение к адресу назначения данного кадра.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Функция Жетфрамедстаддрессоффсет (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673187"
---
# <a name="getframedstaddressoffset-function"></a><span data-ttu-id="802a0-103">Функция Жетфрамедстаддрессоффсет</span><span class="sxs-lookup"><span data-stu-id="802a0-103">GetFrameDstAddressOffset function</span></span>

<span data-ttu-id="802a0-104">Функция **жетфрамедстаддрессоффсет** возвращает смещение к адресу назначения данного кадра.</span><span class="sxs-lookup"><span data-stu-id="802a0-104">The **GetFrameDstAddressOffset** function returns the offset to the destination address of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="802a0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="802a0-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="802a0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="802a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="802a0-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="802a0-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="802a0-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="802a0-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="802a0-109">*AddressType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="802a0-109">*AddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="802a0-110">Тип адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="802a0-110">Type of the destination address.</span></span> <span data-ttu-id="802a0-111">Укажите одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="802a0-111">Specify one of the following values:</span></span>

<span data-ttu-id="802a0-112">\_тип адреса \_ Ethernet адрес \_ тип \_ IP-адреса тип \_ \_ IPX адрес тип \_ \_ токенринг адрес тип \_ \_ FDDI адрес \_ тип \_ КСНС адрес тип адреса \_ \_ Vine \_ IP address \_ Type \_ ATM.</span><span class="sxs-lookup"><span data-stu-id="802a0-112">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_IP ADDRESS\_TYPE\_IPX ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI ADDRESS\_TYPE\_XNS ADDRESS\_TYPE\_VINES\_IP ADDRESS\_TYPE\_ATM.</span></span>

</dd> <dt>

<span data-ttu-id="802a0-113">*Аддрессленгс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="802a0-113">*AddressLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="802a0-114">Длина адреса назначения в байтах.</span><span class="sxs-lookup"><span data-stu-id="802a0-114">Length of the destination address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="802a0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="802a0-115">Return value</span></span>

<span data-ttu-id="802a0-116">Если функция выполнена успешно, возвращается значение смещения (измеряется в байтах) с запрошенным типом адреса.</span><span class="sxs-lookup"><span data-stu-id="802a0-116">If the function is successful, the return value is the offset (measured in bytes) to the requested address type.</span></span>

<span data-ttu-id="802a0-117">Если функция завершилась неудачно, возвращаемое значение равно минус единице (-1).</span><span class="sxs-lookup"><span data-stu-id="802a0-117">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="802a0-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="802a0-118">Remarks</span></span>

<span data-ttu-id="802a0-119">Если параметру *addressType* присвоено \_ \_ значение Ethernet, возвращаемое функция **жетфрамедстаддрессоффсет** всегда равно нулю.</span><span class="sxs-lookup"><span data-stu-id="802a0-119">If the *AddressType* parameter is set to ADDRESS\_TYPE\_ETHERNET, the return value of the **GetFrameDstAddressOffset** function is always zero.</span></span> <span data-ttu-id="802a0-120">Смещение адреса Ethernet всегда равно нулю.</span><span class="sxs-lookup"><span data-stu-id="802a0-120">The offset of an Ethernet address is always zero.</span></span>

<span data-ttu-id="802a0-121">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **жетфрамедстаддрессоффсет** .</span><span class="sxs-lookup"><span data-stu-id="802a0-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameDstAddressOffset** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="802a0-122">Требования</span><span class="sxs-lookup"><span data-stu-id="802a0-122">Requirements</span></span>



| <span data-ttu-id="802a0-123">Требование</span><span class="sxs-lookup"><span data-stu-id="802a0-123">Requirement</span></span> | <span data-ttu-id="802a0-124">Значение</span><span class="sxs-lookup"><span data-stu-id="802a0-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="802a0-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="802a0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="802a0-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="802a0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="802a0-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="802a0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="802a0-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="802a0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="802a0-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="802a0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="802a0-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="802a0-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="802a0-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="802a0-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="802a0-132"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="802a0-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="802a0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="802a0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="802a0-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="802a0-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




