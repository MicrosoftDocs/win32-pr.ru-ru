---
description: 'Дополнительные сведения о: конструктор Есентфрагментатионексцептион (String, JET_err)'
title: Конструктор Есентфрагментатионексцептион (String, JET_err)
TOCTitle: EsentFragmentationException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101778
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3c6492ac4055b985194b3849090672d471390cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154730"
---
# <a name="esentfragmentationexception-constructor-string-jet_err"></a><span data-ttu-id="38df5-103">Конструктор Есентфрагментатионексцептион (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="38df5-103">EsentFragmentationException constructor (String, JET_err)</span></span>

<span data-ttu-id="38df5-104">Инициализирует новый экземпляр класса Есентфрагментатионексцептион.</span><span class="sxs-lookup"><span data-stu-id="38df5-104">Initializes a new instance of the EsentFragmentationException class.</span></span>

<span data-ttu-id="38df5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="38df5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="38df5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="38df5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="38df5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38df5-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentFragmentationException(description, _
    err)
```

``` csharp
protected EsentFragmentationException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="38df5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="38df5-108">Parameters</span></span>

  - <span data-ttu-id="38df5-109">description;</span><span class="sxs-lookup"><span data-stu-id="38df5-109">description</span></span>  
    <span data-ttu-id="38df5-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="38df5-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="38df5-111">Описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="38df5-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="38df5-112">Err</span><span class="sxs-lookup"><span data-stu-id="38df5-112">err</span></span>  
    <span data-ttu-id="38df5-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="38df5-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="38df5-114">Код ошибки исключения.</span><span class="sxs-lookup"><span data-stu-id="38df5-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="38df5-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38df5-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="38df5-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="38df5-116">Reference</span></span>

[<span data-ttu-id="38df5-117">Класс EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="38df5-117">EsentFragmentationException class</span></span>](./esentfragmentationexception-class.md)

[<span data-ttu-id="38df5-118">Элементы Есентфрагментатионексцептион</span><span class="sxs-lookup"><span data-stu-id="38df5-118">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="38df5-119">Перегрузка Есентфрагментатионексцептион</span><span class="sxs-lookup"><span data-stu-id="38df5-119">EsentFragmentationException overload</span></span>](./esentfragmentationexception-constructor.md)

[<span data-ttu-id="38df5-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="38df5-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
