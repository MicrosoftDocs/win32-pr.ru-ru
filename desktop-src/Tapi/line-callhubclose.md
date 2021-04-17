---
description: '\_Сообщение КАЛЛХУБКЛОСЕ линии TAPI отправляется при закрытии концентратора вызовов.'
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: Сообщение LINE_CALLHUBCLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675494"
---
# <a name="line_callhubclose-message"></a><span data-ttu-id="9f4c2-103">Строка \_ сообщения каллхубклосе</span><span class="sxs-lookup"><span data-stu-id="9f4c2-103">LINE\_CALLHUBCLOSE message</span></span>

<span data-ttu-id="9f4c2-104">Сообщение **\_ КАЛЛХУБКЛОСЕ линии** TAPI отправляется при закрытии концентратора вызовов.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-104">The TAPI **LINE\_CALLHUBCLOSE** message is sent when a call hub has been closed.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="9f4c2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f4c2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f4c2-106">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="9f4c2-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9f4c2-107">Маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="9f4c2-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="9f4c2-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="9f4c2-109">Экземпляр обратного вызова, указанный при открытии линии вызова.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="9f4c2-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="9f4c2-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="9f4c2-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-111">Reserved.</span></span> <span data-ttu-id="9f4c2-112">Задайте значение 0.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-112">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9f4c2-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="9f4c2-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="9f4c2-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-114">Reserved.</span></span> <span data-ttu-id="9f4c2-115">Задайте значение 0.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-115">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="9f4c2-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="9f4c2-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="9f4c2-117">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-117">Reserved.</span></span> <span data-ttu-id="9f4c2-118">Задайте значение 0.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-118">Set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f4c2-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f4c2-119">Return value</span></span>

<span data-ttu-id="9f4c2-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f4c2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f4c2-121">Remarks</span></span>

<span data-ttu-id="9f4c2-122">Это сообщение исходит от TAPI, а не от поставщика услуг, поэтому соответствующее сообщение ТСПИ отсутствует.</span><span class="sxs-lookup"><span data-stu-id="9f4c2-122">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f4c2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9f4c2-123">Requirements</span></span>



| <span data-ttu-id="9f4c2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9f4c2-124">Requirement</span></span> | <span data-ttu-id="9f4c2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9f4c2-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9f4c2-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="9f4c2-126">TAPI version</span></span><br/> | <span data-ttu-id="9f4c2-127">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="9f4c2-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="9f4c2-128">Header</span><span class="sxs-lookup"><span data-stu-id="9f4c2-128">Header</span></span><br/>       | <dl> <span data-ttu-id="9f4c2-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f4c2-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




