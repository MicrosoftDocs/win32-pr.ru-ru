---
description: 'Дополнительные сведения о: конструктор Есентдатаексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентдатаексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentDataException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDataException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101275
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43e7578adb10f607ff88062b48d3f2ebb73d34ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263761"
---
# <a name="esentdataexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="3dfa0-103">Конструктор Есентдатаексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="3dfa0-103">EsentDataException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="3dfa0-104">Инициализирует новый экземпляр класса Есентдатаексцептион.</span><span class="sxs-lookup"><span data-stu-id="3dfa0-104">Initializes a new instance of the EsentDataException class.</span></span> <span data-ttu-id="3dfa0-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="3dfa0-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="3dfa0-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3dfa0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3dfa0-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3dfa0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3dfa0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dfa0-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentDataException(info, context)
```

``` csharp
protected EsentDataException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="3dfa0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3dfa0-109">Parameters</span></span>

  - <span data-ttu-id="3dfa0-110">сведения</span><span class="sxs-lookup"><span data-stu-id="3dfa0-110">info</span></span>  
    <span data-ttu-id="3dfa0-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="3dfa0-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="3dfa0-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="3dfa0-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="3dfa0-113">контекст</span><span class="sxs-lookup"><span data-stu-id="3dfa0-113">context</span></span>  
    <span data-ttu-id="3dfa0-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="3dfa0-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="3dfa0-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="3dfa0-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="3dfa0-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dfa0-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3dfa0-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="3dfa0-117">Reference</span></span>

[<span data-ttu-id="3dfa0-118">Класс Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="3dfa0-118">EsentDataException class</span></span>](./esentdataexception-class.md)

[<span data-ttu-id="3dfa0-119">Элементы Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="3dfa0-119">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="3dfa0-120">Перегрузка Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="3dfa0-120">EsentDataException overload</span></span>](./esentdataexception-constructor.md)

[<span data-ttu-id="3dfa0-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3dfa0-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
