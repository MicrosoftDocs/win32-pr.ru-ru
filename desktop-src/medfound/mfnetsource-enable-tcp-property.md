---
description: Указывает, включен ли транспорт TCP для сетевого источника.
ms.assetid: ba655505-dcac-4cea-8ad5-ccd1b55ee9d4
title: Свойство MFNETSOURCE_ENABLE_TCP (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37d5d43fad2ef7132007a9eb037c383ccc2ac9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711266"
---
# <a name="mfnetsource_enable_tcp-property"></a><span data-ttu-id="4c71b-103">МФНЕТСАУРЦЕ \_ включить \_ свойство TCP</span><span class="sxs-lookup"><span data-stu-id="4c71b-103">MFNETSOURCE\_ENABLE\_TCP property</span></span>

<span data-ttu-id="4c71b-104">Указывает, включен ли транспорт TCP для сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="4c71b-104">Specifies whether TCP transport is enabled for the network source.</span></span>



<span data-ttu-id="4c71b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4c71b-105">Data type</span></span>

<span data-ttu-id="4c71b-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="4c71b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="4c71b-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="4c71b-107">PROPVARIANT member</span></span>

<span data-ttu-id="4c71b-108">Логическое значение (**Long**)</span><span class="sxs-lookup"><span data-stu-id="4c71b-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="4c71b-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="4c71b-109">VT\_I4</span></span>

<span data-ttu-id="4c71b-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="4c71b-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="4c71b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c71b-111">Remarks</span></span>

<span data-ttu-id="4c71b-112">Константа **мфнетсаурце \_ акцелератедстреамингдуратион** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="4c71b-112">The constant **MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="4c71b-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="4c71b-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="4c71b-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="4c71b-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="4c71b-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="4c71b-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="4c71b-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="4c71b-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c71b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4c71b-117">Requirements</span></span>



| <span data-ttu-id="4c71b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4c71b-118">Requirement</span></span> | <span data-ttu-id="4c71b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4c71b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c71b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c71b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4c71b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c71b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4c71b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c71b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4c71b-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c71b-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4c71b-124">Header</span><span class="sxs-lookup"><span data-stu-id="4c71b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c71b-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c71b-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c71b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c71b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c71b-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c71b-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="4c71b-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c71b-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="4c71b-129">Поддерживаемые протоколы</span><span class="sxs-lookup"><span data-stu-id="4c71b-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




