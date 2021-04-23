---
description: Дополнительные сведения о методе API. Сериализеобжекттоколумн
title: API. Сериализеобжекттоколумн, метод
TOCTitle: 'SerializeObjectToColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.serializeobjecttocolumn(v=EXCHG.10)
ms:contentKeyID: 55100915
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.SerializeObjectToColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 21b0e421b68287b983fc43482e3a2385b2a160f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265175"
---
# <a name="apiserializeobjecttocolumn-method"></a><span data-ttu-id="459ba-103">API. Сериализеобжекттоколумн, метод</span><span class="sxs-lookup"><span data-stu-id="459ba-103">Api.SerializeObjectToColumn method</span></span>

<span data-ttu-id="459ba-104">Запись сериализованной формы объекта в столбец.</span><span class="sxs-lookup"><span data-stu-id="459ba-104">Write a serialized form of an object to a column.</span></span>

<span data-ttu-id="459ba-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="459ba-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="459ba-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="459ba-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="459ba-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="459ba-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SerializeObjectToColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    value As Object _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim value As ObjectApi.SerializeObjectToColumn(sesid, _
    tableid, columnid, value)
```

``` csharp
public static void SerializeObjectToColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Object value
)
```

#### <a name="parameters"></a><span data-ttu-id="459ba-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="459ba-108">Parameters</span></span>

  - <span data-ttu-id="459ba-109">сесид</span><span class="sxs-lookup"><span data-stu-id="459ba-109">sesid</span></span>  
    <span data-ttu-id="459ba-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="459ba-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="459ba-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="459ba-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="459ba-112">TableID</span><span class="sxs-lookup"><span data-stu-id="459ba-112">tableid</span></span>  
    <span data-ttu-id="459ba-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="459ba-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="459ba-114">Таблица для записи.</span><span class="sxs-lookup"><span data-stu-id="459ba-114">The table to write to.</span></span> <span data-ttu-id="459ba-115">Необходимо подготовить обновление.</span><span class="sxs-lookup"><span data-stu-id="459ba-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="459ba-116">columnid</span><span class="sxs-lookup"><span data-stu-id="459ba-116">columnid</span></span>  
    <span data-ttu-id="459ba-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="459ba-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="459ba-118">Столбец, в который производится запись.</span><span class="sxs-lookup"><span data-stu-id="459ba-118">The column to write to.</span></span>

<!-- end list -->

  - <span data-ttu-id="459ba-119">значение</span><span class="sxs-lookup"><span data-stu-id="459ba-119">value</span></span>  
    <span data-ttu-id="459ba-120">Тип: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="459ba-120">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="459ba-121">Записываемый объект.</span><span class="sxs-lookup"><span data-stu-id="459ba-121">The object to write.</span></span> <span data-ttu-id="459ba-122">Объект должен быть сериализуемым.</span><span class="sxs-lookup"><span data-stu-id="459ba-122">The object must be serializable.</span></span>

## <a name="see-also"></a><span data-ttu-id="459ba-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="459ba-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="459ba-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="459ba-124">Reference</span></span>

[<span data-ttu-id="459ba-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="459ba-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="459ba-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="459ba-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="459ba-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="459ba-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
