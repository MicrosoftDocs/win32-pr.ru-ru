---
description: Функция Компареаддрессес сравнивает два адреса, указывая, что один из адресов больше, меньше или равен другому адресу.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: Функция Компареаддрессес (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663642"
---
# <a name="compareaddresses-function"></a><span data-ttu-id="e1b9c-103">Функция Компареаддрессес</span><span class="sxs-lookup"><span data-stu-id="e1b9c-103">CompareAddresses function</span></span>

<span data-ttu-id="e1b9c-104">Функция **компареаддрессес** сравнивает два адреса, указывая, что один из адресов больше, меньше или равен другому адресу.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-104">The **CompareAddresses** function compares two addresses, indicating that one of the addresses is greater than, less than, or equal to the other address.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b9c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1b9c-105">Syntax</span></span>


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a><span data-ttu-id="e1b9c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1b9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b9c-107">*lpAddress1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1b9c-107">*lpAddress1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b9c-108">Указатель на первый адрес.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-108">Pointer to the first address.</span></span>

</dd> <dt>

<span data-ttu-id="e1b9c-109">*lpAddress2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e1b9c-109">*lpAddress2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b9c-110">Указатель на второй адрес.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-110">Pointer to the second address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b9c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e1b9c-111">Return value</span></span>

<span data-ttu-id="e1b9c-112">Если адреса совпадают, функция возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-112">If the addresses are the same, the function returns zero.</span></span>

<span data-ttu-id="e1b9c-113">Если параметр *lpAddress1* указывает адрес, который меньше, чем адрес, заданный параметром *lpAddress2* , возвращаемое значение является отрицательным числом.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-113">If the *lpAddress1* parameter specifies an address that is less than the address that the *lpAddress2* parameter specifies, the return value is a negative number.</span></span>

<span data-ttu-id="e1b9c-114">Если параметр *lpAddress1* указывает адрес, который больше, чем адрес, заданный параметром *lpAddress2* , возвращаемое значение является положительным числом.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-114">If the *lpAddress1* parameter specifies an address that is greater than the address that the *lpAddress2* parameter specifies, the return value is a positive number.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b9c-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1b9c-115">Remarks</span></span>

<span data-ttu-id="e1b9c-116">Адрес, который меньше другого адреса, указывает на предыдущий кадр.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-116">An address that is less than another address indicates a previous frame.</span></span> <span data-ttu-id="e1b9c-117">Адрес, который больше, чем другой адрес, обозначает более поздний кадр.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-117">An address that is greater than another address indicates a later frame.</span></span>

<span data-ttu-id="e1b9c-118">Сетевой монитор предоставляет две другие функции, [компарефрамедестаддресс](compareframedestaddress.md) и [компарефрамесаурцеаддресс](compareframesourceaddress.md), которые можно использовать для сравнения адресов.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-118">Network Monitor provides two other functions, [CompareFrameDestAddress](compareframedestaddress.md) and [CompareFrameSourceAddress](compareframesourceaddress.md), which you can use to compare addresses.</span></span> <span data-ttu-id="e1b9c-119">Функция **компарефрамедестаддресс** сравнивает заданный адрес с адресом назначения кадра, а функция **компарефрамесаурцеаддресс** сравнивает заданный адрес с исходным адресом кадра.</span><span class="sxs-lookup"><span data-stu-id="e1b9c-119">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareFrameSourceAddress** function compares a given address to the frame's source address.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b9c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e1b9c-120">Requirements</span></span>



| <span data-ttu-id="e1b9c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e1b9c-121">Requirement</span></span> | <span data-ttu-id="e1b9c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e1b9c-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b9c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e1b9c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b9c-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e1b9c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e1b9c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e1b9c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b9c-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e1b9c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e1b9c-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e1b9c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1b9c-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1b9c-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e1b9c-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e1b9c-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1b9c-130"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1b9c-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e1b9c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e1b9c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1b9c-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1b9c-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b9c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1b9c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b9c-134">компарефрамедестаддресс</span><span class="sxs-lookup"><span data-stu-id="e1b9c-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> <dt>

[<span data-ttu-id="e1b9c-135">компарефрамесаурцеаддресс</span><span class="sxs-lookup"><span data-stu-id="e1b9c-135">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




