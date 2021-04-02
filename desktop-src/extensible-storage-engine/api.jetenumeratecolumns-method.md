---
description: Дополнительные сведения о методе API. Жетенумератеколумнс
title: API. Жетенумератеколумнс, метод
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072678"
---
# <a name="apijetenumeratecolumns-method"></a><span data-ttu-id="352c7-103">API. Жетенумератеколумнс, метод</span><span class="sxs-lookup"><span data-stu-id="352c7-103">Api.JetEnumerateColumns method</span></span>

<span data-ttu-id="352c7-104">Эффективно извлекает набор столбцов и их значений из текущей записи курсора или буфера копирования этого курсора.</span><span class="sxs-lookup"><span data-stu-id="352c7-104">Efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="352c7-105">Возвращаемые столбцы и значения могут быть ограничены списком идентификаторов столбцов, Итагсекуенце числами и другими характеристиками.</span><span class="sxs-lookup"><span data-stu-id="352c7-105">The columns and values retrieved can be restricted by a list of column IDs, itagSequence numbers, and other characteristics.</span></span> <span data-ttu-id="352c7-106">Этот интерфейс API извлечения столбца уникален в том, что он возвращает сведения в динамически выделяемой памяти, получаемой с помощью предоставленного пользователем обратного вызова, совместимого с переопределением.</span><span class="sxs-lookup"><span data-stu-id="352c7-106">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided realloc compatible callback.</span></span> <span data-ttu-id="352c7-107">Эта новая гибкость позволяет эффективно получать данные столбцов с определенными характеристиками (например, размер и количество элементов), неизвестных вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="352c7-107">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="352c7-108">Это устраняет необходимость использования режимов обнаружения Жетретриевеколумн для определения этих характеристик, чтобы настроить окончательный вызов Жетретриевеколумн, который будет успешно получать нужные данные.</span><span class="sxs-lookup"><span data-stu-id="352c7-108">This eliminates the need for the use of the discovery modes of JetRetrieveColumn to determine those characteristics in order to setup a final call to JetRetrieveColumn that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="352c7-109">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="352c7-109">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="352c7-110">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="352c7-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="352c7-111">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="352c7-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="352c7-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="352c7-112">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="352c7-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="352c7-113">Parameters</span></span>

  - <span data-ttu-id="352c7-114">сесид</span><span class="sxs-lookup"><span data-stu-id="352c7-114">sesid</span></span>  
    <span data-ttu-id="352c7-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="352c7-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="352c7-116">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="352c7-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="352c7-117">TableID</span><span class="sxs-lookup"><span data-stu-id="352c7-117">tableid</span></span>  
    <span data-ttu-id="352c7-118">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="352c7-118">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="352c7-119">Курсор, из которого извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="352c7-119">The cursor to retrieve data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="352c7-120">нумколумнидс</span><span class="sxs-lookup"><span data-stu-id="352c7-120">numColumnids</span></span>  
    <span data-ttu-id="352c7-121">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="352c7-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="352c7-122">Число JET_ENUMCOLUMNIDS.</span><span class="sxs-lookup"><span data-stu-id="352c7-122">The numbers of JET_ENUMCOLUMNIDS.</span></span>

<!-- end list -->

  - <span data-ttu-id="352c7-123">колумнидс</span><span class="sxs-lookup"><span data-stu-id="352c7-123">columnids</span></span>  
    <span data-ttu-id="352c7-124">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="352c7-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="352c7-125">Необязательный массив идентификаторов столбцов, каждый из которых имеет необязательный массив чисел Итагсекуенце для перечисления.</span><span class="sxs-lookup"><span data-stu-id="352c7-125">An optional array of column IDs, each with an optional array of itagSequence numbers to enumerate.</span></span>

<!-- end list -->

  - <span data-ttu-id="352c7-126">нумколумнвалуес</span><span class="sxs-lookup"><span data-stu-id="352c7-126">numColumnValues</span></span>  
    <span data-ttu-id="352c7-127">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="352c7-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="352c7-128">Возвращает число извлеченных значений столбцов.</span><span class="sxs-lookup"><span data-stu-id="352c7-128">Returns the number of column values retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="352c7-129">колумнвалуес</span><span class="sxs-lookup"><span data-stu-id="352c7-129">columnValues</span></span>  
    <span data-ttu-id="352c7-130">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="352c7-130">Type: \[\]</span></span>  
    
    <span data-ttu-id="352c7-131">Возвращает перечисляемые значения столбцов.</span><span class="sxs-lookup"><span data-stu-id="352c7-131">Returns the enumerated column values.</span></span>

<!-- end list -->

  - <span data-ttu-id="352c7-132">allocator</span><span class="sxs-lookup"><span data-stu-id="352c7-132">allocator</span></span>  
    <span data-ttu-id="352c7-133">Тип: [Microsoft.ISAM.ESENT.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="352c7-133">Type: [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span></span>  
    
    <span data-ttu-id="352c7-134">Обратный вызов, используемый для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="352c7-134">Callback used to allocate memory.</span></span>

<!-- end list -->

  - <span data-ttu-id="352c7-135">аллокаторконтекст</span><span class="sxs-lookup"><span data-stu-id="352c7-135">allocatorContext</span></span>  
    <span data-ttu-id="352c7-136">Тип: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="352c7-136">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="352c7-137">Контекст для обратного вызова выделения.</span><span class="sxs-lookup"><span data-stu-id="352c7-137">Context for the allocation callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="352c7-138">максдатасизе</span><span class="sxs-lookup"><span data-stu-id="352c7-138">maxDataSize</span></span>  
    <span data-ttu-id="352c7-139">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="352c7-139">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="352c7-140">Устанавливает ограничение на объем данных, возвращаемых из длинного текстового или длинного двоичного столбца.</span><span class="sxs-lookup"><span data-stu-id="352c7-140">Sets a cap on the amount of data to return from a long text or long binary column.</span></span> <span data-ttu-id="352c7-141">Этот параметр можно использовать, чтобы предотвратить перечисление слишком большого значения столбца.</span><span class="sxs-lookup"><span data-stu-id="352c7-141">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span>

<!-- end list -->

  - <span data-ttu-id="352c7-142">грбит</span><span class="sxs-lookup"><span data-stu-id="352c7-142">grbit</span></span>  
    <span data-ttu-id="352c7-143">Тип: [Microsoft. ISAM. ESENT. Interop. енумератеколумнсгрбит](./enumeratecolumnsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="352c7-143">Type: [Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="352c7-144">Получение параметров.</span><span class="sxs-lookup"><span data-stu-id="352c7-144">Retrieve options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="352c7-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="352c7-145">Return value</span></span>

<span data-ttu-id="352c7-146">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="352c7-146">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="352c7-147">Предупреждение или успешное завершение.</span><span class="sxs-lookup"><span data-stu-id="352c7-147">A warning or success.</span></span>  

## <a name="see-also"></a><span data-ttu-id="352c7-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="352c7-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="352c7-149">Справочник</span><span class="sxs-lookup"><span data-stu-id="352c7-149">Reference</span></span>

[<span data-ttu-id="352c7-150">Класс API</span><span class="sxs-lookup"><span data-stu-id="352c7-150">Api class</span></span>](./api-class.md)

[<span data-ttu-id="352c7-151">Члены API</span><span class="sxs-lookup"><span data-stu-id="352c7-151">Api members</span></span>](./api-members.md)

[<span data-ttu-id="352c7-152">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="352c7-152">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
