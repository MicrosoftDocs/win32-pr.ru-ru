---
description: Указывает идентификатор поставщика для Microsoft Media Foundation на основе оборудования.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: Атрибут MFT_ENUM_HARDWARE_VENDOR_ID_Attribute
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4d92585936e52cbb0b9b65201a5de0d3a02b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656553"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a><span data-ttu-id="87c2c-103">\_ \_ \_ \_ Атрибут атрибута идентификатора поставщика оборудования \_ перечисления MFT</span><span class="sxs-lookup"><span data-stu-id="87c2c-103">MFT\_ENUM\_HARDWARE\_VENDOR\_ID\_Attribute attribute</span></span>

<span data-ttu-id="87c2c-104">Указывает идентификатор поставщика для преобразования Microsoft Media Foundation на основе оборудования (MFT).</span><span class="sxs-lookup"><span data-stu-id="87c2c-104">Specifies the vendor ID for a hardware-based Microsoft Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="87c2c-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="87c2c-105">Data type</span></span>

<span data-ttu-id="87c2c-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="87c2c-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="87c2c-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="87c2c-107">Get/set</span></span>

<span data-ttu-id="87c2c-108">Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="87c2c-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="87c2c-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="87c2c-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="87c2c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87c2c-110">Remarks</span></span>

<span data-ttu-id="87c2c-111">Этот атрибут является информационным и необязательным.</span><span class="sxs-lookup"><span data-stu-id="87c2c-111">This attribute is informational and optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="87c2c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="87c2c-112">Requirements</span></span>



| <span data-ttu-id="87c2c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="87c2c-113">Requirement</span></span> | <span data-ttu-id="87c2c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="87c2c-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="87c2c-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87c2c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="87c2c-116">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="87c2c-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="87c2c-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87c2c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="87c2c-118">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="87c2c-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="87c2c-119">Header</span><span class="sxs-lookup"><span data-stu-id="87c2c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="87c2c-120"><dt>Мфтрансформ. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87c2c-120"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87c2c-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87c2c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c2c-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="87c2c-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="87c2c-123">Оборудование МФТС</span><span class="sxs-lookup"><span data-stu-id="87c2c-123">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="87c2c-124">Атрибуты преобразования</span><span class="sxs-lookup"><span data-stu-id="87c2c-124">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




