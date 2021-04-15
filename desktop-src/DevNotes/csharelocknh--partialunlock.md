---
description: Освобождает частичную блокировку, так что теперь можно вводить другие монопольные или частичные блокировки.
ms.assetid: 95a3e0d1-4e8b-4e30-b4fd-709b9db465de
title: 'Кшарелоккнх: метод:P Артиалунлокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 930c0f51e199c1668a70f2dd017b0280939b0710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648662"
---
# <a name="csharelocknhpartialunlock-method"></a><span data-ttu-id="2b6a2-103">Кшарелоккнх: метод:P Артиалунлокк</span><span class="sxs-lookup"><span data-stu-id="2b6a2-103">CShareLockNH::PartialUnlock method</span></span>

<span data-ttu-id="2b6a2-104">Освобождает частичную блокировку, так что теперь можно вводить другие монопольные или частичные блокировки.</span><span class="sxs-lookup"><span data-stu-id="2b6a2-104">Releases a partial lock so that other exclusive or partial lock acquirers can now enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6a2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b6a2-105">Syntax</span></span>


```C++
void PartialUnlock();
```



## <a name="parameters"></a><span data-ttu-id="2b6a2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b6a2-106">Parameters</span></span>

<span data-ttu-id="2b6a2-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2b6a2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b6a2-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b6a2-108">Return value</span></span>

<span data-ttu-id="2b6a2-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2b6a2-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b6a2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b6a2-110">Remarks</span></span>

<span data-ttu-id="2b6a2-111">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2b6a2-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b6a2-112">Требования</span><span class="sxs-lookup"><span data-stu-id="2b6a2-112">Requirements</span></span>



| <span data-ttu-id="2b6a2-113">Требование</span><span class="sxs-lookup"><span data-stu-id="2b6a2-113">Requirement</span></span> | <span data-ttu-id="2b6a2-114">Значение</span><span class="sxs-lookup"><span data-stu-id="2b6a2-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6a2-115">DLL</span><span class="sxs-lookup"><span data-stu-id="2b6a2-115">DLL</span></span><br/> | <dl> <span data-ttu-id="2b6a2-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b6a2-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
