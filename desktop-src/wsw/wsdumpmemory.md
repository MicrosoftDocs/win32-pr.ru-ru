---
title: Функция Всдумпмемори (Вебсервицесдебуг. h)
description: Эта функция создает дамп всех выделений памяти для консоли.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Веб-службы Всдумпмемори Function для Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989129"
---
# <a name="wsdumpmemory-function"></a><span data-ttu-id="78c7d-104">Функция Всдумпмемори</span><span class="sxs-lookup"><span data-stu-id="78c7d-104">WsDumpMemory function</span></span>

<span data-ttu-id="78c7d-105">Эта функция создает дамп всех выделений памяти для консоли.</span><span class="sxs-lookup"><span data-stu-id="78c7d-105">This function dumps all memory allocations to the console.</span></span>

> [!Note]  
> <span data-ttu-id="78c7d-106">Эта функция предназначена только для отладки.</span><span class="sxs-lookup"><span data-stu-id="78c7d-106">This function is for DEBUG ONLY.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="78c7d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78c7d-107">Syntax</span></span>


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="78c7d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="78c7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c7d-109">*Ошибка при* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="78c7d-109">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="78c7d-110">Указатель на объект [ \_ ошибки WS](ws-error.md) , в котором необходимо сохранить дополнительные сведения об ошибке в случае сбоя функции.</span><span class="sxs-lookup"><span data-stu-id="78c7d-110">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78c7d-111">Return value</span></span>

<span data-ttu-id="78c7d-112">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="78c7d-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78c7d-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="78c7d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="78c7d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="78c7d-114">Requirements</span></span>



| <span data-ttu-id="78c7d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="78c7d-115">Requirement</span></span> | <span data-ttu-id="78c7d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="78c7d-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78c7d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78c7d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="78c7d-118">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="78c7d-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                             |
| <span data-ttu-id="78c7d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78c7d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="78c7d-120">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="78c7d-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="78c7d-121">Header</span><span class="sxs-lookup"><span data-stu-id="78c7d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="78c7d-122"><dt>Вебсервицесдебуг. h</dt></span><span class="sxs-lookup"><span data-stu-id="78c7d-122"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





