---
description: Указывает, включен ли в сетевом источнике протокол многоадресной рассылки вещания потока мультимедиа (в виде пересылки).
ms.assetid: a46e3b4c-60be-4470-b9dc-041902c2563c
title: Свойство MFNETSOURCE_ENABLE_MSB (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6b2a49876cf504bfc4e086ab1e064e6835283a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682960"
---
# <a name="mfnetsource_enable_msb-property"></a><span data-ttu-id="c60d2-103">МФНЕТСАУРЦЕ включить свойство в виде нестаршего \_ \_ значения</span><span class="sxs-lookup"><span data-stu-id="c60d2-103">MFNETSOURCE\_ENABLE\_MSB property</span></span>

<span data-ttu-id="c60d2-104">Указывает, включен ли в сетевом источнике протокол многоадресной рассылки вещания потока мультимедиа (в виде пересылки).</span><span class="sxs-lookup"><span data-stu-id="c60d2-104">Specifies whether the Media Stream Broadcast (MSB) multicast protocol is enabled in the network source.</span></span>



<span data-ttu-id="c60d2-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c60d2-105">Data type</span></span>

<span data-ttu-id="c60d2-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="c60d2-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c60d2-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="c60d2-107">PROPVARIANT member</span></span>

<span data-ttu-id="c60d2-108">**LONG**</span><span class="sxs-lookup"><span data-stu-id="c60d2-108">**LONG**</span></span>

<span data-ttu-id="c60d2-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c60d2-109">VT\_I4</span></span>

<span data-ttu-id="c60d2-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="c60d2-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c60d2-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c60d2-111">Remarks</span></span>

<span data-ttu-id="c60d2-112">Константа **\_ включения мфнетсаурце \_** для этого ключа свойства определяет идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="c60d2-112">The constant **MFNETSOURCE\_ENABLE\_MSB** defines the GUID for this property key.</span></span> <span data-ttu-id="c60d2-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="c60d2-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="c60d2-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="c60d2-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="c60d2-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="c60d2-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="c60d2-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="c60d2-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c60d2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="c60d2-117">Requirements</span></span>



| <span data-ttu-id="c60d2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="c60d2-118">Requirement</span></span> | <span data-ttu-id="c60d2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="c60d2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c60d2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c60d2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c60d2-121">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c60d2-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c60d2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c60d2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c60d2-123">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c60d2-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c60d2-124">Header</span><span class="sxs-lookup"><span data-stu-id="c60d2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c60d2-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c60d2-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c60d2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c60d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60d2-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c60d2-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c60d2-128">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c60d2-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="c60d2-129">Поддерживаемые протоколы</span><span class="sxs-lookup"><span data-stu-id="c60d2-129">Supported Protocols</span></span>](supported-protocols.md)
</dt> </dl>

 

 




