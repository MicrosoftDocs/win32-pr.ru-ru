---
title: Константы уровня проверки подлинности (Рпкдце. h)
description: Эти значения указывают уровень проверки подлинности, указывающий объем проверки подлинности, предоставляемой для защиты целостности данных. Каждый уровень включает защиту, обеспечиваемую предыдущими уровнями.
ms.assetid: 06c409e4-3772-45cf-8c31-c64f99aca244
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdf922118a1b332bfe1fe8e744114a6d1d6bf4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535447"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="cf424-104">Константы уровня проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="cf424-104">Authentication Level Constants</span></span>

<span data-ttu-id="cf424-105">Эти значения указывают уровень проверки подлинности, указывающий объем проверки подлинности, предоставляемой для защиты целостности данных.</span><span class="sxs-lookup"><span data-stu-id="cf424-105">These values specify an authentication level, which indicates the amount of authentication provided to help protect the integrity of the data.</span></span> <span data-ttu-id="cf424-106">Каждый уровень включает защиту, обеспечиваемую предыдущими уровнями.</span><span class="sxs-lookup"><span data-stu-id="cf424-106">Each level includes the protection provided by the previous levels.</span></span>



| <span data-ttu-id="cf424-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="cf424-107">Constant/value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="cf424-108">Описание</span><span class="sxs-lookup"><span data-stu-id="cf424-108">Description</span></span>                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="cf424-109"><dt>**RPC \_ \_AUTHN \_ уровень \_ по умолчанию**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cf424-109"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="cf424-110">Указывает DCOM выбрать уровень проверки подлинности с помощью обычного алгоритма согласования безопасности общего доступа.</span><span class="sxs-lookup"><span data-stu-id="cf424-110">Tells DCOM to choose the authentication level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="cf424-111">Дополнительные сведения см. в разделе [Безопасность — общий согласование](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="cf424-111">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span> <br/> |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="cf424-112"><dt>**RPC \_ \_ \_ Уровень \_ AUTHN**</dt> No <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cf424-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="cf424-113">Не выполняет проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="cf424-113">Performs no authentication.</span></span><br/>                                                                                                                                                                         |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="cf424-114"><dt>**RPC \_ \_AUTHN на \_ уровне \_ подключения**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cf424-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt> <dt>2</dt></span></span> </dl>                    | <span data-ttu-id="cf424-115">Проверяет подлинность учетных данных клиента только в том случае, если клиент устанавливает связь с сервером.</span><span class="sxs-lookup"><span data-stu-id="cf424-115">Authenticates the credentials of the client only when the client establishes a relationship with the server.</span></span> <span data-ttu-id="cf424-116">Для транспорта датаграмм всегда используется RPC на \_ \_ уровне AUTHN \_ .</span><span class="sxs-lookup"><span data-stu-id="cf424-116">Datagram transports always use RPC\_AUTHN\_LEVEL\_PKT instead.</span></span> <br/>                        |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="cf424-117"><dt>**RPC \_ \_ \_ \_ Вызов уровня 3 в AUTHN**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cf424-117"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt> <dt>3</dt></span></span> </dl>                             | <span data-ttu-id="cf424-118">Проверка подлинности выполняется только в начале каждого удаленного вызова процедуры, когда сервер получает запрос.</span><span class="sxs-lookup"><span data-stu-id="cf424-118">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="cf424-119">Для транспорта датаграмм используется маркер RPC \_ C \_ \_ уровня AUTHN \_ .</span><span class="sxs-lookup"><span data-stu-id="cf424-119">Datagram transports use RPC\_C\_AUTHN\_LEVEL\_PKT instead.</span></span><br/>                                  |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="cf424-120"><dt>**RPC \_ \_AUTHN ( \_ \_ PKT) уровня**</dt> 3 <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cf424-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt> <dt>4</dt></span></span> </dl>                                | <span data-ttu-id="cf424-121">Проверяет, что все полученные данные получены от ожидаемого клиента.</span><span class="sxs-lookup"><span data-stu-id="cf424-121">Authenticates that all data received is from the expected client.</span></span><br/>                                                                                                                                   |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="cf424-122"><dt>**RPC \_ \_ \_ \_ \_ Целостность маркера C AUTHN Level**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="cf424-122"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="cf424-123">Проверка подлинности и проверка того, что ни один из данных, передаваемых между клиентом и сервером, не был изменен.</span><span class="sxs-lookup"><span data-stu-id="cf424-123">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                           |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="cf424-124"><dt>**RPC \_ AUTHN на языке C, \_ \_ PKT, \_ \_ Конфиденциальность**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cf424-124"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="cf424-125">Проверяет подлинность всех предыдущих уровней и шифрует значение аргумента каждого удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="cf424-125">Authenticates all previous levels and encrypts the argument value of each remote procedure call.</span></span><br/>                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="cf424-126">Требования</span><span class="sxs-lookup"><span data-stu-id="cf424-126">Requirements</span></span>



| <span data-ttu-id="cf424-127">Требование</span><span class="sxs-lookup"><span data-stu-id="cf424-127">Requirement</span></span> | <span data-ttu-id="cf424-128">Значение</span><span class="sxs-lookup"><span data-stu-id="cf424-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cf424-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf424-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cf424-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf424-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cf424-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf424-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cf424-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf424-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cf424-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cf424-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf424-134"><dt>Рпкдце. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf424-134"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





