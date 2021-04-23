---
description: 'Дополнительные сведения о: конструктор Есенткорруптионексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есенткорруптионексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentCorruptionException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101038
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0e80255d86ed6f953e4010541e98b794537f97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999541"
---
# <a name="esentcorruptionexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="a6c04-103">Конструктор Есенткорруптионексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="a6c04-103">EsentCorruptionException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="a6c04-104">Инициализирует новый экземпляр класса Есенткорруптионексцептион.</span><span class="sxs-lookup"><span data-stu-id="a6c04-104">Initializes a new instance of the EsentCorruptionException class.</span></span> <span data-ttu-id="a6c04-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="a6c04-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="a6c04-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a6c04-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a6c04-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a6c04-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a6c04-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6c04-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentCorruptionException(info, context)
```

``` csharp
protected EsentCorruptionException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="a6c04-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6c04-109">Parameters</span></span>

  - <span data-ttu-id="a6c04-110">сведения</span><span class="sxs-lookup"><span data-stu-id="a6c04-110">info</span></span>  
    <span data-ttu-id="a6c04-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="a6c04-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="a6c04-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="a6c04-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="a6c04-113">контекст</span><span class="sxs-lookup"><span data-stu-id="a6c04-113">context</span></span>  
    <span data-ttu-id="a6c04-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="a6c04-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="a6c04-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="a6c04-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6c04-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6c04-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a6c04-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="a6c04-117">Reference</span></span>

[<span data-ttu-id="a6c04-118">Класс EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="a6c04-118">EsentCorruptionException class</span></span>](./esentcorruptionexception-class.md)

[<span data-ttu-id="a6c04-119">Элементы Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="a6c04-119">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="a6c04-120">Перегрузка Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="a6c04-120">EsentCorruptionException overload</span></span>](./esentcorruptionexception-constructor.md)

[<span data-ttu-id="a6c04-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a6c04-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
