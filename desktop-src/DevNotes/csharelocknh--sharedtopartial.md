---
description: Изменяет общую блокировку на частичную блокировку.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'Метод Кшарелоккнх:: Шаредтопартиал'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657206"
---
# <a name="csharelocknhsharedtopartial-method"></a><span data-ttu-id="3cb14-103">Метод Кшарелоккнх:: Шаредтопартиал</span><span class="sxs-lookup"><span data-stu-id="3cb14-103">CShareLockNH::SharedToPartial method</span></span>

<span data-ttu-id="3cb14-104">Изменяет общую блокировку на частичную блокировку.</span><span class="sxs-lookup"><span data-stu-id="3cb14-104">Changes a shared lock to a partial lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb14-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cb14-105">Syntax</span></span>


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a><span data-ttu-id="3cb14-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cb14-106">Parameters</span></span>

<span data-ttu-id="3cb14-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3cb14-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3cb14-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3cb14-108">Return value</span></span>

<span data-ttu-id="3cb14-109">Возвращает **значение true** , если получена частичная блокировка. в противном случае возвращается **значение false** , и блокировка остается в общем режиме.</span><span class="sxs-lookup"><span data-stu-id="3cb14-109">Returns **TRUE** if the partial lock is obtained; otherwise, it returns **FALSE** and the lock remains in shared mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb14-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3cb14-110">Remarks</span></span>

<span data-ttu-id="3cb14-111">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="3cb14-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb14-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3cb14-112">Requirements</span></span>



| <span data-ttu-id="3cb14-113">Требование</span><span class="sxs-lookup"><span data-stu-id="3cb14-113">Requirement</span></span> | <span data-ttu-id="3cb14-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3cb14-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb14-115">DLL</span><span class="sxs-lookup"><span data-stu-id="3cb14-115">DLL</span></span><br/> | <dl> <span data-ttu-id="3cb14-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cb14-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
