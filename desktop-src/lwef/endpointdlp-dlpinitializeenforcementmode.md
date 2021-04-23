---
description: Уведомляет систему о требуемых режимах применения для набора операций защиты от потери данных в конечной точке.
title: Функция Длпинитиализинфорцементмоде (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495918"
---
# <a name="dlpinitializeenforcementmode-function"></a><span data-ttu-id="c22ef-103">Функция Длпинитиализинфорцементмоде</span><span class="sxs-lookup"><span data-stu-id="c22ef-103">DlpInitializeEnforcementMode function</span></span>

<span data-ttu-id="c22ef-104">Уведомляет систему о требуемых режимах применения для набора операций защиты от потери данных в конечной точке.</span><span class="sxs-lookup"><span data-stu-id="c22ef-104">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="c22ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c22ef-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a><span data-ttu-id="c22ef-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c22ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c22ef-107">*Количество* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c22ef-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22ef-108">Значение **типа DWORD** , указывающее количество операций, включаемых в массив *оператионенфорцемент* .</span><span class="sxs-lookup"><span data-stu-id="c22ef-108">A **DWORD** specifying the number of operations included in the *OperationEnforcement* array.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="c22ef-109">*Оператионенфорцемент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c22ef-109">*OperationEnforcement* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22ef-110">Массив структур [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) , которые указывают уровень применения для операции защиты от потери данных конечной точки.</span><span class="sxs-lookup"><span data-stu-id="c22ef-110">An array of [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structures that specify the enforcement level for an endpoint DLP operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="c22ef-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c22ef-111">Return value</span></span>

<span data-ttu-id="c22ef-112">Возвращает значение HRESULT, включая (но не ограничиваясь) следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c22ef-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="c22ef-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c22ef-113">HRESULT</span></span> | <span data-ttu-id="c22ef-114">Описание:</span><span class="sxs-lookup"><span data-stu-id="c22ef-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="c22ef-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="c22ef-115">S_OK</span></span> | <span data-ttu-id="c22ef-116">Функция успешно завершена</span><span class="sxs-lookup"><span data-stu-id="c22ef-116">The function completed successfully</span></span> |
| <span data-ttu-id="c22ef-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c22ef-117">E_INVALIDARG</span></span> | <span data-ttu-id="c22ef-118">Один или несколько параметров функции являются недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="c22ef-118">One or more of the function parameters are invalid.</span></span> |
| <span data-ttu-id="c22ef-119">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="c22ef-119">E_OUTOFMEMORY</span></span> | <span data-ttu-id="c22ef-120">Не удалось выделить память для операции.</span><span class="sxs-lookup"><span data-stu-id="c22ef-120">Memory allocation for the operation failed.</span></span> |



## <a name="remarks"></a><span data-ttu-id="c22ef-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="c22ef-121">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="c22ef-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c22ef-122">Requirements</span></span>



| <span data-ttu-id="c22ef-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c22ef-123">Requirement</span></span>          |    <span data-ttu-id="c22ef-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c22ef-124">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c22ef-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c22ef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c22ef-126">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="c22ef-126">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="c22ef-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c22ef-127">DLL</span></span><br/>                      | <span data-ttu-id="c22ef-128">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="c22ef-128">EndpointDlp.dll</span></span> |