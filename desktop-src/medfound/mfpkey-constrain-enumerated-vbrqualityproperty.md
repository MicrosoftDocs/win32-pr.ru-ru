---
description: Указывает, лиметед ли режимы, перечисленные кодировщиком, с требованиями к качеству, заданными МФПКЭЙ \_ требуемым \_ вбркуалити.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: Свойство MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699229"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a><span data-ttu-id="bd23f-103">МФПКЭЙ \_ ограничить \_ перечислимое \_ свойство вбркуалити</span><span class="sxs-lookup"><span data-stu-id="bd23f-103">MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="bd23f-104">Указывает, лиметед ли режимы, перечисленные кодировщиком, с требованиями к качеству, заданными [**мфпкэй \_ требуемым \_ вбркуалити**](mfpkey-desired-vbrqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="bd23f-104">Specifies whether modes enumerated by the encoder are limeted to those that meet a quality requirement given by [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="bd23f-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="bd23f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="bd23f-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="bd23f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="bd23f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bd23f-107">Data Type</span></span>

<span data-ttu-id="bd23f-108">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="bd23f-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="bd23f-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="bd23f-109">Default Value</span></span>

<span data-ttu-id="bd23f-110">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="bd23f-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="bd23f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd23f-111">Remarks</span></span>

<span data-ttu-id="bd23f-112">Чтобы перечислить режимы VBR, соответствующие определенным требованиям к качеству, задайте следующие свойства кодировщика.</span><span class="sxs-lookup"><span data-stu-id="bd23f-112">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="bd23f-113">Задайте для [**мфпкэй \_ Вбренаблед**](mfpkey-vbrenabledproperty.md) значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="bd23f-113">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="bd23f-114">Установите для параметра **мфпкэй \_ ограничение \_ перечисления \_ вбркуалити** значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="bd23f-114">Set **MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY** to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="bd23f-115">Задайте требуемое качество для [**мфпкэй \_ \_ вбркуалити**](mfpkey-desired-vbrqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="bd23f-115">Set [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) to the desired quality.</span></span> <span data-ttu-id="bd23f-116">Для режимов без потерь задайте нужное качество равным 100.</span><span class="sxs-lookup"><span data-stu-id="bd23f-116">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd23f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bd23f-117">Requirements</span></span>



| <span data-ttu-id="bd23f-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bd23f-118">Requirement</span></span> | <span data-ttu-id="bd23f-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bd23f-119">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd23f-120">Клиент</span><span class="sxs-lookup"><span data-stu-id="bd23f-120">Client</span></span><br/> | <span data-ttu-id="bd23f-121">Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="bd23f-121">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="bd23f-122">Header</span><span class="sxs-lookup"><span data-stu-id="bd23f-122">Header</span></span><br/> | <dl> <span data-ttu-id="bd23f-123"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd23f-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd23f-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd23f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd23f-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bd23f-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
