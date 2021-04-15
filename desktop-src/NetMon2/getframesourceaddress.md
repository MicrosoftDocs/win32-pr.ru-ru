---
description: Извлекает исходный адрес кадра.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Функция Жетфрамесаурцеаддресс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682476"
---
# <a name="getframesourceaddress-function"></a><span data-ttu-id="f8a67-103">Функция Жетфрамесаурцеаддресс</span><span class="sxs-lookup"><span data-stu-id="f8a67-103">GetFrameSourceAddress function</span></span>

<span data-ttu-id="f8a67-104">Функция **жетфрамесаурцеаддресс** извлекает исходный адрес кадра.</span><span class="sxs-lookup"><span data-stu-id="f8a67-104">The **GetFrameSourceAddress** function retrieves the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a67-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8a67-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSourceAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="f8a67-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8a67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8a67-107">*хфраме*</span><span class="sxs-lookup"><span data-stu-id="f8a67-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="f8a67-108">Маркер для фрейма, для которого необходимо получить указатель.</span><span class="sxs-lookup"><span data-stu-id="f8a67-108">A handle to the frame for which to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="f8a67-109">*лпаддресс*</span><span class="sxs-lookup"><span data-stu-id="f8a67-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="f8a67-110">Буфер возврата, в котором хранится адрес источника фрейма.</span><span class="sxs-lookup"><span data-stu-id="f8a67-110">A return buffer that stores the frame source address.</span></span>

</dd> <dt>

<span data-ttu-id="f8a67-111">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="f8a67-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="f8a67-112">Тип адреса для поиска, например \_ тип адреса \_ Ethernet или \_ IP типа адреса \_ .</span><span class="sxs-lookup"><span data-stu-id="f8a67-112">The type of address searched for, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="f8a67-113">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="f8a67-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="f8a67-114">Флаги, используемые для изменения возвращенных данных адреса источника.</span><span class="sxs-lookup"><span data-stu-id="f8a67-114">The flags used to modify returned source address data.</span></span>



| <span data-ttu-id="f8a67-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a67-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="f8a67-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a67-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="f8a67-117"><dt>**\_Флаги ADDRESSTYPE \_ нормализация**</dt></span><span class="sxs-lookup"><span data-stu-id="f8a67-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="f8a67-118">Отменяет маршрутизацию и биты групп.</span><span class="sxs-lookup"><span data-stu-id="f8a67-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="f8a67-119"><dt>**\_биты флагов ADDRESSTYPE, \_ \_ обратные**</dt></span><span class="sxs-lookup"><span data-stu-id="f8a67-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="f8a67-120">Преобразует сетевые адреса Token Ring обратно в нормальное состояние.</span><span class="sxs-lookup"><span data-stu-id="f8a67-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8a67-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8a67-121">Return value</span></span>

<span data-ttu-id="f8a67-122">Если функция выполнена успешно, значение *лпаддресс* является допустимым, а возвращаемое значение — бхерр \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f8a67-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="f8a67-123">Если функция завершается неудачно, возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="f8a67-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="f8a67-124">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f8a67-124">Return code</span></span>                                                                                                | <span data-ttu-id="f8a67-125">Описание</span><span class="sxs-lookup"><span data-stu-id="f8a67-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8a67-126"><dt>**\_протокол бхерр \_ не \_ найден**</dt></span><span class="sxs-lookup"><span data-stu-id="f8a67-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="f8a67-127">Протокол, указанный параметром *addressType* , недопустим для кадра.</span><span class="sxs-lookup"><span data-stu-id="f8a67-127">The protocol specified by the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="f8a67-128"><dt>**БХЕРР \_ недопустимое \_ хфраме**</dt></span><span class="sxs-lookup"><span data-stu-id="f8a67-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="f8a67-129">Значение параметра *хфраме* недопустимо.</span><span class="sxs-lookup"><span data-stu-id="f8a67-129">The *hFrame* parameter value is invalid.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="f8a67-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8a67-130">Remarks</span></span>

<span data-ttu-id="f8a67-131">Допускается тип адреса **типа адреса \_ " \_ найти \_ наибольший** ".</span><span class="sxs-lookup"><span data-stu-id="f8a67-131">An address type of **ADDRESS\_TYPE\_FIND\_HIGHEST** is allowed.</span></span> <span data-ttu-id="f8a67-132">При использовании этого типа адреса функция ищет IP-адрес IPX, КСНС, IP или VINEs перед возвратом адреса ETHERNET, ТОКЕНРИНГ или FDDI.</span><span class="sxs-lookup"><span data-stu-id="f8a67-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="f8a67-133">Этот подход удобен для протоколов и сред, в которых две сетевые карты могут быть мультиплексированы по одному адресу сервера.</span><span class="sxs-lookup"><span data-stu-id="f8a67-133">This approach is useful for protocols and environments in which two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a67-134">Требования</span><span class="sxs-lookup"><span data-stu-id="f8a67-134">Requirements</span></span>



| <span data-ttu-id="f8a67-135">Требование</span><span class="sxs-lookup"><span data-stu-id="f8a67-135">Requirement</span></span> | <span data-ttu-id="f8a67-136">Значение</span><span class="sxs-lookup"><span data-stu-id="f8a67-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a67-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8a67-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a67-138">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f8a67-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f8a67-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8a67-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a67-140">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f8a67-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f8a67-141">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f8a67-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a67-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a67-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f8a67-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f8a67-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8a67-144"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8a67-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f8a67-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f8a67-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8a67-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8a67-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




