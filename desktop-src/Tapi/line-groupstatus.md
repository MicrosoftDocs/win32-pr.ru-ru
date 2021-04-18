---
description: Сообщение LINE \_ граупстатус отправляется, когда состояние ACD-группы изменяется в обработчике агента, для которого приложение в настоящий момент имеет открытую строку. Это сообщение создается с помощью функции Линепроксимессаже.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: Сообщение LINE_GROUPSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675373"
---
# <a name="line_groupstatus-message"></a><span data-ttu-id="16309-104">Строка \_ сообщения граупстатус</span><span class="sxs-lookup"><span data-stu-id="16309-104">LINE\_GROUPSTATUS message</span></span>

<span data-ttu-id="16309-105">Сообщение **Line \_ граупстатус** отправляется, когда состояние ACD-группы изменяется в обработчике агента, для которого приложение в настоящий момент имеет открытую строку.</span><span class="sxs-lookup"><span data-stu-id="16309-105">The **LINE\_GROUPSTATUS** message is sent when the status of an ACD group changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="16309-106">Это сообщение создается с помощью функции [**линепроксимессаже**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="16309-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="16309-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="16309-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16309-108">*двдевице*</span><span class="sxs-lookup"><span data-stu-id="16309-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="16309-109">Маркер приложения для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="16309-109">The application's handle to the line device.</span></span> <span data-ttu-id="16309-110">Это связано с обработчиком агента.</span><span class="sxs-lookup"><span data-stu-id="16309-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="16309-111">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="16309-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="16309-112">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="16309-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="16309-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="16309-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="16309-114">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="16309-114">Reserved.</span></span> <span data-ttu-id="16309-115">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="16309-115">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="16309-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="16309-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="16309-117">Указывает состояние группы, которое было изменено.</span><span class="sxs-lookup"><span data-stu-id="16309-117">Specifies the group status that has changed.</span></span> <span data-ttu-id="16309-118">Приложение может вызвать [**линежетграуплист**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) для определения изменений в доступных группах.</span><span class="sxs-lookup"><span data-stu-id="16309-118">The application can invoke [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) to determine the changes in available groups.</span></span> <span data-ttu-id="16309-119">Параметр *dwParam2* является одной или несколькими [**\_ константами линеграупстатус**](linegroupstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="16309-119">The *dwParam2* parameter is one or more of the [**LINEGROUPSTATUS\_ constants**](linegroupstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="16309-120">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="16309-120">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="16309-121">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="16309-121">Reserved.</span></span> <span data-ttu-id="16309-122">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="16309-122">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16309-123">Требования</span><span class="sxs-lookup"><span data-stu-id="16309-123">Requirements</span></span>



| <span data-ttu-id="16309-124">Требование</span><span class="sxs-lookup"><span data-stu-id="16309-124">Requirement</span></span> | <span data-ttu-id="16309-125">Значение</span><span class="sxs-lookup"><span data-stu-id="16309-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="16309-126">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="16309-126">TAPI version</span></span><br/> | <span data-ttu-id="16309-127">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="16309-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="16309-128">Header</span><span class="sxs-lookup"><span data-stu-id="16309-128">Header</span></span><br/>       | <dl> <span data-ttu-id="16309-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="16309-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16309-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16309-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16309-131">**линежетграуплист**</span><span class="sxs-lookup"><span data-stu-id="16309-131">**lineGetGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




