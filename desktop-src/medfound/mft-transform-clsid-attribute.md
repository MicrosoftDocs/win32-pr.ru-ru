---
description: Содержит идентификатор класса (CLSID) Media Foundation преобразования (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: Атрибут MFT_TRANSFORM_CLSID_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991424"
---
# <a name="mft_transform_clsid_attribute-attribute"></a><span data-ttu-id="bdc1d-103">\_ \_ Атрибут атрибута CLSID преобразования MFT \_</span><span class="sxs-lookup"><span data-stu-id="bdc1d-103">MFT\_TRANSFORM\_CLSID\_Attribute attribute</span></span>

<span data-ttu-id="bdc1d-104">Содержит идентификатор класса (CLSID) Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="bdc1d-104">Contains the class identifier (CLSID) of a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="bdc1d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="bdc1d-105">Data type</span></span>

<span data-ttu-id="bdc1d-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="bdc1d-106">**GUID**</span></span>

## <a name="getset"></a><span data-ttu-id="bdc1d-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="bdc1d-107">Get/set</span></span>

<span data-ttu-id="bdc1d-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)InAttribute.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-108">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="bdc1d-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="bdc1d-109">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="bdc1d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bdc1d-110">Remarks</span></span>

<span data-ttu-id="bdc1d-111">Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="bdc1d-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="bdc1d-112">Этот атрибут используется внутренне объектом активации при создании таблицы MFT.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-112">This attribute is used internally by the activation object when it creates the MFT.</span></span> <span data-ttu-id="bdc1d-113">Приложения не должны использовать этот CLSID напрямую для создания MFT, так как объекту активации может потребоваться инициализация MFT.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-113">Applications should not use this CLSID directly to create the MFT, because the activation object might need to initialize the MFT.</span></span> <span data-ttu-id="bdc1d-114">Таким образом, чтобы создать экземпляр MFT, вызовите [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) в объекте активации.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-114">Therefore, to create an instance of the MFT, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the activation object.</span></span>

<span data-ttu-id="bdc1d-115">Обратите внимание, что функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) работает иначе, чем функция [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) в этом отношении.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-115">Note that the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function behaves differently than the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function in this respect.</span></span> <span data-ttu-id="bdc1d-116">Функция **мфтенум** возвращает идентификаторы CLSID, которые приложение передает в функцию **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="bdc1d-116">The **MFTEnum** function returns CLSIDs, which the application passes to the **CoCreateInstance** function.</span></span> <span data-ttu-id="bdc1d-117">Функция **мфтенумекс** возвращает объекты активации, а не CLSID.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-117">The **MFTEnumEx** function returns activation objects rather than CLSIDs.</span></span>

<span data-ttu-id="bdc1d-118">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="bdc1d-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc1d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bdc1d-119">Requirements</span></span>



| <span data-ttu-id="bdc1d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bdc1d-120">Requirement</span></span> | <span data-ttu-id="bdc1d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bdc1d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc1d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bdc1d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc1d-123">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="bdc1d-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="bdc1d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bdc1d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc1d-125">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="bdc1d-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="bdc1d-126">Header</span><span class="sxs-lookup"><span data-stu-id="bdc1d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc1d-127"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdc1d-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc1d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bdc1d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc1d-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bdc1d-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bdc1d-130">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="bdc1d-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




