---
description: 'Дополнительные сведения о: конструктор Есентобсолетиксцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентобсолетиксцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentObsoleteException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102167
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b287a61396f0d908c888b84553e5dc67df907be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711815"
---
# <a name="esentobsoleteexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="882ac-103">Конструктор Есентобсолетиксцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="882ac-103">EsentObsoleteException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="882ac-104">Инициализирует новый экземпляр класса Есентобсолетиксцептион.</span><span class="sxs-lookup"><span data-stu-id="882ac-104">Initializes a new instance of the EsentObsoleteException class.</span></span> <span data-ttu-id="882ac-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="882ac-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="882ac-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="882ac-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="882ac-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="882ac-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="882ac-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="882ac-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentObsoleteException(info, context)
```

``` csharp
protected EsentObsoleteException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="882ac-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="882ac-109">Parameters</span></span>

  - <span data-ttu-id="882ac-110">сведения</span><span class="sxs-lookup"><span data-stu-id="882ac-110">info</span></span>  
    <span data-ttu-id="882ac-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="882ac-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="882ac-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="882ac-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="882ac-113">контекст</span><span class="sxs-lookup"><span data-stu-id="882ac-113">context</span></span>  
    <span data-ttu-id="882ac-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="882ac-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="882ac-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="882ac-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="882ac-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="882ac-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="882ac-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="882ac-117">Reference</span></span>

[<span data-ttu-id="882ac-118">Класс EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="882ac-118">EsentObsoleteException class</span></span>](./esentobsoleteexception-class.md)

[<span data-ttu-id="882ac-119">Элементы Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="882ac-119">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="882ac-120">Перегрузка Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="882ac-120">EsentObsoleteException overload</span></span>](./esentobsoleteexception-constructor.md)

[<span data-ttu-id="882ac-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="882ac-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
