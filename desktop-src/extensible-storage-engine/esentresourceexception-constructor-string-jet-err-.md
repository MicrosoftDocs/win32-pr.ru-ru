---
description: 'Дополнительные сведения о: конструктор Есентресаурцеексцептион (String, JET_err)'
title: Конструктор Есентресаурцеексцептион (String, JET_err)
TOCTitle: EsentResourceException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentResourceException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55107307
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 458b12a80fdc0e6d7883d966f2e50aa8c1f6d69b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545970"
---
# <a name="esentresourceexception-constructor-string-jet_err"></a><span data-ttu-id="c054c-103">Конструктор Есентресаурцеексцептион (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="c054c-103">EsentResourceException constructor (String, JET_err)</span></span>

<span data-ttu-id="c054c-104">Инициализирует новый экземпляр класса Есентресаурцеексцептион.</span><span class="sxs-lookup"><span data-stu-id="c054c-104">Initializes a new instance of the EsentResourceException class.</span></span>

<span data-ttu-id="c054c-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c054c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c054c-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c054c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c054c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c054c-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentResourceException(description, _
    err)
```

``` csharp
protected EsentResourceException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="c054c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c054c-108">Parameters</span></span>

  - <span data-ttu-id="c054c-109">description;</span><span class="sxs-lookup"><span data-stu-id="c054c-109">description</span></span>  
    <span data-ttu-id="c054c-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c054c-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c054c-111">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="c054c-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="c054c-112">Err</span><span class="sxs-lookup"><span data-stu-id="c054c-112">err</span></span>  
    <span data-ttu-id="c054c-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c054c-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="c054c-114">Код ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="c054c-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="c054c-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c054c-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c054c-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="c054c-116">Reference</span></span>

[<span data-ttu-id="c054c-117">Класс EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="c054c-117">EsentResourceException class</span></span>](./esentresourceexception-class.md)

[<span data-ttu-id="c054c-118">Элементы Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="c054c-118">EsentResourceException members</span></span>](./esentresourceexception-members.md)

[<span data-ttu-id="c054c-119">Перегрузка Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="c054c-119">EsentResourceException overload</span></span>](./esentresourceexception-constructor.md)

[<span data-ttu-id="c054c-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c054c-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
