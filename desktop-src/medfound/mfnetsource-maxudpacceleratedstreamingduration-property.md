---
description: Максимальная продолжительность ускоренной потоковой передачи (в миллисекундах), когда сетевой источник использует транспорт UDP.
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: Свойство MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081465"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a><span data-ttu-id="5701a-103">МФНЕТСАУРЦЕ \_ максудпакцелератедстреамингдуратион, свойство</span><span class="sxs-lookup"><span data-stu-id="5701a-103">MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="5701a-104">Максимальная продолжительность ускоренной потоковой передачи (в миллисекундах), когда сетевой источник использует транспорт UDP.</span><span class="sxs-lookup"><span data-stu-id="5701a-104">Maximum duration of accelerated streaming, in milliseconds, when the network source uses UDP transport.</span></span>



<span data-ttu-id="5701a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5701a-105">Data type</span></span>

<span data-ttu-id="5701a-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="5701a-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5701a-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="5701a-107">PROPVARIANT member</span></span>

<span data-ttu-id="5701a-108">**DWORD** (хранится в формате **Long**)</span><span class="sxs-lookup"><span data-stu-id="5701a-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="5701a-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="5701a-109">VT\_I4</span></span>

<span data-ttu-id="5701a-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="5701a-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="5701a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5701a-111">Remarks</span></span>

<span data-ttu-id="5701a-112">Константа **мфнетсаурце \_ максудпакцелератедстреамингдуратион** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="5701a-112">The constant **MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="5701a-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="5701a-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="5701a-114">Для транспорта UDP это свойство переопределяет свойство [**мфнетсаурце \_ акцелератедстреамингдуратион**](mfnetsource-acceleratedstreamingduration-property.md) , если значение этого свойства меньше.</span><span class="sxs-lookup"><span data-stu-id="5701a-114">For UDP transport, this property overrides the [**MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) property if the value of this property is lower.</span></span>

<span data-ttu-id="5701a-115">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="5701a-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="5701a-116">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="5701a-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="5701a-117">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5701a-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="5701a-118">Значение этого свойства по умолчанию равно 8 000 миллисекундам.</span><span class="sxs-lookup"><span data-stu-id="5701a-118">The default value of this property is 8,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="5701a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5701a-119">Requirements</span></span>



| <span data-ttu-id="5701a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5701a-120">Requirement</span></span> | <span data-ttu-id="5701a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5701a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5701a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5701a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5701a-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5701a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5701a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5701a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5701a-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5701a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5701a-126">Header</span><span class="sxs-lookup"><span data-stu-id="5701a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5701a-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5701a-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5701a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5701a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5701a-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5701a-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5701a-130">Компоненты сетевого источника</span><span class="sxs-lookup"><span data-stu-id="5701a-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="5701a-131">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5701a-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




