---
description: Задает уровень качества VBR последнего перечислимого типа выходных данных.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: Свойство MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649077"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a><span data-ttu-id="8644c-103">МФПКЭЙ \_ \_ Последнее \_ перечисленное \_ свойство вбркуалити</span><span class="sxs-lookup"><span data-stu-id="8644c-103">MFPKEY\_MOST\_RECENT\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="8644c-104">Задает уровень качества VBR последнего перечислимого типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8644c-104">Specifies the VBR quality level of the most recently enumerated output type.</span></span> <span data-ttu-id="8644c-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8644c-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8644c-106">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="8644c-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="8644c-107">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="8644c-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8644c-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8644c-108">Data Type</span></span>

<span data-ttu-id="8644c-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="8644c-109">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="8644c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8644c-110">Remarks</span></span>

<span data-ttu-id="8644c-111">Когда кодировщик выступает в качестве Media Foundation преобразования (MFT) и перечисляет тип вывода при вызове [**имфтрансформ:: жетаутпутаваилаблетипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), можно запросить таблицу MFT для свойства **\_ \_ \_ \_ вбркуалити, перечисленного в мфпкэй** .</span><span class="sxs-lookup"><span data-stu-id="8644c-111">When the encoder is acting as an Media Foundation Transform (MFT) and it enumerates an output type on a call to [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="8644c-112">Возвращаемое значение указывает качество VBR последнего возвращенного типа выходного носителя.</span><span class="sxs-lookup"><span data-stu-id="8644c-112">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="8644c-113">Затем это значение можно использовать для задания свойства [**мфпкэй \_ требуемого \_ вбркуалити**](mfpkey-desired-vbrqualityproperty.md) кодировщика.</span><span class="sxs-lookup"><span data-stu-id="8644c-113">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="8644c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="8644c-114">Requirements</span></span>



| <span data-ttu-id="8644c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="8644c-115">Requirement</span></span> | <span data-ttu-id="8644c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="8644c-116">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8644c-117">Клиент</span><span class="sxs-lookup"><span data-stu-id="8644c-117">Client</span></span><br/> | <span data-ttu-id="8644c-118">Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="8644c-118">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="8644c-119">Header</span><span class="sxs-lookup"><span data-stu-id="8644c-119">Header</span></span><br/> | <dl> <span data-ttu-id="8644c-120"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8644c-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8644c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8644c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8644c-122">**МФПКЭЙ \_ вбренаблед**</span><span class="sxs-lookup"><span data-stu-id="8644c-122">**MFPKEY\_VBRENABLED**</span></span>](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[<span data-ttu-id="8644c-123">**МФПКЭЙ \_ ограничение \_ перечисления \_ вбркуалити**</span><span class="sxs-lookup"><span data-stu-id="8644c-123">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="8644c-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8644c-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
