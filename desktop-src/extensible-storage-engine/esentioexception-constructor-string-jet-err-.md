---
description: 'Дополнительные сведения о: конструктор Есентиоексцептион (String, JET_err)'
title: Конструктор Есентиоексцептион (String, JET_err)
TOCTitle: EsentIOException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentIOException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102030
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087f22d7836ff41ac97b65c15be1b51dfac84a8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693116"
---
# <a name="esentioexception-constructor-string-jet_err"></a><span data-ttu-id="bc803-103">Конструктор Есентиоексцептион (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="bc803-103">EsentIOException constructor (String, JET_err)</span></span>

<span data-ttu-id="bc803-104">Инициализирует новый экземпляр класса Есентиоексцептион.</span><span class="sxs-lookup"><span data-stu-id="bc803-104">Initializes a new instance of the EsentIOException class.</span></span>

<span data-ttu-id="bc803-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bc803-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bc803-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bc803-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bc803-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc803-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentIOException(description, _
    err)
```

``` csharp
protected EsentIOException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="bc803-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc803-108">Parameters</span></span>

  - <span data-ttu-id="bc803-109">description;</span><span class="sxs-lookup"><span data-stu-id="bc803-109">description</span></span>  
    <span data-ttu-id="bc803-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="bc803-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="bc803-111">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="bc803-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="bc803-112">Err</span><span class="sxs-lookup"><span data-stu-id="bc803-112">err</span></span>  
    <span data-ttu-id="bc803-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bc803-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="bc803-114">Код ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="bc803-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc803-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc803-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bc803-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="bc803-116">Reference</span></span>

[<span data-ttu-id="bc803-117">Класс EsentIOException</span><span class="sxs-lookup"><span data-stu-id="bc803-117">EsentIOException class</span></span>](./esentioexception-class.md)

[<span data-ttu-id="bc803-118">Элементы Есентиоексцептион</span><span class="sxs-lookup"><span data-stu-id="bc803-118">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="bc803-119">Перегрузка Есентиоексцептион</span><span class="sxs-lookup"><span data-stu-id="bc803-119">EsentIOException overload</span></span>](./esentioexception-constructor.md)

[<span data-ttu-id="bc803-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bc803-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
