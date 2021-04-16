---
description: Получает метрики качества при отмене акустического эха (AEC) из схемы DSP для записи голоса.
ms.assetid: de2e86ae-0469-471f-9105-0bb38a59b428
title: Свойство MFPKEY_WMAAECMA_QUALITY_METRICS (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3740630bc23c4e3e0e824e55b4e34bcd8b1347f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692597"
---
# <a name="mfpkey_wmaaecma_quality_metrics-property"></a><span data-ttu-id="9e0d5-103">\_ \_ Свойство МЕТРИК качества мфпкэй вмааекма \_</span><span class="sxs-lookup"><span data-stu-id="9e0d5-103">MFPKEY\_WMAAECMA\_QUALITY\_METRICS Property</span></span>

<span data-ttu-id="9e0d5-104">Получает метрики качества при отмене акустического эха (AEC) из схемы DSP для записи голоса.</span><span class="sxs-lookup"><span data-stu-id="9e0d5-104">Retrieves quality metrics on acoustic echo cancellation (AEC) from the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9e0d5-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="9e0d5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9e0d5-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="9e0d5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="9e0d5-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9e0d5-107">Data Type</span></span>

<span data-ttu-id="9e0d5-108">\_большой двоичный объект VT</span><span class="sxs-lookup"><span data-stu-id="9e0d5-108">VT\_BLOB</span></span>

## <a name="remarks"></a><span data-ttu-id="9e0d5-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e0d5-109">Remarks</span></span>

<span data-ttu-id="9e0d5-110">Значением этого свойства является структура [ \_ структуры аеккуалитиметрикс](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) .</span><span class="sxs-lookup"><span data-stu-id="9e0d5-110">The value of this property is an [AecQualityMetrics\_Struct](/windows/win32/api/wmcodecdsp/ns-wmcodecdsp-aecqualitymetrics_struct) structure.</span></span> <span data-ttu-id="9e0d5-111">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9e0d5-111">This property is read-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e0d5-112">Требования</span><span class="sxs-lookup"><span data-stu-id="9e0d5-112">Requirements</span></span>



| <span data-ttu-id="9e0d5-113">Требование</span><span class="sxs-lookup"><span data-stu-id="9e0d5-113">Requirement</span></span> | <span data-ttu-id="9e0d5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9e0d5-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e0d5-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e0d5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9e0d5-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e0d5-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9e0d5-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e0d5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9e0d5-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e0d5-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9e0d5-119">Header</span><span class="sxs-lookup"><span data-stu-id="9e0d5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e0d5-120"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e0d5-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e0d5-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e0d5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e0d5-122">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e0d5-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="9e0d5-123">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="9e0d5-123">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
