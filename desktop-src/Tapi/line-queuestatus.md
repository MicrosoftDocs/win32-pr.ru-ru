---
description: Сообщение LINE \_ QUEUESTATUS отправляется при изменении состояния ACD-очереди в обработчике агента, для которого приложение в настоящий момент имеет открытую строку. Это сообщение создается с помощью функции Линепроксимессаже.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: Сообщение LINE_QUEUESTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688925"
---
# <a name="line_queuestatus-message"></a><span data-ttu-id="44d79-104">Строка \_ сообщения QUEUESTATUS</span><span class="sxs-lookup"><span data-stu-id="44d79-104">LINE\_QUEUESTATUS message</span></span>

<span data-ttu-id="44d79-105">Сообщение **Line \_ QUEUESTATUS** отправляется при изменении состояния ACD-очереди в обработчике агента, для которого приложение в настоящий момент имеет открытую строку.</span><span class="sxs-lookup"><span data-stu-id="44d79-105">The **LINE\_QUEUESTATUS** message is sent when the status of an ACD queue changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="44d79-106">Это сообщение создается с помощью функции [**линепроксимессаже**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="44d79-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="44d79-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="44d79-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d79-108">*двдевице*</span><span class="sxs-lookup"><span data-stu-id="44d79-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="44d79-109">Маркер приложения для линейного устройства.</span><span class="sxs-lookup"><span data-stu-id="44d79-109">The application's handle to the line device.</span></span> <span data-ttu-id="44d79-110">Это связано с обработчиком агента.</span><span class="sxs-lookup"><span data-stu-id="44d79-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-111">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="44d79-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="44d79-112">Экземпляр обратного вызова, указанный при открытии строки.</span><span class="sxs-lookup"><span data-stu-id="44d79-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="44d79-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="44d79-114">Идентификатор очереди, состояние которой изменилось.</span><span class="sxs-lookup"><span data-stu-id="44d79-114">The identifier of the queue whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="44d79-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="44d79-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="44d79-116">Указывает состояние очереди, которое было изменено.</span><span class="sxs-lookup"><span data-stu-id="44d79-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="44d79-117">Может быть одной или несколькими [**\_ константами линекуеуестатус**](linequeuestatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="44d79-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="44d79-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="44d79-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="44d79-119">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="44d79-119">Reserved.</span></span> <span data-ttu-id="44d79-120">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="44d79-120">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44d79-121">Требования</span><span class="sxs-lookup"><span data-stu-id="44d79-121">Requirements</span></span>



| <span data-ttu-id="44d79-122">Требование</span><span class="sxs-lookup"><span data-stu-id="44d79-122">Requirement</span></span> | <span data-ttu-id="44d79-123">Значение</span><span class="sxs-lookup"><span data-stu-id="44d79-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="44d79-124">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="44d79-124">TAPI version</span></span><br/> | <span data-ttu-id="44d79-125">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="44d79-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="44d79-126">Header</span><span class="sxs-lookup"><span data-stu-id="44d79-126">Header</span></span><br/>       | <dl> <span data-ttu-id="44d79-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="44d79-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d79-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44d79-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d79-129">**линепроксимессаже**</span><span class="sxs-lookup"><span data-stu-id="44d79-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




