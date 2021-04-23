---
title: Имстскаксевентс Онидлетимеаутнотификатион, метод
description: Вызывается, когда пользователь не наводит мышь или клавиатуру в течение периода времени, заданного \_ методом имсрдпклиентадванцедсеттингс минутестоидлетимеаут.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онидлетимеаутнотификатион
- Службы удаленных рабочих столов метода Онидлетимеаутнотификатион, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онидлетимеаутнотификатион
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672725"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a><span data-ttu-id="b979f-106">Метод Имстскаксевентс:: Онидлетимеаутнотификатион</span><span class="sxs-lookup"><span data-stu-id="b979f-106">IMsTscAxEvents::OnIdleTimeoutNotification method</span></span>

<span data-ttu-id="b979f-107">Вызывается, когда пользователь не наводит мышь или клавиатуру в течение периода времени, заданного методом [**имсрдпклиентадванцедсеттингс::p UT \_ минутестоидлетимеаут**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="b979f-107">Called when there has been no mouse or keyboard input by the user during the period of time set by the [**IMsRdpClientAdvancedSettings::put\_MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b979f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b979f-108">Syntax</span></span>


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a><span data-ttu-id="b979f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b979f-109">Parameters</span></span>

<span data-ttu-id="b979f-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b979f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b979f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b979f-111">Return value</span></span>

<span data-ttu-id="b979f-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b979f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b979f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b979f-113">Remarks</span></span>

<span data-ttu-id="b979f-114">По умолчанию значение свойства [**минутестоидлетимеаут**](imsrdpclientadvancedsettings-minutestoidletimeout.md) равно нулю, и система не отслеживает время ожидания простоя.</span><span class="sxs-lookup"><span data-stu-id="b979f-114">By default, the value of the [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) property is set to zero and the system does not monitor for idle time-outs.</span></span> <span data-ttu-id="b979f-115">Это событие возникает, только если свойству присвоено ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b979f-115">This event occurs only if the property is set to a nonzero value.</span></span>

<span data-ttu-id="b979f-116">Значение параметра [**минутестоидлетимеаут**](imsrdpclientadvancedsettings-minutestoidletimeout.md) автоматически сбрасывается каждый раз при возникновении события.</span><span class="sxs-lookup"><span data-stu-id="b979f-116">The value of [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) is automatically reset each time the event occurs.</span></span>

<span data-ttu-id="b979f-117">Приложения могут использовать [**минутестоидлетимеаут**](imsrdpclientadvancedsettings-minutestoidletimeout.md) в ситуациях, когда полезно отключать пользователя; Например, в режиме киоска или в другом открытом сценарии терминала.</span><span class="sxs-lookup"><span data-stu-id="b979f-117">Applications can use [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) in situations where it is useful to disconnect a user; for example, in a kiosk or other public terminal scenario.</span></span>

## <a name="requirements"></a><span data-ttu-id="b979f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b979f-118">Requirements</span></span>



| <span data-ttu-id="b979f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b979f-119">Requirement</span></span> | <span data-ttu-id="b979f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b979f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b979f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b979f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b979f-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b979f-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b979f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b979f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b979f-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b979f-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b979f-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b979f-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="b979f-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b979f-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b979f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b979f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b979f-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b979f-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b979f-129">IID</span><span class="sxs-lookup"><span data-stu-id="b979f-129">IID</span></span><br/>                      | <span data-ttu-id="b979f-130">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="b979f-130">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b979f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b979f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b979f-132">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="b979f-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





