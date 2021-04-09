---
description: 'Дополнительные сведения о: конструктор Есентдатаексцептион (String, JET_err)'
title: Конструктор Есентдатаексцептион (String, JET_err)
TOCTitle: EsentDataException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDataException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101571
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e39638d6e5458c0dcc555f31bec12e752d84337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155766"
---
# <a name="esentdataexception-constructor-string-jet_err"></a><span data-ttu-id="b891c-103">Конструктор Есентдатаексцептион (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="b891c-103">EsentDataException constructor (String, JET_err)</span></span>

<span data-ttu-id="b891c-104">Инициализирует новый экземпляр класса Есентдатаексцептион.</span><span class="sxs-lookup"><span data-stu-id="b891c-104">Initializes a new instance of the EsentDataException class.</span></span>

<span data-ttu-id="b891c-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b891c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b891c-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b891c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b891c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b891c-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentDataException(description, _
    err)
```

``` csharp
protected EsentDataException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="b891c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b891c-108">Parameters</span></span>

  - <span data-ttu-id="b891c-109">description;</span><span class="sxs-lookup"><span data-stu-id="b891c-109">description</span></span>  
    <span data-ttu-id="b891c-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b891c-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b891c-111">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="b891c-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="b891c-112">Err</span><span class="sxs-lookup"><span data-stu-id="b891c-112">err</span></span>  
    <span data-ttu-id="b891c-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b891c-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="b891c-114">Код ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="b891c-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="b891c-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b891c-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b891c-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="b891c-116">Reference</span></span>

[<span data-ttu-id="b891c-117">Класс Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="b891c-117">EsentDataException class</span></span>](./esentdataexception-class.md)

[<span data-ttu-id="b891c-118">Элементы Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="b891c-118">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="b891c-119">Перегрузка Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="b891c-119">EsentDataException overload</span></span>](./esentdataexception-constructor.md)

[<span data-ttu-id="b891c-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b891c-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
