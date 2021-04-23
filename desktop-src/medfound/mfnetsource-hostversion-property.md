---
description: Значение \# поля &0034; c-хостексевер&\# 0034;, используемое сетевым источником для ведения журнала.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: Свойство MFNETSOURCE_HOSTVERSION (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497655"
---
# <a name="mfnetsource_hostversion-property"></a><span data-ttu-id="5b0af-103">МФНЕТСАУРЦЕ \_ хостверсион, свойство</span><span class="sxs-lookup"><span data-stu-id="5b0af-103">MFNETSOURCE\_HOSTVERSION property</span></span>

<span data-ttu-id="5b0af-104">Значение поля "c-хостексевер", используемое сетевым источником для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="5b0af-104">The value of the "c-hostexever" field that the network source uses for logging.</span></span> <span data-ttu-id="5b0af-105">Приложения могут задать для этого свойства номер версии ведущего приложения.</span><span class="sxs-lookup"><span data-stu-id="5b0af-105">Applications can set this property to the version number of the host application.</span></span> <span data-ttu-id="5b0af-106">Ведущее приложение — это exe-файл, определенный в поле c хостексе.</span><span class="sxs-lookup"><span data-stu-id="5b0af-106">The host application is the .exe file identified by the c-hostexe field.</span></span>



<span data-ttu-id="5b0af-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="5b0af-107">Data type</span></span>

<span data-ttu-id="5b0af-108">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="5b0af-108">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5b0af-109">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="5b0af-109">PROPVARIANT member</span></span>

<span data-ttu-id="5b0af-110">**лонглонг**</span><span class="sxs-lookup"><span data-stu-id="5b0af-110">**LONGLONG**</span></span>

<span data-ttu-id="5b0af-111">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="5b0af-111">VT\_I8</span></span>

<span data-ttu-id="5b0af-112">**хвал**</span><span class="sxs-lookup"><span data-stu-id="5b0af-112">**hVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="5b0af-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b0af-113">Remarks</span></span>

<span data-ttu-id="5b0af-114">Константа **мфнетсаурце \_ хостверсион** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="5b0af-114">The constant **MFNETSOURCE\_HOSTVERSION** defines the GUID for this property key.</span></span> <span data-ttu-id="5b0af-115">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="5b0af-115">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="5b0af-116">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="5b0af-116">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="5b0af-117">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="5b0af-117">To set the property, pass an **IPropertyStore** pointer to the Source resolver.</span></span> <span data-ttu-id="5b0af-118">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5b0af-118">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b0af-119">Требования</span><span class="sxs-lookup"><span data-stu-id="5b0af-119">Requirements</span></span>



| <span data-ttu-id="5b0af-120">Требование</span><span class="sxs-lookup"><span data-stu-id="5b0af-120">Requirement</span></span> | <span data-ttu-id="5b0af-121">Значение</span><span class="sxs-lookup"><span data-stu-id="5b0af-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b0af-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b0af-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b0af-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b0af-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5b0af-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b0af-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b0af-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b0af-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5b0af-126">Header</span><span class="sxs-lookup"><span data-stu-id="5b0af-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b0af-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b0af-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b0af-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b0af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b0af-129">Ведение журнала клиента</span><span class="sxs-lookup"><span data-stu-id="5b0af-129">Client Logging</span></span>](client-logging.md)
</dt> <dt>

[<span data-ttu-id="5b0af-130">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b0af-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5b0af-131">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5b0af-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




