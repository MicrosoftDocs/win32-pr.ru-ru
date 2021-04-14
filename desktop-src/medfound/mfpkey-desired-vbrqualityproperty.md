---
description: Задает требуемый уровень качества (1-проходная) для кодирования звуковых потоков с учетом скорости.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: Свойство MFPKEY_DESIRED_VBRQUALITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647287"
---
# <a name="mfpkey_desired_vbrquality-property"></a><span data-ttu-id="a63b0-103">МФПКЭЙ \_ нужное \_ вбркуалити свойство</span><span class="sxs-lookup"><span data-stu-id="a63b0-103">MFPKEY\_DESIRED\_VBRQUALITY Property</span></span>

<span data-ttu-id="a63b0-104">Задает требуемый уровень качества (1-проходная) для кодирования звуковых потоков с учетом скорости.</span><span class="sxs-lookup"><span data-stu-id="a63b0-104">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding of audio streams.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a63b0-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="a63b0-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a63b0-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="a63b0-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="a63b0-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a63b0-107">Data Type</span></span>

<span data-ttu-id="a63b0-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a63b0-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="a63b0-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a63b0-109">Default Value</span></span>

<span data-ttu-id="a63b0-110">0</span><span class="sxs-lookup"><span data-stu-id="a63b0-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="a63b0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a63b0-111">Remarks</span></span>

<span data-ttu-id="a63b0-112">Это значение может быть от 0 до 100, где 100 — максимальное качество.</span><span class="sxs-lookup"><span data-stu-id="a63b0-112">This value can be from 0 to 100, where 100 is maximum quality.</span></span> <span data-ttu-id="a63b0-113">Значение 0 указывает, что метод кодирования VBR с учетом качества не должен использоваться.</span><span class="sxs-lookup"><span data-stu-id="a63b0-113">A value of 0 indicates that the quality-based VBR encoding method is not to be used.</span></span>

<span data-ttu-id="a63b0-114">Чтобы перечислить режимы VBR, соответствующие определенным требованиям к качеству, задайте следующие свойства кодировщика.</span><span class="sxs-lookup"><span data-stu-id="a63b0-114">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="a63b0-115">Задайте для [**мфпкэй \_ Вбренаблед**](mfpkey-vbrenabledproperty.md) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="a63b0-115">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="a63b0-116">Установите для параметра [**мфпкэй \_ ограничение \_ перечисления \_ вбркуалити**](mfpkey-constrain-enumerated-vbrqualityproperty.md) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="a63b0-116">Set [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="a63b0-117">Задайте требуемое качество для **мфпкэй \_ \_ вбркуалити** .</span><span class="sxs-lookup"><span data-stu-id="a63b0-117">Set **MFPKEY\_DESIRED\_VBRQUALITY** to the desired quality.</span></span> <span data-ttu-id="a63b0-118">Для режимов без потерь задайте нужное качество равным 100.</span><span class="sxs-lookup"><span data-stu-id="a63b0-118">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="a63b0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a63b0-119">Requirements</span></span>



| <span data-ttu-id="a63b0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a63b0-120">Requirement</span></span> | <span data-ttu-id="a63b0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a63b0-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a63b0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a63b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a63b0-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a63b0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a63b0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a63b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a63b0-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a63b0-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a63b0-126">Header</span><span class="sxs-lookup"><span data-stu-id="a63b0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a63b0-127"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a63b0-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a63b0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a63b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a63b0-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a63b0-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
