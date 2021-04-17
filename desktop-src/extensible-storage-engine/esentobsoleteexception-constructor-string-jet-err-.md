---
description: 'Дополнительные сведения о: конструктор Есентобсолетиксцептион (String, JET_err)'
title: Конструктор Есентобсолетиксцептион (String, JET_err)
TOCTitle: EsentObsoleteException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102363
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 435a3db75cb09a47bccc311733b90fae30563c86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711814"
---
# <a name="esentobsoleteexception-constructor-string-jet_err"></a><span data-ttu-id="54a11-103">Конструктор Есентобсолетиксцептион (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="54a11-103">EsentObsoleteException constructor (String, JET_err)</span></span>

<span data-ttu-id="54a11-104">Инициализирует новый экземпляр класса Есентобсолетиксцептион.</span><span class="sxs-lookup"><span data-stu-id="54a11-104">Initializes a new instance of the EsentObsoleteException class.</span></span>

<span data-ttu-id="54a11-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="54a11-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="54a11-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="54a11-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="54a11-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54a11-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentObsoleteException(description, _
    err)
```

``` csharp
protected EsentObsoleteException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="54a11-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="54a11-108">Parameters</span></span>

  - <span data-ttu-id="54a11-109">description;</span><span class="sxs-lookup"><span data-stu-id="54a11-109">description</span></span>  
    <span data-ttu-id="54a11-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="54a11-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="54a11-111">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="54a11-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="54a11-112">Err</span><span class="sxs-lookup"><span data-stu-id="54a11-112">err</span></span>  
    <span data-ttu-id="54a11-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="54a11-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="54a11-114">Код ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="54a11-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="54a11-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54a11-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="54a11-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="54a11-116">Reference</span></span>

[<span data-ttu-id="54a11-117">Класс EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="54a11-117">EsentObsoleteException class</span></span>](./esentobsoleteexception-class.md)

[<span data-ttu-id="54a11-118">Элементы Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="54a11-118">EsentObsoleteException members</span></span>](./esentobsoleteexception-members.md)

[<span data-ttu-id="54a11-119">Перегрузка Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="54a11-119">EsentObsoleteException overload</span></span>](./esentobsoleteexception-constructor.md)

[<span data-ttu-id="54a11-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="54a11-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
