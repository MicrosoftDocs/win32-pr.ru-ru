---
description: Указывает пропускную способность связи для источника сети в битах в секунду.
ms.assetid: 1b71dce1-8744-4114-9629-2a9d0afb7c43
title: Свойство MFNETSOURCE_CONNECTIONBANDWIDTH (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b852b3eb8dbfe5d3abc85e2223e868c5be708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543202"
---
# <a name="mfnetsource_connectionbandwidth-property"></a><span data-ttu-id="8fe88-103">МФНЕТСАУРЦЕ \_ коннектионбандвидс, свойство</span><span class="sxs-lookup"><span data-stu-id="8fe88-103">MFNETSOURCE\_CONNECTIONBANDWIDTH property</span></span>

<span data-ttu-id="8fe88-104">Указывает пропускную способность связи для источника сети в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="8fe88-104">Specifies the link bandwidth for the network source, in bits per second.</span></span>



<span data-ttu-id="8fe88-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8fe88-105">Data type</span></span>

<span data-ttu-id="8fe88-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="8fe88-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8fe88-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="8fe88-107">PROPVARIANT member</span></span>

<span data-ttu-id="8fe88-108">**DWORD** (хранится в формате **Long**)</span><span class="sxs-lookup"><span data-stu-id="8fe88-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="8fe88-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="8fe88-109">VT\_I4</span></span>

<span data-ttu-id="8fe88-110">**лвал**</span><span class="sxs-lookup"><span data-stu-id="8fe88-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="8fe88-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8fe88-111">Remarks</span></span>

<span data-ttu-id="8fe88-112">Константа **мфнетсаурце \_ коннектионбандвидс** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="8fe88-112">The constant **MFNETSOURCE\_CONNECTIONBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="8fe88-113">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="8fe88-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="8fe88-114">Приложения могут использовать это свойство для настройки сетевого источника.</span><span class="sxs-lookup"><span data-stu-id="8fe88-114">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="8fe88-115">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="8fe88-115">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="8fe88-116">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="8fe88-116">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe88-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8fe88-117">Requirements</span></span>



| <span data-ttu-id="8fe88-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8fe88-118">Requirement</span></span> | <span data-ttu-id="8fe88-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8fe88-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe88-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fe88-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe88-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8fe88-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8fe88-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fe88-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe88-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8fe88-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8fe88-124">Header</span><span class="sxs-lookup"><span data-stu-id="8fe88-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe88-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fe88-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe88-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fe88-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe88-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8fe88-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8fe88-128">Компоненты сетевого источника</span><span class="sxs-lookup"><span data-stu-id="8fe88-128">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="8fe88-129">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8fe88-129">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




