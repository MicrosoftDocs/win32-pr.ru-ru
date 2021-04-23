---
description: 'Дополнительные сведения о: конструктор Есентинконсистентексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентинконсистентексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentInconsistentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentInconsistentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101709
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f907288bd4f88cae0b022a74cf558a65415d214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674453"
---
# <a name="esentinconsistentexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="b8f75-103">Конструктор Есентинконсистентексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="b8f75-103">EsentInconsistentException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="b8f75-104">Инициализирует новый экземпляр класса Есентинконсистентексцептион.</span><span class="sxs-lookup"><span data-stu-id="b8f75-104">Initializes a new instance of the EsentInconsistentException class.</span></span> <span data-ttu-id="b8f75-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="b8f75-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="b8f75-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8f75-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8f75-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8f75-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8f75-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8f75-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentInconsistentException(info, context)
```

``` csharp
protected EsentInconsistentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="b8f75-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8f75-109">Parameters</span></span>

  - <span data-ttu-id="b8f75-110">сведения</span><span class="sxs-lookup"><span data-stu-id="b8f75-110">info</span></span>  
    <span data-ttu-id="b8f75-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="b8f75-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="b8f75-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="b8f75-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8f75-113">контекст</span><span class="sxs-lookup"><span data-stu-id="b8f75-113">context</span></span>  
    <span data-ttu-id="b8f75-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="b8f75-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="b8f75-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="b8f75-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8f75-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8f75-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8f75-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="b8f75-117">Reference</span></span>

[<span data-ttu-id="b8f75-118">Класс EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="b8f75-118">EsentInconsistentException class</span></span>](./esentinconsistentexception-class.md)

[<span data-ttu-id="b8f75-119">Элементы Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="b8f75-119">EsentInconsistentException members</span></span>](./esentinconsistentexception-members.md)

[<span data-ttu-id="b8f75-120">Перегрузка Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="b8f75-120">EsentInconsistentException overload</span></span>](./esentinconsistentexception-constructor.md)

[<span data-ttu-id="b8f75-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b8f75-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
