---
description: Указывает протокол управления, используемый сетевым источником.
ms.assetid: 4de8b8ba-97d9-4269-a16c-1853dc02f674
title: Свойство MFNETSOURCE_PROTOCOL (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188eeb1f6669544291f4dca95db8a4a45a50d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541330"
---
# <a name="mfnetsource_protocol-property"></a><span data-ttu-id="1df60-103">\_Свойство протокола мфнетсаурце</span><span class="sxs-lookup"><span data-stu-id="1df60-103">MFNETSOURCE\_PROTOCOL property</span></span>

<span data-ttu-id="1df60-104">Указывает протокол управления, используемый сетевым источником.</span><span class="sxs-lookup"><span data-stu-id="1df60-104">Specifies the control protocol used by the network source.</span></span> <span data-ttu-id="1df60-105">Значение этого свойства является членом перечисления [**\_ \_ типа протокола мфнетсаурце**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="1df60-105">The value of this property is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>



<span data-ttu-id="1df60-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1df60-106">Data type</span></span>

<span data-ttu-id="1df60-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="1df60-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="1df60-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="1df60-108">PROPVARIANT member</span></span>

<span data-ttu-id="1df60-109">**LONG**</span><span class="sxs-lookup"><span data-stu-id="1df60-109">**LONG**</span></span>

<span data-ttu-id="1df60-110">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1df60-110">VT\_I4</span></span>

<span data-ttu-id="1df60-111">**лвал**</span><span class="sxs-lookup"><span data-stu-id="1df60-111">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="1df60-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1df60-112">Remarks</span></span>

<span data-ttu-id="1df60-113">Постоянный **\_ протокол мфнетсаурце** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="1df60-113">The constant **MFNETSOURCE\_PROTOCOL** defines the GUID for this property key.</span></span> <span data-ttu-id="1df60-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="1df60-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="1df60-115">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1df60-115">This property is read-only.</span></span> <span data-ttu-id="1df60-116">Чтобы получить это свойство, выполните запрос к источнику сети для интерфейса **ипропертисторе** и вызовите метод **Ипропертисторе:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="1df60-116">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1df60-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1df60-117">Requirements</span></span>



| <span data-ttu-id="1df60-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1df60-118">Requirement</span></span> | <span data-ttu-id="1df60-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1df60-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1df60-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1df60-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1df60-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1df60-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1df60-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1df60-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1df60-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1df60-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1df60-124">Header</span><span class="sxs-lookup"><span data-stu-id="1df60-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1df60-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1df60-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1df60-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1df60-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df60-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1df60-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1df60-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1df60-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="1df60-129">Поддерживаемые протоколы</span><span class="sxs-lookup"><span data-stu-id="1df60-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




