---
description: Получает блокировку потоков чтения/записи.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'Метод Кшарелоккнх:: Ексклусивелокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657833"
---
# <a name="csharelocknhexclusivelock-method"></a><span data-ttu-id="54cdb-103">Метод Кшарелоккнх:: Ексклусивелокк</span><span class="sxs-lookup"><span data-stu-id="54cdb-103">CShareLockNH::ExclusiveLock method</span></span>

<span data-ttu-id="54cdb-104">Получает блокировку потоков чтения/записи.</span><span class="sxs-lookup"><span data-stu-id="54cdb-104">Acquires a reader/writer lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="54cdb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54cdb-105">Syntax</span></span>


```C++
void ExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="54cdb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="54cdb-106">Parameters</span></span>

<span data-ttu-id="54cdb-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="54cdb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54cdb-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54cdb-108">Return value</span></span>

<span data-ttu-id="54cdb-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="54cdb-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54cdb-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54cdb-110">Remarks</span></span>

<span data-ttu-id="54cdb-111">Каждый вызов **ексклусивелокк** должен быть сопряжен с ровно одним вызовом [**ексклусивеунлокк**](csharelocknh--exclusiveunlock.md) , чтобы избежать риска взаимоблокировки.</span><span class="sxs-lookup"><span data-stu-id="54cdb-111">Each call to **ExclusiveLock** must be paired with exactly one call to [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="54cdb-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="54cdb-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="54cdb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="54cdb-113">Requirements</span></span>



| <span data-ttu-id="54cdb-114">Требование</span><span class="sxs-lookup"><span data-stu-id="54cdb-114">Requirement</span></span> | <span data-ttu-id="54cdb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="54cdb-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="54cdb-116">DLL</span><span class="sxs-lookup"><span data-stu-id="54cdb-116">DLL</span></span><br/> | <dl> <span data-ttu-id="54cdb-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54cdb-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54cdb-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54cdb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54cdb-119">**ексклусивеунлокк**</span><span class="sxs-lookup"><span data-stu-id="54cdb-119">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
