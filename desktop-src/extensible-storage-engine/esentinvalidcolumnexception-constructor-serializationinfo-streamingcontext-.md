---
description: 'Дополнительные сведения о: конструктор Есентинвалидколумнексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентинвалидколумнексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentInvalidColumnException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentInvalidColumnException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidcolumnexception.esentinvalidcolumnexception(v=EXCHG.10)
ms:contentKeyID: 55101741
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidColumnException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f439edeb0dad09f4c7f1bdd9521bb2410ca68be6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999745"
---
# <a name="esentinvalidcolumnexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="995b9-103">Конструктор Есентинвалидколумнексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="995b9-103">EsentInvalidColumnException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="995b9-104">Инициализирует новый экземпляр класса Есентинвалидколумнексцептион.</span><span class="sxs-lookup"><span data-stu-id="995b9-104">Initializes a new instance of the EsentInvalidColumnException class.</span></span> <span data-ttu-id="995b9-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="995b9-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="995b9-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="995b9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="995b9-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="995b9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="995b9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="995b9-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentInvalidColumnException(info, context)
```

``` csharp
protected EsentInvalidColumnException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="995b9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="995b9-109">Parameters</span></span>

  - <span data-ttu-id="995b9-110">сведения</span><span class="sxs-lookup"><span data-stu-id="995b9-110">info</span></span>  
    <span data-ttu-id="995b9-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="995b9-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="995b9-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="995b9-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="995b9-113">контекст</span><span class="sxs-lookup"><span data-stu-id="995b9-113">context</span></span>  
    <span data-ttu-id="995b9-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="995b9-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="995b9-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="995b9-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="995b9-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="995b9-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="995b9-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="995b9-117">Reference</span></span>

[<span data-ttu-id="995b9-118">Класс Есентинвалидколумнексцептион</span><span class="sxs-lookup"><span data-stu-id="995b9-118">EsentInvalidColumnException class</span></span>](./esentinvalidcolumnexception-class.md)

[<span data-ttu-id="995b9-119">Элементы Есентинвалидколумнексцептион</span><span class="sxs-lookup"><span data-stu-id="995b9-119">EsentInvalidColumnException members</span></span>](./esentinvalidcolumnexception-members.md)

[<span data-ttu-id="995b9-120">Перегрузка Есентинвалидколумнексцептион</span><span class="sxs-lookup"><span data-stu-id="995b9-120">EsentInvalidColumnException overload</span></span>](./esentinvalidcolumnexception-constructor2.md)

[<span data-ttu-id="995b9-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="995b9-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
