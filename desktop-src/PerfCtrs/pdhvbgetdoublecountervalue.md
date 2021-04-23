---
description: Функция Пдхвбжетдаублекаунтервалуе возвращает текущее значение указанного счетчика в виде значения с плавающей запятой двойной точности.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: Функция Пдхвбжетдаублекаунтервалуе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345512"
---
# <a name="pdhvbgetdoublecountervalue-function"></a><span data-ttu-id="a1b9e-103">Функция Пдхвбжетдаублекаунтервалуе</span><span class="sxs-lookup"><span data-stu-id="a1b9e-103">PdhVbGetDoubleCounterValue function</span></span>

<span data-ttu-id="a1b9e-104">Функция **пдхвбжетдаублекаунтервалуе** возвращает текущее значение указанного счетчика в виде значения с плавающей запятой двойной точности.</span><span class="sxs-lookup"><span data-stu-id="a1b9e-104">The **PdhVbGetDoubleCounterValue** function returns the current value of the specified counter as a double-precision floating point value.</span></span> <span data-ttu-id="a1b9e-105">Следует проверить *каунтерстатус* перед использованием возвращенного номера, так как счетчик может быть недопустимым при чтении.</span><span class="sxs-lookup"><span data-stu-id="a1b9e-105">You should check *CounterStatus* before using the returned number, because the counter may not be valid when it is read.</span></span> <span data-ttu-id="a1b9e-106">Чтобы проверить состояние счетчика, вызовите функцию [**пдхвбисгудстатус**](pdhvbisgoodstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b9e-106">To check the counter status, call the [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1b9e-107">Функция, описанная в этом разделе, может быть изменена или недоступна в будущем.</span><span class="sxs-lookup"><span data-stu-id="a1b9e-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="a1b9e-108">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="a1b9e-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="a1b9e-109">Function Пдхвбжетдаублекаунтервалуе ( \_ ByVal Каунтерхандле как Long, \_ ByVal Каунтерстатус как long \_ ) как Double</span><span class="sxs-lookup"><span data-stu-id="a1b9e-109">Function PdhVbGetDoubleCounterValue( \_ ByVal CounterHandle As Long, \_ ByVal CounterStatus As Long \_ ) As Double</span></span>

## <a name="parameters"></a><span data-ttu-id="a1b9e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1b9e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b9e-111">*каунтерхандле*</span><span class="sxs-lookup"><span data-stu-id="a1b9e-111">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b9e-112">Идентификатор счетчика, текущее значение которого должно быть считано.</span><span class="sxs-lookup"><span data-stu-id="a1b9e-112">ID of the counter whose current value is to be read.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9e-113">*каунтерстатус*</span><span class="sxs-lookup"><span data-stu-id="a1b9e-113">*CounterStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b9e-114">Переменная, в которой текущее состояние значения счетчика возвращается вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="a1b9e-114">Variable in which the current status of the counter value is returned to the caller.</span></span> <span data-ttu-id="a1b9e-115">Возвращаемое значение данных является допустимым только в том случае, если значение, возвращенное в Каунтерстатус, является PDH \_ кстатус \_ допустимыми \_ данными или PDH \_ кстатус \_ новых \_ данных (см. коды ошибок PDH).</span><span class="sxs-lookup"><span data-stu-id="a1b9e-115">The returned data value is valid if and only if the value returned in CounterStatus is PDH\_CSTATUS\_VALID\_DATA or PDH\_CSTATUS\_NEW\_DATA (see PDH error codes).</span></span> <span data-ttu-id="a1b9e-116">Если значение, возвращаемое в Каунтерстатус, является любым другим значением, не используйте данные.</span><span class="sxs-lookup"><span data-stu-id="a1b9e-116">If the value returned in CounterStatus is any other value, do not use the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1b9e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1b9e-117">Return value</span></span>

<span data-ttu-id="a1b9e-118">Функция возвращает значение текущего счетчика с плавающей запятой двойной точности, вычисленное и отформатированное как определенное типом счетчика.</span><span class="sxs-lookup"><span data-stu-id="a1b9e-118">The function returns the double-precision floating point value of the current counter, computed and formatted as defined by the counter type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b9e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a1b9e-119">Requirements</span></span>



| <span data-ttu-id="a1b9e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a1b9e-120">Requirement</span></span> | <span data-ttu-id="a1b9e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a1b9e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b9e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1b9e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b9e-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a1b9e-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1b9e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1b9e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b9e-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a1b9e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a1b9e-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a1b9e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1b9e-127"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9e-127"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="a1b9e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a1b9e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1b9e-129"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9e-129"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1b9e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1b9e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b9e-131">**пдхвбисгудстатус**</span><span class="sxs-lookup"><span data-stu-id="a1b9e-131">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




