---
description: Дополнительные сведения см. в статье метод обновления. Save (Byte, Int32, Int32).
title: Метод Update. Save (Byte, Int32, Int32)
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2c798f22039ced1bab30ecaa9c3f650079be0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497619"
---
# <a name="updatesave-method-byte--int32-int32"></a><span data-ttu-id="46dd3-103">Метод Update. Save (Byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="46dd3-103">Update.Save method (Byte , Int32, Int32)</span></span>

<span data-ttu-id="46dd3-104">Обновите TableID.</span><span class="sxs-lookup"><span data-stu-id="46dd3-104">Update the tableid.</span></span>

<span data-ttu-id="46dd3-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="46dd3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="46dd3-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="46dd3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="46dd3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46dd3-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="46dd3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="46dd3-108">Parameters</span></span>

  - <span data-ttu-id="46dd3-109">закладка</span><span class="sxs-lookup"><span data-stu-id="46dd3-109">bookmark</span></span>  
    <span data-ttu-id="46dd3-110">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="46dd3-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="46dd3-111">Возвращает закладку обновленной записи.</span><span class="sxs-lookup"><span data-stu-id="46dd3-111">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="46dd3-112">Может принимать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="46dd3-112">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="46dd3-113">букмарксизе</span><span class="sxs-lookup"><span data-stu-id="46dd3-113">bookmarkSize</span></span>  
    <span data-ttu-id="46dd3-114">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="46dd3-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="46dd3-115">Размер буфера закладок.</span><span class="sxs-lookup"><span data-stu-id="46dd3-115">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="46dd3-116">актуалбукмарксизе</span><span class="sxs-lookup"><span data-stu-id="46dd3-116">actualBookmarkSize</span></span>  
    <span data-ttu-id="46dd3-117">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="46dd3-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="46dd3-118">Возвращает фактический размер закладки.</span><span class="sxs-lookup"><span data-stu-id="46dd3-118">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="46dd3-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46dd3-119">Remarks</span></span>

<span data-ttu-id="46dd3-120">Сохранение является последним шагом в выполнении вставки или обновления.</span><span class="sxs-lookup"><span data-stu-id="46dd3-120">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="46dd3-121">Обновление начинается с вызова метода создания объекта Update, а затем путем вызова Жетсетколумн или Жетсетколумнс один или несколько раз для задания состояния записи.</span><span class="sxs-lookup"><span data-stu-id="46dd3-121">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="46dd3-122">Наконец, для завершения операции обновления вызывается обновление.</span><span class="sxs-lookup"><span data-stu-id="46dd3-122">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="46dd3-123">Индексы обновляются только с помощью Update, а не во время Жетсетколумн или Жетсетколумнс.</span><span class="sxs-lookup"><span data-stu-id="46dd3-123">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="46dd3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46dd3-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="46dd3-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="46dd3-125">Reference</span></span>

[<span data-ttu-id="46dd3-126">Класс обновления</span><span class="sxs-lookup"><span data-stu-id="46dd3-126">Update class</span></span>](./update-class.md)

[<span data-ttu-id="46dd3-127">Обновить элементы</span><span class="sxs-lookup"><span data-stu-id="46dd3-127">Update members</span></span>](./update-members.md)

[<span data-ttu-id="46dd3-128">Сохранить перегрузку</span><span class="sxs-lookup"><span data-stu-id="46dd3-128">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="46dd3-129">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="46dd3-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
