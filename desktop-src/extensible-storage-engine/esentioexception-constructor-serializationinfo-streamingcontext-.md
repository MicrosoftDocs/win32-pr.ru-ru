---
description: 'Дополнительные сведения о: конструктор Есентиоексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентиоексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentIOException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentIOException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102032
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29d6b0666f4a1b38441c4f9878575b9867ae10c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703370"
---
# <a name="esentioexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="7f62f-103">Конструктор Есентиоексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="7f62f-103">EsentIOException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="7f62f-104">Инициализирует новый экземпляр класса Есентиоексцептион.</span><span class="sxs-lookup"><span data-stu-id="7f62f-104">Initializes a new instance of the EsentIOException class.</span></span> <span data-ttu-id="7f62f-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="7f62f-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="7f62f-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7f62f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7f62f-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7f62f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7f62f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f62f-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentIOException(info, context)
```

``` csharp
protected EsentIOException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="7f62f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f62f-109">Parameters</span></span>

  - <span data-ttu-id="7f62f-110">сведения</span><span class="sxs-lookup"><span data-stu-id="7f62f-110">info</span></span>  
    <span data-ttu-id="7f62f-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="7f62f-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="7f62f-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="7f62f-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="7f62f-113">контекст</span><span class="sxs-lookup"><span data-stu-id="7f62f-113">context</span></span>  
    <span data-ttu-id="7f62f-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="7f62f-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="7f62f-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="7f62f-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f62f-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f62f-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7f62f-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="7f62f-117">Reference</span></span>

[<span data-ttu-id="7f62f-118">Класс EsentIOException</span><span class="sxs-lookup"><span data-stu-id="7f62f-118">EsentIOException class</span></span>](./esentioexception-class.md)

[<span data-ttu-id="7f62f-119">Элементы Есентиоексцептион</span><span class="sxs-lookup"><span data-stu-id="7f62f-119">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="7f62f-120">Перегрузка Есентиоексцептион</span><span class="sxs-lookup"><span data-stu-id="7f62f-120">EsentIOException overload</span></span>](./esentioexception-constructor.md)

[<span data-ttu-id="7f62f-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7f62f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
