---
description: Дополнительные сведения о методе API. Жетопентабле
title: API. Жетопентабле, метод
TOCTitle: 'JetOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentable(v=EXCHG.10)
ms:contentKeyID: 55100776
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5764138d4ea387b68c94805c6966f7ce0e817c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999487"
---
# <a name="apijetopentable-method"></a><span data-ttu-id="02caf-103">API. Жетопентабле, метод</span><span class="sxs-lookup"><span data-stu-id="02caf-103">Api.JetOpenTable method</span></span>

<span data-ttu-id="02caf-104">Открывает курсор для ранее созданной таблицы.</span><span class="sxs-lookup"><span data-stu-id="02caf-104">Opens a cursor on a previously created table.</span></span>

<span data-ttu-id="02caf-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="02caf-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="02caf-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="02caf-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="02caf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02caf-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    parameters As Byte(), _
    parametersSize As Integer, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim parameters As Byte()
Dim parametersSize As Integer
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As JET_wrn

returnValue = Api.JetOpenTable(sesid, _
    dbid, tablename, parameters, parametersSize, _
    grbit, tableid)
```

``` csharp
public static JET_wrn JetOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    byte[] parameters,
    int parametersSize,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="02caf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="02caf-108">Parameters</span></span>

  - <span data-ttu-id="02caf-109">сесид</span><span class="sxs-lookup"><span data-stu-id="02caf-109">sesid</span></span>  
    <span data-ttu-id="02caf-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="02caf-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="02caf-111">Используемый сеанс базы данных.</span><span class="sxs-lookup"><span data-stu-id="02caf-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="02caf-112">dbid</span><span class="sxs-lookup"><span data-stu-id="02caf-112">dbid</span></span>  
    <span data-ttu-id="02caf-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="02caf-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="02caf-114">База данных, в которой будет открыта таблица.</span><span class="sxs-lookup"><span data-stu-id="02caf-114">The database to open the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="02caf-115">tablename</span><span class="sxs-lookup"><span data-stu-id="02caf-115">tablename</span></span>  
    <span data-ttu-id="02caf-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="02caf-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="02caf-117">Имя открываемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="02caf-117">The name of the table to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="02caf-118">parameters</span><span class="sxs-lookup"><span data-stu-id="02caf-118">parameters</span></span>  
    <span data-ttu-id="02caf-119">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="02caf-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="02caf-120">Параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="02caf-120">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="02caf-121">параметерссизе</span><span class="sxs-lookup"><span data-stu-id="02caf-121">parametersSize</span></span>  
    <span data-ttu-id="02caf-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="02caf-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="02caf-123">Параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="02caf-123">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="02caf-124">грбит</span><span class="sxs-lookup"><span data-stu-id="02caf-124">grbit</span></span>  
    <span data-ttu-id="02caf-125">Тип: [Microsoft. ISAM. ESENT. Interop. опентаблегрбит](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="02caf-125">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="02caf-126">Параметры открытия таблицы.</span><span class="sxs-lookup"><span data-stu-id="02caf-126">Table open options.</span></span>

<!-- end list -->

  - <span data-ttu-id="02caf-127">TableID</span><span class="sxs-lookup"><span data-stu-id="02caf-127">tableid</span></span>  
    <span data-ttu-id="02caf-128">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="02caf-128">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="02caf-129">Возвращает открытую таблицу.</span><span class="sxs-lookup"><span data-stu-id="02caf-129">Returns the opened table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="02caf-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02caf-130">Return value</span></span>

<span data-ttu-id="02caf-131">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="02caf-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="02caf-132">Предупреждение ESENT.</span><span class="sxs-lookup"><span data-stu-id="02caf-132">An ESENT warning.</span></span>  

## <a name="see-also"></a><span data-ttu-id="02caf-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02caf-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02caf-134">Справочник</span><span class="sxs-lookup"><span data-stu-id="02caf-134">Reference</span></span>

[<span data-ttu-id="02caf-135">Класс API</span><span class="sxs-lookup"><span data-stu-id="02caf-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="02caf-136">Члены API</span><span class="sxs-lookup"><span data-stu-id="02caf-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="02caf-137">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="02caf-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
