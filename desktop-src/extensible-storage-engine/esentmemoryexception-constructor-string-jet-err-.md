---
description: 'Дополнительные сведения о: конструктор Есентмеморексцептион (String, JET_err)'
title: Конструктор Есентмеморексцептион (String, JET_err)
TOCTitle: EsentMemoryException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102199
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60cdb6fda03695a4afb41d82e83aaeeb9415f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692942"
---
# <a name="esentmemoryexception-constructor-string-jet_err"></a><span data-ttu-id="6a0f4-103">Конструктор Есентмеморексцептион (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="6a0f4-103">EsentMemoryException constructor (String, JET_err)</span></span>

<span data-ttu-id="6a0f4-104">Инициализирует новый экземпляр класса Есентмеморексцептион.</span><span class="sxs-lookup"><span data-stu-id="6a0f4-104">Initializes a new instance of the EsentMemoryException class.</span></span>

<span data-ttu-id="6a0f4-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a0f4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a0f4-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a0f4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a0f4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a0f4-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentMemoryException(description, _
    err)
```

``` csharp
protected EsentMemoryException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="6a0f4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a0f4-108">Parameters</span></span>

  - <span data-ttu-id="6a0f4-109">description;</span><span class="sxs-lookup"><span data-stu-id="6a0f4-109">description</span></span>  
    <span data-ttu-id="6a0f4-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6a0f4-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6a0f4-111">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="6a0f4-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="6a0f4-112">Err</span><span class="sxs-lookup"><span data-stu-id="6a0f4-112">err</span></span>  
    <span data-ttu-id="6a0f4-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6a0f4-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="6a0f4-114">Код ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="6a0f4-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a0f4-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a0f4-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a0f4-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="6a0f4-116">Reference</span></span>

[<span data-ttu-id="6a0f4-117">Класс EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="6a0f4-117">EsentMemoryException class</span></span>](./esentmemoryexception-class.md)

[<span data-ttu-id="6a0f4-118">Элементы Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="6a0f4-118">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="6a0f4-119">Перегрузка Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="6a0f4-119">EsentMemoryException overload</span></span>](./esentmemoryexception-constructor.md)

[<span data-ttu-id="6a0f4-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6a0f4-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
