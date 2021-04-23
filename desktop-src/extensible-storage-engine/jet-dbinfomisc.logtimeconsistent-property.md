---
description: 'Дополнительные сведения о свойстве: JET_DBINFOMISC. Логтимеконсистент'
title: Свойство JET_DBINFOMISC. Логтимеконсистент
TOCTitle: 'logtimeConsistent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.logtimeconsistent(v=EXCHG.10)
ms:contentKeyID: 39513228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_logtimeConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_logtimeConsistent
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d46302373df17e147095c5ac5c37f02ffef1eb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143627"
---
# <a name="jet_dbinfomisclogtimeconsistent-property"></a><span data-ttu-id="51ca0-103">Свойство JET_DBINFOMISC. Логтимеконсистент</span><span class="sxs-lookup"><span data-stu-id="51ca0-103">JET_DBINFOMISC.logtimeConsistent property</span></span>

<span data-ttu-id="51ca0-104">Возвращает время, когда база данных была сделана целостной.</span><span class="sxs-lookup"><span data-stu-id="51ca0-104">Gets the time when the database was made consistent.</span></span> <span data-ttu-id="51ca0-105">Если база данных не согласуется, это значение равно null.</span><span class="sxs-lookup"><span data-stu-id="51ca0-105">This value is null if the database is inconsistent.</span></span>

<span data-ttu-id="51ca0-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="51ca0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="51ca0-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="51ca0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="51ca0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51ca0-108">Syntax</span></span>

``` vb
'Declaration
Public Property logtimeConsistent As JET_LOGTIME
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LOGTIME

value = instance.logtimeConsistent
```

``` csharp
public JET_LOGTIME logtimeConsistent { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="51ca0-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="51ca0-109">Property value</span></span>

<span data-ttu-id="51ca0-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="51ca0-110">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="51ca0-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51ca0-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="51ca0-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="51ca0-112">Reference</span></span>

[<span data-ttu-id="51ca0-113">Класс JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="51ca0-113">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="51ca0-114">Элементы JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="51ca0-114">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="51ca0-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="51ca0-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
