---
description: Функция Компарефрамедестаддресс сравнивает адрес с адресом назначения кадра.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: Функция Компарефрамедестаддресс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909415"
---
# <a name="compareframedestaddress-function"></a><span data-ttu-id="be4b5-103">Функция Компарефрамедестаддресс</span><span class="sxs-lookup"><span data-stu-id="be4b5-103">CompareFrameDestAddress function</span></span>

<span data-ttu-id="be4b5-104">Функция **компарефрамедестаддресс** сравнивает адрес с адресом назначения кадра.</span><span class="sxs-lookup"><span data-stu-id="be4b5-104">The **CompareFrameDestAddress** function compares an address to the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="be4b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be4b5-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="be4b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be4b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be4b5-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be4b5-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be4b5-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="be4b5-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="be4b5-109">*лпаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be4b5-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be4b5-110">Указатель на адрес.</span><span class="sxs-lookup"><span data-stu-id="be4b5-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be4b5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be4b5-111">Return value</span></span>

<span data-ttu-id="be4b5-112">Если адреса совпадают, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="be4b5-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="be4b5-113">Если адреса не совпадают, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="be4b5-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="be4b5-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be4b5-114">Remarks</span></span>

<span data-ttu-id="be4b5-115">Чтобы функция **компарефрамедестаддресс** успешно возвращалась, тип адреса назначения должен совпадать с типом адреса, указанным в параметре *лпаддресс* .</span><span class="sxs-lookup"><span data-stu-id="be4b5-115">For the **CompareFrameDestAddress** function to return successfully, the destination address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="be4b5-116">Сетевой монитор предоставляет две другие функции, [компарефрамесаурцеаддресс](compareframesourceaddress.md) и [компареаддрессес](compareaddresses.md), которые можно использовать для сравнения адресов.</span><span class="sxs-lookup"><span data-stu-id="be4b5-116">Network Monitor provides two other functions, [CompareFrameSourceAddress](compareframesourceaddress.md) and [CompareAddresses](compareaddresses.md), which you can use to compare addresses.</span></span> <span data-ttu-id="be4b5-117">Функция **компарефрамесаурцеаддресс** сравнивает заданный адрес с исходным адресом кадра, а функция **компареаддресс** сравнивает два заданных адреса.</span><span class="sxs-lookup"><span data-stu-id="be4b5-117">The **CompareFrameSourceAddress** function compares a given address to the frame's source address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="be4b5-118">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **компарефрамедестаддресс** .</span><span class="sxs-lookup"><span data-stu-id="be4b5-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameDestAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="be4b5-119">Требования</span><span class="sxs-lookup"><span data-stu-id="be4b5-119">Requirements</span></span>



| <span data-ttu-id="be4b5-120">Требование</span><span class="sxs-lookup"><span data-stu-id="be4b5-120">Requirement</span></span> | <span data-ttu-id="be4b5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="be4b5-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="be4b5-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be4b5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="be4b5-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be4b5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="be4b5-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be4b5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="be4b5-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be4b5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="be4b5-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="be4b5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="be4b5-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="be4b5-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="be4b5-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="be4b5-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="be4b5-129"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be4b5-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="be4b5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="be4b5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be4b5-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be4b5-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be4b5-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be4b5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be4b5-133">компареаддрессес</span><span class="sxs-lookup"><span data-stu-id="be4b5-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="be4b5-134">компарефрамесаурцеаддресс</span><span class="sxs-lookup"><span data-stu-id="be4b5-134">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




