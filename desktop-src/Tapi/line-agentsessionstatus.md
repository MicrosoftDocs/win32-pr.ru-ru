---
description: Сообщение LINE \_ ажентсессионстатус отправляется, когда состояние сеанса агента ACD изменяется в обработчике агента, для которого приложение в настоящий момент имеет открытую строку. Это сообщение создается с помощью функции Линепроксимессаже.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: Сообщение LINE_AGENTSESSIONSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689163"
---
# <a name="line_agentsessionstatus-message"></a><span data-ttu-id="0127c-104">Строка \_ сообщения ажентсессионстатус</span><span class="sxs-lookup"><span data-stu-id="0127c-104">LINE\_AGENTSESSIONSTATUS message</span></span>

<span data-ttu-id="0127c-105">Сообщение **Line \_ ажентсессионстатус** отправляется, когда состояние сеанса агента ACD изменяется в обработчике агента, для которого приложение в настоящий момент имеет открытую строку.</span><span class="sxs-lookup"><span data-stu-id="0127c-105">The **LINE\_AGENTSESSIONSTATUS** message is sent when the status of an ACD agent session changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="0127c-106">Это сообщение создается с помощью функции [**линепроксимессаже**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="0127c-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="0127c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0127c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0127c-108">*двдевице*</span><span class="sxs-lookup"><span data-stu-id="0127c-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="0127c-109">Обработчик приложения для линейного устройства, на котором изменилось состояние сеанса агента.</span><span class="sxs-lookup"><span data-stu-id="0127c-109">The application's handle to the line device on which the agent session status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="0127c-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="0127c-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="0127c-111">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="0127c-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="0127c-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0127c-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="0127c-113">Маркер сеанса агента, состояние которого изменилось.</span><span class="sxs-lookup"><span data-stu-id="0127c-113">A handle of the agent session whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="0127c-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0127c-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="0127c-115">Указывает состояние сеанса агента, которое было изменено.</span><span class="sxs-lookup"><span data-stu-id="0127c-115">Specifies the agent session status that has changed.</span></span> <span data-ttu-id="0127c-116">Может быть одной или несколькими **строками \_ ажентсессионстатус**.</span><span class="sxs-lookup"><span data-stu-id="0127c-116">Can be one or more of the **LINE\_AGENTSESSIONSTATUS**.</span></span>

</dd> <dt>

<span data-ttu-id="0127c-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="0127c-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="0127c-118">Если *dwParam2* включает \_ бит состояния линеажентстатусекс, *dwParam3* указывает новое значение состояния агента, которое является одной из [**\_ констант линеажентстатикс**](lineagentstateex--constants.md).</span><span class="sxs-lookup"><span data-stu-id="0127c-118">If *dwParam2* includes the LINEAGENTSTATUSEX\_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="0127c-119">В противном случае *dwParam3* имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="0127c-119">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0127c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="0127c-120">Requirements</span></span>



| <span data-ttu-id="0127c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="0127c-121">Requirement</span></span> | <span data-ttu-id="0127c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0127c-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0127c-123">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="0127c-123">TAPI version</span></span><br/> | <span data-ttu-id="0127c-124">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="0127c-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="0127c-125">Header</span><span class="sxs-lookup"><span data-stu-id="0127c-125">Header</span></span><br/>       | <dl> <span data-ttu-id="0127c-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0127c-126"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0127c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0127c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0127c-128">**линежетажентсессионинфо**</span><span class="sxs-lookup"><span data-stu-id="0127c-128">**lineGetAgentSessionInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[<span data-ttu-id="0127c-129">**линепроксимессаже**</span><span class="sxs-lookup"><span data-stu-id="0127c-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




