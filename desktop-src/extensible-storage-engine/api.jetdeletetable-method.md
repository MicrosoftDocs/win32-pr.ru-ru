---
description: Дополнительные сведения о методе API. Жетделететабле
title: API. Жетделететабле, метод
TOCTitle: 'JetDeleteTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletetable(v=EXCHG.10)
ms:contentKeyID: 55100683
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b4128ae81484343bec7fb4f52a736db149f0eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144350"
---
# <a name="apijetdeletetable-method"></a><span data-ttu-id="ace33-103">API. Жетделететабле, метод</span><span class="sxs-lookup"><span data-stu-id="ace33-103">Api.JetDeleteTable method</span></span>

<span data-ttu-id="ace33-104">Удаляет таблицу из базы данных.</span><span class="sxs-lookup"><span data-stu-id="ace33-104">Deletes a table from a database.</span></span>

<span data-ttu-id="ace33-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ace33-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ace33-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ace33-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ace33-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ace33-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As StringApi.JetDeleteTable(sesid, dbid, _
    table)
```

``` csharp
public static void JetDeleteTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table
)
```

#### <a name="parameters"></a><span data-ttu-id="ace33-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ace33-108">Parameters</span></span>

  - <span data-ttu-id="ace33-109">сесид</span><span class="sxs-lookup"><span data-stu-id="ace33-109">sesid</span></span>  
    <span data-ttu-id="ace33-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ace33-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ace33-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="ace33-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ace33-112">dbid</span><span class="sxs-lookup"><span data-stu-id="ace33-112">dbid</span></span>  
    <span data-ttu-id="ace33-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ace33-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="ace33-114">База данных, из которой удаляется таблица.</span><span class="sxs-lookup"><span data-stu-id="ace33-114">The database to delete the table from.</span></span>

<!-- end list -->

  - <span data-ttu-id="ace33-115">table</span><span class="sxs-lookup"><span data-stu-id="ace33-115">table</span></span>  
    <span data-ttu-id="ace33-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="ace33-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="ace33-117">Имя таблицы для удаления.</span><span class="sxs-lookup"><span data-stu-id="ace33-117">The name of the table to delete.</span></span>

## <a name="see-also"></a><span data-ttu-id="ace33-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ace33-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ace33-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="ace33-119">Reference</span></span>

[<span data-ttu-id="ace33-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="ace33-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ace33-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="ace33-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ace33-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ace33-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
