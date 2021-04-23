---
description: 'Дополнительные сведения: перечисление JET_cbtyp'
title: Перечисление JET_cbtyp
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d2e545fea9c1942dc09df82eb93eafa1d3e4e89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673405"
---
# <a name="jet_cbtyp-enumeration"></a><span data-ttu-id="647fd-103">Перечисление JET_cbtyp</span><span class="sxs-lookup"><span data-stu-id="647fd-103">JET_cbtyp enumeration</span></span>

<span data-ttu-id="647fd-104">Тип отчета о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="647fd-104">Type of progress being reported.</span></span>

<span data-ttu-id="647fd-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="647fd-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="647fd-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="647fd-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="647fd-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="647fd-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="647fd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="647fd-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
```

## <a name="members"></a><span data-ttu-id="647fd-109">Члены</span><span class="sxs-lookup"><span data-stu-id="647fd-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="647fd-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="647fd-110">Member name</span></span></th>
<th><span data-ttu-id="647fd-111">Описание</span><span class="sxs-lookup"><span data-stu-id="647fd-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="647fd-112">NULL</span><span class="sxs-lookup"><span data-stu-id="647fd-112">Null</span></span></td>
<td><span data-ttu-id="647fd-113">Этот обратный вызов зарезервирован и всегда считается недопустимым.</span><span class="sxs-lookup"><span data-stu-id="647fd-113">This callback is reserved and always considered invalid.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="647fd-114">Завершение</span><span class="sxs-lookup"><span data-stu-id="647fd-114">Finalize</span></span></td>
<td><span data-ttu-id="647fd-115">Заключительный столбец имеет нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="647fd-115">A finalizable column has gone to zero.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="647fd-116">бефореинсерт</span><span class="sxs-lookup"><span data-stu-id="647fd-116">BeforeInsert</span></span></td>
<td><span data-ttu-id="647fd-117">Этот обратный вызов выполняется непосредственно перед вставкой новой записи в таблицу с помощью вызова Жетупдате.</span><span class="sxs-lookup"><span data-stu-id="647fd-117">This callback will occur just before a new record is inserted into a table by a call to JetUpdate.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="647fd-118">афтеринсерт</span><span class="sxs-lookup"><span data-stu-id="647fd-118">AfterInsert</span></span></td>
<td><span data-ttu-id="647fd-119">Этот обратный вызов выполняется сразу после вставки новой записи в таблицу с помощью вызова Жетупдате, но до возврата Жетупдате.</span><span class="sxs-lookup"><span data-stu-id="647fd-119">This callback will occur just after a new record has been inserted into a table by a call to JetUpdate but before JetUpdate returns.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="647fd-120">бефоререплаце</span><span class="sxs-lookup"><span data-stu-id="647fd-120">BeforeReplace</span></span></td>
<td><span data-ttu-id="647fd-121">Этот обратный вызов выполняется непосредственно перед существующей записью в таблице, измененной с помощью вызова Жетупдате.</span><span class="sxs-lookup"><span data-stu-id="647fd-121">This callback will occur just prior to an existing record in a table being changed by a call to JetUpdate.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="647fd-122">афтерреплаце</span><span class="sxs-lookup"><span data-stu-id="647fd-122">AfterReplace</span></span></td>
<td><span data-ttu-id="647fd-123">Этот обратный вызов выполняется сразу после изменения существующей записи в таблице с помощью вызова Жетупдате, но до Жетупдате возврата.</span><span class="sxs-lookup"><span data-stu-id="647fd-123">This callback will occur just after an existing record in a table has been changed by a call to JetUpdate but prior to JetUpdate returning.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="647fd-124">BeforeDelete</span><span class="sxs-lookup"><span data-stu-id="647fd-124">BeforeDelete</span></span></td>
<td><span data-ttu-id="647fd-125">Этот обратный вызов выполняется непосредственно перед удалением существующей записи в таблице путем вызова Жетделете.</span><span class="sxs-lookup"><span data-stu-id="647fd-125">This callback will occur just before an existing record in a table is deleted by a call to JetDelete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="647fd-126">афтерделете</span><span class="sxs-lookup"><span data-stu-id="647fd-126">AfterDelete</span></span></td>
<td><span data-ttu-id="647fd-127">Этот обратный вызов выполняется сразу после удаления существующей записи в таблице путем вызова Жетделете.</span><span class="sxs-lookup"><span data-stu-id="647fd-127">This callback will occur just after an existing record in a table is deleted by a call to JetDelete.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="647fd-128">усердефинеддефаултвалуе</span><span class="sxs-lookup"><span data-stu-id="647fd-128">UserDefinedDefaultValue</span></span></td>
<td><span data-ttu-id="647fd-129">Этот обратный вызов выполняется, когда подсистеме требуется получить определенное пользователем значение столбца из приложения.</span><span class="sxs-lookup"><span data-stu-id="647fd-129">This callback will occur when the engine needs to retrieve the user defined default value of a column from the application.</span></span> <span data-ttu-id="647fd-130">Этот обратный вызов по сути является ограниченной реализацией Жетретриевеколумн, которая оценивается приложением.</span><span class="sxs-lookup"><span data-stu-id="647fd-130">This callback is essentially a limited implementation of JetRetrieveColumn that is evaluated by the application.</span></span> <span data-ttu-id="647fd-131">Для определяемого пользователем значения по умолчанию может быть возвращено не более одного значения столбца.</span><span class="sxs-lookup"><span data-stu-id="647fd-131">A maximum of one column value can be returned for a user defined default value.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="647fd-132">онлинедефрагкомплетед</span><span class="sxs-lookup"><span data-stu-id="647fd-132">OnlineDefragCompleted</span></span></td>
<td><span data-ttu-id="647fd-133">Этот обратный вызов происходит, когда оперативная дефрагментация базы данных, инициированной Жетдефрагмент, была остановлена из-за завершения процесса или превышения предельного значения времени.</span><span class="sxs-lookup"><span data-stu-id="647fd-133">This callback will occur when the online defragmentation of a database as initiated by JetDefragment has stopped due to either the process being completed or the time limit being reached.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="647fd-134">фрикурсорлс</span><span class="sxs-lookup"><span data-stu-id="647fd-134">FreeCursorLS</span></span></td>
<td><span data-ttu-id="647fd-135">Этот обратный вызов происходит, когда приложению необходимо очистить контекстный обработчик для локального хранилища, связанного с курсором, который освобождается ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="647fd-135">This callback will occur when the application needs to clean up the context handle for the Local Storage associated with a cursor that is being released by the database engine.</span></span> <span data-ttu-id="647fd-136">Дополнительные сведения см. в разделе Жетсетлс.</span><span class="sxs-lookup"><span data-stu-id="647fd-136">For more information, see JetSetLS.</span></span> <span data-ttu-id="647fd-137">Делегат для этой причины обратного вызова настраивается средствами Жетсетсистемпараметер с JET_paramRuntimeCallback.</span><span class="sxs-lookup"><span data-stu-id="647fd-137">The delegate for this callback reason is configured by means of JetSetSystemParameter with JET_paramRuntimeCallback.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="647fd-138">фритаблелс</span><span class="sxs-lookup"><span data-stu-id="647fd-138">FreeTableLS</span></span></td>
<td><span data-ttu-id="647fd-139">Этот обратный вызов будет выполняться в результате необходимости в приложении очистить контекстный обработчик для локального хранилища, связанного с таблицей, которая освобождается ядром СУБД.</span><span class="sxs-lookup"><span data-stu-id="647fd-139">This callback will occur as the result of the need for the application to cleanup the context handle for the Local Storage associated with a table that is being released by the database engine.</span></span> <span data-ttu-id="647fd-140">Дополнительные сведения см. в разделе Жетсетлс.</span><span class="sxs-lookup"><span data-stu-id="647fd-140">For more information, see JetSetLS.</span></span> <span data-ttu-id="647fd-141">Делегат для этой причины обратного вызова настраивается средствами Жетсетсистемпараметер с JET_paramRuntimeCallback.</span><span class="sxs-lookup"><span data-stu-id="647fd-141">The delegate for this callback reason is configured by means of JetSetSystemParameter with JET_paramRuntimeCallback.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="647fd-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="647fd-142">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="647fd-143">Справочник</span><span class="sxs-lookup"><span data-stu-id="647fd-143">Reference</span></span>

[<span data-ttu-id="647fd-144">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="647fd-144">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
