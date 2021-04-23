---
description: Инициализирует библиотеку AUX \_ клиб.
ms.assetid: 516bb359-d3a3-415b-90af-09e544366a12
title: Функция Ауксклибинитиализе (AUX \_ клиб. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibInitialize
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: d16ea418d2012b24ce19ad14afab12e198e7ab2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649018"
---
# <a name="auxklibinitialize-function"></a><span data-ttu-id="73a31-103">Функция Ауксклибинитиализе</span><span class="sxs-lookup"><span data-stu-id="73a31-103">AuxKlibInitialize function</span></span>

<span data-ttu-id="73a31-104">Инициализирует библиотеку AUX \_ клиб.</span><span class="sxs-lookup"><span data-stu-id="73a31-104">Initializes the Aux\_klib library.</span></span> <span data-ttu-id="73a31-105">Эта функция должна вызываться до вызова любой другой функции в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="73a31-105">This function must be called before any other function in the library can be called.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a31-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73a31-106">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="73a31-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="73a31-107">Parameters</span></span>

<span data-ttu-id="73a31-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="73a31-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73a31-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73a31-109">Return value</span></span>

<span data-ttu-id="73a31-110">Если функция завершается успешно, возвращается значение STATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="73a31-110">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="73a31-111">Если функция завершается ошибкой, возвращаемое значение может быть одним из кодов состояния, определенных в файле Ntstatus. h, который доступен в WDK.</span><span class="sxs-lookup"><span data-stu-id="73a31-111">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="73a31-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73a31-112">Remarks</span></span>

<span data-ttu-id="73a31-113">Библиотеку объектов, реализующих этот API, можно скачать [отсюда](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="73a31-113">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="73a31-114">Требования</span><span class="sxs-lookup"><span data-stu-id="73a31-114">Requirements</span></span>



| <span data-ttu-id="73a31-115">Требование</span><span class="sxs-lookup"><span data-stu-id="73a31-115">Requirement</span></span> | <span data-ttu-id="73a31-116">Значение</span><span class="sxs-lookup"><span data-stu-id="73a31-116">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73a31-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="73a31-117">Redistributable</span></span><br/> | <span data-ttu-id="73a31-118">Библиотека вспомогательных API Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="73a31-118">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="73a31-119">Header</span><span class="sxs-lookup"><span data-stu-id="73a31-119">Header</span></span><br/>          | <dl> <span data-ttu-id="73a31-120"><dt>AUX \_ клиб. h</dt></span><span class="sxs-lookup"><span data-stu-id="73a31-120"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="73a31-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="73a31-121">Library</span></span><br/>         | <dl> <span data-ttu-id="73a31-122"><dt>AUX \_ клиб. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73a31-122"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a31-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73a31-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a31-124">**ауксклибкуеримодулеинформатион**</span><span class="sxs-lookup"><span data-stu-id="73a31-124">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




