---
description: Дополнительные сведения о методе API. Жетдефрагмент
title: API. Жетдефрагмент, метод
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69428d785bf9d607199cb62bfe02d2e373e7dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710955"
---
# <a name="apijetdefragment-method"></a><span data-ttu-id="9bd30-103">API. Жетдефрагмент, метод</span><span class="sxs-lookup"><span data-stu-id="9bd30-103">Api.JetDefragment method</span></span>

<span data-ttu-id="9bd30-104">Запускает и останавливает задачи дефрагментации базы данных, которые улучшают организацию данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="9bd30-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="9bd30-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9bd30-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9bd30-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9bd30-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9bd30-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9bd30-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="9bd30-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bd30-108">Parameters</span></span>

  - <span data-ttu-id="9bd30-109">сесид</span><span class="sxs-lookup"><span data-stu-id="9bd30-109">sesid</span></span>  
    <span data-ttu-id="9bd30-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bd30-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9bd30-111">Сеанс, используемый для вызова.</span><span class="sxs-lookup"><span data-stu-id="9bd30-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bd30-112">dbid</span><span class="sxs-lookup"><span data-stu-id="9bd30-112">dbid</span></span>  
    <span data-ttu-id="9bd30-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9bd30-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="9bd30-114">Дефрагментированная база данных.</span><span class="sxs-lookup"><span data-stu-id="9bd30-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bd30-115">tableName</span><span class="sxs-lookup"><span data-stu-id="9bd30-115">tableName</span></span>  
    <span data-ttu-id="9bd30-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9bd30-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9bd30-117">Неиспользуемый параметр.</span><span class="sxs-lookup"><span data-stu-id="9bd30-117">Unused parameter.</span></span> <span data-ttu-id="9bd30-118">Дефрагментация выполняется для всей базы данных, описанной по заданному ИДЕНТИФИКАТОРу базы данных.</span><span class="sxs-lookup"><span data-stu-id="9bd30-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bd30-119">соответствующий</span><span class="sxs-lookup"><span data-stu-id="9bd30-119">passes</span></span>  
    <span data-ttu-id="9bd30-120">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9bd30-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9bd30-121">При запуске задачи дефрагментации в оперативном режиме этот параметр задает максимальное число проходов дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="9bd30-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="9bd30-122">При остановке задачи дефрагментации в оперативном режиме для этого параметра задается количество выполненных проходов.</span><span class="sxs-lookup"><span data-stu-id="9bd30-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bd30-123">секунд</span><span class="sxs-lookup"><span data-stu-id="9bd30-123">seconds</span></span>  
    <span data-ttu-id="9bd30-124">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="9bd30-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="9bd30-125">При запуске задачи дефрагментации в оперативном режиме этот параметр задает максимальное время для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="9bd30-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="9bd30-126">При остановке задачи дефрагментации в оперативном режиме этот выходной буфер задается в течение времени, используемого для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="9bd30-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="9bd30-127">грбит</span><span class="sxs-lookup"><span data-stu-id="9bd30-127">grbit</span></span>  
    <span data-ttu-id="9bd30-128">Тип: [Microsoft. ISAM. ESENT. Interop. дефраггрбит](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9bd30-128">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="9bd30-129">Параметры дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="9bd30-129">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9bd30-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bd30-130">Return value</span></span>

<span data-ttu-id="9bd30-131">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9bd30-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="9bd30-132">Код предупреждения.</span><span class="sxs-lookup"><span data-stu-id="9bd30-132">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9bd30-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bd30-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9bd30-134">Справочник</span><span class="sxs-lookup"><span data-stu-id="9bd30-134">Reference</span></span>

[<span data-ttu-id="9bd30-135">Класс API</span><span class="sxs-lookup"><span data-stu-id="9bd30-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9bd30-136">Члены API</span><span class="sxs-lookup"><span data-stu-id="9bd30-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9bd30-137">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9bd30-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
