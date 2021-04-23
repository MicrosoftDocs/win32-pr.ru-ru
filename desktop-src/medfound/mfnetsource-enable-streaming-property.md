---
description: Указывает, включены ли все протоколы потоковой передачи.
ms.assetid: cf072572-58f7-429a-954a-8808d05248f0
title: Свойство MFNETSOURCE_ENABLE_STREAMING (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29fc8ae10dedd5cb904e43ee79ff64e8f451e37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543194"
---
# <a name="mfnetsource_enable_streaming-property"></a><span data-ttu-id="908d8-103">МФНЕТСАУРЦЕ \_ включить \_ потоковую передачу свойства</span><span class="sxs-lookup"><span data-stu-id="908d8-103">MFNETSOURCE\_ENABLE\_STREAMING property</span></span>

<span data-ttu-id="908d8-104">Указывает, включены ли все протоколы потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="908d8-104">Specifies whether all streaming protocols are enabled.</span></span>



<span data-ttu-id="908d8-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="908d8-105">Data type</span></span>

<span data-ttu-id="908d8-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="908d8-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="908d8-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="908d8-107">PROPVARIANT member</span></span>

<span data-ttu-id="908d8-108">Логическое значение (**Long**)</span><span class="sxs-lookup"><span data-stu-id="908d8-108">Boolean (**LONG**)</span></span>

<span data-ttu-id="908d8-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="908d8-109">VT\_I4</span></span>

<span data-ttu-id="908d8-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="908d8-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="908d8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="908d8-111">Remarks</span></span>

<span data-ttu-id="908d8-112">Константа **мфнетсаурце \_ Enable \_ Streaming** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="908d8-112">The constant **MFNETSOURCE\_ENABLE\_STREAMING** defines the GUID for this property key.</span></span> <span data-ttu-id="908d8-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="908d8-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="908d8-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="908d8-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="908d8-115">Чтобы задать свойство, передайте **ипропертисторе** указатель на [конфигурацию источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="908d8-115">To set the property, pass an **IPropertyStore** pointer to the [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="908d8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="908d8-116">Requirements</span></span>



| <span data-ttu-id="908d8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="908d8-117">Requirement</span></span> | <span data-ttu-id="908d8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="908d8-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="908d8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="908d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="908d8-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="908d8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="908d8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="908d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="908d8-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="908d8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="908d8-123">Header</span><span class="sxs-lookup"><span data-stu-id="908d8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="908d8-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="908d8-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="908d8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="908d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908d8-126">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="908d8-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="908d8-127">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="908d8-127">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="908d8-128">Поддерживаемые протоколы</span><span class="sxs-lookup"><span data-stu-id="908d8-128">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




