---
description: '\_Константы побитового флага линетрансфермоде описывают различные способы разрешения запросов на пересылку вызовов.'
ms.assetid: 0a01131f-b63c-45ef-a0a9-17d69a0dacf9
title: Константы LINETRANSFERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fff01f68ab4c43cf15a532639ade9d357a269ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674967"
---
# <a name="linetransfermode_-constants"></a><span data-ttu-id="433b1-103">\_Константы линетрансфермоде</span><span class="sxs-lookup"><span data-stu-id="433b1-103">LINETRANSFERMODE\_ Constants</span></span>

<span data-ttu-id="433b1-104">Константы побитового флага **линетрансфермоде \_** описывают различные способы разрешения запросов на пересылку вызовов.</span><span class="sxs-lookup"><span data-stu-id="433b1-104">The **LINETRANSFERMODE\_** bit-flag constants describe different ways of resolving call transfer requests.</span></span>

<dl> <dt>

<span data-ttu-id="433b1-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**\_Конференция линетрансфермоде**</span><span class="sxs-lookup"><span data-stu-id="433b1-105"><span id="LINETRANSFERMODE_CONFERENCE"></span><span id="linetransfermode_conference"></span>**LINETRANSFERMODE\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="433b1-106">Перенос разрешается путем создания односторонней конференции между приложением, стороной, подключенной к первому вызову, и стороной, подключенной к вызову консультации.</span><span class="sxs-lookup"><span data-stu-id="433b1-106">The transfer is resolved by establishing a three-way conference between the application, the party connected to the initial call, and the party connected to the consultation call.</span></span> <span data-ttu-id="433b1-107">При выборе этого параметра создается вызов Конференции.</span><span class="sxs-lookup"><span data-stu-id="433b1-107">A conference call is created when this option is selected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="433b1-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**\_Перенос линетрансфермоде**</span><span class="sxs-lookup"><span data-stu-id="433b1-108"><span id="LINETRANSFERMODE_TRANSFER"></span><span id="linetransfermode_transfer"></span>**LINETRANSFERMODE\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="433b1-109">Передача разрешается путем передачи начального вызова в вызов консультации.</span><span class="sxs-lookup"><span data-stu-id="433b1-109">The transfer is resolved by transferring the initial call to the consultation call.</span></span> <span data-ttu-id="433b1-110">Оба вызова превращаются в состояние простоя приложения.</span><span class="sxs-lookup"><span data-stu-id="433b1-110">Both calls will become idle to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="433b1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="433b1-111">Remarks</span></span>

<span data-ttu-id="433b1-112">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="433b1-112">No extensibility.</span></span> <span data-ttu-id="433b1-113">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="433b1-113">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="433b1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="433b1-114">Requirements</span></span>



| <span data-ttu-id="433b1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="433b1-115">Requirement</span></span> | <span data-ttu-id="433b1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="433b1-116">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="433b1-117">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="433b1-117">TAPI version</span></span><br/> | <span data-ttu-id="433b1-118">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="433b1-118">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="433b1-119">Header</span><span class="sxs-lookup"><span data-stu-id="433b1-119">Header</span></span><br/>       | <dl> <span data-ttu-id="433b1-120"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="433b1-120"><dt>Tapi.h</dt></span></span> </dl> |



 

 




