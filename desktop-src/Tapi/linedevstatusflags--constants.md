---
description: '\_Константы побитового флага линедевстатусфлагс описывают коллекцию элементов состояния логического устройства линии.'
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: Константы LINEDEVSTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674926"
---
# <a name="linedevstatusflags_-constants"></a><span data-ttu-id="6e392-103">\_Константы линедевстатусфлагс</span><span class="sxs-lookup"><span data-stu-id="6e392-103">LINEDEVSTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="6e392-104">Константы побитового флага **линедевстатусфлагс \_** описывают коллекцию элементов состояния логического устройства линии.</span><span class="sxs-lookup"><span data-stu-id="6e392-104">The **LINEDEVSTATUSFLAGS\_** bit-flag constants describe a collection of Boolean line device status items.</span></span>

<dl> <dt>

<span data-ttu-id="6e392-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**ЛИНЕДЕВСТАТУСФЛАГС \_ подключен**</span><span class="sxs-lookup"><span data-stu-id="6e392-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6e392-106">Указывает, подключена ли линия к TAPI.</span><span class="sxs-lookup"><span data-stu-id="6e392-106">Specifies whether the line is connected to TAPI.</span></span> <span data-ttu-id="6e392-107">Если **значение равно true**, линия подключена, а TAPI может использовать устройство линии.</span><span class="sxs-lookup"><span data-stu-id="6e392-107">If **TRUE**, the line is connected and TAPI is able to operate on the line device.</span></span> <span data-ttu-id="6e392-108">Если **значение равно false**, строка отсоединяется и приложение не может управлять устройством линии через TAPI.</span><span class="sxs-lookup"><span data-stu-id="6e392-108">If **FALSE**, the line is disconnected and the application is unable to control the line device through TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e392-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**ЛИНЕДЕВСТАТУСФЛАГС \_**</span><span class="sxs-lookup"><span data-stu-id="6e392-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6e392-110">Указывает, находится ли строка в службе.</span><span class="sxs-lookup"><span data-stu-id="6e392-110">Indicates whether the line is in service.</span></span> <span data-ttu-id="6e392-111">Если **значение равно true**, строка находится в службе; Если **значение равно false**, строка находится вне службы.</span><span class="sxs-lookup"><span data-stu-id="6e392-111">If **TRUE**, the line is in service; if **FALSE**, the line is out of service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e392-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**ЛИНЕДЕВСТАТУСФЛАГС \_ заблокирована**</span><span class="sxs-lookup"><span data-stu-id="6e392-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6e392-113">Указывает, заблокирована или разблокирована строка.</span><span class="sxs-lookup"><span data-stu-id="6e392-113">Indicates whether the line is locked or unlocked.</span></span> <span data-ttu-id="6e392-114">Этот бит чаще всего используется с линейными устройствами, связанными с сотовыми телефонами.</span><span class="sxs-lookup"><span data-stu-id="6e392-114">This bit is most often used with line devices associated with cellular phones.</span></span> <span data-ttu-id="6e392-115">Многие Сотовые телефоны имеют механизм безопасности, требующий ввода пароля, чтобы телефон могли размещать вызовы.</span><span class="sxs-lookup"><span data-stu-id="6e392-115">Many cellular phones have a security mechanism that requires the entry of a password to enable the phone to place calls.</span></span> <span data-ttu-id="6e392-116">Этот бит можно использовать для обозначения приложений, заблокированных телефоном, и не может размещать вызовы до тех пор, пока пароль не будет указан в пользовательском интерфейсе телефона, чтобы приложение предприняло соответствующее предупреждение пользователю.</span><span class="sxs-lookup"><span data-stu-id="6e392-116">This bit can be used to indicate to applications that the phone is locked and cannot place calls until the password is entered on the user interface of the phone so that the application can present an appropriate alert to the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6e392-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**ЛИНЕДЕВСТАТУСФЛАГС \_ мсгваит**</span><span class="sxs-lookup"><span data-stu-id="6e392-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS\_MSGWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6e392-118">Указывает, ожидает ли строка сообщения.</span><span class="sxs-lookup"><span data-stu-id="6e392-118">Indicates whether the line has a message waiting.</span></span> <span data-ttu-id="6e392-119">Если **значение равно true**, сообщение находится в состоянии ожидания; Если **значение равно false**, сообщение не ожидает выполнения.</span><span class="sxs-lookup"><span data-stu-id="6e392-119">If **TRUE**, a message is waiting; if **FALSE**, no message is waiting.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e392-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6e392-120">Remarks</span></span>

<span data-ttu-id="6e392-121">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="6e392-121">No extensibility.</span></span> <span data-ttu-id="6e392-122">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="6e392-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="6e392-123">\_Константы линедевстатусфлагс используются в элементе **двдевстатусфлагс** структуры данных [**линедевстатус**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) .</span><span class="sxs-lookup"><span data-stu-id="6e392-123">LINEDEVSTATUSFLAGS\_ constants are used within the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e392-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6e392-124">Requirements</span></span>



| <span data-ttu-id="6e392-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6e392-125">Requirement</span></span> | <span data-ttu-id="6e392-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6e392-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6e392-127">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="6e392-127">TAPI version</span></span><br/> | <span data-ttu-id="6e392-128">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6e392-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6e392-129">Header</span><span class="sxs-lookup"><span data-stu-id="6e392-129">Header</span></span><br/>       | <dl> <span data-ttu-id="6e392-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e392-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




