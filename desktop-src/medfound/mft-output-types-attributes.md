---
description: Содержит зарегистрированные типы выходных данных для Media Foundation преобразования (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: Атрибут MFT_OUTPUT_TYPES_Attributes (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701804"
---
# <a name="mft_output_types_attributes-attribute"></a><span data-ttu-id="69581-103">\_ \_ Атрибут атрибутов типов выходных данных MFT \_</span><span class="sxs-lookup"><span data-stu-id="69581-103">MFT\_OUTPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="69581-104">Содержит зарегистрированные типы выходных данных для Media Foundation преобразования (MFT).</span><span class="sxs-lookup"><span data-stu-id="69581-104">Contains the registered output types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="69581-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="69581-105">Data type</span></span>

<span data-ttu-id="69581-106">**MFT \_ \_ \_ Сведения \[ о \] типе регистрации** хранятся в виде **байта \[ \]**</span><span class="sxs-lookup"><span data-stu-id="69581-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="remarks"></a><span data-ttu-id="69581-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69581-107">Remarks</span></span>

<span data-ttu-id="69581-108">Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="69581-108">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="69581-109">Этот атрибут содержит массив структур [**\_ \_ \_ сведений о типе регистра MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) , описывающих один или несколько выходных форматов, поддерживаемых MFT.</span><span class="sxs-lookup"><span data-stu-id="69581-109">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more output formats supported by the MFT.</span></span> <span data-ttu-id="69581-110">Эти значения берутся из реестра и предназначены в качестве подсказки для приложения.</span><span class="sxs-lookup"><span data-stu-id="69581-110">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="69581-111">Таблица MFT может поддерживать дополнительные форматы.</span><span class="sxs-lookup"><span data-stu-id="69581-111">The MFT might support additional formats.</span></span> <span data-ttu-id="69581-112">Чтобы задать реальный формат вывода, необходимо создать таблицу MFT и вызвать [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="69581-112">To set the actual output format, you must create the MFT and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="69581-113">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="69581-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="69581-114">Требования</span><span class="sxs-lookup"><span data-stu-id="69581-114">Requirements</span></span>



| <span data-ttu-id="69581-115">Требование</span><span class="sxs-lookup"><span data-stu-id="69581-115">Requirement</span></span> | <span data-ttu-id="69581-116">Значение</span><span class="sxs-lookup"><span data-stu-id="69581-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="69581-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69581-117">Minimum supported client</span></span><br/> | <span data-ttu-id="69581-118">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="69581-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="69581-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69581-119">Minimum supported server</span></span><br/> | <span data-ttu-id="69581-120">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="69581-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="69581-121">Header</span><span class="sxs-lookup"><span data-stu-id="69581-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="69581-122"><dt>Мфтрансформ. h</dt></span><span class="sxs-lookup"><span data-stu-id="69581-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69581-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69581-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69581-124">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="69581-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="69581-125">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="69581-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




