---
description: 'Дополнительные сведения о: Колумнстреам Class'
title: Класс Колумнстреам
TOCTitle: ColumnStream class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100939
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eea249347acd18ec71f03fcdc82b8a2baa1da9ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265173"
---
# <a name="columnstream-class"></a><span data-ttu-id="a43a9-103">Класс Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="a43a9-103">ColumnStream class</span></span>

<span data-ttu-id="a43a9-104">Этот класс предоставляет потоковый интерфейс для столбца с длинным значением (т. е. столбца типа [лонгбинари](./jet-coltyp-enumeration.md) или [LongText](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="a43a9-104">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a43a9-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="a43a9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a43a9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a43a9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a43a9-107">System.MarshalByRefObject</span><span class="sxs-lookup"><span data-stu-id="a43a9-107">System.MarshalByRefObject</span></span>](/dotnet/api/system.marshalbyrefobject)  
    [<span data-ttu-id="a43a9-108">System. IO. Stream</span><span class="sxs-lookup"><span data-stu-id="a43a9-108">System.IO.Stream</span></span>](/dotnet/api/system.io.stream)  
      <span data-ttu-id="a43a9-109">Microsoft. ISAM. ESENT. Interop. Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="a43a9-109">Microsoft.Isam.Esent.Interop.ColumnStream</span></span>  

<span data-ttu-id="a43a9-110">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a43a9-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a43a9-111">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a43a9-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a43a9-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a43a9-112">Syntax</span></span>

``` vb
'Declaration
Public Class ColumnStream _
    Inherits Stream
'Usage
Dim instance As ColumnStream
```

``` csharp
public class ColumnStream : Stream
```

## <a name="thread-safety"></a><span data-ttu-id="a43a9-113">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="a43a9-113">Thread safety</span></span>

<span data-ttu-id="a43a9-114">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="a43a9-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a43a9-115">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="a43a9-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a43a9-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a43a9-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a43a9-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="a43a9-117">Reference</span></span>

[<span data-ttu-id="a43a9-118">Элементы Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="a43a9-118">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="a43a9-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a43a9-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
