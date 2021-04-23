---
description: 'Дополнительные сведения о свойстве: JET_THREADSTATS. Кпажедиртиед'
title: Свойство JET_THREADSTATS. Кпажедиртиед (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cPageDirtied property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpagedirtied(v=EXCHG.10)
ms:contentKeyID: 39512428
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageDirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageDirtied
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageDirtied
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d1f628ce821a6e35c231ccf4b469b5b1c1ff60c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540018"
---
# <a name="jet_threadstatscpagedirtied-property"></a><span data-ttu-id="7a72c-103">Свойство JET_THREADSTATS. Кпажедиртиед</span><span class="sxs-lookup"><span data-stu-id="7a72c-103">JET_THREADSTATS.cPageDirtied property</span></span>

<span data-ttu-id="7a72c-104">Возвращает общее число страниц базы данных без незаписанных изменений, которые были изменены ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="7a72c-104">Gets the total number of database pages, with no unwritten changes, that have been modified by the database engine on the current thread.</span></span>

<span data-ttu-id="7a72c-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7a72c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="7a72c-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7a72c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7a72c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a72c-107">Syntax</span></span>

``` vb
'Declaration
Public Property cPageDirtied As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageDirtied
```

``` csharp
public int cPageDirtied { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="7a72c-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7a72c-108">Property value</span></span>

<span data-ttu-id="7a72c-109">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7a72c-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="7a72c-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a72c-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a72c-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="7a72c-111">Reference</span></span>

[<span data-ttu-id="7a72c-112">Структура JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="7a72c-112">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="7a72c-113">Элементы JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="7a72c-113">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="7a72c-114">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="7a72c-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
