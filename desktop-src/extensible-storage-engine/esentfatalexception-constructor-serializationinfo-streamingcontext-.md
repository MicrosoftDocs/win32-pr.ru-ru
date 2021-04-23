---
description: 'Дополнительные сведения о: конструктор Есентфаталексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентфаталексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentFatalException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFatalException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101554
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2264e3852eb6809f321b9bae162a833e86d7b513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080353"
---
# <a name="esentfatalexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="34706-103">Конструктор Есентфаталексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="34706-103">EsentFatalException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="34706-104">Инициализирует новый экземпляр класса Есентфаталексцептион.</span><span class="sxs-lookup"><span data-stu-id="34706-104">Initializes a new instance of the EsentFatalException class.</span></span> <span data-ttu-id="34706-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="34706-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="34706-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34706-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34706-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34706-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34706-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34706-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentFatalException(info, context)
```

``` csharp
protected EsentFatalException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="34706-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="34706-109">Parameters</span></span>

  - <span data-ttu-id="34706-110">сведения</span><span class="sxs-lookup"><span data-stu-id="34706-110">info</span></span>  
    <span data-ttu-id="34706-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="34706-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="34706-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="34706-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="34706-113">контекст</span><span class="sxs-lookup"><span data-stu-id="34706-113">context</span></span>  
    <span data-ttu-id="34706-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="34706-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="34706-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="34706-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="34706-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="34706-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34706-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="34706-117">Reference</span></span>

[<span data-ttu-id="34706-118">Класс EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="34706-118">EsentFatalException class</span></span>](./esentfatalexception-class.md)

[<span data-ttu-id="34706-119">Элементы Есентфаталексцептион</span><span class="sxs-lookup"><span data-stu-id="34706-119">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="34706-120">Перегрузка Есентфаталексцептион</span><span class="sxs-lookup"><span data-stu-id="34706-120">EsentFatalException overload</span></span>](./esentfatalexception-constructor.md)

[<span data-ttu-id="34706-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="34706-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
