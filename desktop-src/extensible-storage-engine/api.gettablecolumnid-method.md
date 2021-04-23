---
description: Дополнительные сведения о методе API. Жеттаблеколумнид
title: API. Жеттаблеколумнид, метод
TOCTitle: 'GetTableColumnid method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumnid(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumnid(v=EXCHG.10)
ms:contentKeyID: 55107215
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec91b014401709b6312b3363d8dae9e7da3d200e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539746"
---
# <a name="apigettablecolumnid-method"></a><span data-ttu-id="f27ac-103">API. Жеттаблеколумнид, метод</span><span class="sxs-lookup"><span data-stu-id="f27ac-103">Api.GetTableColumnid method</span></span>

<span data-ttu-id="f27ac-104">Получение columnid указанного столбца.</span><span class="sxs-lookup"><span data-stu-id="f27ac-104">Get the columnid of the specified column.</span></span>

<span data-ttu-id="f27ac-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f27ac-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f27ac-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f27ac-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f27ac-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f27ac-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumnid ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String _
) As JET_COLUMNID
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim returnValue As JET_COLUMNID

returnValue = Api.GetTableColumnid(sesid, _
    tableid, columnName)
```

``` csharp
public static JET_COLUMNID GetTableColumnid(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName
)
```

#### <a name="parameters"></a><span data-ttu-id="f27ac-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f27ac-108">Parameters</span></span>

  - <span data-ttu-id="f27ac-109">сесид</span><span class="sxs-lookup"><span data-stu-id="f27ac-109">sesid</span></span>  
    <span data-ttu-id="f27ac-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f27ac-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f27ac-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="f27ac-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f27ac-112">TableID</span><span class="sxs-lookup"><span data-stu-id="f27ac-112">tableid</span></span>  
    <span data-ttu-id="f27ac-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f27ac-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f27ac-114">Таблица, содержащей столбец.</span><span class="sxs-lookup"><span data-stu-id="f27ac-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="f27ac-115">columnName</span><span class="sxs-lookup"><span data-stu-id="f27ac-115">columnName</span></span>  
    <span data-ttu-id="f27ac-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f27ac-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f27ac-117">Имя столбца.</span><span class="sxs-lookup"><span data-stu-id="f27ac-117">The name of the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f27ac-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f27ac-118">Return value</span></span>

<span data-ttu-id="f27ac-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f27ac-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
<span data-ttu-id="f27ac-120">Идентификатор столбца.</span><span class="sxs-lookup"><span data-stu-id="f27ac-120">The id of the column.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f27ac-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f27ac-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f27ac-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="f27ac-122">Reference</span></span>

[<span data-ttu-id="f27ac-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="f27ac-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f27ac-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="f27ac-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f27ac-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f27ac-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
