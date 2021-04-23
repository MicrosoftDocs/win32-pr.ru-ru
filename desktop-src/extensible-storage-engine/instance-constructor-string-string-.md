---
description: 'Дополнительные сведения: конструктор экземпляров (строка, строка)'
title: Конструктор экземпляров (строка, строка)
TOCTitle: Instance constructor (String, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103267
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02cb629cdfaba17ce9a137b52eb1a6d6fdbaa56b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344232"
---
# <a name="instance-constructor-string-string"></a><span data-ttu-id="99d07-103">Конструктор экземпляров (строка, строка)</span><span class="sxs-lookup"><span data-stu-id="99d07-103">Instance constructor (String, String)</span></span>

<span data-ttu-id="99d07-104">Инициализирует новый экземпляр класса экземпляра.</span><span class="sxs-lookup"><span data-stu-id="99d07-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="99d07-105">Базовый JET_INSTANCE выделяется, но не инициализируется.</span><span class="sxs-lookup"><span data-stu-id="99d07-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="99d07-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="99d07-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="99d07-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="99d07-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="99d07-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99d07-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String _
)
'Usage
Dim name As String
Dim displayName As String

Dim instance As New Instance(name, displayName)
```

``` csharp
public Instance(
    string name,
    string displayName
)
```

#### <a name="parameters"></a><span data-ttu-id="99d07-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="99d07-109">Parameters</span></span>

  - <span data-ttu-id="99d07-110">name</span><span class="sxs-lookup"><span data-stu-id="99d07-110">name</span></span>  
    <span data-ttu-id="99d07-111">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="99d07-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="99d07-112">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="99d07-112">The name of the instance.</span></span> <span data-ttu-id="99d07-113">Эта строка должна быть уникальной в пределах данного процесса, в котором размещается ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="99d07-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="99d07-114">displayName</span><span class="sxs-lookup"><span data-stu-id="99d07-114">displayName</span></span>  
    <span data-ttu-id="99d07-115">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="99d07-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="99d07-116">Отображаемое имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="99d07-116">A display name for the instance.</span></span> <span data-ttu-id="99d07-117">Он будет использоваться в записях журнала событий.</span><span class="sxs-lookup"><span data-stu-id="99d07-117">This will be used in eventlog entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="99d07-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99d07-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="99d07-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="99d07-119">Reference</span></span>

[<span data-ttu-id="99d07-120">Класс экземпляра</span><span class="sxs-lookup"><span data-stu-id="99d07-120">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="99d07-121">Члены экземпляра</span><span class="sxs-lookup"><span data-stu-id="99d07-121">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="99d07-122">Перегрузка экземпляра</span><span class="sxs-lookup"><span data-stu-id="99d07-122">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="99d07-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="99d07-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
