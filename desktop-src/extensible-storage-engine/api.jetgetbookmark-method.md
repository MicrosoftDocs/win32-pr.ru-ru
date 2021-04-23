---
description: Дополнительные сведения о методе API. Жетжетбукмарк
title: API. Жетжетбукмарк, метод
TOCTitle: 'JetGetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetbookmark(v=EXCHG.10)
ms:contentKeyID: 55100702
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0eaac3c0c92fa9d6cfa1a5bca660791b81efe5ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719322"
---
# <a name="apijetgetbookmark-method"></a><span data-ttu-id="997eb-103">API. Жетжетбукмарк, метод</span><span class="sxs-lookup"><span data-stu-id="997eb-103">Api.JetGetBookmark method</span></span>

<span data-ttu-id="997eb-104">Извлекает закладку для записи, связанной с элементом индекса, в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="997eb-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="997eb-105">Эту закладку можно использовать для перемещения курсора обратно в ту же запись с помощью [жетготобукмарк (JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetgotobookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="997eb-105">This bookmark can then be used to reposition that cursor back to the same record using [JetGotoBookmark(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetgotobookmark-method.md).</span></span> <span data-ttu-id="997eb-106">Длина закладки не должна превышать [букмаркмост](./systemparameters.bookmarkmost-property.md) байт.</span><span class="sxs-lookup"><span data-stu-id="997eb-106">The bookmark will be no longer than [BookmarkMost](./systemparameters.bookmarkmost-property.md) bytes.</span></span> <span data-ttu-id="997eb-107">См. также [Закладка (JET_SESID, JET_TABLEID)](./api.getbookmark-method.md).</span><span class="sxs-lookup"><span data-stu-id="997eb-107">Also see [GetBookmark(JET_SESID, JET_TABLEID)](./api.getbookmark-method.md).</span></span>

<span data-ttu-id="997eb-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="997eb-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="997eb-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="997eb-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="997eb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="997eb-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetGetBookmark(sesid, tableid, _
    bookmark, bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetGetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="997eb-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="997eb-111">Parameters</span></span>

  - <span data-ttu-id="997eb-112">сесид</span><span class="sxs-lookup"><span data-stu-id="997eb-112">sesid</span></span>  
    <span data-ttu-id="997eb-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="997eb-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="997eb-114">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="997eb-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="997eb-115">TableID</span><span class="sxs-lookup"><span data-stu-id="997eb-115">tableid</span></span>  
    <span data-ttu-id="997eb-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="997eb-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="997eb-117">Курсор, из которого извлекается закладка.</span><span class="sxs-lookup"><span data-stu-id="997eb-117">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="997eb-118">закладка</span><span class="sxs-lookup"><span data-stu-id="997eb-118">bookmark</span></span>  
    <span data-ttu-id="997eb-119">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="997eb-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="997eb-120">Буфер для хранения закладки.</span><span class="sxs-lookup"><span data-stu-id="997eb-120">Buffer to contain the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="997eb-121">букмарксизе</span><span class="sxs-lookup"><span data-stu-id="997eb-121">bookmarkSize</span></span>  
    <span data-ttu-id="997eb-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="997eb-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="997eb-123">Размер буфера закладок.</span><span class="sxs-lookup"><span data-stu-id="997eb-123">Size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="997eb-124">актуалбукмарксизе</span><span class="sxs-lookup"><span data-stu-id="997eb-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="997eb-125">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="997eb-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="997eb-126">Возвращает фактический размер закладки.</span><span class="sxs-lookup"><span data-stu-id="997eb-126">Returns the actual size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="997eb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="997eb-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="997eb-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="997eb-128">Reference</span></span>

[<span data-ttu-id="997eb-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="997eb-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="997eb-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="997eb-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="997eb-131">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="997eb-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
