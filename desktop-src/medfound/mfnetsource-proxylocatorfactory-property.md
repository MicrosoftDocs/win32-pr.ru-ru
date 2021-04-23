---
description: Содержит указатель на интерфейс Имфнетпроксилокаторфактори.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: Свойство MFNETSOURCE_PROXYLOCATORFACTORY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1199333e9eb343ab9d8f96864372b2dc385ab7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155558"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a><span data-ttu-id="7917d-103">МФНЕТСАУРЦЕ \_ проксилокаторфактори, свойство</span><span class="sxs-lookup"><span data-stu-id="7917d-103">MFNETSOURCE\_PROXYLOCATORFACTORY property</span></span>

<span data-ttu-id="7917d-104">Содержит указатель на интерфейс [**имфнетпроксилокаторфактори**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .</span><span class="sxs-lookup"><span data-stu-id="7917d-104">Contains a pointer to the [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) interface.</span></span>



<span data-ttu-id="7917d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7917d-105">Data type</span></span>

<span data-ttu-id="7917d-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="7917d-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="7917d-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="7917d-107">PROPVARIANT member</span></span>

<span data-ttu-id="7917d-108">Указатель **IUnknown**</span><span class="sxs-lookup"><span data-stu-id="7917d-108">**IUnknown** pointer</span></span>

<span data-ttu-id="7917d-109">VT \_ Unknown</span><span class="sxs-lookup"><span data-stu-id="7917d-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="7917d-110">**пунквал**</span><span class="sxs-lookup"><span data-stu-id="7917d-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="7917d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7917d-111">Remarks</span></span>

<span data-ttu-id="7917d-112">Константа **мфнетсаурце \_ проксилокаторфактори** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="7917d-112">The constant **MFNETSOURCE\_PROXYLOCATORFACTORY** defines the GUID for this property key.</span></span> <span data-ttu-id="7917d-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="7917d-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="7917d-114">Приложения могут использовать это свойство для предоставления пользовательского указателя прокси-сервера для сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="7917d-114">Applications can use this property to provide a custom proxy locator for the network source.</span></span> <span data-ttu-id="7917d-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="7917d-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="7917d-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="7917d-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7917d-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7917d-117">Requirements</span></span>



| <span data-ttu-id="7917d-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7917d-118">Requirement</span></span> | <span data-ttu-id="7917d-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7917d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7917d-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7917d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7917d-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7917d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7917d-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7917d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7917d-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7917d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7917d-124">Header</span><span class="sxs-lookup"><span data-stu-id="7917d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7917d-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7917d-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7917d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7917d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7917d-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7917d-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="7917d-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7917d-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="7917d-129">Поддержка прокси-сервера для сетевых источников</span><span class="sxs-lookup"><span data-stu-id="7917d-129">Proxy Support for Network Sources</span></span>](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




