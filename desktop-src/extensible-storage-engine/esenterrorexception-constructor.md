---
description: 'Дополнительные сведения о: конструктор Есентеррорексцептион'
title: Конструктор Есентеррорексцептион
TOCTitle: 'EsentErrorException constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0728eb316c7d5a5d3cf4a1ad13c2e35451318225
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347022"
---
# <a name="esenterrorexception-constructor"></a><span data-ttu-id="b6c74-103">Конструктор Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="b6c74-103">EsentErrorException constructor</span></span>

<span data-ttu-id="b6c74-104">Инициализирует новый экземпляр класса Есентеррорексцептион.</span><span class="sxs-lookup"><span data-stu-id="b6c74-104">Initializes a new instance of the EsentErrorException class.</span></span> <span data-ttu-id="b6c74-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="b6c74-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="b6c74-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b6c74-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b6c74-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b6c74-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c74-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6c74-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentErrorException(info, context)
```

``` csharp
protected EsentErrorException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="b6c74-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b6c74-109">Parameters</span></span>

  - <span data-ttu-id="b6c74-110">сведения</span><span class="sxs-lookup"><span data-stu-id="b6c74-110">info</span></span>  
    <span data-ttu-id="b6c74-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="b6c74-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="b6c74-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="b6c74-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6c74-113">контекст</span><span class="sxs-lookup"><span data-stu-id="b6c74-113">context</span></span>  
    <span data-ttu-id="b6c74-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="b6c74-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="b6c74-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="b6c74-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6c74-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6c74-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b6c74-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="b6c74-117">Reference</span></span>

[<span data-ttu-id="b6c74-118">Класс EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b6c74-118">EsentErrorException class</span></span>](./esenterrorexception-class.md)

[<span data-ttu-id="b6c74-119">Элементы Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="b6c74-119">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="b6c74-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b6c74-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
