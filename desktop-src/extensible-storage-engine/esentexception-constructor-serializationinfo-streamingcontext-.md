---
description: 'Дополнительные сведения о: конструктор Есентексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентексцептион (SerializationInfo, StreamingContext) (Microsoft. ISAM. ESENT)
TOCTitle: EsentException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100719
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bdcfe5c3b37746f50926850b45763f9d70de893
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703380"
---
# <a name="esentexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="21b92-103">Конструктор Есентексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="21b92-103">EsentException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="21b92-104">Инициализирует новый экземпляр класса Есентексцептион.</span><span class="sxs-lookup"><span data-stu-id="21b92-104">Initializes a new instance of the EsentException class.</span></span> <span data-ttu-id="21b92-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="21b92-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="21b92-106">**Пространство имен:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="21b92-106">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="21b92-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="21b92-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="21b92-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="21b92-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentException(info, context)
```

``` csharp
protected EsentException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="21b92-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="21b92-109">Parameters</span></span>

  - <span data-ttu-id="21b92-110">сведения</span><span class="sxs-lookup"><span data-stu-id="21b92-110">info</span></span>  
    <span data-ttu-id="21b92-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="21b92-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="21b92-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="21b92-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="21b92-113">контекст</span><span class="sxs-lookup"><span data-stu-id="21b92-113">context</span></span>  
    <span data-ttu-id="21b92-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="21b92-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="21b92-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="21b92-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="21b92-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="21b92-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21b92-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="21b92-117">Reference</span></span>

[<span data-ttu-id="21b92-118">Класс Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="21b92-118">EsentException class</span></span>](./esentexception-class.md)

[<span data-ttu-id="21b92-119">Элементы Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="21b92-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="21b92-120">Перегрузка Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="21b92-120">EsentException overload</span></span>](./esentexception-constructor.md)

[<span data-ttu-id="21b92-121">Пространство имен Microsoft. ISAM. ESENT</span><span class="sxs-lookup"><span data-stu-id="21b92-121">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
