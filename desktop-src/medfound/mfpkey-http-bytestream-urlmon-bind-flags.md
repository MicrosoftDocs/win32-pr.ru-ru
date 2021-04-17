---
description: Задает флаги привязки моникера для Microsoft Media Foundation байтового потока HTTP.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: Свойство MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694653"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a><span data-ttu-id="455af-103">\_ \_ \_ \_ Свойство флагов привязки мфпкэй HTTP ByteStream Urlmon \_</span><span class="sxs-lookup"><span data-stu-id="455af-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Bind\_Flags property</span></span>

<span data-ttu-id="455af-104">Задает флаги привязки моникера для Microsoft Media Foundation байтового потока HTTP.</span><span class="sxs-lookup"><span data-stu-id="455af-104">Sets the moniker binding flags for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="455af-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="455af-105">Data type</span></span>

<span data-ttu-id="455af-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="455af-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="455af-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="455af-107">PROPVARIANT member</span></span>

<span data-ttu-id="455af-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="455af-108">**ULONG**</span></span>

<span data-ttu-id="455af-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="455af-109">VT\_UI4</span></span>

<span data-ttu-id="455af-110">**улвал**</span><span class="sxs-lookup"><span data-stu-id="455af-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="455af-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="455af-111">Remarks</span></span>

<span data-ttu-id="455af-112">Это свойство используется для настройки потока байтов HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="455af-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="455af-113">Чтобы задать свойство, передайте указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="455af-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="455af-114">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="455af-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="455af-115">Значение этого свойства является **побитовым** для флагов перечисления **биндф** .</span><span class="sxs-lookup"><span data-stu-id="455af-115">The value of this property is a bitwise **OR** of flags from the **BINDF** enumeration.</span></span> <span data-ttu-id="455af-116">Это свойство применяется только в том случае, если свойство [мфпкэй \_ HTTP \_ ByteStream \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) имеет значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="455af-116">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="455af-117">Требования</span><span class="sxs-lookup"><span data-stu-id="455af-117">Requirements</span></span>



| <span data-ttu-id="455af-118">Требование</span><span class="sxs-lookup"><span data-stu-id="455af-118">Requirement</span></span> | <span data-ttu-id="455af-119">Значение</span><span class="sxs-lookup"><span data-stu-id="455af-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="455af-120">Header</span><span class="sxs-lookup"><span data-stu-id="455af-120">Header</span></span><br/> | <dl> <span data-ttu-id="455af-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="455af-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="455af-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="455af-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455af-123">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="455af-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
