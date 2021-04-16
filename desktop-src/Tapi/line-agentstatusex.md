---
description: Сообщение LINE \_ ажентстатусекс отправляется при изменении состояния ACD-агента в обработчике агента, для которого в настоящий момент в приложении есть открытая строка. Это сообщение создается с помощью функции Линепроксимессаже.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: Сообщение LINE_AGENTSTATUSEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679590"
---
# <a name="line_agentstatusex-message"></a><span data-ttu-id="f249a-104">Строка \_ сообщения ажентстатусекс</span><span class="sxs-lookup"><span data-stu-id="f249a-104">LINE\_AGENTSTATUSEX message</span></span>

<span data-ttu-id="f249a-105">Сообщение **Line \_ ажентстатусекс** отправляется при изменении состояния ACD-агента в обработчике агента, для которого в настоящий момент в приложении есть открытая строка.</span><span class="sxs-lookup"><span data-stu-id="f249a-105">The **LINE\_AGENTSTATUSEX** message is sent when the status of an ACD agent changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="f249a-106">Это сообщение создается с помощью функции [**линепроксимессаже**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="f249a-106">This message is generated using [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="f249a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f249a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f249a-108">*двдевице*</span><span class="sxs-lookup"><span data-stu-id="f249a-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f249a-109">Маркер приложения для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="f249a-109">The application's handle to the line device.</span></span> <span data-ttu-id="f249a-110">Это связано с обработчиком агента.</span><span class="sxs-lookup"><span data-stu-id="f249a-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="f249a-111">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="f249a-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f249a-112">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="f249a-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="f249a-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f249a-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f249a-114">Маркер агента, состояние которого изменилось.</span><span class="sxs-lookup"><span data-stu-id="f249a-114">The handle of the agent whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="f249a-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f249a-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f249a-116">Указывает состояние очереди, которое было изменено.</span><span class="sxs-lookup"><span data-stu-id="f249a-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="f249a-117">Может быть одной или несколькими [**\_ константами линекуеуестатус**](linequeuestatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="f249a-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f249a-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f249a-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f249a-119">Если *dwParam2* включает \_ бит состояния линеажентстатусекс, *dwParam3* указывает новое значение состояния агента, которое является одной из [**\_ констант линеажентстатикс**](lineagentstateex--constants.md).</span><span class="sxs-lookup"><span data-stu-id="f249a-119">If *dwParam2* includes the LINEAGENTSTATUSEX \_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="f249a-120">В противном случае *dwParam3* имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="f249a-120">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f249a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="f249a-121">Requirements</span></span>



| <span data-ttu-id="f249a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="f249a-122">Requirement</span></span> | <span data-ttu-id="f249a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="f249a-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f249a-124">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="f249a-124">TAPI version</span></span><br/> | <span data-ttu-id="f249a-125">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="f249a-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="f249a-126">Header</span><span class="sxs-lookup"><span data-stu-id="f249a-126">Header</span></span><br/>       | <dl> <span data-ttu-id="f249a-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f249a-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f249a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f249a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f249a-129">**линежетажентинфо**</span><span class="sxs-lookup"><span data-stu-id="f249a-129">**lineGetAgentInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[<span data-ttu-id="f249a-130">**линепроксимессаже**</span><span class="sxs-lookup"><span data-stu-id="f249a-130">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




