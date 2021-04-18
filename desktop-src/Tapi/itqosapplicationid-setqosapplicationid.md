---
description: Метод Сеткосаппликатионид задает идентификатор качества обслуживания для приложения.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'Метод Иткосаппликатионид:: Сеткосаппликатионид (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680055"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a><span data-ttu-id="7989c-103">Метод Иткосаппликатионид:: Сеткосаппликатионид</span><span class="sxs-lookup"><span data-stu-id="7989c-103">ITQOSApplicationID::SetQOSApplicationID method</span></span>

<span data-ttu-id="7989c-104">\[ Этот метод недоступен для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7989c-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7989c-105">API клиента RTC предоставляет аналогичные функциональные возможности.\]</span><span class="sxs-lookup"><span data-stu-id="7989c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7989c-106">Метод **сеткосаппликатионид** задает идентификатор качества обслуживания для приложения.</span><span class="sxs-lookup"><span data-stu-id="7989c-106">The **SetQOSApplicationID** method sets the QOS identifier for the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="7989c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7989c-107">Syntax</span></span>


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a><span data-ttu-id="7989c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7989c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7989c-109">*паппликатионид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7989c-109">*pApplicationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7989c-110">Уникальный идентификатор процесса приложения.</span><span class="sxs-lookup"><span data-stu-id="7989c-110">Unique identifier for the application process.</span></span>

</dd> <dt>

<span data-ttu-id="7989c-111">*паппликатионгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7989c-111">*pApplicationGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7989c-112">GUID приложения.</span><span class="sxs-lookup"><span data-stu-id="7989c-112">Application GUID.</span></span>

</dd> <dt>

<span data-ttu-id="7989c-113">*псубидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7989c-113">*pSubIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7989c-114">Sub-IDs, связанный с текущим вызовом.</span><span class="sxs-lookup"><span data-stu-id="7989c-114">Sub-IDs associated with the current call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7989c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7989c-115">Return value</span></span>

<span data-ttu-id="7989c-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="7989c-116">This method can return one of these values.</span></span>



| <span data-ttu-id="7989c-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7989c-117">Return code</span></span>                                                                                   | <span data-ttu-id="7989c-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7989c-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7989c-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7989c-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7989c-120">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7989c-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7989c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7989c-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7989c-122">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="7989c-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7989c-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7989c-123">Requirements</span></span>



| <span data-ttu-id="7989c-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7989c-124">Requirement</span></span> | <span data-ttu-id="7989c-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7989c-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7989c-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="7989c-126">TAPI version</span></span><br/> | <span data-ttu-id="7989c-127">Требуется TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7989c-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="7989c-128">Header</span><span class="sxs-lookup"><span data-stu-id="7989c-128">Header</span></span><br/>       | <dl> <span data-ttu-id="7989c-129"><dt>Ипмсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7989c-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7989c-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7989c-130">Library</span></span><br/>      | <dl> <span data-ttu-id="7989c-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7989c-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="7989c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7989c-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="7989c-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7989c-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7989c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7989c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7989c-135">**иткосаппликатионид**</span><span class="sxs-lookup"><span data-stu-id="7989c-135">**ITQOSApplicationID**</span></span>](itqosapplicationid.md)
</dt> </dl>

 

 




