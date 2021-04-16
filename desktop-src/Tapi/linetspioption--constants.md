---
description: '\_Константы линетспиоптион описывают поставщики услуг по заказам, которые должны быть вызваны.'
ms.assetid: af91f466-d87e-4767-a2c6-d882b9108f21
title: Константы LINETSPIOPTION_ (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e8fa13047dcbad60472fac371b255f7533809c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689468"
---
# <a name="linetspioption_-constants"></a><span data-ttu-id="1b92d-103">\_Константы линетспиоптион</span><span class="sxs-lookup"><span data-stu-id="1b92d-103">LINETSPIOPTION\_ Constants</span></span>

<span data-ttu-id="1b92d-104">**\_ Константы линетспиоптион** описывают поставщики услуг по заказам, которые должны быть вызваны.</span><span class="sxs-lookup"><span data-stu-id="1b92d-104">The **LINETSPIOPTION\_ constants** describes the order service providers should be called.</span></span>

<dl> <dt>

<span data-ttu-id="1b92d-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**ЛИНЕТСПИОПТИОН \_ нонринтрант**</span><span class="sxs-lookup"><span data-stu-id="1b92d-105"><span id="LINETSPIOPTION_NONREENTRANT"></span><span id="linetspioption_nonreentrant"></span>**LINETSPIOPTION\_NONREENTRANT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1b92d-106">TAPI должен по одному вызывать функции этого поставщика услуг; перед вызовом той же или другой функции в том же или другом потоке он должен ожидать от каждой функции возврата (но не для завершения асинхронных функций).</span><span class="sxs-lookup"><span data-stu-id="1b92d-106">TAPI should call functions in this service provider one at a time; it should wait from each function to return (but not for asynchronous functions to complete) before calling the same or another function, either on the same or a different thread, on the same or a different processor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b92d-107">Требования</span><span class="sxs-lookup"><span data-stu-id="1b92d-107">Requirements</span></span>



| <span data-ttu-id="1b92d-108">Требование</span><span class="sxs-lookup"><span data-stu-id="1b92d-108">Requirement</span></span> | <span data-ttu-id="1b92d-109">Значение</span><span class="sxs-lookup"><span data-stu-id="1b92d-109">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1b92d-110">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="1b92d-110">TAPI version</span></span><br/> | <span data-ttu-id="1b92d-111">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1b92d-111">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1b92d-112">Header</span><span class="sxs-lookup"><span data-stu-id="1b92d-112">Header</span></span><br/>       | <dl> <span data-ttu-id="1b92d-113"><dt>Тспи. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b92d-113"><dt>Tspi.h</dt></span></span> </dl> |



 

 




