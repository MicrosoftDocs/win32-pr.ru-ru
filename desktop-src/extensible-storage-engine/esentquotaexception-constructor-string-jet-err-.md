---
description: 'Дополнительные сведения о: конструктор Есенткуотаексцептион (String, JET_err)'
title: Конструктор Есенткуотаексцептион (String, JET_err)
TOCTitle: EsentQuotaException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentQuotaException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102558
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f615cf2a46beb8c504de3dcc7d6fab1fc23da47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702272"
---
# <a name="esentquotaexception-constructor-string-jet_err"></a><span data-ttu-id="09481-103">Конструктор Есенткуотаексцептион (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="09481-103">EsentQuotaException constructor (String, JET_err)</span></span>

<span data-ttu-id="09481-104">Инициализирует новый экземпляр класса Есенткуотаексцептион.</span><span class="sxs-lookup"><span data-stu-id="09481-104">Initializes a new instance of the EsentQuotaException class.</span></span>

<span data-ttu-id="09481-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="09481-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="09481-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="09481-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="09481-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09481-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentQuotaException(description, _
    err)
```

``` csharp
protected EsentQuotaException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="09481-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="09481-108">Parameters</span></span>

  - <span data-ttu-id="09481-109">description;</span><span class="sxs-lookup"><span data-stu-id="09481-109">description</span></span>  
    <span data-ttu-id="09481-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="09481-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="09481-111">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="09481-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="09481-112">Err</span><span class="sxs-lookup"><span data-stu-id="09481-112">err</span></span>  
    <span data-ttu-id="09481-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="09481-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="09481-114">Код ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="09481-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="09481-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09481-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="09481-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="09481-116">Reference</span></span>

[<span data-ttu-id="09481-117">Класс EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="09481-117">EsentQuotaException class</span></span>](./esentquotaexception-class.md)

[<span data-ttu-id="09481-118">Элементы Есенткуотаексцептион</span><span class="sxs-lookup"><span data-stu-id="09481-118">EsentQuotaException members</span></span>](./esentquotaexception-members.md)

[<span data-ttu-id="09481-119">Перегрузка Есенткуотаексцептион</span><span class="sxs-lookup"><span data-stu-id="09481-119">EsentQuotaException overload</span></span>](./esentquotaexception-constructor.md)

[<span data-ttu-id="09481-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="09481-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
