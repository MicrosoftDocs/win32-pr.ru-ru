---
description: Указывает, копирует ли Media Foundation преобразование (MFT) атрибуты из входных образцов в выходные.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: Свойство MFPKEY_EXATTRIBUTE_SUPPORTED (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908779"
---
# <a name="mfpkey_exattribute_supported-property"></a><span data-ttu-id="c23fb-103">МФПКЭЙ \_ ексаттрибуте \_ поддерживаемое свойство</span><span class="sxs-lookup"><span data-stu-id="c23fb-103">MFPKEY\_EXATTRIBUTE\_SUPPORTED property</span></span>

<span data-ttu-id="c23fb-104">Указывает, копирует ли Media Foundation преобразование (MFT) атрибуты из входных образцов в выходные.</span><span class="sxs-lookup"><span data-stu-id="c23fb-104">Specifies whether a Media Foundation transform (MFT) copies attributes from input samples to output samples.</span></span>



<span data-ttu-id="c23fb-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c23fb-105">Data type</span></span>

<span data-ttu-id="c23fb-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="c23fb-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c23fb-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="c23fb-107">PROPVARIANT member</span></span>

<span data-ttu-id="c23fb-108">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c23fb-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="c23fb-109">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="c23fb-109">VT\_BOOL</span></span>

<span data-ttu-id="c23fb-110">**булвал**</span><span class="sxs-lookup"><span data-stu-id="c23fb-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c23fb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c23fb-111">Remarks</span></span>

<span data-ttu-id="c23fb-112">Этот атрибут может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c23fb-112">This attribute can have the following values.</span></span>



| <span data-ttu-id="c23fb-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c23fb-113">Value</span></span>              | <span data-ttu-id="c23fb-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c23fb-114">Description</span></span>                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c23fb-115">**ВАРИАНТ \_ true**</span><span class="sxs-lookup"><span data-stu-id="c23fb-115">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="c23fb-116">MFT копирует атрибуты из входных примеров в выходные образцы.</span><span class="sxs-lookup"><span data-stu-id="c23fb-116">The MFT copies attributes from the input samples to the output samples.</span></span>                                                                                 |
| <span data-ttu-id="c23fb-117">**ВАРИАНТ \_ false**</span><span class="sxs-lookup"><span data-stu-id="c23fb-117">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="c23fb-118">Сеанс мультимедиа копирует атрибуты из входных примеров в выходные образцы.</span><span class="sxs-lookup"><span data-stu-id="c23fb-118">The Media Session copies attributes from input samples to output samples.</span></span> <span data-ttu-id="c23fb-119">Он не перезаписывает никакие атрибуты, которые задаются MFT в выходных образцах.</span><span class="sxs-lookup"><span data-stu-id="c23fb-119">It does not overwrite any attributes that the MFT sets on the output samples.</span></span> |



 

<span data-ttu-id="c23fb-120">Чтобы получить этот атрибут, вызовите **QueryInterface** в MFT для интерфейса **ипропертисторе** .</span><span class="sxs-lookup"><span data-stu-id="c23fb-120">To get this attribute, call **QueryInterface** on the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="c23fb-121">Значение по умолчанию — **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="c23fb-121">The default value is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="c23fb-122">Если таблица MFT не предоставляет интерфейс **ипропертисторе** или если это свойство не задано, то следует рассматривать значение как **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="c23fb-122">If the MFT does not expose the **IPropertyStore** interface, or if this property is not set, treat the value as **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="c23fb-123">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c23fb-123">This property is read-only.</span></span>

> [!NOTE] 
> <span data-ttu-id="c23fb-124">Этот атрибут не применяется к асинхронному МФТС.</span><span class="sxs-lookup"><span data-stu-id="c23fb-124">This attribute does not apply to asynchronous MFTs.</span></span> <span data-ttu-id="c23fb-125">Атрибуты не будут скопированы из входных примеров в выходные данные для асинхронного МФТС, независимо от значения этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="c23fb-125">Attributes will not be copied from the input samples to the output samples for asynchronous MFTs, regardless of the value of this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="c23fb-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="c23fb-126">Examples</span></span>

<span data-ttu-id="c23fb-127">В следующем примере возвращается значение VARIANT \_ true, если в MFT копируются образцы атрибутов.</span><span class="sxs-lookup"><span data-stu-id="c23fb-127">The following example returns VARIANT\_TRUE if an MFT copies sample attributes.</span></span>


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a><span data-ttu-id="c23fb-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c23fb-128">Requirements</span></span>



| <span data-ttu-id="c23fb-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c23fb-129">Requirement</span></span> | <span data-ttu-id="c23fb-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c23fb-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c23fb-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c23fb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c23fb-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c23fb-132">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c23fb-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c23fb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c23fb-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c23fb-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c23fb-135">Header</span><span class="sxs-lookup"><span data-stu-id="c23fb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c23fb-136"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="c23fb-136"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c23fb-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c23fb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c23fb-138">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c23fb-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c23fb-139">Примеры атрибутов</span><span class="sxs-lookup"><span data-stu-id="c23fb-139">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="c23fb-140">**Имфтрансформ::P Роцессаутпут**</span><span class="sxs-lookup"><span data-stu-id="c23fb-140">**IMFTransform::ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




