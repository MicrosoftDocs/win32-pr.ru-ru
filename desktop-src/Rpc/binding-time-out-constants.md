---
title: Константы времени ожидания привязки (Рпкдце. h)
description: В библиотеке RPC используются константы времени ожидания привязки, чтобы указать относительное количество времени, которое должно быть затрачено на установку привязки к серверу.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672593"
---
# <a name="binding-time-out-constants"></a><span data-ttu-id="bded0-103">Константы времени ожидания привязки</span><span class="sxs-lookup"><span data-stu-id="bded0-103">Binding Time-out Constants</span></span>

<span data-ttu-id="bded0-104">В библиотеке RPC используются константы времени ожидания привязки, чтобы указать относительное количество времени, которое должно быть затрачено на установку привязки к серверу.</span><span class="sxs-lookup"><span data-stu-id="bded0-104">The RPC library uses the binding time-out constants to specify the relative amount of time that should be spent to establish a binding to the server before giving up.</span></span> <span data-ttu-id="bded0-105">Время ожидания можно включить с помощью вызова функции [**рпкмгмтсеткомтимеаут**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) .</span><span class="sxs-lookup"><span data-stu-id="bded0-105">The timeout can be enabled with a call to the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function.</span></span> <span data-ttu-id="bded0-106">В следующем списке содержатся допустимые значения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="bded0-106">The following list contains the valid time-out values.</span></span>



| <span data-ttu-id="bded0-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="bded0-107">Constant/value</span></span>                                                                                                                                                                                                                                                                | <span data-ttu-id="bded0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="bded0-108">Description</span></span>                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <span data-ttu-id="bded0-109"><dt>**RPC \_ \_ \_ Бесконечное \_ время ожидания привязки C**</dt> <dt> 10</dt></span><span class="sxs-lookup"><span data-stu-id="bded0-109"><dt>**RPC\_C\_BINDING\_INFINITE\_TIMEOUT**</dt> <dt> 10 </dt></span></span> </dl> | <span data-ttu-id="bded0-110">Постоянно пытается установить связь.</span><span class="sxs-lookup"><span data-stu-id="bded0-110">Keeps trying to establish communications forever.</span></span><br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <span data-ttu-id="bded0-111"><dt>**RPC \_ \_ \_ Минимальное \_ время ожидания привязки C**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bded0-111"><dt>**RPC\_C\_BINDING\_MIN\_TIMEOUT**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="bded0-112">Пытается установить минимальное количество времени для используемого сетевого протокола.</span><span class="sxs-lookup"><span data-stu-id="bded0-112">Tries the minimum amount of time for the network protocol being used.</span></span> <span data-ttu-id="bded0-113">Это значение отдает предпочтение времени отклика относительно правильности определения того, работает ли сервер.</span><span class="sxs-lookup"><span data-stu-id="bded0-113">This value favors response time over correctness in determining whether the server is running.</span></span><br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <span data-ttu-id="bded0-114"><dt>**RPC \_ \_ \_ \_ Время ожидания привязки C по умолчанию**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="bded0-114"><dt>**RPC\_C\_BINDING\_DEFAULT\_TIMEOUT**</dt> <dt>5</dt></span></span> </dl>       | <span data-ttu-id="bded0-115">Пытается использовать средний интервал времени для используемого сетевого протокола.</span><span class="sxs-lookup"><span data-stu-id="bded0-115">Tries an average amount of time for the network protocol being used.</span></span> <span data-ttu-id="bded0-116">Это значение дает возможность определить, работает ли сервер, и возвращает время ответа равным весу.</span><span class="sxs-lookup"><span data-stu-id="bded0-116">This value gives correctness in determining whether a server is running and gives response time equal weight.</span></span> <span data-ttu-id="bded0-117">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bded0-117">This is the default value.</span></span><br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <span data-ttu-id="bded0-118"><dt>**RPC \_ \_ \_ Максимальное \_ время ожидания привязки C**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="bded0-118"><dt>**RPC\_C\_BINDING\_MAX\_TIMEOUT**</dt> <dt>9</dt></span></span> </dl>                   | <span data-ttu-id="bded0-119">Пытается использовать для сетевого протокола самое длинное время.</span><span class="sxs-lookup"><span data-stu-id="bded0-119">Tries the longest amount of time for the network protocol being used.</span></span> <span data-ttu-id="bded0-120">Это значение подходит для определения того, работает ли сервер в течение времени ответа.</span><span class="sxs-lookup"><span data-stu-id="bded0-120">This value favors correctness in determining whether a server is running over response time.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="bded0-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bded0-121">Remarks</span></span>

<span data-ttu-id="bded0-122">Значения в приведенной выше таблице не могут быть в секундах.</span><span class="sxs-lookup"><span data-stu-id="bded0-122">The values in the preceding table are not in seconds.</span></span> <span data-ttu-id="bded0-123">Эти значения представляют относительное количество времени в масштабе от нуля до 10.</span><span class="sxs-lookup"><span data-stu-id="bded0-123">These values represent a relative amount of time on a scale of zero to 10.</span></span> <span data-ttu-id="bded0-124">Дополнительные сведения о предотвращении задержки связи см. в статье предотвращение зависаний на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="bded0-124">For more information on avoiding communication delays, refer to Preventing Client-side Hangs.</span></span>

## <a name="requirements"></a><span data-ttu-id="bded0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="bded0-125">Requirements</span></span>



| <span data-ttu-id="bded0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="bded0-126">Requirement</span></span> | <span data-ttu-id="bded0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="bded0-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bded0-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bded0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bded0-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bded0-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bded0-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bded0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bded0-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bded0-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bded0-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bded0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bded0-133"><dt>Рпкдце. h</dt></span><span class="sxs-lookup"><span data-stu-id="bded0-133"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





