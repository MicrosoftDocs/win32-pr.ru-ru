---
description: Указывает минимальную скорость в битах в секунду. Это свойство применяется только к режимам кодирования с постоянным битом (CBR) и переменной скоростью с переменным битом (VBR).
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: Свойство Авенккоммонминбитрате (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c9b6e84675994d2aca7548f6c13d6558ebc020
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682310"
---
# <a name="avenccommonminbitrate-property"></a><span data-ttu-id="0acd2-104">Авенккоммонминбитрате, свойство</span><span class="sxs-lookup"><span data-stu-id="0acd2-104">AVEncCommonMinBitRate property</span></span>

<span data-ttu-id="0acd2-105">Указывает минимальную скорость в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="0acd2-105">Specifies the minimum bit rate, in bits per second.</span></span> <span data-ttu-id="0acd2-106">Это свойство применяется только к режимам кодирования с постоянным битом (CBR) и переменной скоростью с переменным битом (VBR).</span><span class="sxs-lookup"><span data-stu-id="0acd2-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="0acd2-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="0acd2-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="0acd2-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0acd2-108">Data type</span></span>

<span data-ttu-id="0acd2-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="0acd2-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="0acd2-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="0acd2-110">Property GUID</span></span>

<span data-ttu-id="0acd2-111">**КОДЕКАПИ \_ авенккоммонминбитрате**</span><span class="sxs-lookup"><span data-stu-id="0acd2-111">**CODECAPI\_AVEncCommonMinBitRate**</span></span>

## <a name="property-value"></a><span data-ttu-id="0acd2-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0acd2-112">Property value</span></span>

<span data-ttu-id="0acd2-113">Это свойство имеет линейный Диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="0acd2-113">This property has a linear range of values.</span></span> <span data-ttu-id="0acd2-114">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="0acd2-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="0acd2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0acd2-115">Remarks</span></span>

<span data-ttu-id="0acd2-116">Кодировщик применяет минимальную скорость, увеличивая качество кодирования по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="0acd2-116">The encoder enforces the minimum bit rate by increasing the encoding quality as necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="0acd2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="0acd2-117">Requirements</span></span>



| <span data-ttu-id="0acd2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="0acd2-118">Requirement</span></span> | <span data-ttu-id="0acd2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="0acd2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0acd2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0acd2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0acd2-121">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0acd2-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0acd2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0acd2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0acd2-123">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="0acd2-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0acd2-124">Header</span><span class="sxs-lookup"><span data-stu-id="0acd2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0acd2-125"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="0acd2-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0acd2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0acd2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0acd2-127">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="0acd2-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="0acd2-128">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="0acd2-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




