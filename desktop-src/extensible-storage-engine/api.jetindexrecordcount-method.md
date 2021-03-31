---
description: Дополнительные сведения о методе API. Жетиндексрекордкаунт
title: API. Жетиндексрекордкаунт, метод
TOCTitle: 'JetIndexRecordCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetindexrecordcount(v=EXCHG.10)
ms:contentKeyID: 55100758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 429239ab7734a594fd2c5a3510650d8f410e94f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817593"
---
# <a name="apijetindexrecordcount-method"></a><span data-ttu-id="d45b2-103">API. Жетиндексрекордкаунт, метод</span><span class="sxs-lookup"><span data-stu-id="d45b2-103">Api.JetIndexRecordCount method</span></span>

<span data-ttu-id="d45b2-104">Подсчитывает количество записей в текущем индексе до текущей позиции вперед.</span><span class="sxs-lookup"><span data-stu-id="d45b2-104">Counts the number of entries in the current index from the current position forward.</span></span> <span data-ttu-id="d45b2-105">Текущая позицией включается в число.</span><span class="sxs-lookup"><span data-stu-id="d45b2-105">The current position is included in the count.</span></span> <span data-ttu-id="d45b2-106">Число может быть больше, чем общее число записей в таблице, если текущий индекс находится над многозначным столбцом, а экземпляры столбца имеют несколько значений.</span><span class="sxs-lookup"><span data-stu-id="d45b2-106">The count can be greater than the total number of records in the table if the current index is over a multi-valued column and instances of the column have multiple-values.</span></span> <span data-ttu-id="d45b2-107">Если таблица пуста, для счетчика будет возвращено значение 0.</span><span class="sxs-lookup"><span data-stu-id="d45b2-107">If the table is empty, then 0 will be returned for the count.</span></span>

<span data-ttu-id="d45b2-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d45b2-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d45b2-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d45b2-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d45b2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d45b2-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetIndexRecordCount ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef numRecords As Integer, _
    maxRecordsToCount As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRecords As Integer
Dim maxRecordsToCount As IntegerApi.JetIndexRecordCount(sesid, _
    tableid, numRecords, maxRecordsToCount)
```

``` csharp
public static void JetIndexRecordCount(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int numRecords,
    int maxRecordsToCount
)
```

#### <a name="parameters"></a><span data-ttu-id="d45b2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d45b2-111">Parameters</span></span>

  - <span data-ttu-id="d45b2-112">сесид</span><span class="sxs-lookup"><span data-stu-id="d45b2-112">sesid</span></span>  
    <span data-ttu-id="d45b2-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d45b2-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d45b2-114">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="d45b2-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d45b2-115">TableID</span><span class="sxs-lookup"><span data-stu-id="d45b2-115">tableid</span></span>  
    <span data-ttu-id="d45b2-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d45b2-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="d45b2-117">Курсор для подсчета записей в.</span><span class="sxs-lookup"><span data-stu-id="d45b2-117">The cursor to count the records in.</span></span>

<!-- end list -->

  - <span data-ttu-id="d45b2-118">нумрекордс</span><span class="sxs-lookup"><span data-stu-id="d45b2-118">numRecords</span></span>  
    <span data-ttu-id="d45b2-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d45b2-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d45b2-120">Возвращает число записей.</span><span class="sxs-lookup"><span data-stu-id="d45b2-120">Returns the number of records.</span></span>

<!-- end list -->

  - <span data-ttu-id="d45b2-121">максрекордстокаунт</span><span class="sxs-lookup"><span data-stu-id="d45b2-121">maxRecordsToCount</span></span>  
    <span data-ttu-id="d45b2-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d45b2-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d45b2-123">Максимальное число записей для подсчета.</span><span class="sxs-lookup"><span data-stu-id="d45b2-123">The maximum number of records to count.</span></span> <span data-ttu-id="d45b2-124">Значение 0 указывает, что число не ограничено.</span><span class="sxs-lookup"><span data-stu-id="d45b2-124">A value of 0 indicates that the count is unlimited.</span></span>

## <a name="see-also"></a><span data-ttu-id="d45b2-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d45b2-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d45b2-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="d45b2-126">Reference</span></span>

[<span data-ttu-id="d45b2-127">Класс API</span><span class="sxs-lookup"><span data-stu-id="d45b2-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d45b2-128">Члены API</span><span class="sxs-lookup"><span data-stu-id="d45b2-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d45b2-129">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d45b2-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
