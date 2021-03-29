---
description: 'Дополнительные сведения о: конструктор Есенткорруптионексцептион (String, JET_err)'
title: Конструктор Есенткорруптионексцептион (String, JET_err)
TOCTitle: EsentCorruptionException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101380
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30ed98ea56fe791ed949edc82b548990371c9671
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540114"
---
# <a name="esentcorruptionexception-constructor-string-jet_err"></a><span data-ttu-id="25267-103">Конструктор Есенткорруптионексцептион (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="25267-103">EsentCorruptionException constructor (String, JET_err)</span></span>

<span data-ttu-id="25267-104">Инициализирует новый экземпляр класса Есенткорруптионексцептион.</span><span class="sxs-lookup"><span data-stu-id="25267-104">Initializes a new instance of the EsentCorruptionException class.</span></span>

<span data-ttu-id="25267-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25267-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25267-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25267-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25267-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25267-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentCorruptionException(description, _
    err)
```

``` csharp
protected EsentCorruptionException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="25267-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="25267-108">Parameters</span></span>

  - <span data-ttu-id="25267-109">description;</span><span class="sxs-lookup"><span data-stu-id="25267-109">description</span></span>  
    <span data-ttu-id="25267-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="25267-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="25267-111">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="25267-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="25267-112">Err</span><span class="sxs-lookup"><span data-stu-id="25267-112">err</span></span>  
    <span data-ttu-id="25267-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="25267-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="25267-114">Код ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="25267-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="25267-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25267-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25267-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="25267-116">Reference</span></span>

[<span data-ttu-id="25267-117">Класс EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="25267-117">EsentCorruptionException class</span></span>](./esentcorruptionexception-class.md)

[<span data-ttu-id="25267-118">Элементы Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="25267-118">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="25267-119">Перегрузка Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="25267-119">EsentCorruptionException overload</span></span>](./esentcorruptionexception-constructor.md)

[<span data-ttu-id="25267-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="25267-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
