---
title: Структура подключений (Напенфорцементклиент. h)
description: Содержит сведения о списке соединений, поддерживаемых средством применения.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Структура подключений NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989420"
---
# <a name="connections-structure"></a><span data-ttu-id="27128-104">Структура соединений</span><span class="sxs-lookup"><span data-stu-id="27128-104">Connections structure</span></span>

> [!Note]  
> <span data-ttu-id="27128-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="27128-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="27128-106">Структура **Connections** содержит сведения о списке соединений, обслуживаемых средством применения.</span><span class="sxs-lookup"><span data-stu-id="27128-106">The **Connections** structure contains information about the list of connections maintained by an enforcer.</span></span>

## <a name="syntax"></a><span data-ttu-id="27128-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27128-107">Syntax</span></span>


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a><span data-ttu-id="27128-108">Члены</span><span class="sxs-lookup"><span data-stu-id="27128-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="27128-109">**count**</span><span class="sxs-lookup"><span data-stu-id="27128-109">**count**</span></span>
</dt> <dd>

<span data-ttu-id="27128-110">Число активных соединений, которые в настоящее время поддерживаются принудительно в диапазоне от 0 (нуля) до [**максконнектионкаунтперенфорцер**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="27128-110">The number of active connections currently maintained by an enforcer within the range 0 (zero) to [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="27128-111">**соединение**</span><span class="sxs-lookup"><span data-stu-id="27128-111">**connections**</span></span>
</dt> <dd>

<span data-ttu-id="27128-112">COM-указатель на список интерфейсов [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) , представляющих клиентские соединения.</span><span class="sxs-lookup"><span data-stu-id="27128-112">A COM pointer to a list of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interfaces that represent client connections.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27128-113">Требования</span><span class="sxs-lookup"><span data-stu-id="27128-113">Requirements</span></span>



| <span data-ttu-id="27128-114">Требование</span><span class="sxs-lookup"><span data-stu-id="27128-114">Requirement</span></span> | <span data-ttu-id="27128-115">Значение</span><span class="sxs-lookup"><span data-stu-id="27128-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27128-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27128-116">Minimum supported client</span></span><br/> | <span data-ttu-id="27128-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27128-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="27128-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27128-118">Minimum supported server</span></span><br/> | <span data-ttu-id="27128-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27128-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="27128-120">Header</span><span class="sxs-lookup"><span data-stu-id="27128-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="27128-121"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="27128-121"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="27128-122">IDL</span><span class="sxs-lookup"><span data-stu-id="27128-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="27128-123"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="27128-123"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27128-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27128-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27128-125">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="27128-125">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="27128-126">Структуры NAP</span><span class="sxs-lookup"><span data-stu-id="27128-126">NAP Structures</span></span>](nap-structures.md)
</dt> <dt>

[<span data-ttu-id="27128-127">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="27128-127">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





