---
description: Дополнительные сведения о методе API. Жетготобукмарк
title: API. Жетготобукмарк, метод
TOCTitle: 'JetGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55100753
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 362a174e3da4dad864fd504e1678b4a3a1477e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546962"
---
# <a name="apijetgotobookmark-method"></a><span data-ttu-id="9bd81-103">API. Жетготобукмарк, метод</span><span class="sxs-lookup"><span data-stu-id="9bd81-103">Api.JetGotoBookmark method</span></span>

<span data-ttu-id="9bd81-104">Позиционирует курсор на запись индекса для записи, связанной с указанной закладкой.</span><span class="sxs-lookup"><span data-stu-id="9bd81-104">Positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="9bd81-105">Закладку можно использовать с любым индексом, определенным для таблицы.</span><span class="sxs-lookup"><span data-stu-id="9bd81-105">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="9bd81-106">Закладку для записи можно получить с помощью [жетжетбукмарк (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetgetbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="9bd81-106">The bookmark for a record can be retrieved using [JetGetBookmark(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetgetbookmark-method.md).</span></span>

<span data-ttu-id="9bd81-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9bd81-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9bd81-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9bd81-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9bd81-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bd81-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As IntegerApi.JetGotoBookmark(sesid, tableid, _
    bookmark, bookmarkSize)
```

``` csharp
public static void JetGotoBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="9bd81-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bd81-110">Parameters</span></span>

  - <span data-ttu-id="9bd81-111">сесид</span><span class="sxs-lookup"><span data-stu-id="9bd81-111">sesid</span></span>  
    <span data-ttu-id="9bd81-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bd81-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9bd81-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="9bd81-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bd81-114">TableID</span><span class="sxs-lookup"><span data-stu-id="9bd81-114">tableid</span></span>  
    <span data-ttu-id="9bd81-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bd81-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9bd81-116">Курсор для позиции.</span><span class="sxs-lookup"><span data-stu-id="9bd81-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bd81-117">закладка</span><span class="sxs-lookup"><span data-stu-id="9bd81-117">bookmark</span></span>  
    <span data-ttu-id="9bd81-118">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="9bd81-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="9bd81-119">Закладка, используемая для позиционирования курсора.</span><span class="sxs-lookup"><span data-stu-id="9bd81-119">The bookmark used to position the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bd81-120">букмарксизе</span><span class="sxs-lookup"><span data-stu-id="9bd81-120">bookmarkSize</span></span>  
    <span data-ttu-id="9bd81-121">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9bd81-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9bd81-122">Размер закладки.</span><span class="sxs-lookup"><span data-stu-id="9bd81-122">The size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="9bd81-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bd81-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9bd81-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="9bd81-124">Reference</span></span>

[<span data-ttu-id="9bd81-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="9bd81-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9bd81-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="9bd81-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9bd81-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9bd81-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
