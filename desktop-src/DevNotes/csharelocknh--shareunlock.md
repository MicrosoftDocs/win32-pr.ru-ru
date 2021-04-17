---
description: Освобождает общую блокировку.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'Метод Кшарелоккнх:: Шареунлокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657205"
---
# <a name="csharelocknhshareunlock-method"></a><span data-ttu-id="4d968-103">Метод Кшарелоккнх:: Шареунлокк</span><span class="sxs-lookup"><span data-stu-id="4d968-103">CShareLockNH::ShareUnlock method</span></span>

<span data-ttu-id="4d968-104">Освобождает общую блокировку.</span><span class="sxs-lookup"><span data-stu-id="4d968-104">Releases a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d968-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d968-105">Syntax</span></span>


```C++
void ShareUnlock();
```



## <a name="parameters"></a><span data-ttu-id="4d968-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d968-106">Parameters</span></span>

<span data-ttu-id="4d968-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4d968-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d968-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d968-108">Return value</span></span>

<span data-ttu-id="4d968-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4d968-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d968-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d968-110">Remarks</span></span>

<span data-ttu-id="4d968-111">Каждый вызов [**шарелокк**](csharelocknh--sharelock.md) должен быть сопряжен с ровно одним вызовом **шареунлокк**.</span><span class="sxs-lookup"><span data-stu-id="4d968-111">Each call to [**ShareLock**](csharelocknh--sharelock.md) must be paired with exactly one call to **ShareUnlock**.</span></span> <span data-ttu-id="4d968-112">Только поток, который успешно вызывает **шарелокк** , может вызвать **шареунлокк**; в противном случае может возникнуть взаимоблокировка.</span><span class="sxs-lookup"><span data-stu-id="4d968-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="4d968-113">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4d968-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d968-114">Требования</span><span class="sxs-lookup"><span data-stu-id="4d968-114">Requirements</span></span>



| <span data-ttu-id="4d968-115">Требование</span><span class="sxs-lookup"><span data-stu-id="4d968-115">Requirement</span></span> | <span data-ttu-id="4d968-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4d968-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4d968-117">DLL</span><span class="sxs-lookup"><span data-stu-id="4d968-117">DLL</span></span><br/> | <dl> <span data-ttu-id="4d968-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d968-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d968-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d968-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d968-120">**шарелокк**</span><span class="sxs-lookup"><span data-stu-id="4d968-120">**ShareLock**</span></span>](csharelocknh--sharelock.md)
</dt> </dl>

 

 
