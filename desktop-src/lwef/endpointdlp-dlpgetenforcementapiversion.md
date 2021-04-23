---
description: Извлекает версию API защиты от потери данных для конечной точки на текущем устройстве.
title: Функция Длпжетенфорцементапиверсион (ендпоинтдлп. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495948"
---
# <a name="dlpgetenforcementapiversion-function"></a><span data-ttu-id="ac55c-103">Функция Длпжетенфорцементапиверсион</span><span class="sxs-lookup"><span data-stu-id="ac55c-103">DlpGetEnforcementApiVersion function</span></span>

<span data-ttu-id="ac55c-104">Извлекает версию API защиты от потери данных для конечной точки на текущем устройстве.</span><span class="sxs-lookup"><span data-stu-id="ac55c-104">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac55c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac55c-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a><span data-ttu-id="ac55c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac55c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac55c-107">*Majorversion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac55c-107">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac55c-108">Значение **типа DWORD** , указывающее основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="ac55c-108">A **DWORD** specifying the major version number.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="ac55c-109">*Majorversion* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac55c-109">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac55c-110">Значение **типа DWORD** , указывающее дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="ac55c-110">A **DWORD** specifying the minor version number.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="ac55c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac55c-111">Return value</span></span>

<span data-ttu-id="ac55c-112">Возвращает значение HRESULT, включая (но не ограничиваясь) следующие значения.</span><span class="sxs-lookup"><span data-stu-id="ac55c-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="ac55c-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ac55c-113">HRESULT</span></span> | <span data-ttu-id="ac55c-114">Описание:</span><span class="sxs-lookup"><span data-stu-id="ac55c-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="ac55c-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac55c-115">S_OK</span></span> | <span data-ttu-id="ac55c-116">Функция успешно завершена</span><span class="sxs-lookup"><span data-stu-id="ac55c-116">The function completed successfully</span></span> |




## <a name="remarks"></a><span data-ttu-id="ac55c-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="ac55c-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="ac55c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ac55c-118">Requirements</span></span>



| <span data-ttu-id="ac55c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ac55c-119">Requirement</span></span>          |    <span data-ttu-id="ac55c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ac55c-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac55c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ac55c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ac55c-122">Windows 10, версия 1809 (10,0; Сборка 17763)</span><span class="sxs-lookup"><span data-stu-id="ac55c-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="ac55c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ac55c-123">DLL</span></span><br/>                      | <span data-ttu-id="ac55c-124">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="ac55c-124">EndpointDlp.dll</span></span> |