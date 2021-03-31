---
description: Дополнительные сведения о методе API. Жеткомпакт
title: API. Жеткомпакт, метод
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990997"
---
# <a name="apijetcompact-method"></a><span data-ttu-id="9dd8a-103">API. Жеткомпакт, метод</span><span class="sxs-lookup"><span data-stu-id="9dd8a-103">Api.JetCompact method</span></span>

<span data-ttu-id="9dd8a-104">Создает копию существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-104">Makes a copy of an existing database.</span></span> <span data-ttu-id="9dd8a-105">Копия сжимается в состояние, оптимальное для использования.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-105">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="9dd8a-106">Данные в скопированных данных будут упаковываться в соответствии с мерами, выбранными для индексов при создании индекса.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-106">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="9dd8a-107">Таким образом, сжатые данные могут храниться как можно более плотно.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-107">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="9dd8a-108">Кроме того, сжатые данные могут резервировать пространство для последующего роста записи или вставки индекса.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-108">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

<span data-ttu-id="9dd8a-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9dd8a-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9dd8a-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9dd8a-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd8a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9dd8a-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9dd8a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="9dd8a-112">Parameters</span></span>

  - <span data-ttu-id="9dd8a-113">сесид</span><span class="sxs-lookup"><span data-stu-id="9dd8a-113">sesid</span></span>  
    <span data-ttu-id="9dd8a-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9dd8a-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9dd8a-115">Сеанс, используемый для вызова.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-115">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="9dd8a-116">sourceDatabase</span><span class="sxs-lookup"><span data-stu-id="9dd8a-116">sourceDatabase</span></span>  
    <span data-ttu-id="9dd8a-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9dd8a-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9dd8a-118">База данных источника, которая будет сжата.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-118">The source database that will be compacted.</span></span>

<!-- end list -->

  - <span data-ttu-id="9dd8a-119">destinationDatabase</span><span class="sxs-lookup"><span data-stu-id="9dd8a-119">destinationDatabase</span></span>  
    <span data-ttu-id="9dd8a-120">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9dd8a-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9dd8a-121">Имя, используемое для сжатой базы данных.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-121">The name to use for the compacted database.</span></span>

<!-- end list -->

  - <span data-ttu-id="9dd8a-122">статускаллбакк</span><span class="sxs-lookup"><span data-stu-id="9dd8a-122">statusCallback</span></span>  
    <span data-ttu-id="9dd8a-123">Тип: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="9dd8a-123">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="9dd8a-124">Функция обратного вызова, которую можно периодически вызывать с помощью операции Database Compact для отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-124">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="9dd8a-125">не учитывается</span><span class="sxs-lookup"><span data-stu-id="9dd8a-125">ignored</span></span>  
    <span data-ttu-id="9dd8a-126">Тип: [Microsoft.ISAM.ESENT.Interop.JET_CONVERT](./jet-convert-class.md)</span><span class="sxs-lookup"><span data-stu-id="9dd8a-126">Type: [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)</span></span>  
    
    <span data-ttu-id="9dd8a-127">Этот параметр игнорируется и должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-127">This parameter is ignored and should be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="9dd8a-128">грбит</span><span class="sxs-lookup"><span data-stu-id="9dd8a-128">grbit</span></span>  
    <span data-ttu-id="9dd8a-129">Тип: [Microsoft. ISAM. ESENT. Interop. компактгрбит](./compactgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9dd8a-129">Type: [Microsoft.Isam.Esent.Interop.CompactGrbit](./compactgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9dd8a-130">Параметры сжатия.</span><span class="sxs-lookup"><span data-stu-id="9dd8a-130">Compact options.</span></span>

## <a name="see-also"></a><span data-ttu-id="9dd8a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9dd8a-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9dd8a-132">Справочник</span><span class="sxs-lookup"><span data-stu-id="9dd8a-132">Reference</span></span>

[<span data-ttu-id="9dd8a-133">Класс API</span><span class="sxs-lookup"><span data-stu-id="9dd8a-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9dd8a-134">Члены API</span><span class="sxs-lookup"><span data-stu-id="9dd8a-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9dd8a-135">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9dd8a-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
