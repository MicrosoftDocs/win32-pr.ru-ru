---
description: Сообщение ТСПИ LINE \_ косинфо заставляет TAPI запустить событие QoS. Дополнительные сведения см. в разделе Иткосевент.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: Сообщение LINE_QOSINFO (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675678"
---
# <a name="line_qosinfo-message"></a><span data-ttu-id="9fc8f-104">Строка \_ сообщения косинфо</span><span class="sxs-lookup"><span data-stu-id="9fc8f-104">LINE\_QOSINFO message</span></span>

<span data-ttu-id="9fc8f-105">Сообщение ТСПИ **Line \_ КОСИНФО** заставляет TAPI запустить событие QoS.</span><span class="sxs-lookup"><span data-stu-id="9fc8f-105">The TSPI **LINE\_QOSINFO** message causes TAPI to fire a QOS event.</span></span> <span data-ttu-id="9fc8f-106">Дополнительные сведения см. в разделе [**иткосевент**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) .</span><span class="sxs-lookup"><span data-stu-id="9fc8f-106">See [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) for additional information.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="9fc8f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="9fc8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fc8f-108">*хтлине*</span><span class="sxs-lookup"><span data-stu-id="9fc8f-108">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc8f-109">Маркер TAPI для линии.</span><span class="sxs-lookup"><span data-stu-id="9fc8f-109">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="9fc8f-110">*хткалл*</span><span class="sxs-lookup"><span data-stu-id="9fc8f-110">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc8f-111">Маркер TAPI для вызова.</span><span class="sxs-lookup"><span data-stu-id="9fc8f-111">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="9fc8f-112">*двмсг*</span><span class="sxs-lookup"><span data-stu-id="9fc8f-112">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc8f-113">Строка значения \_ косинфо.</span><span class="sxs-lookup"><span data-stu-id="9fc8f-113">The value LINE\_QOSINFO.</span></span>

</dd> <dt>

<span data-ttu-id="9fc8f-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="9fc8f-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc8f-115">Член перечислителя [**\_ событий QoS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) , определяющий тип события.</span><span class="sxs-lookup"><span data-stu-id="9fc8f-115">A member of the [**QOS\_EVENT**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) enumerator that identifies the type of event.</span></span>

</dd> <dt>

<span data-ttu-id="9fc8f-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="9fc8f-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc8f-117">Константа [типа мультимедиа](./tapiprotocol--constants.md) , определяющая носитель вызова, связанного с этим событием.</span><span class="sxs-lookup"><span data-stu-id="9fc8f-117">A [media type](./tapiprotocol--constants.md) constant that identifies the media of the call associated with this event.</span></span>

</dd> <dt>

<span data-ttu-id="9fc8f-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="9fc8f-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="9fc8f-119">Не используется.</span><span class="sxs-lookup"><span data-stu-id="9fc8f-119">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9fc8f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="9fc8f-120">Requirements</span></span>



| <span data-ttu-id="9fc8f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="9fc8f-121">Requirement</span></span> | <span data-ttu-id="9fc8f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="9fc8f-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9fc8f-123">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="9fc8f-123">TAPI version</span></span><br/> | <span data-ttu-id="9fc8f-124">Требуется TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="9fc8f-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="9fc8f-125">Header</span><span class="sxs-lookup"><span data-stu-id="9fc8f-125">Header</span></span><br/>       | <dl> <span data-ttu-id="9fc8f-126"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fc8f-126"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fc8f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fc8f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fc8f-128">**событие качества обслуживания \_**</span><span class="sxs-lookup"><span data-stu-id="9fc8f-128">**QOS\_EVENT**</span></span>](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[<span data-ttu-id="9fc8f-129">**иткосевент**</span><span class="sxs-lookup"><span data-stu-id="9fc8f-129">**ITQOSEvent**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

