---
description: 'Дополнительные сведения: конструктор экземпляров (String)'
title: Конструктор экземпляров (String)
TOCTitle: Instance constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.instance(v=EXCHG.10)
ms:contentKeyID: 55103263
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
ms.openlocfilehash: 8cf184fc9b8d921b1d8bd1003b960bc65a6ffb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273011"
---
# <a name="instance-constructor-string"></a><span data-ttu-id="ecf69-103">Конструктор экземпляров (String)</span><span class="sxs-lookup"><span data-stu-id="ecf69-103">Instance constructor (String)</span></span>

<span data-ttu-id="ecf69-104">Инициализирует новый экземпляр класса экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ecf69-104">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="ecf69-105">Базовый JET_INSTANCE выделяется, но не инициализируется.</span><span class="sxs-lookup"><span data-stu-id="ecf69-105">The underlying JET_INSTANCE is allocated, but not initialized.</span></span>

<span data-ttu-id="ecf69-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ecf69-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ecf69-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ecf69-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf69-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecf69-108">Syntax</span></span>

``` vb
'Declaration
Public Sub New ( _
    name As String _
)
'Usage
Dim name As String

Dim instance As New Instance(name)
```

``` csharp
public Instance(
    string name
)
```

#### <a name="parameters"></a><span data-ttu-id="ecf69-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecf69-109">Parameters</span></span>

  - <span data-ttu-id="ecf69-110">name</span><span class="sxs-lookup"><span data-stu-id="ecf69-110">name</span></span>  
    <span data-ttu-id="ecf69-111">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ecf69-111">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ecf69-112">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ecf69-112">The name of the instance.</span></span> <span data-ttu-id="ecf69-113">Эта строка должна быть уникальной в пределах данного процесса, в котором размещается ядро СУБД.</span><span class="sxs-lookup"><span data-stu-id="ecf69-113">This string must be unique within a given process hosting the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="ecf69-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecf69-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ecf69-115">Справочник</span><span class="sxs-lookup"><span data-stu-id="ecf69-115">Reference</span></span>

[<span data-ttu-id="ecf69-116">Класс экземпляра</span><span class="sxs-lookup"><span data-stu-id="ecf69-116">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="ecf69-117">Члены экземпляра</span><span class="sxs-lookup"><span data-stu-id="ecf69-117">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="ecf69-118">Перегрузка экземпляра</span><span class="sxs-lookup"><span data-stu-id="ecf69-118">Instance overload</span></span>](./instance-constructor.md)

[<span data-ttu-id="ecf69-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ecf69-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
