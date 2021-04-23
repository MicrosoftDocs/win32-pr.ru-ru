---
description: '\_Константы побитового флага линетерммоде описывают различные типы событий в телефонной линии, которые могут направляться на устройство терминала.'
ms.assetid: 60af1687-8958-4918-be21-a13780c60974
title: Константы LINETERMMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e689e2e4e432d6cf804e64babd462e749e7e9e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675310"
---
# <a name="linetermmode_-constants"></a><span data-ttu-id="1152f-103">\_Константы линетерммоде</span><span class="sxs-lookup"><span data-stu-id="1152f-103">LINETERMMODE\_ Constants</span></span>

<span data-ttu-id="1152f-104">Константы побитового флага **линетерммоде \_** описывают различные типы событий в телефонной линии, которые могут направляться на устройство терминала.</span><span class="sxs-lookup"><span data-stu-id="1152f-104">The **LINETERMMODE\_** bit-flag constants describe different types of events on a phone line that can be routed to a terminal device.</span></span>

<dl> <dt>

<span data-ttu-id="1152f-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**\_кнопки линетерммоде**</span><span class="sxs-lookup"><span data-stu-id="1152f-105"><span id="LINETERMMODE_BUTTONS"></span><span id="linetermmode_buttons"></span>**LINETERMMODE\_BUTTONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1152f-106">Это события нажатия кнопки, отправленные с терминала на линию.</span><span class="sxs-lookup"><span data-stu-id="1152f-106">These are button-press events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1152f-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**ЛИНЕТЕРММОДЕ \_ дисплей**</span><span class="sxs-lookup"><span data-stu-id="1152f-107"><span id="LINETERMMODE_DISPLAY"></span><span id="linetermmode_display"></span>**LINETERMMODE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1152f-108">Это отображает сведения, отправляемые из строки в терминал.</span><span class="sxs-lookup"><span data-stu-id="1152f-108">This is display information sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1152f-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**ЛИНЕТЕРММОДЕ \_ хуксвитч**</span><span class="sxs-lookup"><span data-stu-id="1152f-109"><span id="LINETERMMODE_HOOKSWITCH"></span><span id="linetermmode_hookswitch"></span>**LINETERMMODE\_HOOKSWITCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1152f-110">Это хуксвитч события, отправляемые из терминала в строку.</span><span class="sxs-lookup"><span data-stu-id="1152f-110">These are hookswitch events sent from the terminal to the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1152f-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**ЛИНЕТЕРММОДЕ \_ лампы**</span><span class="sxs-lookup"><span data-stu-id="1152f-111"><span id="LINETERMMODE_LAMPS"></span><span id="linetermmode_lamps"></span>**LINETERMMODE\_LAMPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1152f-112">Это события лампы, отправляемые из линии в терминал.</span><span class="sxs-lookup"><span data-stu-id="1152f-112">These are lamp events sent from the line to the terminal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1152f-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**ЛИНЕТЕРММОДЕ \_ медиабидирект**</span><span class="sxs-lookup"><span data-stu-id="1152f-113"><span id="LINETERMMODE_MEDIABIDIRECT"></span><span id="linetermmode_mediabidirect"></span>**LINETERMMODE\_MEDIABIDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1152f-114">Это двунаправленный поток мультимедиа, связанный с вызовом в строке и в терминале.</span><span class="sxs-lookup"><span data-stu-id="1152f-114">This is the bidirectional media stream associated with a call on the line and the terminal.</span></span> <span data-ttu-id="1152f-115">Используйте это значение, если маршрутизация обоих однонаправленных каналов потока мультимедиа вызова не может контролироваться независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="1152f-115">Use this value when the routing of both unidirectional channels of a call's media stream cannot be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1152f-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**ЛИНЕТЕРММОДЕ \_ медиафромлине**</span><span class="sxs-lookup"><span data-stu-id="1152f-116"><span id="LINETERMMODE_MEDIAFROMLINE"></span><span id="linetermmode_mediafromline"></span>**LINETERMMODE\_MEDIAFROMLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1152f-117">Это однонаправленный поток мультимедиа из линии в терминал, связанный с вызовом в строке.</span><span class="sxs-lookup"><span data-stu-id="1152f-117">This is the unidirectional media stream from the line to the terminal associated with a call on the line.</span></span> <span data-ttu-id="1152f-118">Используйте это значение, если маршрутизация обоих однонаправленных каналов потока мультимедиа вызова может осуществляться независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="1152f-118">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1152f-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**ЛИНЕТЕРММОДЕ \_ медиатолине**</span><span class="sxs-lookup"><span data-stu-id="1152f-119"><span id="LINETERMMODE_MEDIATOLINE"></span><span id="linetermmode_mediatoline"></span>**LINETERMMODE\_MEDIATOLINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1152f-120">Это однонаправленный поток мультимедиа от терминала до линии, связанной с вызовом в строке.</span><span class="sxs-lookup"><span data-stu-id="1152f-120">This is the unidirectional media stream from the terminal to the line associated with a call on the line.</span></span> <span data-ttu-id="1152f-121">Используйте это значение, если маршрутизация обоих однонаправленных каналов потока мультимедиа вызова может осуществляться независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="1152f-121">Use this value when the routing of both unidirectional channels of a call's media stream can be controlled independently.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1152f-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**ЛИНЕТЕРММОДЕ \_ Ring**</span><span class="sxs-lookup"><span data-stu-id="1152f-122"><span id="LINETERMMODE_RINGER"></span><span id="linetermmode_ringer"></span>**LINETERMMODE\_RINGER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1152f-123">Это сведения об управлении звонками, отправляемые с коммутатора в терминал.</span><span class="sxs-lookup"><span data-stu-id="1152f-123">This is ringer-control information sent from the switch to the terminal.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1152f-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1152f-124">Remarks</span></span>

<span data-ttu-id="1152f-125">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="1152f-125">No extensibility.</span></span> <span data-ttu-id="1152f-126">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="1152f-126">All 32 bits are reserved.</span></span>

<span data-ttu-id="1152f-127">Эти константы описывают классы элементов управления и информационных потоков, которые могут направляться напрямую между линейным устройством и устройством терминала (например, набором телефонов).</span><span class="sxs-lookup"><span data-stu-id="1152f-127">These constants describe the classes of control and information streams that can be routed directly between a line device and a terminal device (such as a phone set).</span></span>

## <a name="requirements"></a><span data-ttu-id="1152f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1152f-128">Requirements</span></span>



| <span data-ttu-id="1152f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1152f-129">Requirement</span></span> | <span data-ttu-id="1152f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1152f-130">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1152f-131">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="1152f-131">TAPI version</span></span><br/> | <span data-ttu-id="1152f-132">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1152f-132">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1152f-133">Header</span><span class="sxs-lookup"><span data-stu-id="1152f-133">Header</span></span><br/>       | <dl> <span data-ttu-id="1152f-134"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1152f-134"><dt>Tapi.h</dt></span></span> </dl> |



 

 




