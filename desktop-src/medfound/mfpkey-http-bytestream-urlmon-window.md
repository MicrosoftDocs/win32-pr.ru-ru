---
description: Задает окно для Microsoft Media Foundation байтового потока HTTP.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: Свойство MFPKEY_HTTP_ByteStream_Urlmon_Window (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708574"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a><span data-ttu-id="1f9d5-103">\_Свойство окна мфпкэй HTTP \_ ByteStream \_ Urlmon \_</span><span class="sxs-lookup"><span data-stu-id="1f9d5-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Window property</span></span>

<span data-ttu-id="1f9d5-104">Задает окно для Microsoft Media Foundation байтового потока HTTP.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-104">Sets a window for the Microsoft Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="1f9d5-105">Это окно используется для представления сведений в пользовательском интерфейсе во время операции привязки.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-105">The window is used to present information in the user interface during a bind operation.</span></span>



<span data-ttu-id="1f9d5-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1f9d5-106">Data type</span></span>

<span data-ttu-id="1f9d5-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="1f9d5-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1f9d5-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="1f9d5-108">PROPVARIANT member</span></span>

<span data-ttu-id="1f9d5-109">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="1f9d5-109">**IUnknown\***</span></span>

<span data-ttu-id="1f9d5-110">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="1f9d5-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="1f9d5-111">**пунквал**</span><span class="sxs-lookup"><span data-stu-id="1f9d5-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1f9d5-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1f9d5-112">Remarks</span></span>

<span data-ttu-id="1f9d5-113">Это свойство используется для настройки потока байтов HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-113">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="1f9d5-114">Чтобы задать свойство, передайте указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-114">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="1f9d5-115">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="1f9d5-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="1f9d5-116">Значение этого свойства является указателем на интерфейс **ивиндовфорбиндингуи** .</span><span class="sxs-lookup"><span data-stu-id="1f9d5-116">The value of this property is a pointer to the **IWindowForBindingUI** interface.</span></span> <span data-ttu-id="1f9d5-117">Это свойство применяется только в том случае, если свойство [мфпкэй \_ HTTP \_ ByteStream \_ Enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) имеет значение **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="1f9d5-117">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f9d5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1f9d5-118">Requirements</span></span>



| <span data-ttu-id="1f9d5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1f9d5-119">Requirement</span></span> | <span data-ttu-id="1f9d5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1f9d5-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9d5-121">Header</span><span class="sxs-lookup"><span data-stu-id="1f9d5-121">Header</span></span><br/> | <dl> <span data-ttu-id="1f9d5-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f9d5-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9d5-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f9d5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9d5-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f9d5-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
