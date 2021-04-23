---
description: '\_Сообщение агент находится линии TAPI отправляется, когда состояние ACD-агента изменяется в строке, в которой открыто приложение. Приложение может вызвать Линежетажентстатус, чтобы определить текущее состояние агента.'
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: Сообщение LINE_AGENTSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689161"
---
# <a name="line_agentstatus-message"></a><span data-ttu-id="8712b-104">Строка \_ сообщения агент находится</span><span class="sxs-lookup"><span data-stu-id="8712b-104">LINE\_AGENTSTATUS message</span></span>

<span data-ttu-id="8712b-105">Сообщение **\_ Агент находится линии** TAPI отправляется, когда состояние ACD-агента изменяется в строке, в которой открыто приложение.</span><span class="sxs-lookup"><span data-stu-id="8712b-105">The TAPI **LINE\_AGENTSTATUS** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="8712b-106">Приложение может вызвать [**линежетажентстатус**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) , чтобы определить текущее состояние агента.</span><span class="sxs-lookup"><span data-stu-id="8712b-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="8712b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8712b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8712b-108">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="8712b-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="8712b-109">Маркер приложения для линейного устройства, на котором изменилось состояние агента.</span><span class="sxs-lookup"><span data-stu-id="8712b-109">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="8712b-110">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="8712b-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="8712b-111">Экземпляр обратного вызова, указанный при открытии линии вызова.</span><span class="sxs-lookup"><span data-stu-id="8712b-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="8712b-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="8712b-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="8712b-113">Идентификатор адреса в строке, в которой изменилось состояние агента.</span><span class="sxs-lookup"><span data-stu-id="8712b-113">Identifier of the address on the line on which the agent status changed.</span></span> <span data-ttu-id="8712b-114">Идентификатор адреса постоянно связан с адресом; Идентификатор остается постоянным при обновлении операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8712b-114">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="8712b-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="8712b-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="8712b-116">Указывает состояние агента, которое было изменено; может быть сочетанием [**\_ констант линеажентстатус**](lineagentstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="8712b-116">Specifies the agent status that has changed; can be a combination of [**LINEAGENTSTATUS\_ constants**](lineagentstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="8712b-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="8712b-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="8712b-118">Если *dwParam2* включает \_ бит состояния Линеажентстатус, то *dwParam3* указывает новое значение элемента **двстате** в [**линеажентстатус**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span><span class="sxs-lookup"><span data-stu-id="8712b-118">If *dwParam2* includes the LINEAGENTSTATUS\_STATE bit, then *dwParam3* indicates the new value of the **dwState** member in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span></span> <span data-ttu-id="8712b-119">В противном случае этот параметр имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="8712b-119">Otherwise, this parameter is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8712b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8712b-120">Return value</span></span>

<span data-ttu-id="8712b-121">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8712b-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8712b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8712b-122">Remarks</span></span>

<span data-ttu-id="8712b-123">**Строка \_ Агент находится** сообщения не отправляется в приложения, поддерживающие более старые версии TAPI.</span><span class="sxs-lookup"><span data-stu-id="8712b-123">The **LINE\_AGENTSTATUS** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="8712b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8712b-124">Requirements</span></span>



| <span data-ttu-id="8712b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8712b-125">Requirement</span></span> | <span data-ttu-id="8712b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8712b-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8712b-127">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="8712b-127">TAPI version</span></span><br/> | <span data-ttu-id="8712b-128">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8712b-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8712b-129">Header</span><span class="sxs-lookup"><span data-stu-id="8712b-129">Header</span></span><br/>       | <dl> <span data-ttu-id="8712b-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="8712b-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8712b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8712b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8712b-132">**линеажентстатус**</span><span class="sxs-lookup"><span data-stu-id="8712b-132">**LINEAGENTSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[<span data-ttu-id="8712b-133">**линежетажентстатус**</span><span class="sxs-lookup"><span data-stu-id="8712b-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




