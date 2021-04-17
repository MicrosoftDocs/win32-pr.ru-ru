---
description: Указывает интервал времени, в течение которого применяется средняя скорость. Это свойство используется в сочетании со свойством Авенккоммонмеанбитрате.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Свойство Авенккоммонмеанбитратеинтервал (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495645"
---
# <a name="avenccommonmeanbitrateinterval-property"></a><span data-ttu-id="ee58d-104">Авенккоммонмеанбитратеинтервал, свойство</span><span class="sxs-lookup"><span data-stu-id="ee58d-104">AVEncCommonMeanBitRateInterval property</span></span>

<span data-ttu-id="ee58d-105">Указывает интервал времени, в течение которого применяется средняя скорость.</span><span class="sxs-lookup"><span data-stu-id="ee58d-105">Specifies the time interval over which the average bit rate applies.</span></span> <span data-ttu-id="ee58d-106">Это свойство используется в сочетании со свойством [**авенккоммонмеанбитрате**](avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="ee58d-106">This property is used in conjunction with the [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property.</span></span>

<span data-ttu-id="ee58d-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ee58d-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ee58d-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ee58d-108">Data type</span></span>

<span data-ttu-id="ee58d-109">**UINT64** (**VT \_ UI8**)</span><span class="sxs-lookup"><span data-stu-id="ee58d-109">**UINT64** (**VT\_UI8**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ee58d-110">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="ee58d-110">Property GUID</span></span>

<span data-ttu-id="ee58d-111">**КОДЕКАПИ \_ авенккоммонмеанбитратеинтервал**</span><span class="sxs-lookup"><span data-stu-id="ee58d-111">**CODECAPI\_AVEncCommonMeanBitRateInterval**</span></span>

## <a name="property-value"></a><span data-ttu-id="ee58d-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ee58d-112">Property value</span></span>

<span data-ttu-id="ee58d-113">Это свойство имеет линейный Диапазон значений.</span><span class="sxs-lookup"><span data-stu-id="ee58d-113">This property has a linear range of values.</span></span> <span data-ttu-id="ee58d-114">Чтобы получить поддерживаемый диапазон, вызовите метод [**икодекапи:: жетпараметерранже**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="ee58d-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee58d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee58d-115">Remarks</span></span>

<span data-ttu-id="ee58d-116">Для кодирования с переменной скоростью с двумя проходами (VBR) нулевое значение указывает, что интервал времени является всей длительностью содержимого.</span><span class="sxs-lookup"><span data-stu-id="ee58d-116">For two-pass variable bit rate (VBR) encoding, the value zero indicates that the time interval is the entire duration of the content.</span></span> <span data-ttu-id="ee58d-117">Для кодировки постоянной однопроходной скорости (CBR) значение ноль указывает, что кодировщик выбирает интервал (обычно 0,5 секунд).</span><span class="sxs-lookup"><span data-stu-id="ee58d-117">For single-pass constant bit rate (CBR) encoding, the value zero indicates that the encoder selects the interval (typically 0.5 seconds).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee58d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ee58d-118">Requirements</span></span>



| <span data-ttu-id="ee58d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ee58d-119">Requirement</span></span> | <span data-ttu-id="ee58d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ee58d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ee58d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee58d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ee58d-122">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ee58d-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ee58d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee58d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ee58d-124">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="ee58d-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ee58d-125">Header</span><span class="sxs-lookup"><span data-stu-id="ee58d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee58d-126"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee58d-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee58d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee58d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee58d-128">Свойства кодека API</span><span class="sxs-lookup"><span data-stu-id="ee58d-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ee58d-129">**Интерфейс Икодекапи**</span><span class="sxs-lookup"><span data-stu-id="ee58d-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




