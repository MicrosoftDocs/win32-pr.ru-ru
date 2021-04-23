---
description: 'Дополнительные сведения о: конструктор Есентмеморексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентмеморексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentMemoryException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102121
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7bf198808de480964b02801c809ab3cff50d35fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692943"
---
# <a name="esentmemoryexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="4ab38-103">Конструктор Есентмеморексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="4ab38-103">EsentMemoryException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="4ab38-104">Инициализирует новый экземпляр класса Есентмеморексцептион.</span><span class="sxs-lookup"><span data-stu-id="4ab38-104">Initializes a new instance of the EsentMemoryException class.</span></span> <span data-ttu-id="4ab38-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="4ab38-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="4ab38-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ab38-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ab38-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ab38-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ab38-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ab38-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentMemoryException(info, context)
```

``` csharp
protected EsentMemoryException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="4ab38-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ab38-109">Parameters</span></span>

  - <span data-ttu-id="4ab38-110">сведения</span><span class="sxs-lookup"><span data-stu-id="4ab38-110">info</span></span>  
    <span data-ttu-id="4ab38-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="4ab38-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="4ab38-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="4ab38-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ab38-113">контекст</span><span class="sxs-lookup"><span data-stu-id="4ab38-113">context</span></span>  
    <span data-ttu-id="4ab38-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="4ab38-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="4ab38-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="4ab38-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ab38-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ab38-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ab38-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="4ab38-117">Reference</span></span>

[<span data-ttu-id="4ab38-118">Класс EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="4ab38-118">EsentMemoryException class</span></span>](./esentmemoryexception-class.md)

[<span data-ttu-id="4ab38-119">Элементы Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="4ab38-119">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="4ab38-120">Перегрузка Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="4ab38-120">EsentMemoryException overload</span></span>](./esentmemoryexception-constructor.md)

[<span data-ttu-id="4ab38-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4ab38-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
