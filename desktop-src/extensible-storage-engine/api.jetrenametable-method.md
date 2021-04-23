---
description: Дополнительные сведения о методе API. Жетренаметабле
title: API. Жетренаметабле, метод
TOCTitle: 'JetRenameTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRenameTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrenametable(v=EXCHG.10)
ms:contentKeyID: 55100788
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRenameTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRenameTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6bb108498501df50a43964f5b069860d10c39258
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072670"
---
# <a name="apijetrenametable-method"></a><span data-ttu-id="79091-103">API. Жетренаметабле, метод</span><span class="sxs-lookup"><span data-stu-id="79091-103">Api.JetRenameTable method</span></span>

<span data-ttu-id="79091-104">Изменяет имя существующей таблицы.</span><span class="sxs-lookup"><span data-stu-id="79091-104">Changes the name of an existing table.</span></span>

<span data-ttu-id="79091-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="79091-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="79091-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="79091-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="79091-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79091-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRenameTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    newTableName As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim newTableName As StringApi.JetRenameTable(sesid, dbid, _
    tableName, newTableName)
```

``` csharp
public static void JetRenameTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string newTableName
)
```

#### <a name="parameters"></a><span data-ttu-id="79091-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="79091-108">Parameters</span></span>

  - <span data-ttu-id="79091-109">сесид</span><span class="sxs-lookup"><span data-stu-id="79091-109">sesid</span></span>  
    <span data-ttu-id="79091-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79091-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="79091-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="79091-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="79091-112">dbid</span><span class="sxs-lookup"><span data-stu-id="79091-112">dbid</span></span>  
    <span data-ttu-id="79091-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79091-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="79091-114">База данных, содержащая таблицу.</span><span class="sxs-lookup"><span data-stu-id="79091-114">The database containing the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="79091-115">tableName</span><span class="sxs-lookup"><span data-stu-id="79091-115">tableName</span></span>  
    <span data-ttu-id="79091-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="79091-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="79091-117">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="79091-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="79091-118">невтабленаме</span><span class="sxs-lookup"><span data-stu-id="79091-118">newTableName</span></span>  
    <span data-ttu-id="79091-119">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="79091-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="79091-120">Новое имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="79091-120">The new name of the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="79091-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79091-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="79091-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="79091-122">Reference</span></span>

[<span data-ttu-id="79091-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="79091-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="79091-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="79091-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="79091-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="79091-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
