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
# <a name="server2003grbitsforwardonly-field"></a><span data-ttu-id="38233-103">Server2003Grbits. Форвардонли, поле</span><span class="sxs-lookup"><span data-stu-id="38233-103">Server2003Grbits.ForwardOnly field</span></span>

<span data-ttu-id="38233-104">Этот параметр запрашивает создание временной таблицы только в том случае, если диспетчер временных таблиц может использовать реализацию, оптимизированную для промежуточных результатов запроса.</span><span class="sxs-lookup"><span data-stu-id="38233-104">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="38233-105">Если любая характеристика временной таблицы не позволит использовать эту оптимизацию, операция завершится с JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="38233-105">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="38233-106">Побочный результат этого параметра — Разрешить временной таблице содержать записи с повторяющимися ключами индекса.</span><span class="sxs-lookup"><span data-stu-id="38233-106">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="38233-107">Дополнительные сведения см. в разделе [UNIQUE](./temptablegrbit-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="38233-107">See [Unique](./temptablegrbit-enumeration.md) for more information.</span></span>

<span data-ttu-id="38233-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="38233-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="38233-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="38233-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="38233-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38233-110">Syntax</span></span>

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

## <a name="see-also"></a><span data-ttu-id="38233-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38233-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="38233-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="38233-112">Reference</span></span>

[<span data-ttu-id="38233-113">Класс Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="38233-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="38233-114">Элементы Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="38233-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="38233-115">Пространство имен Microsoft. ISAM. ESENT. Interop. server2003</span><span class="sxs-lookup"><span data-stu-id="38233-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
