---
title: UUID
description: Предоставляет уникальное обозначение объекта, такого как интерфейс, вектор точки входа диспетчера или объект клиента.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133294"
---
# <a name="uuid-structure"></a><span data-ttu-id="9db47-103">Структура UUID</span><span class="sxs-lookup"><span data-stu-id="9db47-103">UUID structure</span></span>

<span data-ttu-id="9db47-104">Структура **UUID** определяет универсальный уникальный идентификатор (UUID).</span><span class="sxs-lookup"><span data-stu-id="9db47-104">The **UUID** structure defines a Universally Unique Identifier (UUID).</span></span> <span data-ttu-id="9db47-105">**UUID** обеспечивает уникальное обозначение объекта, такого как интерфейс, вектор точки входа диспетчера или объект клиента.</span><span class="sxs-lookup"><span data-stu-id="9db47-105">A **UUID** provides a unique designation of an object such as an interface, a manager entry-point vector, or a client object.</span></span>

<span data-ttu-id="9db47-106">Структура **UUID** является `typedef` синонимом для структуры [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) .</span><span class="sxs-lookup"><span data-stu-id="9db47-106">The **UUID** structure is a `typedef`'d synonym for the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db47-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9db47-107">Syntax</span></span>

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a><span data-ttu-id="9db47-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="9db47-108">Remarks</span></span>

<span data-ttu-id="9db47-109">Библиотеки времени выполнения RPC используют **UUID** s для проверки совместимости между клиентами и серверами, а также для выбора из нескольких реализаций интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9db47-109">The RPC run-time libraries use **UUID** s to check for compatibility between clients and servers, and to select among multiple implementations of an interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="9db47-110">Требования</span><span class="sxs-lookup"><span data-stu-id="9db47-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9db47-111">**Header**</span><span class="sxs-lookup"><span data-stu-id="9db47-111">**Header**</span></span> | <span data-ttu-id="9db47-112">Определено в рпкдце. h; включить RPC. h</span><span class="sxs-lookup"><span data-stu-id="9db47-112">Defined in rpcdce.h; include rpc.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="9db47-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9db47-113">See also</span></span>

<span data-ttu-id="9db47-114">[Идентификатор GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VECTOR (вектор](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector) )</span><span class="sxs-lookup"><span data-stu-id="9db47-114">[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)
[UUID\_VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)</span></span>