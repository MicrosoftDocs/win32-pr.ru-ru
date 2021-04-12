---
description: Функция Компарефрамесаурцеаддресс сравнивает адрес с исходным адресом кадра.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Функция Компарефрамесаурцеаддресс (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265818"
---
# <a name="compareframesourceaddress-function"></a><span data-ttu-id="d9636-103">Функция Компарефрамесаурцеаддресс</span><span class="sxs-lookup"><span data-stu-id="d9636-103">CompareFrameSourceAddress function</span></span>

<span data-ttu-id="d9636-104">Функция **компарефрамесаурцеаддресс** сравнивает адрес с исходным адресом кадра.</span><span class="sxs-lookup"><span data-stu-id="d9636-104">The **CompareFrameSourceAddress** function compares an address to the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9636-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9636-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="d9636-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9636-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9636-107">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9636-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9636-108">Обработчик для фрейма.</span><span class="sxs-lookup"><span data-stu-id="d9636-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="d9636-109">*лпаддресс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d9636-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9636-110">Указатель на адрес.</span><span class="sxs-lookup"><span data-stu-id="d9636-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9636-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9636-111">Return value</span></span>

<span data-ttu-id="d9636-112">Если адреса совпадают, возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="d9636-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="d9636-113">Если адреса не совпадают, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="d9636-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9636-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9636-114">Remarks</span></span>

<span data-ttu-id="d9636-115">Чтобы функция **компарефрамесаурцеаддресс** была выполнена, тип адреса источника должен совпадать с типом адреса, указанным в параметре *лпаддресс* .</span><span class="sxs-lookup"><span data-stu-id="d9636-115">For the **CompareFrameSourceAddress** function to succeed, the source address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="d9636-116">Сетевой монитор предоставляет две другие функции для сравнения адресов: [компарефрамедестаддресс](compareframedestaddress.md) и [компареаддрессес](compareaddresses.md).</span><span class="sxs-lookup"><span data-stu-id="d9636-116">Network Monitor provides two other functions for comparing addresses: [CompareFrameDestAddress](compareframedestaddress.md) and [CompareAddresses](compareaddresses.md).</span></span> <span data-ttu-id="d9636-117">Функция **компарефрамедестаддресс** сравнивает заданный адрес с адресом назначения кадра, а функция **компареаддресс** сравнивает два заданных адреса.</span><span class="sxs-lookup"><span data-stu-id="d9636-117">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="d9636-118">[*Эксперты*](e.md) и [*средства синтаксического анализа*](p.md) могут вызывать функцию **компарефрамесаурцеаддресс** .</span><span class="sxs-lookup"><span data-stu-id="d9636-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameSourceAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9636-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d9636-119">Requirements</span></span>



| <span data-ttu-id="d9636-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d9636-120">Requirement</span></span> | <span data-ttu-id="d9636-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d9636-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d9636-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9636-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d9636-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9636-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d9636-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9636-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d9636-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d9636-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d9636-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d9636-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9636-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9636-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d9636-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d9636-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d9636-129"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9636-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d9636-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d9636-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9636-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9636-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9636-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9636-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9636-133">компареаддрессес</span><span class="sxs-lookup"><span data-stu-id="d9636-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="d9636-134">компарефрамедестаддресс</span><span class="sxs-lookup"><span data-stu-id="d9636-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> </dl>

 

 




