---
description: Дополнительные сведения о методе API. JetDefragment2
title: API. JetDefragment2, метод
TOCTitle: 'JetDefragment2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.JET_CALLBACK,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment2(v=EXCHG.10)
ms:contentKeyID: 55100696
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b22c89b304103954a2088bf05ba98797777489be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710954"
---
# <a name="apijetdefragment2-method"></a><span data-ttu-id="4660c-103">API. JetDefragment2, метод</span><span class="sxs-lookup"><span data-stu-id="4660c-103">Api.JetDefragment2 method</span></span>

<span data-ttu-id="4660c-104">Запускает и останавливает задачи дефрагментации базы данных, которые улучшают организацию данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="4660c-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="4660c-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4660c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4660c-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4660c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4660c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4660c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment2 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    callback As JET_CALLBACK, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim callback As JET_CALLBACK
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment2(sesid, _
    dbid, tableName, passes, seconds, _
    callback, grbit)
```

``` csharp
public static JET_wrn JetDefragment2(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    JET_CALLBACK callback,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="4660c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4660c-108">Parameters</span></span>

  - <span data-ttu-id="4660c-109">сесид</span><span class="sxs-lookup"><span data-stu-id="4660c-109">sesid</span></span>  
    <span data-ttu-id="4660c-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4660c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4660c-111">Сеанс, используемый для вызова.</span><span class="sxs-lookup"><span data-stu-id="4660c-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="4660c-112">dbid</span><span class="sxs-lookup"><span data-stu-id="4660c-112">dbid</span></span>  
    <span data-ttu-id="4660c-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4660c-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="4660c-114">Дефрагментированная база данных.</span><span class="sxs-lookup"><span data-stu-id="4660c-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="4660c-115">tableName</span><span class="sxs-lookup"><span data-stu-id="4660c-115">tableName</span></span>  
    <span data-ttu-id="4660c-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4660c-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4660c-117">Неиспользуемый параметр.</span><span class="sxs-lookup"><span data-stu-id="4660c-117">Unused parameter.</span></span> <span data-ttu-id="4660c-118">Дефрагментация выполняется для всей базы данных, описанной по заданному ИДЕНТИФИКАТОРу базы данных.</span><span class="sxs-lookup"><span data-stu-id="4660c-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="4660c-119">соответствующий</span><span class="sxs-lookup"><span data-stu-id="4660c-119">passes</span></span>  
    <span data-ttu-id="4660c-120">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4660c-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4660c-121">При запуске задачи дефрагментации в оперативном режиме этот параметр задает максимальное число проходов дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="4660c-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="4660c-122">При остановке задачи дефрагментации в оперативном режиме для этого параметра задается количество выполненных проходов.</span><span class="sxs-lookup"><span data-stu-id="4660c-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="4660c-123">секунд</span><span class="sxs-lookup"><span data-stu-id="4660c-123">seconds</span></span>  
    <span data-ttu-id="4660c-124">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4660c-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4660c-125">При запуске задачи дефрагментации в оперативном режиме этот параметр задает максимальное время для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="4660c-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="4660c-126">При остановке задачи дефрагментации в оперативном режиме этот выходной буфер задается в течение времени, используемого для дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="4660c-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="4660c-127">обратный вызов</span><span class="sxs-lookup"><span data-stu-id="4660c-127">callback</span></span>  
    <span data-ttu-id="4660c-128">Тип: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="4660c-128">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="4660c-129">Функция обратного вызова, используемая для отчета о ходе выполнения в дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="4660c-129">Callback function that defrag uses to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="4660c-130">грбит</span><span class="sxs-lookup"><span data-stu-id="4660c-130">grbit</span></span>  
    <span data-ttu-id="4660c-131">Тип: [Microsoft. ISAM. ESENT. Interop. дефраггрбит](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4660c-131">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4660c-132">Параметры дефрагментации.</span><span class="sxs-lookup"><span data-stu-id="4660c-132">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4660c-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4660c-133">Return value</span></span>

<span data-ttu-id="4660c-134">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4660c-134">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="4660c-135">Код предупреждения.</span><span class="sxs-lookup"><span data-stu-id="4660c-135">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="4660c-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4660c-136">Remarks</span></span>

<span data-ttu-id="4660c-137">Обратный вызов, передаваемый в JetDefragment2, может выполняться асинхронно.</span><span class="sxs-lookup"><span data-stu-id="4660c-137">The callback passed to JetDefragment2 can be executed asynchronously.</span></span> <span data-ttu-id="4660c-138">Сборщик мусора не знает, что неуправляемый код имеет ссылку на обратный вызов, поэтому важно убедиться, что обратный вызов не собирается.</span><span class="sxs-lookup"><span data-stu-id="4660c-138">The GC doesn't know that the unmanaged code has a reference to the callback so it is important to make sure the callback isn't collected.</span></span>

## <a name="see-also"></a><span data-ttu-id="4660c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4660c-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4660c-140">Справочник</span><span class="sxs-lookup"><span data-stu-id="4660c-140">Reference</span></span>

[<span data-ttu-id="4660c-141">Класс API</span><span class="sxs-lookup"><span data-stu-id="4660c-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4660c-142">Члены API</span><span class="sxs-lookup"><span data-stu-id="4660c-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4660c-143">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4660c-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
