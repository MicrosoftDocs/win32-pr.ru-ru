---
description: Указывает пропускную способность для пары пакетов и полосу пропускания во время выполнения, обнаруженную сетевым источником.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: Свойство MFNETSOURCE_PPBANDWIDTH (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719448"
---
# <a name="mfnetsource_ppbandwidth-property"></a><span data-ttu-id="6ae0b-103">МФНЕТСАУРЦЕ \_ ппбандвидс, свойство</span><span class="sxs-lookup"><span data-stu-id="6ae0b-103">MFNETSOURCE\_PPBANDWIDTH property</span></span>

<span data-ttu-id="6ae0b-104">Указывает пропускную способность для пары пакетов и полосу пропускания во время выполнения, обнаруженную сетевым источником.</span><span class="sxs-lookup"><span data-stu-id="6ae0b-104">Specifies the packet-pair bandwidth and run-time bandwidth detected by the network source.</span></span> <span data-ttu-id="6ae0b-105">Значение свойства представляет собой массив из двух значений:</span><span class="sxs-lookup"><span data-stu-id="6ae0b-105">The property value is a array of two values:</span></span>

-   <span data-ttu-id="6ae0b-106">Пропускная способность пары пакетов в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="6ae0b-106">Packet-pair bandwidth, in bits per second.</span></span>
-   <span data-ttu-id="6ae0b-107">Пропускная способность во время выполнения в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="6ae0b-107">Run-time bandwidth, in bits per second.</span></span>



<span data-ttu-id="6ae0b-108">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6ae0b-108">Data type</span></span>

<span data-ttu-id="6ae0b-109">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="6ae0b-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="6ae0b-110">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="6ae0b-110">PROPVARIANT member</span></span>

<span data-ttu-id="6ae0b-111">Массив значений типа **ulong** (**Каул**)</span><span class="sxs-lookup"><span data-stu-id="6ae0b-111">Array of **ULONG** values (**CAUL**)</span></span>

<span data-ttu-id="6ae0b-112">VT \_ вектор \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="6ae0b-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="6ae0b-113">**каул**</span><span class="sxs-lookup"><span data-stu-id="6ae0b-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="6ae0b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6ae0b-114">Remarks</span></span>

<span data-ttu-id="6ae0b-115">Константа **мфнетсаурце \_ ппбандвидс** определяет идентификатор GUID для этого ключа свойства.</span><span class="sxs-lookup"><span data-stu-id="6ae0b-115">The constant **MFNETSOURCE\_PPBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="6ae0b-116">Идентификатор свойства (PID) равен нулю.</span><span class="sxs-lookup"><span data-stu-id="6ae0b-116">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="6ae0b-117">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6ae0b-117">This property is read-only.</span></span> <span data-ttu-id="6ae0b-118">Чтобы получить это свойство, выполните запрос к источнику сети для интерфейса **ипропертисторе** и вызовите метод **Ипропертисторе:: GetValue**.</span><span class="sxs-lookup"><span data-stu-id="6ae0b-118">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae0b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="6ae0b-119">Requirements</span></span>



| <span data-ttu-id="6ae0b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="6ae0b-120">Requirement</span></span> | <span data-ttu-id="6ae0b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="6ae0b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae0b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6ae0b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6ae0b-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ae0b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6ae0b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6ae0b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6ae0b-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6ae0b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6ae0b-126">Header</span><span class="sxs-lookup"><span data-stu-id="6ae0b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ae0b-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ae0b-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ae0b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6ae0b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ae0b-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ae0b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="6ae0b-130">Компоненты сетевого источника</span><span class="sxs-lookup"><span data-stu-id="6ae0b-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="6ae0b-131">Сетевые подключения в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ae0b-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




