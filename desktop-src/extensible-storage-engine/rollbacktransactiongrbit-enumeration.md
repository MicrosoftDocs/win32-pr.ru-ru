---
description: Дополнительные сведения о перечислении Роллбакктрансактионгрбит
title: Перечисление Роллбакктрансактионгрбит
TOCTitle: RollbackTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.rollbacktransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39513584
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf2635d94070fc47bebbd6cdd0e53deddeb4c5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683580"
---
# <a name="rollbacktransactiongrbit-enumeration"></a><span data-ttu-id="37d57-103">Перечисление Роллбакктрансактионгрбит</span><span class="sxs-lookup"><span data-stu-id="37d57-103">RollbackTransactionGrbit enumeration</span></span>

<span data-ttu-id="37d57-104">Параметры для Жетроллбакктрансактион.</span><span class="sxs-lookup"><span data-stu-id="37d57-104">Options for JetRollbackTransaction.</span></span>

<span data-ttu-id="37d57-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="37d57-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="37d57-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="37d57-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="37d57-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="37d57-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="37d57-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37d57-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RollbackTransactionGrbit
'Usage
Dim instance As RollbackTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum RollbackTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="37d57-109">Члены</span><span class="sxs-lookup"><span data-stu-id="37d57-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="37d57-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="37d57-110">Member name</span></span></th>
<th><span data-ttu-id="37d57-111">Описание</span><span class="sxs-lookup"><span data-stu-id="37d57-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="37d57-112">Нет</span><span class="sxs-lookup"><span data-stu-id="37d57-112">None</span></span></td>
<td><span data-ttu-id="37d57-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="37d57-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="37d57-114">роллбаккалл</span><span class="sxs-lookup"><span data-stu-id="37d57-114">RollbackAll</span></span></td>
<td><span data-ttu-id="37d57-115">Этот параметр запрашивает отмену всех изменений, внесенных в состояние базы данных во время всех точек сохранения.</span><span class="sxs-lookup"><span data-stu-id="37d57-115">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="37d57-116">В результате сеанс выполнит выход из транзакции.</span><span class="sxs-lookup"><span data-stu-id="37d57-116">As a result, the session will exit the transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="37d57-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37d57-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="37d57-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="37d57-118">Reference</span></span>

[<span data-ttu-id="37d57-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="37d57-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
