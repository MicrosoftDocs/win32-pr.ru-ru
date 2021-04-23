---
description: Освобождает блокировку, полученную с помощью Ексклусивелокк в общем режиме.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'Метод Кшарелоккнх:: Ексклусивеунлокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657832"
---
# <a name="csharelocknhexclusiveunlock-method"></a><span data-ttu-id="aa967-103">Метод Кшарелоккнх:: Ексклусивеунлокк</span><span class="sxs-lookup"><span data-stu-id="aa967-103">CShareLockNH::ExclusiveUnlock method</span></span>

<span data-ttu-id="aa967-104">Освобождает блокировку, полученную с помощью [**ексклусивелокк**](csharelocknh--exclusivelock.md) в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="aa967-104">Releases a lock acquired by using [**ExclusiveLock**](csharelocknh--exclusivelock.md) to shared mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa967-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa967-105">Syntax</span></span>


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a><span data-ttu-id="aa967-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aa967-106">Parameters</span></span>

<span data-ttu-id="aa967-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="aa967-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa967-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aa967-108">Return value</span></span>

<span data-ttu-id="aa967-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="aa967-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa967-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa967-110">Remarks</span></span>

<span data-ttu-id="aa967-111">Каждый вызов [**ексклусивелокк**](csharelocknh--exclusivelock.md) должен быть сопряжен с ровно одним вызовом **ексклусивеунлокк** , чтобы избежать риска взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="aa967-111">Each call to [**ExclusiveLock**](csharelocknh--exclusivelock.md) must be paired with exactly one call to **ExclusiveUnlock** to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="aa967-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="aa967-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa967-113">Требования</span><span class="sxs-lookup"><span data-stu-id="aa967-113">Requirements</span></span>



| <span data-ttu-id="aa967-114">Требование</span><span class="sxs-lookup"><span data-stu-id="aa967-114">Requirement</span></span> | <span data-ttu-id="aa967-115">Значение</span><span class="sxs-lookup"><span data-stu-id="aa967-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aa967-116">DLL</span><span class="sxs-lookup"><span data-stu-id="aa967-116">DLL</span></span><br/> | <dl> <span data-ttu-id="aa967-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa967-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa967-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa967-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa967-119">**ексклусивелокк**</span><span class="sxs-lookup"><span data-stu-id="aa967-119">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
