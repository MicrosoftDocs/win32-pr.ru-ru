---
description: '\_Сообщение АЖЕНТСПЕЦИФИК линии TAPI отправляется, когда состояние ACD-агента изменяется в строке, в которой открыто приложение. Приложение может вызвать Линежетажентстатус, чтобы определить текущее состояние агента.'
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: Сообщение LINE_AGENTSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679595"
---
# <a name="line_agentspecific-message"></a><span data-ttu-id="ea699-104">Строка \_ сообщения ажентспеЦифик</span><span class="sxs-lookup"><span data-stu-id="ea699-104">LINE\_AGENTSPECIFIC message</span></span>

<span data-ttu-id="ea699-105">Сообщение **\_ АЖЕНТСПЕЦИФИК линии** TAPI отправляется, когда состояние ACD-агента изменяется в строке, в которой открыто приложение.</span><span class="sxs-lookup"><span data-stu-id="ea699-105">The TAPI **LINE\_AGENTSPECIFIC** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="ea699-106">Приложение может вызвать [**линежетажентстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) , чтобы определить текущее состояние агента.</span><span class="sxs-lookup"><span data-stu-id="ea699-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="ea699-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea699-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea699-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="ea699-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="ea699-109">Маркер приложения для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="ea699-109">The application's handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="ea699-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="ea699-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ea699-111">Экземпляр обратного вызова, указанный при открытии линии вызова.</span><span class="sxs-lookup"><span data-stu-id="ea699-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="ea699-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ea699-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="ea699-113">Индекс в массиве идентификаторов расширения обработчика в структуре [**линеаженткапс**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) расширения обработчика, с которым связано сообщение.</span><span class="sxs-lookup"><span data-stu-id="ea699-113">The index into the array of handler extension identifiers in the [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) structure of the handler extension with which the message is associated.</span></span>

</dd> <dt>

<span data-ttu-id="ea699-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ea699-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="ea699-115">Относится к расширению обработчика.</span><span class="sxs-lookup"><span data-stu-id="ea699-115">Specific to the handler extension.</span></span> <span data-ttu-id="ea699-116">Как правило, это значение используется, чтобы приложение вызывало функцию [**линеажентспеЦифик**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) для получения дополнительных сведений о сообщении.</span><span class="sxs-lookup"><span data-stu-id="ea699-116">Generally, this value is used to cause the application to invoke a [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) function to fetch further details about the message.</span></span>

</dd> <dt>

<span data-ttu-id="ea699-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="ea699-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="ea699-118">Относится к расширению обработчика.</span><span class="sxs-lookup"><span data-stu-id="ea699-118">Specific to the handler extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea699-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea699-119">Return value</span></span>

<span data-ttu-id="ea699-120">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ea699-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea699-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea699-121">Remarks</span></span>

<span data-ttu-id="ea699-122">**Строка \_ ажентспеЦифик** сообщения не отправляется в приложения, поддерживающие более старые версии TAPI.</span><span class="sxs-lookup"><span data-stu-id="ea699-122">The **LINE\_AGENTSPECIFIC** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea699-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ea699-123">Requirements</span></span>



| <span data-ttu-id="ea699-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ea699-124">Requirement</span></span> | <span data-ttu-id="ea699-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ea699-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ea699-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="ea699-126">TAPI version</span></span><br/> | <span data-ttu-id="ea699-127">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="ea699-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ea699-128">Header</span><span class="sxs-lookup"><span data-stu-id="ea699-128">Header</span></span><br/>       | <dl> <span data-ttu-id="ea699-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea699-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea699-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea699-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea699-131">**линеаженткапс**</span><span class="sxs-lookup"><span data-stu-id="ea699-131">**LINEAGENTCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[<span data-ttu-id="ea699-132">**линеажентспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="ea699-132">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[<span data-ttu-id="ea699-133">**линежетажентстатус**</span><span class="sxs-lookup"><span data-stu-id="ea699-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




