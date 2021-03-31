---
description: Указывает число проходов кодирования, поддерживаемых кодировщиком.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Свойство Авенккоммонмултипассмоде (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895021"
---
# <a name="avenccommonmultipassmode-property"></a><span data-ttu-id="d63bb-103">Авенккоммонмултипассмоде, свойство</span><span class="sxs-lookup"><span data-stu-id="d63bb-103">AVEncCommonMultipassMode property</span></span>

<span data-ttu-id="d63bb-104">Указывает число проходов кодирования, поддерживаемых кодировщиком.</span><span class="sxs-lookup"><span data-stu-id="d63bb-104">Specifies the number of encoding passes that the encoder supports.</span></span>

<span data-ttu-id="d63bb-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d63bb-105">This property is read-only.</span></span>

## <a name="data-type"></a><span data-ttu-id="d63bb-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d63bb-106">Data type</span></span>

<span data-ttu-id="d63bb-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="d63bb-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d63bb-108">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="d63bb-108">Property GUID</span></span>

<span data-ttu-id="d63bb-109">**КОДЕКАПИ \_ авенккоммонмултипассмоде**</span><span class="sxs-lookup"><span data-stu-id="d63bb-109">**CODECAPI\_AVEncCommonMultipassMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="d63bb-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d63bb-110">Property value</span></span>

<span data-ttu-id="d63bb-111">Это свойство возвращается в виде диапазона значений.</span><span class="sxs-lookup"><span data-stu-id="d63bb-111">This property is returned as a range of values.</span></span> <span data-ttu-id="d63bb-112">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="d63bb-112">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="d63bb-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d63bb-113">Remarks</span></span>

<span data-ttu-id="d63bb-114">Задержка декодирования определяется как объем данных, которые декодер должен забуферировать.</span><span class="sxs-lookup"><span data-stu-id="d63bb-114">Decoding latency is defined as the amount of data the decoder must buffer.</span></span> <span data-ttu-id="d63bb-115">Например, установка этого свойства в значение **\_ true** в кодировщике видео MPEG ОГРАНИЧИВАЕТ типы структур GOP, которые может использовать кодировщик.</span><span class="sxs-lookup"><span data-stu-id="d63bb-115">For example, setting this property to **VARIANT\_TRUE** on an MPEG video encoder limits the types of GOP structures the encoder can use.</span></span>

<span data-ttu-id="d63bb-116">Чтобы задать текущий проход кодировки, задайте свойство [**авенккоммонпассстарт**](avenccommonpassstart-property.md) .</span><span class="sxs-lookup"><span data-stu-id="d63bb-116">To set the current encoding pass, set the [**AVEncCommonPassStart**](avenccommonpassstart-property.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d63bb-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d63bb-117">Requirements</span></span>



| <span data-ttu-id="d63bb-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d63bb-118">Requirement</span></span> | <span data-ttu-id="d63bb-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d63bb-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d63bb-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d63bb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d63bb-121">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d63bb-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="d63bb-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d63bb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d63bb-123">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="d63bb-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d63bb-124">Header</span><span class="sxs-lookup"><span data-stu-id="d63bb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d63bb-125"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="d63bb-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d63bb-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d63bb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d63bb-127">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="d63bb-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="d63bb-128">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="d63bb-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




