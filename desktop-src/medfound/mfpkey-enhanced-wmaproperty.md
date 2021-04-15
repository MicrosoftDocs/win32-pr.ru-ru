---
description: Указывает, использует ли основной кодировщик &\# 0034; Плюс&\# 0034;.
ms.assetid: 1ace09da-7dee-469e-a533-63b40ac747ab
title: Свойство MFPKEY_ENHANCED_WMA (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df1c7ddc0e7bfb6d62d51e535f10b257eac6f2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649106"
---
# <a name="mfpkey_enhanced_wma-property"></a><span data-ttu-id="a456c-103">МФПКЭЙ \_ Расширенное \_ свойство WMA</span><span class="sxs-lookup"><span data-stu-id="a456c-103">MFPKEY\_ENHANCED\_WMA Property</span></span>

<span data-ttu-id="a456c-104">Указывает, использует ли основной кодировщик функцию "плюс".</span><span class="sxs-lookup"><span data-stu-id="a456c-104">Specifies whether the core encoder uses the "Plus" feature.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a456c-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="a456c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a456c-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="a456c-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="a456c-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a456c-107">Data Type</span></span>

<span data-ttu-id="a456c-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="a456c-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="a456c-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a456c-109">Default Value</span></span>

<span data-ttu-id="a456c-110">0</span><span class="sxs-lookup"><span data-stu-id="a456c-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="a456c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a456c-111">Remarks</span></span>

<span data-ttu-id="a456c-112">Это свойство доступно только для Windows Media Audio без потерь.</span><span class="sxs-lookup"><span data-stu-id="a456c-112">This property is available only for Windows Media Audio Lossless.</span></span>

<span data-ttu-id="a456c-113">Если оставить это свойство со значением по умолчанию 0 или установить его равным 1, основной кодировщик решит, следует ли использовать часть "плюс".</span><span class="sxs-lookup"><span data-stu-id="a456c-113">If you leave this property at its default value of 0, or if you set it to 1, the core encoder decides whether the "Plus" portion should be used.</span></span> <span data-ttu-id="a456c-114">Если задать для этого свойства значение 2, то основной кодировщик не будет использовать функцию "плюс".</span><span class="sxs-lookup"><span data-stu-id="a456c-114">If you set this property to 2, the core encoder does not use the "Plus" feature.</span></span>

<span data-ttu-id="a456c-115">Это свойство изменяет перечислимые типы носителей, поэтому, если оно задано, необходимо сделать это, прежде чем задавать тип выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a456c-115">This property alters the enumerated media types, so if you set it, you must do so before you set the output type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a456c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a456c-116">Requirements</span></span>



| <span data-ttu-id="a456c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a456c-117">Requirement</span></span> | <span data-ttu-id="a456c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a456c-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a456c-119">Клиент</span><span class="sxs-lookup"><span data-stu-id="a456c-119">Client</span></span><br/> | <span data-ttu-id="a456c-120">Windows Vista или Windows 7</span><span class="sxs-lookup"><span data-stu-id="a456c-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="a456c-121">Header</span><span class="sxs-lookup"><span data-stu-id="a456c-121">Header</span></span><br/> | <dl> <span data-ttu-id="a456c-122"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a456c-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a456c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a456c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a456c-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a456c-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
