---
description: Указывает транспортный протокол, используемый сетевым источником.
ms.assetid: 7c8598ff-f408-42d0-9eee-3ef1e82f0466
title: Свойство MFNETSOURCE_TRANSPORT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd41653f2b5ea0686527af4d6ee8c8b9962005aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897925"
---
# <a name="mfnetsource_transport-property"></a><span data-ttu-id="36c84-103">МФНЕТСАУРЦЕ, \_ свойство транспорта</span><span class="sxs-lookup"><span data-stu-id="36c84-103">MFNETSOURCE\_TRANSPORT property</span></span>

<span data-ttu-id="36c84-104">Указывает транспортный протокол, используемый сетевым источником.</span><span class="sxs-lookup"><span data-stu-id="36c84-104">Specifies the transport protocol used by the network source.</span></span> <span data-ttu-id="36c84-105">Значение этого свойства является членом перечисления [**\_ \_ типа транспорта мфнетсаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .</span><span class="sxs-lookup"><span data-stu-id="36c84-105">The value of this property is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>



<span data-ttu-id="36c84-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="36c84-106">Data type</span></span>

<span data-ttu-id="36c84-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="36c84-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="36c84-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="36c84-108">PROPVARIANT member</span></span>

<span data-ttu-id="36c84-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="36c84-109">**LONG**</span></span>

<span data-ttu-id="36c84-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="36c84-110">VT\_I4</span></span>

<span data-ttu-id="36c84-111">**лвал**</span><span class="sxs-lookup"><span data-stu-id="36c84-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="36c84-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36c84-112">Remarks</span></span>

<span data-ttu-id="36c84-113">Постоянный **мфнетсаурце \_ транспорт** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="36c84-113">The constant **MFNETSOURCE\_TRANSPORT** defines the GUID for this property key.</span></span> <span data-ttu-id="36c84-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="36c84-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="36c84-115">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="36c84-115">This property is read-only.</span></span> <span data-ttu-id="36c84-116">Чтобы получить это свойство, выполните запрос к источнику сети для интерфейса **ипропертисторе** и вызовите метод **Ипропертисторе:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="36c84-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="36c84-117">Требования</span><span class="sxs-lookup"><span data-stu-id="36c84-117">Requirements</span></span>



| <span data-ttu-id="36c84-118">Требование</span><span class="sxs-lookup"><span data-stu-id="36c84-118">Requirement</span></span> | <span data-ttu-id="36c84-119">Значение</span><span class="sxs-lookup"><span data-stu-id="36c84-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36c84-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36c84-120">Minimum supported client</span></span><br/> | <span data-ttu-id="36c84-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36c84-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="36c84-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36c84-122">Minimum supported server</span></span><br/> | <span data-ttu-id="36c84-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36c84-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="36c84-124">Header</span><span class="sxs-lookup"><span data-stu-id="36c84-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="36c84-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="36c84-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36c84-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36c84-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36c84-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36c84-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="36c84-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36c84-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="36c84-129">Поддерживаемые протоколы</span><span class="sxs-lookup"><span data-stu-id="36c84-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




