---
description: Дополнительные сведения о методе API. JetCreateTableColumnIndex3
title: API. JetCreateTableColumnIndex3, метод
TOCTitle: 'JetCreateTableColumnIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetablecolumnindex3(v=EXCHG.10)
ms:contentKeyID: 55100678
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a967db8f6a322ac29ba8a1e9352972ff1f4f4b76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497160"
---
# <a name="apijetcreatetablecolumnindex3-method"></a><span data-ttu-id="5c47e-103">API. JetCreateTableColumnIndex3, метод</span><span class="sxs-lookup"><span data-stu-id="5c47e-103">Api.JetCreateTableColumnIndex3 method</span></span>

<span data-ttu-id="5c47e-104">Создает таблицу, добавляет столбцы и индексы для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="5c47e-104">Creates a table, adds columns, and indices on that table.</span></span>

<span data-ttu-id="5c47e-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5c47e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5c47e-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5c47e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5c47e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c47e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTableColumnIndex3 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablecreate As JET_TABLECREATE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablecreate As JET_TABLECREATEApi.JetCreateTableColumnIndex3(sesid, _
    dbid, tablecreate)
```

``` csharp
public static void JetCreateTableColumnIndex3(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLECREATE tablecreate
)
```

#### <a name="parameters"></a><span data-ttu-id="5c47e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c47e-108">Parameters</span></span>

  - <span data-ttu-id="5c47e-109">сесид</span><span class="sxs-lookup"><span data-stu-id="5c47e-109">sesid</span></span>  
    <span data-ttu-id="5c47e-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5c47e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5c47e-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="5c47e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5c47e-112">dbid</span><span class="sxs-lookup"><span data-stu-id="5c47e-112">dbid</span></span>  
    <span data-ttu-id="5c47e-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5c47e-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="5c47e-114">База данных, в которую добавляется новая таблица.</span><span class="sxs-lookup"><span data-stu-id="5c47e-114">The database to which to add the new table.</span></span>

<!-- end list -->

  - <span data-ttu-id="5c47e-115">таблекреате</span><span class="sxs-lookup"><span data-stu-id="5c47e-115">tablecreate</span></span>  
    <span data-ttu-id="5c47e-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="5c47e-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span></span>  
    
    <span data-ttu-id="5c47e-117">Объект, описывающий создаваемую таблицу.</span><span class="sxs-lookup"><span data-stu-id="5c47e-117">Object describing the table to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c47e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c47e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5c47e-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="5c47e-119">Reference</span></span>

[<span data-ttu-id="5c47e-120">Класс API</span><span class="sxs-lookup"><span data-stu-id="5c47e-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5c47e-121">Члены API</span><span class="sxs-lookup"><span data-stu-id="5c47e-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5c47e-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5c47e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
