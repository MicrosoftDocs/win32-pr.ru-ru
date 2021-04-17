---
description: '\_Константы побитового флага фонестатусфлагс описывают различные сведения о состоянии телефонного устройства.'
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Константы PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675135"
---
# <a name="phonestatusflags_-constants"></a><span data-ttu-id="5ee16-103">\_Константы фонестатусфлагс</span><span class="sxs-lookup"><span data-stu-id="5ee16-103">PHONESTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="5ee16-104">Константы побитового флага **фонестатусфлагс \_** описывают различные сведения о состоянии телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="5ee16-104">The **PHONESTATUSFLAGS\_** bit-flag constants describe a variety of phone device status information.</span></span>

<dl> <dt>

<span data-ttu-id="5ee16-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**ФОНЕСТАТУСФЛАГС \_ подключен**</span><span class="sxs-lookup"><span data-stu-id="5ee16-105"><span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5ee16-106">Указывает, подключен ли телефон к TAPI в данный момент.</span><span class="sxs-lookup"><span data-stu-id="5ee16-106">Specifies whether the phone is currently connected to TAPI.</span></span> <span data-ttu-id="5ee16-107">**Значение true** , если соединение установлено; в противном случае — **false** .</span><span class="sxs-lookup"><span data-stu-id="5ee16-107">**TRUE** if connected, **FALSE** otherwise.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5ee16-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**ФОНЕСТАТУСФЛАГС \_ приостановлен**</span><span class="sxs-lookup"><span data-stu-id="5ee16-108"><span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5ee16-109">Указывает, приостановлена ли работа TAPI телефонного устройства.</span><span class="sxs-lookup"><span data-stu-id="5ee16-109">Specifies whether TAPI's manipulation of the phone device is suspended.</span></span> <span data-ttu-id="5ee16-110">**Значение true** , если suspended, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5ee16-110">**TRUE** if suspended, **FALSE** otherwise.</span></span> <span data-ttu-id="5ee16-111">Использование приложения телефонного устройства может быть временно приостановлено, когда коммутатор хочет управлять телефонным способом, который не допускает помех от приложения.</span><span class="sxs-lookup"><span data-stu-id="5ee16-111">An application's use of a phone device can be temporarily suspended when the switch wants to manipulate the phone in a way that cannot tolerate interference from the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ee16-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ee16-112">Remarks</span></span>

<span data-ttu-id="5ee16-113">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="5ee16-113">No extensibility.</span></span> <span data-ttu-id="5ee16-114">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="5ee16-114">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee16-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5ee16-115">Requirements</span></span>



| <span data-ttu-id="5ee16-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5ee16-116">Requirement</span></span> | <span data-ttu-id="5ee16-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5ee16-117">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5ee16-118">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="5ee16-118">TAPI version</span></span><br/> | <span data-ttu-id="5ee16-119">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="5ee16-119">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="5ee16-120">Header</span><span class="sxs-lookup"><span data-stu-id="5ee16-120">Header</span></span><br/>       | <dl> <span data-ttu-id="5ee16-121"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ee16-121"><dt>Tapi.h</dt></span></span> </dl> |



 

 




