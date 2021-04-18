---
description: Дополнительные сведения о методе API. Жетсеткуррентиндекс
title: API. Жетсеткуррентиндекс, метод
TOCTitle: 'JetSetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed3c069962fe879e250f90e34744780dfe2eb862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674349"
---
# <a name="apijetsetcurrentindex-method"></a><span data-ttu-id="df6e2-103">API. Жетсеткуррентиндекс, метод</span><span class="sxs-lookup"><span data-stu-id="df6e2-103">Api.JetSetCurrentIndex method</span></span>

<span data-ttu-id="df6e2-104">Задает текущий индекс курсора.</span><span class="sxs-lookup"><span data-stu-id="df6e2-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="df6e2-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="df6e2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="df6e2-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="df6e2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="df6e2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df6e2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As StringApi.JetSetCurrentIndex(sesid, tableid, _
    index)
```

``` csharp
public static void JetSetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index
)
```

#### <a name="parameters"></a><span data-ttu-id="df6e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="df6e2-108">Parameters</span></span>

  - <span data-ttu-id="df6e2-109">сесид</span><span class="sxs-lookup"><span data-stu-id="df6e2-109">sesid</span></span>  
    <span data-ttu-id="df6e2-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="df6e2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="df6e2-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="df6e2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="df6e2-112">TableID</span><span class="sxs-lookup"><span data-stu-id="df6e2-112">tableid</span></span>  
    <span data-ttu-id="df6e2-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="df6e2-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="df6e2-114">Курсор, для которого задается индекс.</span><span class="sxs-lookup"><span data-stu-id="df6e2-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="df6e2-115">index</span><span class="sxs-lookup"><span data-stu-id="df6e2-115">index</span></span>  
    <span data-ttu-id="df6e2-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="df6e2-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="df6e2-117">Имя выбранного индекса.</span><span class="sxs-lookup"><span data-stu-id="df6e2-117">The name of the index to be selected.</span></span> <span data-ttu-id="df6e2-118">Если это значение равно null или пуст, первичный индекс будет выбран.</span><span class="sxs-lookup"><span data-stu-id="df6e2-118">If this is null or empty the primary index will be selected.</span></span>

## <a name="see-also"></a><span data-ttu-id="df6e2-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df6e2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="df6e2-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="df6e2-120">Reference</span></span>

[<span data-ttu-id="df6e2-121">Класс API</span><span class="sxs-lookup"><span data-stu-id="df6e2-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="df6e2-122">Члены API</span><span class="sxs-lookup"><span data-stu-id="df6e2-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="df6e2-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="df6e2-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
