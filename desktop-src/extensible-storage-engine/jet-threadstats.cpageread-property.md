---
description: 'Дополнительные сведения о свойстве: JET_THREADSTATS. Кпажереад'
title: Свойство JET_THREADSTATS. Кпажереад (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cPageRead property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRead
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cpageread(v=EXCHG.10)
ms:contentKeyID: 39516296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRead
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cPageRead
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cPageRead
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cPageRead
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c5a8ed28a4f45abe57ca71eff89ab2ce374bf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712729"
---
# <a name="jet_threadstatscpageread-property"></a><span data-ttu-id="1cf3e-103">Свойство JET_THREADSTATS. Кпажереад</span><span class="sxs-lookup"><span data-stu-id="1cf3e-103">JET_THREADSTATS.cPageRead property</span></span>

<span data-ttu-id="1cf3e-104">Возвращает общее число страниц базы данных, извлекаемых с диска ядром СУБД в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="1cf3e-104">Gets the total number of database pages fetched from disk by the database engine on the current thread.</span></span>

<span data-ttu-id="1cf3e-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1cf3e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="1cf3e-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1cf3e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf3e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1cf3e-107">Syntax</span></span>

``` vb
'Declaration
Public Property cPageRead As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cPageRead
```

``` csharp
public int cPageRead { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="1cf3e-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1cf3e-108">Property value</span></span>

<span data-ttu-id="1cf3e-109">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1cf3e-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1cf3e-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1cf3e-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1cf3e-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="1cf3e-111">Reference</span></span>

[<span data-ttu-id="1cf3e-112">Структура JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="1cf3e-112">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="1cf3e-113">Элементы JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="1cf3e-113">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="1cf3e-114">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="1cf3e-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
