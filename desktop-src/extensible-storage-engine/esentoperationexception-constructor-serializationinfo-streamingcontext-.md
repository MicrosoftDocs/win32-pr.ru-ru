---
description: 'Дополнительные сведения о: конструктор Есентоператионексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентоператионексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentOperationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentOperationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102312
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ee281a47ae8e24ff51ffe5c3d6a4ef4f4b1873e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264147"
---
# <a name="esentoperationexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="c2afb-103">Конструктор Есентоператионексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="c2afb-103">EsentOperationException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="c2afb-104">Инициализирует новый экземпляр класса Есентоператионексцептион.</span><span class="sxs-lookup"><span data-stu-id="c2afb-104">Initializes a new instance of the EsentOperationException class.</span></span> <span data-ttu-id="c2afb-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="c2afb-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="c2afb-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c2afb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c2afb-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c2afb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c2afb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2afb-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentOperationException(info, context)
```

``` csharp
protected EsentOperationException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="c2afb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2afb-109">Parameters</span></span>

  - <span data-ttu-id="c2afb-110">сведения</span><span class="sxs-lookup"><span data-stu-id="c2afb-110">info</span></span>  
    <span data-ttu-id="c2afb-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="c2afb-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="c2afb-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="c2afb-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="c2afb-113">контекст</span><span class="sxs-lookup"><span data-stu-id="c2afb-113">context</span></span>  
    <span data-ttu-id="c2afb-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="c2afb-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="c2afb-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="c2afb-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2afb-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2afb-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c2afb-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="c2afb-117">Reference</span></span>

[<span data-ttu-id="c2afb-118">Класс EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c2afb-118">EsentOperationException class</span></span>](./esentoperationexception-class.md)

[<span data-ttu-id="c2afb-119">Элементы Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="c2afb-119">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="c2afb-120">Перегрузка Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="c2afb-120">EsentOperationException overload</span></span>](./esentoperationexception-constructor.md)

[<span data-ttu-id="c2afb-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c2afb-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
