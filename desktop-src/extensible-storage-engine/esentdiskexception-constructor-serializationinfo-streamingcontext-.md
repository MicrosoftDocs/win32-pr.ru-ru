---
description: 'Дополнительные сведения о: конструктор Есентдискексцептион (SerializationInfo, StreamingContext)'
title: Конструктор Есентдискексцептион (SerializationInfo, StreamingContext)
TOCTitle: EsentDiskException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDiskException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4abe19b16d9e6eb6d94d5b4fe1dd067b68c2c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349535"
---
# <a name="esentdiskexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="741ae-103">Конструктор Есентдискексцептион (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="741ae-103">EsentDiskException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="741ae-104">Инициализирует новый экземпляр класса Есентдискексцептион.</span><span class="sxs-lookup"><span data-stu-id="741ae-104">Initializes a new instance of the EsentDiskException class.</span></span> <span data-ttu-id="741ae-105">Этот конструктор используется для десериализации сериализованного исключения.</span><span class="sxs-lookup"><span data-stu-id="741ae-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="741ae-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="741ae-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="741ae-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="741ae-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="741ae-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="741ae-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentDiskException(info, context)
```

``` csharp
protected EsentDiskException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="741ae-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="741ae-109">Parameters</span></span>

  - <span data-ttu-id="741ae-110">сведения</span><span class="sxs-lookup"><span data-stu-id="741ae-110">info</span></span>  
    <span data-ttu-id="741ae-111">Тип: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="741ae-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="741ae-112">Данные, необходимые для десериализации объекта.</span><span class="sxs-lookup"><span data-stu-id="741ae-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="741ae-113">контекст</span><span class="sxs-lookup"><span data-stu-id="741ae-113">context</span></span>  
    <span data-ttu-id="741ae-114">Тип: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="741ae-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="741ae-115">Контекст десериализации.</span><span class="sxs-lookup"><span data-stu-id="741ae-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="741ae-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="741ae-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="741ae-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="741ae-117">Reference</span></span>

[<span data-ttu-id="741ae-118">Класс Есентдискексцептион</span><span class="sxs-lookup"><span data-stu-id="741ae-118">EsentDiskException class</span></span>](./esentdiskexception-class.md)

[<span data-ttu-id="741ae-119">Элементы Есентдискексцептион</span><span class="sxs-lookup"><span data-stu-id="741ae-119">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="741ae-120">Перегрузка Есентдискексцептион</span><span class="sxs-lookup"><span data-stu-id="741ae-120">EsentDiskException overload</span></span>](./esentdiskexception-constructor.md)

[<span data-ttu-id="741ae-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="741ae-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
