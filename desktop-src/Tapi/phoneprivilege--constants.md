---
description: '\_Константы побитового флага фонепривилеже описывают различные способы открытия телефонного устройства.'
ms.assetid: 1dc2fab9-b044-4ae3-8c16-fa450f9ef714
title: Константы PHONEPRIVILEGE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6d04c074e03d6f0b7f7a6c58e4268e0bd5057a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689530"
---
# <a name="phoneprivilege_-constants"></a><span data-ttu-id="23dac-103">\_Константы фонепривилеже</span><span class="sxs-lookup"><span data-stu-id="23dac-103">PHONEPRIVILEGE\_ Constants</span></span>

<span data-ttu-id="23dac-104">Константы побитового флага **фонепривилеже \_** описывают различные способы открытия телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="23dac-104">The **PHONEPRIVILEGE\_** bit-flag constants describe the various ways in which a phone device can be opened.</span></span>

<dl> <dt>

<span data-ttu-id="23dac-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**\_монитор фонепривилеже**</span><span class="sxs-lookup"><span data-stu-id="23dac-105"><span id="PHONEPRIVILEGE_MONITOR"></span><span id="phoneprivilege_monitor"></span>**PHONEPRIVILEGE\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="23dac-106">Приложение, открывающее телефонное устройство с правами монитора, уведомляет о событиях и изменениях состояния, происходящих на телефоне.</span><span class="sxs-lookup"><span data-stu-id="23dac-106">An application that opens a phone device with the monitor privilege is informed about events and state changes occurring on the phone.</span></span> <span data-ttu-id="23dac-107">Приложение не может вызывать никаких операций на телефонном устройстве, которые могли бы изменить свое состояние, поэтому могут быть вызваны только операции состояния.</span><span class="sxs-lookup"><span data-stu-id="23dac-107">The application cannot invoke any operations on the phone device that would change its state, so only status operations can be invoked.</span></span> <span data-ttu-id="23dac-108">Несколько приложений могут отслеживать телефонное устройство в любое заданное время.</span><span class="sxs-lookup"><span data-stu-id="23dac-108">Multiple applications can monitor a phone device at any given time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="23dac-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**\_владелец фонепривилеже**</span><span class="sxs-lookup"><span data-stu-id="23dac-109"><span id="PHONEPRIVILEGE_OWNER"></span><span id="phoneprivilege_owner"></span>**PHONEPRIVILEGE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="23dac-110">Приложение, открывающее телефонное устройство с правами владельца, может изменять состояние блоков ламп, колец, дисплея, хуксвитч и данных телефона.</span><span class="sxs-lookup"><span data-stu-id="23dac-110">An application that opens a phone device with the owner privilege is allowed to change the state of the lamps, ringer, display, hookswitch, and data blocks of the phone.</span></span> <span data-ttu-id="23dac-111">Открытие телефонного устройства в режиме владельца также обеспечивает мониторинг телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="23dac-111">Opening a phone device in owner mode also provides monitoring of the phone device.</span></span> <span data-ttu-id="23dac-112">Только одно приложение может быть владельцем телефонного устройства в любое заданное время.</span><span class="sxs-lookup"><span data-stu-id="23dac-112">Only one application is allowed to be the owner of a phone device at any given time.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23dac-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23dac-113">Remarks</span></span>

<span data-ttu-id="23dac-114">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="23dac-114">No extensibility.</span></span> <span data-ttu-id="23dac-115">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="23dac-115">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="23dac-116">Требования</span><span class="sxs-lookup"><span data-stu-id="23dac-116">Requirements</span></span>



| <span data-ttu-id="23dac-117">Требование</span><span class="sxs-lookup"><span data-stu-id="23dac-117">Requirement</span></span> | <span data-ttu-id="23dac-118">Значение</span><span class="sxs-lookup"><span data-stu-id="23dac-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="23dac-119">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="23dac-119">TAPI version</span></span><br/> | <span data-ttu-id="23dac-120">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="23dac-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="23dac-121">Header</span><span class="sxs-lookup"><span data-stu-id="23dac-121">Header</span></span><br/>       | <dl> <span data-ttu-id="23dac-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="23dac-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




