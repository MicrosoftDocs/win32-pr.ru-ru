---
description: 'Дополнительные сведения о: Server2003Grbits. Форвардонли поле'
title: Поле Server2003Grbits. Форвардонли (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: ForwardOnly field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.forwardonly(v=EXCHG.10)
ms:contentKeyID: 55104214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.ForwardOnly
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec4427628e8d6bfee427fa91c15ed6aee3887314
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155003"
---
# <a name="server2003grbitsforwardonly-field"></a>Server2003Grbits. Форвардонли, поле

Этот параметр запрашивает создание временной таблицы только в том случае, если диспетчер временных таблиц может использовать реализацию, оптимизированную для промежуточных результатов запроса. Если любая характеристика временной таблицы не позволит использовать эту оптимизацию, операция завершится с JET_errCannotMaterializeForwardOnlySort. Побочный результат этого параметра — Разрешить временной таблице содержать записи с повторяющимися ключами индекса. Дополнительные сведения см. в разделе [UNIQUE](./temptablegrbit-enumeration.md) .

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Const ForwardOnly As TempTableGrbit
'Usage
Dim value As TempTableGrbit

value = Server2003Grbits.ForwardOnly
```

``` csharp
public const TempTableGrbit ForwardOnly
```

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Server2003Grbits](./server2003grbits-class.md)

[Элементы Server2003Grbits](./server2003grbits-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
