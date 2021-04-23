---
description: Сообщение TAPI LINE \_ аппневкаллхуб отправляется для информирования приложения о создании нового концентратора вызовов.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: Сообщение LINE_APPNEWCALLHUB (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634dd82aadd5e3c8a7664572136b54f8bbdf8a52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679589"
---
# <a name="line_appnewcallhub-message"></a><span data-ttu-id="bcba7-103">Строка \_ сообщения аппневкаллхуб</span><span class="sxs-lookup"><span data-stu-id="bcba7-103">LINE\_APPNEWCALLHUB message</span></span>

<span data-ttu-id="bcba7-104">Сообщение TAPI **Line \_ аппневкаллхуб** отправляется для информирования приложения о создании нового концентратора вызовов.</span><span class="sxs-lookup"><span data-stu-id="bcba7-104">The TAPI **LINE\_APPNEWCALLHUB** message is sent to inform an application when a new call hub has been created.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="bcba7-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="bcba7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcba7-106">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="bcba7-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="bcba7-107">Маркер вызова.</span><span class="sxs-lookup"><span data-stu-id="bcba7-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="bcba7-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="bcba7-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="bcba7-109">Экземпляр обратного вызова, указанный при открытии линии вызова.</span><span class="sxs-lookup"><span data-stu-id="bcba7-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="bcba7-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="bcba7-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="bcba7-111">Уровень отслеживания в новом концентраторе, как определено одной из [**\_ констант линекаллхубтраккинг**](linecallhubtracking--constants.md).</span><span class="sxs-lookup"><span data-stu-id="bcba7-111">The tracking level on the new hub, as defined by one of the [**LINECALLHUBTRACKING\_ Constants**](linecallhubtracking--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcba7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bcba7-112">Return value</span></span>

<span data-ttu-id="bcba7-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="bcba7-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcba7-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bcba7-114">Remarks</span></span>

<span data-ttu-id="bcba7-115">Это сообщение исходит от TAPI, а не от поставщика услуг, поэтому соответствующее сообщение ТСПИ отсутствует.</span><span class="sxs-lookup"><span data-stu-id="bcba7-115">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcba7-116">Требования</span><span class="sxs-lookup"><span data-stu-id="bcba7-116">Requirements</span></span>



| <span data-ttu-id="bcba7-117">Требование</span><span class="sxs-lookup"><span data-stu-id="bcba7-117">Requirement</span></span> | <span data-ttu-id="bcba7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bcba7-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bcba7-119">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="bcba7-119">TAPI version</span></span><br/> | <span data-ttu-id="bcba7-120">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="bcba7-120">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="bcba7-121">Header</span><span class="sxs-lookup"><span data-stu-id="bcba7-121">Header</span></span><br/>       | <dl> <span data-ttu-id="bcba7-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcba7-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




