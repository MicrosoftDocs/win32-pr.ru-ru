---
description: '\_Константы побитового флага линепаркмоде описывают различные способы вызовов парковки.'
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: Константы LINEPARKMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689174"
---
# <a name="lineparkmode_-constants"></a><span data-ttu-id="19a0e-103">\_Константы линепаркмоде</span><span class="sxs-lookup"><span data-stu-id="19a0e-103">LINEPARKMODE\_ Constants</span></span>

<span data-ttu-id="19a0e-104">Константы побитового флага **линепаркмоде \_** описывают различные способы вызовов парковки.</span><span class="sxs-lookup"><span data-stu-id="19a0e-104">The **LINEPARKMODE\_** bit-flag constants describe different ways of parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="19a0e-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**ЛИНЕПАРКМОДЕ \_**</span><span class="sxs-lookup"><span data-stu-id="19a0e-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE\_DIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19a0e-106">Указывает приостановку направленного вызова.</span><span class="sxs-lookup"><span data-stu-id="19a0e-106">Specifies directed call park.</span></span> <span data-ttu-id="19a0e-107">Адрес для приостановки вызова должен быть указан в параметре.</span><span class="sxs-lookup"><span data-stu-id="19a0e-107">The address where the call is to be parked must be supplied to the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="19a0e-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**ЛИНЕПАРКМОДЕ \_ НЕнаправленный**</span><span class="sxs-lookup"><span data-stu-id="19a0e-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE\_NONDIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="19a0e-109">Указывает приостановку ненаправленного вызова.</span><span class="sxs-lookup"><span data-stu-id="19a0e-109">Specifies nondirected call park.</span></span> <span data-ttu-id="19a0e-110">Адрес, по которому приостановлен звонок, выбирается параметром и предоставляется коммутатором в приложении.</span><span class="sxs-lookup"><span data-stu-id="19a0e-110">The address where the call is parked is selected by the switch and provided by the switch to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19a0e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19a0e-111">Remarks</span></span>

<span data-ttu-id="19a0e-112">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="19a0e-112">No extensibility.</span></span> <span data-ttu-id="19a0e-113">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="19a0e-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="19a0e-114">**\_ Константы линепаркмоде** используются при вызове функции парковки.</span><span class="sxs-lookup"><span data-stu-id="19a0e-114">The **LINEPARKMODE\_ constants** are used when parking a call.</span></span> <span data-ttu-id="19a0e-115">Чтобы узнать, какой режим парковки доступен, ознакомьтесь с возможностями адресной строки устройства.</span><span class="sxs-lookup"><span data-stu-id="19a0e-115">Consult a line's address device capabilities to find out which park mode is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="19a0e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="19a0e-116">Requirements</span></span>



| <span data-ttu-id="19a0e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="19a0e-117">Requirement</span></span> | <span data-ttu-id="19a0e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="19a0e-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="19a0e-119">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="19a0e-119">TAPI version</span></span><br/> | <span data-ttu-id="19a0e-120">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="19a0e-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="19a0e-121">Header</span><span class="sxs-lookup"><span data-stu-id="19a0e-121">Header</span></span><br/>       | <dl> <span data-ttu-id="19a0e-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="19a0e-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




