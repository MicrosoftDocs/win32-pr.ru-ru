---
description: Разрешает потоку байтов HTTP Microsoft Media Foundation использовать моникеры URL-адресов (также называемые Urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: Свойство MFPKEY_HTTP_ByteStream_Enable_Urlmon (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675015"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a><span data-ttu-id="2c96e-103">МФПКЭЙ \_ HTTP \_ ByteStream \_ Enable \_ Urlmon, свойство</span><span class="sxs-lookup"><span data-stu-id="2c96e-103">MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon property</span></span>

<span data-ttu-id="2c96e-104">Разрешает потоку байтов HTTP Microsoft Media Foundation использовать моникеры URL-адресов (также называемые *Urlmon*).</span><span class="sxs-lookup"><span data-stu-id="2c96e-104">Enables the Microsoft Media Foundation HTTP byte stream to use URL monikers (also called *Urlmon*).</span></span>



<span data-ttu-id="2c96e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2c96e-105">Data type</span></span>

<span data-ttu-id="2c96e-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="2c96e-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2c96e-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="2c96e-107">PROPVARIANT member</span></span>

<span data-ttu-id="2c96e-108">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="2c96e-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="2c96e-109">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="2c96e-109">VT\_BOOL</span></span>

<span data-ttu-id="2c96e-110">**булвал**</span><span class="sxs-lookup"><span data-stu-id="2c96e-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2c96e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c96e-111">Remarks</span></span>

<span data-ttu-id="2c96e-112">Это свойство используется для настройки потока байтов HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2c96e-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="2c96e-113">Чтобы задать свойство, передайте указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="2c96e-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="2c96e-114">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2c96e-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="2c96e-115">Если значение является **вариантным \_ true**, то поток байтов HTTP использует Urlmon для транспорта HTTP.</span><span class="sxs-lookup"><span data-stu-id="2c96e-115">If the value is **VARIANT\_TRUE**, the HTTP byte stream uses Urlmon for HTTP transport.</span></span> <span data-ttu-id="2c96e-116">В противном случае, если значение является **вариантным \_ false**, байтовый поток использует WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="2c96e-116">Otherwise, if the value is **VARIANT\_FALSE**, the byte stream uses WinHTTP.</span></span>

<span data-ttu-id="2c96e-117">Значение по умолчанию — **вариант \_ true** для приложений Магазина Windows и **вариант \_ false** для классического приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="2c96e-117">The default value is **VARIANT\_TRUE** for Windows Store apps and **VARIANT\_FALSE** for Windows desktop application.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c96e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2c96e-118">Requirements</span></span>



| <span data-ttu-id="2c96e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2c96e-119">Requirement</span></span> | <span data-ttu-id="2c96e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2c96e-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c96e-121">Header</span><span class="sxs-lookup"><span data-stu-id="2c96e-121">Header</span></span><br/> | <dl> <span data-ttu-id="2c96e-122"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c96e-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c96e-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c96e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c96e-124">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c96e-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
