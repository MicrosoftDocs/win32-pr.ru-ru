---
description: 'Дополнительные сведения о: конструктор Есентфрагментатионексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентфрагментатионексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentFragmentationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101633
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 251e4beaacb1e895c1da1d501b38cf03f211dd99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350522"
---
# <a name="esentfragmentationexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="6b964-103">Конструктор Есентфрагментатионексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="6b964-103">EsentFragmentationException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="6b964-104">Инициализирует новый экземпляр класса Есентфрагментатионексцептион.</span><span class="sxs-lookup"><span data-stu-id="6b964-104">Initializes a new instance of the EsentFragmentationException class.</span></span> <span data-ttu-id="6b964-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="6b964-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="6b964-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6b964-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6b964-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6b964-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6b964-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b964-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentFragmentationException(info, context)
```

``` csharp
protected EsentFragmentationException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="6b964-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b964-109">Parameters</span></span>

  - <span data-ttu-id="6b964-110">сведения</span><span class="sxs-lookup"><span data-stu-id="6b964-110">info</span></span>  
    <span data-ttu-id="6b964-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="6b964-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="6b964-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="6b964-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b964-113">контекст</span><span class="sxs-lookup"><span data-stu-id="6b964-113">context</span></span>  
    <span data-ttu-id="6b964-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="6b964-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="6b964-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="6b964-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b964-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b964-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6b964-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="6b964-117">Reference</span></span>

[<span data-ttu-id="6b964-118">Класс EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="6b964-118">EsentFragmentationException class</span></span>](./esentfragmentationexception-class.md)

[<span data-ttu-id="6b964-119">Элементы Есентфрагментатионексцептион</span><span class="sxs-lookup"><span data-stu-id="6b964-119">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="6b964-120">Перегрузка Есентфрагментатионексцептион</span><span class="sxs-lookup"><span data-stu-id="6b964-120">EsentFragmentationException overload</span></span>](./esentfragmentationexception-constructor.md)

[<span data-ttu-id="6b964-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6b964-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
