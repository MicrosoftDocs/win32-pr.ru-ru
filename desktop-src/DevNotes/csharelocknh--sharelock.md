---
description: Получает общую блокировку.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'Метод Кшарелоккнх:: Шарелокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648660"
---
# <a name="csharelocknhsharelock-method"></a><span data-ttu-id="3d904-103">Метод Кшарелоккнх:: Шарелокк</span><span class="sxs-lookup"><span data-stu-id="3d904-103">CShareLockNH::ShareLock method</span></span>

<span data-ttu-id="3d904-104">Получает общую блокировку.</span><span class="sxs-lookup"><span data-stu-id="3d904-104">Obtains a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d904-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d904-105">Syntax</span></span>


```C++
void ShareLock();
```



## <a name="parameters"></a><span data-ttu-id="3d904-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d904-106">Parameters</span></span>

<span data-ttu-id="3d904-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3d904-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d904-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d904-108">Return value</span></span>

<span data-ttu-id="3d904-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3d904-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d904-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d904-110">Remarks</span></span>

<span data-ttu-id="3d904-111">Каждый вызов **шарелокк** должен быть сопряжен с ровно одним вызовом [**шареунлокк**](csharelocknh--shareunlock.md).</span><span class="sxs-lookup"><span data-stu-id="3d904-111">Each call to **ShareLock** must be paired with exactly one call to [**ShareUnlock**](csharelocknh--shareunlock.md).</span></span> <span data-ttu-id="3d904-112">Только поток, который успешно вызывает **шарелокк** , может вызвать **шареунлокк**; в противном случае может возникнуть взаимоблокировка.</span><span class="sxs-lookup"><span data-stu-id="3d904-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="3d904-113">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3d904-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d904-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3d904-114">Requirements</span></span>



| <span data-ttu-id="3d904-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3d904-115">Requirement</span></span> | <span data-ttu-id="3d904-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3d904-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3d904-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3d904-117">DLL</span></span><br/> | <dl> <span data-ttu-id="3d904-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d904-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d904-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d904-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d904-120">**шареунлокк**</span><span class="sxs-lookup"><span data-stu-id="3d904-120">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
