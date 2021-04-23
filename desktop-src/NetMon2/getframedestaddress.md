---
description: Извлекает адрес назначения кадра.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: Функция Жетфрамедестаддресс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990908"
---
# <a name="getframedestaddress-function"></a><span data-ttu-id="a2abd-103">Функция Жетфрамедестаддресс</span><span class="sxs-lookup"><span data-stu-id="a2abd-103">GetFrameDestAddress function</span></span>

<span data-ttu-id="a2abd-104">Функция **жетфрамедестаддресс** извлекает адрес назначения кадра.</span><span class="sxs-lookup"><span data-stu-id="a2abd-104">The **GetFrameDestAddress** function retrieves the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2abd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2abd-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDestAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="a2abd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2abd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2abd-107">*хфраме*</span><span class="sxs-lookup"><span data-stu-id="a2abd-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="a2abd-108">Маркер кадра, на который необходимо получить указатель.</span><span class="sxs-lookup"><span data-stu-id="a2abd-108">A handle of the frame to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="a2abd-109">*лпаддресс*</span><span class="sxs-lookup"><span data-stu-id="a2abd-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="a2abd-110">Буфер возврата, в котором хранится адрес назначения фрейма.</span><span class="sxs-lookup"><span data-stu-id="a2abd-110">A return buffer that stores the frame destination address.</span></span>

</dd> <dt>

<span data-ttu-id="a2abd-111">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="a2abd-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="a2abd-112">Тип адреса, например \_ тип адреса \_ Ethernet или \_ IP типа адреса \_ .</span><span class="sxs-lookup"><span data-stu-id="a2abd-112">A type of address, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="a2abd-113">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="a2abd-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="a2abd-114">Флаги, используемые для изменения возвращенных данных адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="a2abd-114">The flags used to modify returned destination address data.</span></span>



| <span data-ttu-id="a2abd-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a2abd-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="a2abd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a2abd-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="a2abd-117"><dt>**\_Флаги ADDRESSTYPE \_ нормализация**</dt></span><span class="sxs-lookup"><span data-stu-id="a2abd-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="a2abd-118">Отменяет маршрутизацию и биты групп.</span><span class="sxs-lookup"><span data-stu-id="a2abd-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="a2abd-119"><dt>**\_биты флагов ADDRESSTYPE, \_ \_ обратные**</dt></span><span class="sxs-lookup"><span data-stu-id="a2abd-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="a2abd-120">Преобразует сетевые адреса Token Ring обратно в нормальное состояние.</span><span class="sxs-lookup"><span data-stu-id="a2abd-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2abd-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2abd-121">Return value</span></span>

<span data-ttu-id="a2abd-122">Если функция выполнена успешно, значение *лпаддресс* является допустимым, а возвращаемое значение — бхерр \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a2abd-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="a2abd-123">Если функция завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="a2abd-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="a2abd-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a2abd-124">Return code</span></span>                                                                                                | <span data-ttu-id="a2abd-125">Описание</span><span class="sxs-lookup"><span data-stu-id="a2abd-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2abd-126"><dt>**\_протокол бхерр \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="a2abd-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="a2abd-127">Указанный протокол в параметре *addressType* недопустим для кадра.</span><span class="sxs-lookup"><span data-stu-id="a2abd-127">The specified protocol in the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="a2abd-128"><dt>**БХЕРР \_ недопустимое \_ хфраме**</dt></span><span class="sxs-lookup"><span data-stu-id="a2abd-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="a2abd-129">Недопустимое значение *хфраме* .</span><span class="sxs-lookup"><span data-stu-id="a2abd-129">The *hFrame* value is invalid.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="a2abd-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2abd-130">Remarks</span></span>

<span data-ttu-id="a2abd-131">Допустимый тип адреса — " **\_ \_ Поиск \_ наибольшего** адреса".</span><span class="sxs-lookup"><span data-stu-id="a2abd-131">The **ADDRESS\_TYPE\_FIND\_HIGHEST** address type is allowed.</span></span> <span data-ttu-id="a2abd-132">При использовании этого типа адреса функция ищет IP-адрес IPX, КСНС, IP или VINEs перед возвратом адреса ETHERNET, ТОКЕНРИНГ или FDDI.</span><span class="sxs-lookup"><span data-stu-id="a2abd-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="a2abd-133">Этот подход полезен для протоколов и в средах, где два сетевых адаптера могут быть мультиплексированы по одному адресу сервера.</span><span class="sxs-lookup"><span data-stu-id="a2abd-133">This approach is useful for protocols and in environments where two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2abd-134">Требования</span><span class="sxs-lookup"><span data-stu-id="a2abd-134">Requirements</span></span>



| <span data-ttu-id="a2abd-135">Требование</span><span class="sxs-lookup"><span data-stu-id="a2abd-135">Requirement</span></span> | <span data-ttu-id="a2abd-136">Значение</span><span class="sxs-lookup"><span data-stu-id="a2abd-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a2abd-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2abd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a2abd-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2abd-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a2abd-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2abd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a2abd-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a2abd-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a2abd-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a2abd-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2abd-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2abd-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a2abd-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a2abd-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2abd-144"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2abd-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a2abd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a2abd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2abd-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2abd-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




