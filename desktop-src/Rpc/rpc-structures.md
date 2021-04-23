---
title: Структуры RPC
description: В этом разделе объясняются структуры, определенные и используемые в Microsoft RPC.
ms.assetid: 8d2f31f6-21d3-402c-b84b-960a2d03ff40
keywords:
- Удаленный вызов процедур RPC, ссылки, структуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94d03209af8b14f87cd8b15929389b6eb524833
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793201"
---
# <a name="rpc-structures"></a><span data-ttu-id="1f07b-104">Структуры RPC</span><span class="sxs-lookup"><span data-stu-id="1f07b-104">RPC Structures</span></span>

<span data-ttu-id="1f07b-105">В этом разделе объясняются структуры, определенные и используемые в Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="1f07b-105">This section explains the structures defined and used by Microsoft RPC.</span></span>

-   <span data-ttu-id="1f07b-106">[**NDR \_ сконтекст**](/previous-versions/aa374336(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="1f07b-106">[**NDR\_SCONTEXT**](/previous-versions/aa374336(v=vs.80))</span></span>
-   [<span data-ttu-id="1f07b-107">**УСТРОЙСТВА**</span><span class="sxs-lookup"><span data-stu-id="1f07b-107">**GUID**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
-   [<span data-ttu-id="1f07b-108">**\_ \_ сведения о МАРШАЛИРОВАНИИ пользователя NDR \_**</span><span class="sxs-lookup"><span data-stu-id="1f07b-108">**NDR\_USER\_MARSHAL\_INFO**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info)
-   [<span data-ttu-id="1f07b-109">**\_ \_ Сведения о МАРШАЛИРОВАНИИ пользователя NDR \_ \_ level1**</span><span class="sxs-lookup"><span data-stu-id="1f07b-109">**NDR\_USER\_MARSHAL\_INFO\_LEVEL1**</span></span>](/windows/win32/api/Rpcndr/ns-rpcndr-ndr_user_marshal_info_level1)
-   [<span data-ttu-id="1f07b-110">**\_асинхронные \_ сведения об УВЕДОМЛЕНии RPC \_**</span><span class="sxs-lookup"><span data-stu-id="1f07b-110">**RPC\_ASYNC\_NOTIFICATION\_INFO**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_notification_info)
-   [<span data-ttu-id="1f07b-111">**\_асинхронное \_ Состояние RPC**</span><span class="sxs-lookup"><span data-stu-id="1f07b-111">**RPC\_ASYNC\_STATE**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_async_state)
-   [<span data-ttu-id="1f07b-112">**\_ \_ Параметры обработчика привязки RPC \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="1f07b-112">**RPC\_BINDING\_HANDLE\_OPTIONS\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_options_v1)
-   [<span data-ttu-id="1f07b-113">**\_ \_ Безопасность маркера привязки RPC \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="1f07b-113">**RPC\_BINDING\_HANDLE\_SECURITY\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a)
-   [<span data-ttu-id="1f07b-114">**\_ \_ Шаблон маркера привязки RPC \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="1f07b-114">**RPC\_BINDING\_HANDLE\_TEMPLATE\_V1**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a)
-   [<span data-ttu-id="1f07b-115">**\_вектор привязки \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="1f07b-115">**RPC\_BINDING\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_binding_vector)
-   [<span data-ttu-id="1f07b-116">**\_ \_ \_ \_ дескриптор проверки подлинности "RPC C opt" \_**</span><span class="sxs-lookup"><span data-stu-id="1f07b-116">**RPC\_C\_OPT\_COOKIE\_AUTH\_DESCRIPTOR**</span></span>](/windows/win32/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor)
-   [<span data-ttu-id="1f07b-117">**\_Атрибуты вызова \_ RPC \_ v1**</span><span class="sxs-lookup"><span data-stu-id="1f07b-117">**RPC\_CALL\_ATTRIBUTES\_V1**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v1_a)
-   [<span data-ttu-id="1f07b-118">**\_Атрибуты вызова \_ RPC \_ v2**</span><span class="sxs-lookup"><span data-stu-id="1f07b-118">**RPC\_CALL\_ATTRIBUTES\_V2**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a)
-   [<span data-ttu-id="1f07b-119">**\_Локальный адрес удаленного вызова процедур \_ \_ \_ v1**</span><span class="sxs-lookup"><span data-stu-id="1f07b-119">**RPC\_CALL\_LOCAL\_ADDRESS\_V1**</span></span>](/windows/win32/api/Rpcasync/ns-rpcasync-rpc_call_local_address_v1)
-   [<span data-ttu-id="1f07b-120">**\_клиентский \_ интерфейс RPC**</span><span class="sxs-lookup"><span data-stu-id="1f07b-120">**RPC\_CLIENT\_INTERFACE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_client_interface)
-   [<span data-ttu-id="1f07b-121">**\_Таблица ДИСПЕТЧЕРИЗАЦИИ \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="1f07b-121">**RPC\_DISPATCH\_TABLE**</span></span>](/windows/win32/api/RpcdceP/ns-rpcdcep-rpc_dispatch_table)
-   [<span data-ttu-id="1f07b-122">**\_ \_ параметр сведений RPC \_ ee**</span><span class="sxs-lookup"><span data-stu-id="1f07b-122">**RPC\_EE\_INFO\_PARAM**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_ee_info_param)
-   [<span data-ttu-id="1f07b-123">**\_шаблон конечной точки RPC \_**</span><span class="sxs-lookup"><span data-stu-id="1f07b-123">**RPC\_ENDPOINT\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_endpoint_template)
-   [<span data-ttu-id="1f07b-124">**\_ \_ маркер ПЕРЕЧИСЛЕНИЯ ошибок \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="1f07b-124">**RPC\_ERROR\_ENUM\_HANDLE**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_error_enum_handle)
-   [<span data-ttu-id="1f07b-125">**\_Расширенные \_ сведения об ОШИБКе RPC \_**</span><span class="sxs-lookup"><span data-stu-id="1f07b-125">**RPC\_EXTENDED\_ERROR\_INFO**</span></span>](/windows/win32/api/rpcasync/ns-rpcasync-rpc_extended_error_info)
-   [<span data-ttu-id="1f07b-126">**\_ \_ \_ учетные данные транспорта HTTP RPC**</span><span class="sxs-lookup"><span data-stu-id="1f07b-126">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_a)
-   [<span data-ttu-id="1f07b-127">**\_ \_ Учетные данные транспорта HTTP для RPC \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="1f07b-127">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v2_a)
-   [<span data-ttu-id="1f07b-128">**\_ \_ \_ Учетные данные транспорта HTTP RPC \_ v3**</span><span class="sxs-lookup"><span data-stu-id="1f07b-128">**RPC\_HTTP\_TRANSPORT\_CREDENTIALS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_http_transport_credentials_v3_a)
-   [<span data-ttu-id="1f07b-129">**Идентификатор RPC, \_ Если \_ ИД**</span><span class="sxs-lookup"><span data-stu-id="1f07b-129">**RPC\_IF\_ID**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id)
-   [<span data-ttu-id="1f07b-130">**RPC, \_ Если \_ идентификатор \_ вектора**</span><span class="sxs-lookup"><span data-stu-id="1f07b-130">**RPC\_IF\_ID\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_if_id_vector)
-   [<span data-ttu-id="1f07b-131">**\_шаблон интерфейса \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="1f07b-131">**RPC\_INTERFACE\_TEMPLATE**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_interface_template)
-   [<span data-ttu-id="1f07b-132">**\_Политика RPC**</span><span class="sxs-lookup"><span data-stu-id="1f07b-132">**RPC\_POLICY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_policy)
-   [<span data-ttu-id="1f07b-133">**\_вектор ПРОТСЕК \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="1f07b-133">**RPC\_PROTSEQ\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_protseq_vector)
-   [<span data-ttu-id="1f07b-134">**Служба \_ безопасности RPC \_ QoS**</span><span class="sxs-lookup"><span data-stu-id="1f07b-134">**RPC\_SECURITY\_QOS**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos)
-   [<span data-ttu-id="1f07b-135">**RPC \_ Security \_ QoS \_ v2**</span><span class="sxs-lookup"><span data-stu-id="1f07b-135">**RPC\_SECURITY\_QOS\_V2**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v2_a)
-   [<span data-ttu-id="1f07b-136">**RPC \_ Security \_ QoS \_ v3**</span><span class="sxs-lookup"><span data-stu-id="1f07b-136">**RPC\_SECURITY\_QOS\_V3**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v3_a)
-   [<span data-ttu-id="1f07b-137">**RPC \_ Security \_ QoS \_ v4**</span><span class="sxs-lookup"><span data-stu-id="1f07b-137">**RPC\_SECURITY\_QOS\_V4**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v4_a)
-   [<span data-ttu-id="1f07b-138">**RPC \_ Security \_ QoS \_ V5**</span><span class="sxs-lookup"><span data-stu-id="1f07b-138">**RPC\_SECURITY\_QOS\_V5**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_security_qos_v5_a)
-   [<span data-ttu-id="1f07b-139">**\_вектор статистики \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="1f07b-139">**RPC\_STATS\_VECTOR**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-rpc_stats_vector)
-   [<span data-ttu-id="1f07b-140">**с \_ WinNT \_ AUTH \_ Identity**</span><span class="sxs-lookup"><span data-stu-id="1f07b-140">**SEC\_WINNT\_AUTH\_IDENTITY**</span></span>](/windows/win32/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a)
-   [<span data-ttu-id="1f07b-141">**UUID**</span><span class="sxs-lookup"><span data-stu-id="1f07b-141">**UUID**</span></span>](./rpcdce/ns-rpcdce-uuid.md)
-   [<span data-ttu-id="1f07b-142">**\_вектор UUID**</span><span class="sxs-lookup"><span data-stu-id="1f07b-142">**UUID\_VECTOR**</span></span>](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)

 

 