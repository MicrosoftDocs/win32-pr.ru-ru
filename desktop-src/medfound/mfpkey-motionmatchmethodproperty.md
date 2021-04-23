---
description: Указывает метод, используемый для сопоставления движения.
ms.assetid: 75bbc189-3092-4813-9f45-54e8e48b05cd
title: Свойство MFPKEY_MOTIONMATCHMETHOD (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09496e714633dd394f55122b7461f29a2daa3656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991603"
---
# <a name="mfpkey_motionmatchmethod-property"></a><span data-ttu-id="81473-103">МФПКЭЙ \_ мотионматчмесод, свойство</span><span class="sxs-lookup"><span data-stu-id="81473-103">MFPKEY\_MOTIONMATCHMETHOD Property</span></span>

<span data-ttu-id="81473-104">Указывает метод, используемый для сопоставления движения.</span><span class="sxs-lookup"><span data-stu-id="81473-104">Specifies the method to use for motion matching.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="81473-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="81473-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="81473-106">g \_ всзвмвкмотионматчмесод</span><span class="sxs-lookup"><span data-stu-id="81473-106">g\_wszWMVCMotionMatchMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="81473-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="81473-107">Data Type</span></span>

<span data-ttu-id="81473-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="81473-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="81473-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="81473-109">Default Value</span></span>

<span data-ttu-id="81473-110">0</span><span class="sxs-lookup"><span data-stu-id="81473-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="81473-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="81473-111">Remarks</span></span>

<span data-ttu-id="81473-112">Для этого свойства можно задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="81473-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="81473-113">Значение</span><span class="sxs-lookup"><span data-stu-id="81473-113">Value</span></span> | <span data-ttu-id="81473-114">Используемый метод</span><span class="sxs-lookup"><span data-stu-id="81473-114">Method used</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="81473-115">0</span><span class="sxs-lookup"><span data-stu-id="81473-115">0</span></span>     | <span data-ttu-id="81473-116">Сумма абсолютных различий (SAD)</span><span class="sxs-lookup"><span data-stu-id="81473-116">sum of absolute differences (SAD)</span></span> |
| <span data-ttu-id="81473-117">1</span><span class="sxs-lookup"><span data-stu-id="81473-117">1</span></span>     | <span data-ttu-id="81473-118">Hadamard</span><span class="sxs-lookup"><span data-stu-id="81473-118">Hadamard</span></span>                          |
| <span data-ttu-id="81473-119">-1</span><span class="sxs-lookup"><span data-stu-id="81473-119">-1</span></span>    | <span data-ttu-id="81473-120">Макроблокк — адаптивный.</span><span class="sxs-lookup"><span data-stu-id="81473-120">Macroblock-adaptive.</span></span>              |



 

<span data-ttu-id="81473-121">Сумма абсолютных различий (SAD) — это более быстрый, но менее точный метод, чем преобразование Хадамард.</span><span class="sxs-lookup"><span data-stu-id="81473-121">The sum of absolute differences (SAD) is a faster but less accurate method than the Hadamard transform.</span></span> <span data-ttu-id="81473-122">Преобразование Хадамард является более точным, но трудоемким.</span><span class="sxs-lookup"><span data-stu-id="81473-122">The Hadamard transform is more accurate but computationally intensive.</span></span> <span data-ttu-id="81473-123">Адаптивный режим макроблокк обеспечивает адекватный компромисс между двумя методами путем динамического выбора между двумя преобразованиями, выбирая преобразование Хадамард только при необходимости.</span><span class="sxs-lookup"><span data-stu-id="81473-123">The macroblock-adaptive mode provides a reasonable compromise between the two methods by dynamically choosing between the two transforms, selecting the Hadamard transform only when appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="81473-124">Требования</span><span class="sxs-lookup"><span data-stu-id="81473-124">Requirements</span></span>



| <span data-ttu-id="81473-125">Требование</span><span class="sxs-lookup"><span data-stu-id="81473-125">Requirement</span></span> | <span data-ttu-id="81473-126">Значение</span><span class="sxs-lookup"><span data-stu-id="81473-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81473-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81473-127">Minimum supported client</span></span><br/> | <span data-ttu-id="81473-128">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="81473-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="81473-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81473-129">Minimum supported server</span></span><br/> | <span data-ttu-id="81473-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81473-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81473-131">Header</span><span class="sxs-lookup"><span data-stu-id="81473-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="81473-132"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="81473-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81473-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81473-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81473-134">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="81473-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




