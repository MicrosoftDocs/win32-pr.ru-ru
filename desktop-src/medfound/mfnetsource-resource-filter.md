---
description: Содержит указатель на интерфейс обратного вызова Имфнетресаурцефилтер для Microsoft Media Foundation байтового потока HTTP.
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: Свойство MFNETSOURCE_RESOURCE_FILTER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811843"
---
# <a name="mfnetsource_resource_filter-property"></a><span data-ttu-id="9e844-103">\_ \_ Свойство фильтра ресурсов мфнетсаурце</span><span class="sxs-lookup"><span data-stu-id="9e844-103">MFNETSOURCE\_RESOURCE\_FILTER property</span></span>

<span data-ttu-id="9e844-104">Содержит указатель на интерфейс обратного вызова [**имфнетресаурцефилтер**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) для Microsoft Media Foundation байтового потока HTTP.</span><span class="sxs-lookup"><span data-stu-id="9e844-104">Contains a pointer to the [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) callback interface for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="9e844-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9e844-105">Data type</span></span>

<span data-ttu-id="9e844-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="9e844-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="9e844-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="9e844-107">PROPVARIANT member</span></span>

<span data-ttu-id="9e844-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="9e844-108">\**IUnknown\** _</span></span>

<span data-ttu-id="9e844-109">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="9e844-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="9e844-110">_ *пунквал*\*</span><span class="sxs-lookup"><span data-stu-id="9e844-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="9e844-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e844-111">Remarks</span></span>

<span data-ttu-id="9e844-112">Это свойство используется для настройки потока байтов HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9e844-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="9e844-113">Чтобы задать свойство, передайте указатель [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="9e844-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="9e844-114">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="9e844-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e844-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9e844-115">Requirements</span></span>



| <span data-ttu-id="9e844-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9e844-116">Requirement</span></span> | <span data-ttu-id="9e844-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9e844-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e844-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e844-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9e844-119">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9e844-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9e844-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e844-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9e844-121">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9e844-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9e844-122">Header</span><span class="sxs-lookup"><span data-stu-id="9e844-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e844-123"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e844-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e844-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e844-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e844-125">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e844-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
