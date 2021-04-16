---
description: Включает или отключает докладчика, заполняя аудио-декодер или обработчик цифровых сигналов (DSP).
ms.assetid: 5a42d4c9-d593-4d7f-bfee-37271c48e5cf
title: Свойство Авдспспеакерфилл (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16bcdda053439b76c9445f2f9c866ee26afb4858
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655611"
---
# <a name="avdspspeakerfill-property"></a><span data-ttu-id="b7cdd-103">Авдспспеакерфилл, свойство</span><span class="sxs-lookup"><span data-stu-id="b7cdd-103">AVDSPSpeakerFill property</span></span>

<span data-ttu-id="b7cdd-104">Включает или отключает докладчика, заполняя аудио-декодер или обработчик цифровых сигналов (DSP).</span><span class="sxs-lookup"><span data-stu-id="b7cdd-104">Enables or disables speaker fill in an audio decoder or digital signal processor (DSP).</span></span>

<span data-ttu-id="b7cdd-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b7cdd-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b7cdd-106">Data type</span></span>

<span data-ttu-id="b7cdd-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b7cdd-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b7cdd-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="b7cdd-108">Property GUID</span></span>

<span data-ttu-id="b7cdd-109">**КОДЕКАПИ \_ авдспспеакерфилл**</span><span class="sxs-lookup"><span data-stu-id="b7cdd-109">**CODECAPI\_AVDSPSpeakerFill**</span></span>

## <a name="property-value"></a><span data-ttu-id="b7cdd-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b7cdd-110">Property value</span></span>

<span data-ttu-id="b7cdd-111">Значение этого свойства является членом перечисления [**еавдспспеакерфилл**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill) .</span><span class="sxs-lookup"><span data-stu-id="b7cdd-111">The value of this property is a member of the [**eAVDSPSpeakerFill**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7cdd-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b7cdd-112">Remarks</span></span>

<span data-ttu-id="b7cdd-113">Заливка докладчика — это процесс DSP, который преобразует моно или стерео-аудио в многоканальный звук.</span><span class="sxs-lookup"><span data-stu-id="b7cdd-113">Speaker fill is a DSP process that converts mono or stereo audio into multichannel audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7cdd-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b7cdd-114">Requirements</span></span>



| <span data-ttu-id="b7cdd-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b7cdd-115">Requirement</span></span> | <span data-ttu-id="b7cdd-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b7cdd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7cdd-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7cdd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7cdd-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b7cdd-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b7cdd-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7cdd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7cdd-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="b7cdd-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b7cdd-121">Header</span><span class="sxs-lookup"><span data-stu-id="b7cdd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7cdd-122"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7cdd-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7cdd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7cdd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7cdd-124">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="b7cdd-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b7cdd-125">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="b7cdd-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




