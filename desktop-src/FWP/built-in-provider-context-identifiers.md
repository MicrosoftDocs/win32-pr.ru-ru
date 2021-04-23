---
title: Встроенные идентификаторы контекста поставщика (Фвпму. h)
description: Встроенные контексты поставщика указывают политики по умолчанию для использования с защищенными сокетами.
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488997"
---
# <a name="built-in-provider-context-identifiers"></a><span data-ttu-id="31b99-103">Встроенные идентификаторы контекста поставщика</span><span class="sxs-lookup"><span data-stu-id="31b99-103">Built-in Provider Context Identifiers</span></span>

<span data-ttu-id="31b99-104">Идентификаторы для контекстов поставщиков, встроенных в платформу фильтрации Windows (WFP), представляются идентификаторами GUID.</span><span class="sxs-lookup"><span data-stu-id="31b99-104">The identifiers for the provider contexts that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="31b99-105">Эти встроенные контексты поставщика указывают политики по умолчанию для использования с защищенными сокетами.</span><span class="sxs-lookup"><span data-stu-id="31b99-105">These built-in provider contexts identify the default policies to use with secure sockets.</span></span>

<span data-ttu-id="31b99-106">Эти идентификаторы определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="31b99-106">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="31b99-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**\_контекст поставщика \_ фвпм \_ безопасный \_ сокет \_ AUTHIP**</span><span class="sxs-lookup"><span data-stu-id="31b99-107"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="31b99-108">Политика по умолчанию для протокола AuthIP в основном режиме для защищенных сокетов.</span><span class="sxs-lookup"><span data-stu-id="31b99-108">Authenticated Internet Protocol (AuthIP) main mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31b99-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**\_ \_ \_ защищенный \_ сокет IPSec контекста \_ поставщика фвпм**</span><span class="sxs-lookup"><span data-stu-id="31b99-109"><span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**FWPM\_PROVIDER\_CONTEXT\_SECURE\_SOCKET\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="31b99-110">Политика по умолчанию быстрого режима IPsec для защищенных сокетов.</span><span class="sxs-lookup"><span data-stu-id="31b99-110">Internet Protocol Security (IPsec) quick mode default policy for secure sockets.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31b99-111">Требования</span><span class="sxs-lookup"><span data-stu-id="31b99-111">Requirements</span></span>



| <span data-ttu-id="31b99-112">Требование</span><span class="sxs-lookup"><span data-stu-id="31b99-112">Requirement</span></span> | <span data-ttu-id="31b99-113">Значение</span><span class="sxs-lookup"><span data-stu-id="31b99-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="31b99-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31b99-114">Minimum supported client</span></span><br/> | <span data-ttu-id="31b99-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31b99-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="31b99-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31b99-116">Minimum supported server</span></span><br/> | <span data-ttu-id="31b99-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31b99-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="31b99-118">Header</span><span class="sxs-lookup"><span data-stu-id="31b99-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b99-119"><dt>Фвпму. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b99-119"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





