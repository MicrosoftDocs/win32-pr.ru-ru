---
description: 'Дополнительные сведения: метод API. onbookmark'
title: Метод API. onbookmark
TOCTitle: 'GetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getbookmark(v=EXCHG.10)
ms:contentKeyID: 55100654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edcdfe7ddefadd993ef9c96e6dcc1416080b413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539751"
---
# <a name="apigetbookmark-method"></a><span data-ttu-id="caf3d-103">Метод API. onbookmark</span><span class="sxs-lookup"><span data-stu-id="caf3d-103">Api.GetBookmark method</span></span>

<span data-ttu-id="caf3d-104">Извлекает закладку для записи, связанной с элементом индекса, в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="caf3d-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="caf3d-105">Эту закладку можно использовать для перемещения курсора обратно в ту же запись с помощью Жетготобукмарк.</span><span class="sxs-lookup"><span data-stu-id="caf3d-105">This bookmark can then be used to reposition that cursor back to the same record using JetGotoBookmark.</span></span>

<span data-ttu-id="caf3d-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="caf3d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="caf3d-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="caf3d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="caf3d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="caf3d-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Byte()

returnValue = Api.GetBookmark(sesid, _
    tableid)
```

``` csharp
public static byte[] GetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="caf3d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="caf3d-109">Parameters</span></span>

  - <span data-ttu-id="caf3d-110">сесид</span><span class="sxs-lookup"><span data-stu-id="caf3d-110">sesid</span></span>  
    <span data-ttu-id="caf3d-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="caf3d-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="caf3d-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="caf3d-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="caf3d-113">TableID</span><span class="sxs-lookup"><span data-stu-id="caf3d-113">tableid</span></span>  
    <span data-ttu-id="caf3d-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="caf3d-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="caf3d-115">Курсор, из которого извлекается закладка.</span><span class="sxs-lookup"><span data-stu-id="caf3d-115">The cursor to retrieve the bookmark from.</span></span>

#### <a name="return-value"></a><span data-ttu-id="caf3d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="caf3d-116">Return value</span></span>

<span data-ttu-id="caf3d-117">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="caf3d-117">Type: \[\]</span></span>  
<span data-ttu-id="caf3d-118">Закладка записи.</span><span class="sxs-lookup"><span data-stu-id="caf3d-118">The bookmark of the record.</span></span>  

## <a name="see-also"></a><span data-ttu-id="caf3d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="caf3d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="caf3d-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="caf3d-120">Reference</span></span>

[<span data-ttu-id="caf3d-121">Класс API</span><span class="sxs-lookup"><span data-stu-id="caf3d-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="caf3d-122">Члены API</span><span class="sxs-lookup"><span data-stu-id="caf3d-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="caf3d-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="caf3d-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
