---
description: Значение \# поля &0034; c-плайерверсион&\# 0034;, используемое сетевым источником для ведения журнала.
ms.assetid: 7bc485de-345b-475c-bbae-0776aa63c93a
title: Свойство MFNETSOURCE_PLAYERVERSION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ddaee0fe3e476b2b6e078551b1191fe9fc96cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817913"
---
# <a name="mfnetsource_playerversion-property"></a><span data-ttu-id="19dc7-103">МФНЕТСАУРЦЕ \_ плайерверсион, свойство</span><span class="sxs-lookup"><span data-stu-id="19dc7-103">MFNETSOURCE\_PLAYERVERSION property</span></span>

<span data-ttu-id="19dc7-104">Значение поля "c-плайерверсион", используемое сетевым источником для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="19dc7-104">The value of the "c-playerversion" field that the network source uses for logging.</span></span> <span data-ttu-id="19dc7-105">Приложения могут задать для этого свойства номер версии приложения.</span><span class="sxs-lookup"><span data-stu-id="19dc7-105">Applications can set this property to the version number of the application.</span></span>



<span data-ttu-id="19dc7-106">Тип данных</span><span class="sxs-lookup"><span data-stu-id="19dc7-106">Data type</span></span>

<span data-ttu-id="19dc7-107">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="19dc7-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="19dc7-108">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="19dc7-108">PROPVARIANT member</span></span>

<span data-ttu-id="19dc7-109">**лонглонг**</span><span class="sxs-lookup"><span data-stu-id="19dc7-109">**LONGLONG**</span></span>

<span data-ttu-id="19dc7-110">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="19dc7-110">VT\_I8</span></span>

<span data-ttu-id="19dc7-111">**хвал**</span><span class="sxs-lookup"><span data-stu-id="19dc7-111">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="19dc7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19dc7-112">Remarks</span></span>

<span data-ttu-id="19dc7-113">Константа **мфнетсаурце \_ плайерверсион** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="19dc7-113">The constant **MFNETSOURCE\_PLAYERVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="19dc7-114">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="19dc7-114">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="19dc7-115">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="19dc7-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="19dc7-116">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="19dc7-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="19dc7-117">Дополнительные сведения см. в разделе [сопоставитель источников](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="19dc7-117">For more information, see [Source Resolver](source-resolver.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19dc7-118">Требования</span><span class="sxs-lookup"><span data-stu-id="19dc7-118">Requirements</span></span>



| <span data-ttu-id="19dc7-119">Требование</span><span class="sxs-lookup"><span data-stu-id="19dc7-119">Requirement</span></span> | <span data-ttu-id="19dc7-120">Значение</span><span class="sxs-lookup"><span data-stu-id="19dc7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19dc7-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19dc7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="19dc7-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19dc7-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="19dc7-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19dc7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="19dc7-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19dc7-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="19dc7-125">Header</span><span class="sxs-lookup"><span data-stu-id="19dc7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="19dc7-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="19dc7-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19dc7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19dc7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19dc7-128">Ведение журнала клиента</span><span class="sxs-lookup"><span data-stu-id="19dc7-128">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="19dc7-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19dc7-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="19dc7-130">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19dc7-130">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




