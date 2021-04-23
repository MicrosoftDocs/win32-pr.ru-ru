---
description: Получает монопольную блокировку, если на данный момент она не удерживается другими.
ms.assetid: d655b89c-f2c8-4965-a21b-f539b1598296
title: 'Метод Кшарелоккнх:: Трексклусивелокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.TryExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8465e247807c4229821acef552e0786a5604a3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648659"
---
# <a name="csharelocknhtryexclusivelock-method"></a><span data-ttu-id="9eeee-103">Метод Кшарелоккнх:: Трексклусивелокк</span><span class="sxs-lookup"><span data-stu-id="9eeee-103">CShareLockNH::TryExclusiveLock method</span></span>

<span data-ttu-id="9eeee-104">Получает монопольную блокировку, если на данный момент она не удерживается другими.</span><span class="sxs-lookup"><span data-stu-id="9eeee-104">Obtains a lock exclusively if no others are currently hold it.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eeee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9eeee-105">Syntax</span></span>


```C++
BOOL TryExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="9eeee-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9eeee-106">Parameters</span></span>

<span data-ttu-id="9eeee-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9eeee-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9eeee-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9eeee-108">Return value</span></span>

<span data-ttu-id="9eeee-109">Возвращает **значение true** , если функция выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="9eeee-109">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eeee-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9eeee-110">Remarks</span></span>

<span data-ttu-id="9eeee-111">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9eeee-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eeee-112">Требования</span><span class="sxs-lookup"><span data-stu-id="9eeee-112">Requirements</span></span>



| <span data-ttu-id="9eeee-113">Требование</span><span class="sxs-lookup"><span data-stu-id="9eeee-113">Requirement</span></span> | <span data-ttu-id="9eeee-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9eeee-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9eeee-115">DLL</span><span class="sxs-lookup"><span data-stu-id="9eeee-115">DLL</span></span><br/> | <dl> <span data-ttu-id="9eeee-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eeee-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
