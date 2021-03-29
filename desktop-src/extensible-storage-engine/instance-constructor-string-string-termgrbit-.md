---
description: 'Дополнительные сведения: конструктор экземпляров (строка, строка, Термгрбит)'
title: Конструктор экземпляров (строка, строка, Термгрбит)
TOCTitle: Instance constructor (String, String, TermGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String,System.String,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103289
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9cf90f9678db1074594c7772eb67d895a8a5b8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811128"
---
# <a name="instance-constructor-string-string-termgrbit"></a><span data-ttu-id="27d53-103">Конструктор экземпляров (строка, строка, Термгрбит)</span><span class="sxs-lookup"><span data-stu-id="27d53-103">Instance constructor (String, String, TermGrbit)</span></span>

<span data-ttu-id="27d53-104">Инициализирует новый экземпляр класса экземпляра.</span><span class="sxs-lookup"><span data-stu-id="27d53-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="27d53-105">Базовый JET_INSTANCE выделяется, но не инициализируется.</span><span class="sxs-lookup"><span data-stu-id="27d53-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="27d53-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="27d53-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="27d53-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="27d53-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="27d53-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27d53-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String, _
    displayName As String, _
    termGrbit As TermGrbit _
)
'Usage
Dim name As String
Dim displayName As String
Dim termGrbit As TermGrbit

Dim instance As New Instance(name, displayName, _
    termGrbit)
```

``` csharp
public Instance(
    string name,
    string displayName,
    TermGrbit termGrbit
)
```

#### <a name="parameters"></a><span data-ttu-id="27d53-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="27d53-109">Parameters</span></span>

  - <span data-ttu-id="27d53-110">name</span><span class="sxs-lookup"><span data-stu-id="27d53-110">name</span></span>  
    <span data-ttu-id="27d53-111">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="27d53-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="27d53-112">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="27d53-112">The name of the instance.</span></span> <span data-ttu-id="27d53-113">Эта строка должна быть уникальной в пределах данного процесса, в котором размещается ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="27d53-113">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="27d53-114">displayName</span><span class="sxs-lookup"><span data-stu-id="27d53-114">displayName</span></span>  
    <span data-ttu-id="27d53-115">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="27d53-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="27d53-116">Отображаемое имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="27d53-116">A display name for the instance.</span></span> <span data-ttu-id="27d53-117">Он будет использоваться в записях журнала событий.</span><span class="sxs-lookup"><span data-stu-id="27d53-117">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="27d53-118">термгрбит</span><span class="sxs-lookup"><span data-stu-id="27d53-118">termGrbit</span></span>  
    <span data-ttu-id="27d53-119">Тип: [Microsoft. ISAM. ESENT. Interop. термгрбит](./termgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="27d53-119">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="27d53-120">Термгрбит, который будет использоваться во время Жеттерм.</span><span class="sxs-lookup"><span data-stu-id="27d53-120">The TermGrbit to be used at JetTerm time.</span></span>

## <a name="see-also"></a><span data-ttu-id="27d53-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27d53-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="27d53-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="27d53-122">Reference</span></span>

[<span data-ttu-id="27d53-123">Класс экземпляра</span><span class="sxs-lookup"><span data-stu-id="27d53-123">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="27d53-124">Члены экземпляра</span><span class="sxs-lookup"><span data-stu-id="27d53-124">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="27d53-125">Перегрузка экземпляра</span><span class="sxs-lookup"><span data-stu-id="27d53-125">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="27d53-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="27d53-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
