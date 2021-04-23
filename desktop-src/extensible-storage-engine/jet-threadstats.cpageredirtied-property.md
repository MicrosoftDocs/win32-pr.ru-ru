---
description: 'Дополнительные сведения о свойстве: JET_THREADSTATS. Кпажередиртиед'
title: Свойство JET_THREADSTATS. Кпажередиртиед (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cPageRedirtied property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRedirtied
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpageredirtied(v=EXCHG.10)
ms:contentKeyID: 39515312
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRedirtied
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRedirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageRedirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageRedirtied
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0ed97a93958ba52231439dc6c2125db982296ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684144"
---
# <a name="jet_threadstatscpageredirtied-property"></a><span data-ttu-id="7d38b-103">Свойство JET_THREADSTATS. Кпажередиртиед</span><span class="sxs-lookup"><span data-stu-id="7d38b-103">JET_THREADSTATS.cPageRedirtied property</span></span>

<span data-ttu-id="7d38b-104">Возвращает общее число страниц базы данных с незаписанными изменениями, которые были изменены ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="7d38b-104">Gets the total number of database pages, with unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="7d38b-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d38b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="7d38b-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d38b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d38b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d38b-107">Syntax</span></span>

``` vb
'Declaration
Public Property cPageRedirtied As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageRedirtied
```

``` csharp
public int cPageRedirtied { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="7d38b-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7d38b-108">Property value</span></span>

<span data-ttu-id="7d38b-109">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7d38b-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7d38b-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d38b-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d38b-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="7d38b-111">Reference</span></span>

[<span data-ttu-id="7d38b-112">Структура JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="7d38b-112">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="7d38b-113">Элементы JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="7d38b-113">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="7d38b-114">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="7d38b-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
