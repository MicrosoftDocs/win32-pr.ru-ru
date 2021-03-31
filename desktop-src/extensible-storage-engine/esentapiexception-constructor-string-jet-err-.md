---
description: 'Дополнительные сведения о: конструктор Есентапиексцептион (String, JET_err)'
title: Конструктор Есентапиексцептион (String, JET_err)
TOCTitle: EsentApiException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101058
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 568cf61a1c5852b70d0e08647a39ab70140d2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808230"
---
# <a name="esentapiexception-constructor-string-jet_err"></a><span data-ttu-id="af459-103">Конструктор Есентапиексцептион (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="af459-103">EsentApiException constructor (String, JET_err)</span></span>

<span data-ttu-id="af459-104">Инициализирует новый экземпляр класса Есентапиексцептион.</span><span class="sxs-lookup"><span data-stu-id="af459-104">Initializes a new instance of the EsentApiException class.</span></span>

<span data-ttu-id="af459-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="af459-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="af459-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="af459-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="af459-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af459-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentApiException(description, _
    err)
```

``` csharp
protected EsentApiException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="af459-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="af459-108">Parameters</span></span>

  - <span data-ttu-id="af459-109">description;</span><span class="sxs-lookup"><span data-stu-id="af459-109">description</span></span>  
    <span data-ttu-id="af459-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="af459-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="af459-111">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="af459-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="af459-112">Err</span><span class="sxs-lookup"><span data-stu-id="af459-112">err</span></span>  
    <span data-ttu-id="af459-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="af459-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="af459-114">Код ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="af459-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="af459-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af459-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af459-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="af459-116">Reference</span></span>

[<span data-ttu-id="af459-117">Класс Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="af459-117">EsentApiException class</span></span>](./esentapiexception-class.md)

[<span data-ttu-id="af459-118">Элементы Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="af459-118">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="af459-119">Перегрузка Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="af459-119">EsentApiException overload</span></span>](./esentapiexception-constructor.md)

[<span data-ttu-id="af459-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="af459-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
