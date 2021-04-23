---
description: 'Дополнительные сведения о: JET_ENUMCOLUMNVALUE классе'
title: Класс JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103622
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2066e6b4b3039ba150f17630afaef967c215823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719290"
---
# <a name="jet_enumcolumnvalue-class"></a><span data-ttu-id="3399c-103">Класс JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="3399c-103">JET_ENUMCOLUMNVALUE class</span></span>

<span data-ttu-id="3399c-104">Перечисляет значения столбца записи с помощью функции Жетенумератеколумнс.</span><span class="sxs-lookup"><span data-stu-id="3399c-104">Enumerates the column values of a record using the JetEnumerateColumns function.</span></span> <span data-ttu-id="3399c-105">[Жетенумератеколумнс (JET_SESID, JET_TABLEID, Int32, \[ \] , int32, \[ \] , JET_PFNREALLOC, IntPtr, Int32, енумератеколумнсгрбит)](./api.jetenumeratecolumns-method.md) возвращает массив структур JET_ENUMCOLUMNVALUE.</span><span class="sxs-lookup"><span data-stu-id="3399c-105">[JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, \[\], Int32, \[\], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)](./api.jetenumeratecolumns-method.md) returns an array of JET_ENUMCOLUMNVALUE structures.</span></span> <span data-ttu-id="3399c-106">Массив возвращается в память, которая была выделена с помощью обратного вызова, предоставленного для этой функции.</span><span class="sxs-lookup"><span data-stu-id="3399c-106">The array is returned in memory that was allocated using the callback that was supplied to that function.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3399c-107">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="3399c-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="3399c-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="3399c-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="3399c-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="3399c-109">Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNVALUE</span></span>  

<span data-ttu-id="3399c-110">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3399c-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3399c-111">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3399c-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3399c-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3399c-112">Syntax</span></span>

``` vb
'Declaration
Public Class JET_ENUMCOLUMNVALUE
'Usage
Dim instance As JET_ENUMCOLUMNVALUE
```

``` csharp
public class JET_ENUMCOLUMNVALUE
```

## <a name="thread-safety"></a><span data-ttu-id="3399c-113">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="3399c-113">Thread safety</span></span>

<span data-ttu-id="3399c-114">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="3399c-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3399c-115">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="3399c-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3399c-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3399c-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3399c-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="3399c-117">Reference</span></span>

[<span data-ttu-id="3399c-118">Элементы JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="3399c-118">JET_ENUMCOLUMNVALUE members</span></span>](./jet-enumcolumnvalue-members.md)

[<span data-ttu-id="3399c-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3399c-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
