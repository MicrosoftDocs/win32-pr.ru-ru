---
description: Дополнительные сведения о методе API. Жетделетеиндекс
title: API. Жетделетеиндекс, метод
TOCTitle: 'JetDeleteIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeleteindex(v=EXCHG.10)
ms:contentKeyID: 55100682
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteIndex
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de04966aae4aee3f4ab7b14a846b898f55f887be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540871"
---
# <a name="apijetdeleteindex-method"></a><span data-ttu-id="4cd00-103">API. Жетделетеиндекс, метод</span><span class="sxs-lookup"><span data-stu-id="4cd00-103">Api.JetDeleteIndex method</span></span>

<span data-ttu-id="4cd00-104">Удаляет индекс из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="4cd00-104">Deletes an index from a database table.</span></span>

<span data-ttu-id="4cd00-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4cd00-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4cd00-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4cd00-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd00-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cd00-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As StringApi.JetDeleteIndex(sesid, tableid, _
    index)
```

``` csharp
public static void JetDeleteIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index
)
```

#### <a name="parameters"></a><span data-ttu-id="4cd00-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cd00-108">Parameters</span></span>

  - <span data-ttu-id="4cd00-109">сесид</span><span class="sxs-lookup"><span data-stu-id="4cd00-109">sesid</span></span>  
    <span data-ttu-id="4cd00-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4cd00-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4cd00-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4cd00-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4cd00-112">TableID</span><span class="sxs-lookup"><span data-stu-id="4cd00-112">tableid</span></span>  
    <span data-ttu-id="4cd00-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4cd00-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4cd00-114">Курсор в таблице, из которого удаляется индекс.</span><span class="sxs-lookup"><span data-stu-id="4cd00-114">A cursor on the table to delete the index from.</span></span>

<!-- end list -->

  - <span data-ttu-id="4cd00-115">index</span><span class="sxs-lookup"><span data-stu-id="4cd00-115">index</span></span>  
    <span data-ttu-id="4cd00-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4cd00-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4cd00-117">Имя удаляемого индекса.</span><span class="sxs-lookup"><span data-stu-id="4cd00-117">The name of the index to be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="4cd00-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cd00-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4cd00-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="4cd00-119">Reference</span></span>

[<span data-ttu-id="4cd00-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="4cd00-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4cd00-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="4cd00-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4cd00-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4cd00-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
