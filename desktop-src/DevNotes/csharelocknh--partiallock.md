---
description: Предотвращает получение блокировки более чем одним потоком.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: 'Кшарелоккнх: метод:P Артиаллокк'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 0b7b7d55c9fd8d979aa14f12939df922e7a89099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657209"
---
# <a name="csharelocknhpartiallock-method"></a><span data-ttu-id="5696a-103">Кшарелоккнх: метод:P Артиаллокк</span><span class="sxs-lookup"><span data-stu-id="5696a-103">CShareLockNH::PartialLock method</span></span>

<span data-ttu-id="5696a-104">Предотвращает получение блокировки более чем одним потоком.</span><span class="sxs-lookup"><span data-stu-id="5696a-104">Prevents more than one thread from completing acquiring a lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="5696a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5696a-105">Syntax</span></span>


```C++
void PartialLock();
```



## <a name="parameters"></a><span data-ttu-id="5696a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5696a-106">Parameters</span></span>

<span data-ttu-id="5696a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="5696a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5696a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5696a-108">Return value</span></span>

<span data-ttu-id="5696a-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5696a-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5696a-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5696a-110">Remarks</span></span>

<span data-ttu-id="5696a-111">Хотя **партиаллокк** действует, другие потоки, вызывающие [**шарелокк**](csharelocknh--sharelock.md) , могут войти в блокировку.</span><span class="sxs-lookup"><span data-stu-id="5696a-111">While **PartialLock** is in effect, other threads calling [**ShareLock**](csharelocknh--sharelock.md) can enter the lock.</span></span>

<span data-ttu-id="5696a-112">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="5696a-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5696a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5696a-113">Requirements</span></span>



| <span data-ttu-id="5696a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5696a-114">Requirement</span></span> | <span data-ttu-id="5696a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5696a-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5696a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5696a-116">DLL</span></span><br/> | <dl> <span data-ttu-id="5696a-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5696a-117"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
