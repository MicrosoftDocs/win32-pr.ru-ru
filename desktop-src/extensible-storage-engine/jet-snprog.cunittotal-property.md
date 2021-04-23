---
description: 'Дополнительные сведения о свойстве: JET_SNPROG. Куниттотал'
title: Свойство JET_SNPROG. Куниттотал
TOCTitle: 'cunitTotal property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snprog.cunittotal(v=EXCHG.10)
ms:contentKeyID: 55103955
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNPROG.set_cunitTotal
- Microsoft.Isam.Esent.Interop.JET_SNPROG.cunitTotal
- Microsoft.Isam.Esent.Interop.JET_SNPROG.get_cunitTotal
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 983e07dd56dd75b374a6e869f5614662ad92d5a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662160"
---
# <a name="jet_snprogcunittotal-property"></a><span data-ttu-id="df1f5-103">Свойство JET_SNPROG. Куниттотал</span><span class="sxs-lookup"><span data-stu-id="df1f5-103">JET_SNPROG.cunitTotal property</span></span>

<span data-ttu-id="df1f5-104">Возвращает число единиц работы, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="df1f5-104">Gets the number of work units that need to be completed.</span></span> <span data-ttu-id="df1f5-105">Это значение всегда будет больше или равно Кунитдоне.</span><span class="sxs-lookup"><span data-stu-id="df1f5-105">This value will always be bigger than or equal to cunitDone.</span></span>

<span data-ttu-id="df1f5-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="df1f5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="df1f5-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="df1f5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="df1f5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df1f5-108">Syntax</span></span>

``` vb
'Declaration
Public Property cunitTotal As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_SNPROG
Dim value As Integer

value = instance.cunitTotal
```

``` csharp
public int cunitTotal { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="df1f5-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="df1f5-109">Property value</span></span>

<span data-ttu-id="df1f5-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="df1f5-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="df1f5-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df1f5-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="df1f5-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="df1f5-112">Reference</span></span>

[<span data-ttu-id="df1f5-113">Класс JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="df1f5-113">JET_SNPROG class</span></span>](./jet-snprog-class.md)

[<span data-ttu-id="df1f5-114">Элементы JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="df1f5-114">JET_SNPROG members</span></span>](./jet-snprog-members.md)

[<span data-ttu-id="df1f5-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="df1f5-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
