---
description: '\_Константы побитового флага линеаддрессшаринг описывают различные способы совместного использования адреса различными линиями.'
ms.assetid: f37ba549-c8dc-4a7c-bfe6-8e5f733d9750
title: Константы LINEADDRESSSHARING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785c7e924ffc958d3fe14b739bb2eb28dec322a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675563"
---
# <a name="lineaddresssharing_-constants"></a><span data-ttu-id="cc6ca-103">\_Константы линеаддрессшаринг</span><span class="sxs-lookup"><span data-stu-id="cc6ca-103">LINEADDRESSSHARING\_ Constants</span></span>

<span data-ttu-id="cc6ca-104">Константы побитового флага **линеаддрессшаринг \_** описывают различные способы совместного использования адреса различными линиями.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-104">The **LINEADDRESSSHARING\_** bit-flag constants describe various ways an address can be shared between lines.</span></span>

<dl> <dt>

<span data-ttu-id="cc6ca-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**ЛИНЕАДДРЕССШАРИНГ \_ закрытый**</span><span class="sxs-lookup"><span data-stu-id="cc6ca-105"><span id="LINEADDRESSSHARING_PRIVATE"></span><span id="lineaddresssharing_private"></span>**LINEADDRESSSHARING\_PRIVATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc6ca-106">Адрес является частным для строки пользователя; она не назначена какой-либо другой станции.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-106">The address is private to the user's line; it is not assigned to any other station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cc6ca-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**ЛИНЕАДДРЕССШАРИНГ \_ бриджедекскл**</span><span class="sxs-lookup"><span data-stu-id="cc6ca-107"><span id="LINEADDRESSSHARING_BRIDGEDEXCL"></span><span id="lineaddresssharing_bridgedexcl"></span>**LINEADDRESSSHARING\_BRIDGEDEXCL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc6ca-108">Этот адрес связан с одной или несколькими станциями.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-108">The address is bridged to one or more other stations.</span></span> <span data-ttu-id="cc6ca-109">Первая строка для активации вызова в строке будет иметь эксклюзивный доступ к адресу и в нем могут существовать вызовы.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-109">The first line to activate a call on the line will have exclusive access to the address and calls that may exist on it.</span></span> <span data-ttu-id="cc6ca-110">Другие линии не смогут использовать адрес моста, пока он используется.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-110">Other lines will not be able to use the bridged address while it is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cc6ca-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**ЛИНЕАДДРЕССШАРИНГ \_ бриджеднев**</span><span class="sxs-lookup"><span data-stu-id="cc6ca-111"><span id="LINEADDRESSSHARING_BRIDGEDNEW"></span><span id="lineaddresssharing_bridgednew"></span>**LINEADDRESSSHARING\_BRIDGEDNEW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc6ca-112">Адрес моста связан с одной или несколькими станциями.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-112">The address is bridged with one or more other stations.</span></span> <span data-ttu-id="cc6ca-113">Первая строка для активации вызова в строке будет иметь монопольный доступ только к соответствующему вызову.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-113">The first line to activate a call on the line will have exclusive access to only the corresponding call.</span></span> <span data-ttu-id="cc6ca-114">Другие приложения, использующие этот адрес, приведут к созданию нового и отдельного внешнего вида вызовов.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-114">Other applications that use the address will result in new and separate call appearances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cc6ca-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**ЛИНЕАДДРЕССШАРИНГ \_ бриджедшаред**</span><span class="sxs-lookup"><span data-stu-id="cc6ca-115"><span id="LINEADDRESSSHARING_BRIDGEDSHARED"></span><span id="lineaddresssharing_bridgedshared"></span>**LINEADDRESSSHARING\_BRIDGEDSHARED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc6ca-116">Адрес моста связан с одной или несколькими строками.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-116">The address is bridged with one or more other lines.</span></span> <span data-ttu-id="cc6ca-117">Все мосты могут совместно использовать вызовы по адресу, которые затем функционируют как Конференция.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-117">All bridged parties can share in calls on the address, which then functions as a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cc6ca-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**ЛИНЕАДДРЕССШАРИНГ \_ отслеживается**</span><span class="sxs-lookup"><span data-stu-id="cc6ca-118"><span id="LINEADDRESSSHARING_MONITORED"></span><span id="lineaddresssharing_monitored"></span>**LINEADDRESSSHARING\_MONITORED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc6ca-119">Это адрес, состояние простоя или занятости которого становится доступным для этой строки.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-119">This is an address whose idle/busy status is made available to this line.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc6ca-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc6ca-120">Remarks</span></span>

<span data-ttu-id="cc6ca-121">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-121">No extensibility.</span></span> <span data-ttu-id="cc6ca-122">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="cc6ca-123">Способ, которым адрес совместно используется в разных строках, может повлиять на поведение этого адреса.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-123">The way in which an address is shared across lines can affect the behavior of that address.</span></span> <span data-ttu-id="cc6ca-124">[**Строка \_ Сообщения КАЛЛСТАТЕ**](line-callstate.md) и [**Line \_ аддрессстате**](line-addressstate.md) отправляются в приложение в ответ на действия, направляемые станциями моста.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-124">[**LINE\_CALLSTATE**](line-callstate.md) and [**LINE\_ADDRESSSTATE**](line-addressstate.md) messages are sent to the application in response to activities by the bridging stations.</span></span> <span data-ttu-id="cc6ca-125">Это сообщения, которые приложение может отвести от состояния адреса.</span><span class="sxs-lookup"><span data-stu-id="cc6ca-125">It is through these messages that an application can track the status of the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc6ca-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cc6ca-126">Requirements</span></span>



| <span data-ttu-id="cc6ca-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cc6ca-127">Requirement</span></span> | <span data-ttu-id="cc6ca-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6ca-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cc6ca-129">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="cc6ca-129">TAPI version</span></span><br/> | <span data-ttu-id="cc6ca-130">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="cc6ca-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cc6ca-131">Header</span><span class="sxs-lookup"><span data-stu-id="cc6ca-131">Header</span></span><br/>       | <dl> <span data-ttu-id="cc6ca-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc6ca-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc6ca-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc6ca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc6ca-134">**Строка \_ аддрессстате**</span><span class="sxs-lookup"><span data-stu-id="cc6ca-134">**LINE\_ADDRESSSTATE**</span></span>](line-addressstate.md)
</dt> <dt>

[<span data-ttu-id="cc6ca-135">**Строка \_ каллстате**</span><span class="sxs-lookup"><span data-stu-id="cc6ca-135">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> </dl>

 

 




