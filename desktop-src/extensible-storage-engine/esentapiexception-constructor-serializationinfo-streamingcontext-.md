---
description: 'Дополнительные сведения о: конструктор Есентапиексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентапиексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentApiException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101059
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a00204c254378956521a1ae5fe02480dd879c832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498159"
---
# <a name="esentapiexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="45f30-103">Конструктор Есентапиексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="45f30-103">EsentApiException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="45f30-104">Инициализирует новый экземпляр класса Есентапиексцептион.</span><span class="sxs-lookup"><span data-stu-id="45f30-104">Initializes a new instance of the EsentApiException class.</span></span> <span data-ttu-id="45f30-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="45f30-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="45f30-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="45f30-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="45f30-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="45f30-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="45f30-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45f30-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentApiException(info, context)
```

``` csharp
protected EsentApiException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="45f30-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="45f30-109">Parameters</span></span>

  - <span data-ttu-id="45f30-110">сведения</span><span class="sxs-lookup"><span data-stu-id="45f30-110">info</span></span>  
    <span data-ttu-id="45f30-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="45f30-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="45f30-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="45f30-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="45f30-113">контекст</span><span class="sxs-lookup"><span data-stu-id="45f30-113">context</span></span>  
    <span data-ttu-id="45f30-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="45f30-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="45f30-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="45f30-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="45f30-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45f30-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="45f30-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="45f30-117">Reference</span></span>

[<span data-ttu-id="45f30-118">Класс Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="45f30-118">EsentApiException class</span></span>](./esentapiexception-class.md)

[<span data-ttu-id="45f30-119">Элементы Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="45f30-119">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="45f30-120">Перегрузка Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="45f30-120">EsentApiException overload</span></span>](./esentapiexception-constructor.md)

[<span data-ttu-id="45f30-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="45f30-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
