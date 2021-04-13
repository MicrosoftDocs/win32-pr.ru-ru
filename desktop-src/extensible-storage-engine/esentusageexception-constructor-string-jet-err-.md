---
description: 'Дополнительные сведения о: конструктор Есентусажеексцептион (String, JET_err)'
title: Конструктор Есентусажеексцептион (String, JET_err)
TOCTitle: EsentUsageException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103223
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f9d38ebc5be25eb8f036583404d340a8882de6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350462"
---
# <a name="esentusageexception-constructor-string-jet_err"></a><span data-ttu-id="851c1-103">Конструктор Есентусажеексцептион (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="851c1-103">EsentUsageException constructor (String, JET_err)</span></span>

<span data-ttu-id="851c1-104">Инициализирует новый экземпляр класса Есентусажеексцептион.</span><span class="sxs-lookup"><span data-stu-id="851c1-104">Initializes a new instance of the EsentUsageException class.</span></span>

<span data-ttu-id="851c1-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="851c1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="851c1-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="851c1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="851c1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="851c1-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentUsageException(description, _
    err)
```

``` csharp
protected EsentUsageException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="851c1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="851c1-108">Parameters</span></span>

  - <span data-ttu-id="851c1-109">description;</span><span class="sxs-lookup"><span data-stu-id="851c1-109">description</span></span>  
    <span data-ttu-id="851c1-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="851c1-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="851c1-111">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="851c1-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="851c1-112">Err</span><span class="sxs-lookup"><span data-stu-id="851c1-112">err</span></span>  
    <span data-ttu-id="851c1-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="851c1-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="851c1-114">Код ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="851c1-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="851c1-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="851c1-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="851c1-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="851c1-116">Reference</span></span>

[<span data-ttu-id="851c1-117">Класс EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="851c1-117">EsentUsageException class</span></span>](./esentusageexception-class.md)

[<span data-ttu-id="851c1-118">Элементы Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="851c1-118">EsentUsageException members</span></span>](./esentusageexception-members.md)

[<span data-ttu-id="851c1-119">Перегрузка Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="851c1-119">EsentUsageException overload</span></span>](./esentusageexception-constructor.md)

[<span data-ttu-id="851c1-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="851c1-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
