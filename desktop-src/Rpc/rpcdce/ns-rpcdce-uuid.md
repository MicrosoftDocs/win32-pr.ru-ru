---
title: UUID
description: Предоставляет уникальное обозначение объекта, такого как интерфейс, вектор точки входа диспетчера или объект клиента.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 31ff8eb22a234020e0da5b5ebb5799d5ddb0c8d1dca7bc094394f79a5ceb0c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925951"
---
# <a name="uuid-structure"></a>Структура UUID

Структура **UUID** определяет универсальный уникальный идентификатор (UUID). **UUID** обеспечивает уникальное обозначение объекта, такого как интерфейс, вектор точки входа диспетчера или объект клиента.

Структура **UUID** является `typedef` синонимом для структуры [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) .

## <a name="syntax"></a>Синтаксис

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Remarks

Библиотеки времени выполнения RPC используют **UUID** s для проверки совместимости между клиентами и серверами, а также для выбора из нескольких реализаций интерфейса.

## <a name="requirements"></a>Requirements (Требования)

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | Определено в рпкдце. h; включить RPC. h |

## <a name="see-also"></a>См. также раздел

[Идентификатор GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VECTOR (вектор](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector) )