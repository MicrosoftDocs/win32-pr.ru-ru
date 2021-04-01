---
description: 'Дополнительные сведения о: конструктор Есентусажеексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентусажеексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentUsageException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103026
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46100a5f359616b18e5eae0d7b9d9a04b0c2fc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819137"
---
# <a name="esentusageexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="4a2c6-103">Конструктор Есентусажеексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="4a2c6-103">EsentUsageException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="4a2c6-104">Инициализирует новый экземпляр класса Есентусажеексцептион.</span><span class="sxs-lookup"><span data-stu-id="4a2c6-104">Initializes a new instance of the EsentUsageException class.</span></span> <span data-ttu-id="4a2c6-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="4a2c6-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="4a2c6-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4a2c6-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4a2c6-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4a2c6-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2c6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a2c6-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentUsageException(info, context)
```

``` csharp
protected EsentUsageException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="4a2c6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a2c6-109">Parameters</span></span>

  - <span data-ttu-id="4a2c6-110">сведения</span><span class="sxs-lookup"><span data-stu-id="4a2c6-110">info</span></span>  
    <span data-ttu-id="4a2c6-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="4a2c6-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="4a2c6-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="4a2c6-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a2c6-113">контекст</span><span class="sxs-lookup"><span data-stu-id="4a2c6-113">context</span></span>  
    <span data-ttu-id="4a2c6-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="4a2c6-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="4a2c6-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="4a2c6-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a2c6-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a2c6-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a2c6-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="4a2c6-117">Reference</span></span>

[<span data-ttu-id="4a2c6-118">Класс EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="4a2c6-118">EsentUsageException class</span></span>](./esentusageexception-class.md)

[<span data-ttu-id="4a2c6-119">Элементы Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="4a2c6-119">EsentUsageException members</span></span>](./esentusageexception-members.md)

[<span data-ttu-id="4a2c6-120">Перегрузка Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="4a2c6-120">EsentUsageException overload</span></span>](./esentusageexception-constructor.md)

[<span data-ttu-id="4a2c6-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4a2c6-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
