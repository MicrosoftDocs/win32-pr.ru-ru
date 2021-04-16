---
description: Задает корневой идентификатор безопасности для Microsoft Media Foundation байтового потока HTTP.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: Свойство MFPKEY_HTTP_ByteStream_Urlmon_Security_Id (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699112"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a><span data-ttu-id="6238e-103">\_ \_ \_ \_ Свойство идентификатора безопасности мфпкэй HTTP ByteStream Urlmon \_</span><span class="sxs-lookup"><span data-stu-id="6238e-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Security\_Id property</span></span>

<span data-ttu-id="6238e-104">Задает корневой идентификатор безопасности для Microsoft Media Foundation байтового потока HTTP.</span><span class="sxs-lookup"><span data-stu-id="6238e-104">Sets the root security identifier for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="6238e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6238e-105">Data type</span></span>

<span data-ttu-id="6238e-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="6238e-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6238e-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="6238e-107">PROPVARIANT member</span></span>

<span data-ttu-id="6238e-108">**кауб**</span><span class="sxs-lookup"><span data-stu-id="6238e-108">**CAUB**</span></span>

<span data-ttu-id="6238e-109">VT \_ вектор \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="6238e-109">VT\_VECTOR \| VT\_UI1</span></span>

<span data-ttu-id="6238e-110">**кауб**</span><span class="sxs-lookup"><span data-stu-id="6238e-110">**caub**</span></span>



## <a name="remarks"></a><span data-ttu-id="6238e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6238e-111">Remarks</span></span>

<span data-ttu-id="6238e-112">Это свойство используется для настройки потока байтов HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6238e-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="6238e-113">Чтобы задать свойство, передайте указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="6238e-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="6238e-114">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="6238e-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="6238e-115">Это свойство применяется только в том случае, если свойство [мфпкэй \_ HTTP \_ ByteStream \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) имеет значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="6238e-115">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6238e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6238e-116">Requirements</span></span>



| <span data-ttu-id="6238e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6238e-117">Requirement</span></span> | <span data-ttu-id="6238e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6238e-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6238e-119">Header</span><span class="sxs-lookup"><span data-stu-id="6238e-119">Header</span></span><br/> | <dl> <span data-ttu-id="6238e-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6238e-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6238e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6238e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6238e-122">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6238e-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
