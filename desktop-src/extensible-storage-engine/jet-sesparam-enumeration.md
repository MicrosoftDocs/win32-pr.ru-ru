---
description: 'Дополнительные сведения: перечисление JET_sesparam'
title: Перечисление JET_sesparam (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: JET_sesparam enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_sesparam(v=EXCHG.10)
ms:contentKeyID: 55104452
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.Base
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitGenericContext
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam.CommitDefault
- Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5ddfd613eecf5e9a6d9b6cec9eebcbab04e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144251"
---
# <a name="jet_sesparam-enumeration"></a><span data-ttu-id="c04be-103">Перечисление JET_sesparam</span><span class="sxs-lookup"><span data-stu-id="c04be-103">JET_sesparam enumeration</span></span>

<span data-ttu-id="c04be-104">Параметры сеанса ESENT.</span><span class="sxs-lookup"><span data-stu-id="c04be-104">ESENT session parameters.</span></span>

<span data-ttu-id="c04be-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c04be-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="c04be-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c04be-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c04be-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c04be-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_sesparam
'Usage
Dim instance As JET_sesparam
```

``` csharp
public enum JET_sesparam
```

## <a name="members"></a><span data-ttu-id="c04be-108">Члены</span><span class="sxs-lookup"><span data-stu-id="c04be-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c04be-109">Имя участника</span><span class="sxs-lookup"><span data-stu-id="c04be-109">Member name</span></span></th>
<th><span data-ttu-id="c04be-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c04be-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c04be-111">Основной</span><span class="sxs-lookup"><span data-stu-id="c04be-111">Base</span></span></td>
<td><span data-ttu-id="c04be-112">Этот параметр не предназначен для использования.</span><span class="sxs-lookup"><span data-stu-id="c04be-112">This parameter is not meant to be used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c04be-113">коммитдефаулт</span><span class="sxs-lookup"><span data-stu-id="c04be-113">CommitDefault</span></span></td>
<td><span data-ttu-id="c04be-114">Этот параметр задает грбитс для фиксации.</span><span class="sxs-lookup"><span data-stu-id="c04be-114">This parameter sets the grbits for commit.</span></span> <span data-ttu-id="c04be-115">Он функционально аналогичен системному параметру JET_param. Коммитдефаулт при использовании с экземпляром и сесид.</span><span class="sxs-lookup"><span data-stu-id="c04be-115">It is functionally the same as the system parameter JET_param.CommitDefault when used with an instance and a sesid.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c04be-116">коммитженерикконтекст</span><span class="sxs-lookup"><span data-stu-id="c04be-116">CommitGenericContext</span></span></td>
<td><span data-ttu-id="c04be-117">Этот параметр задает пользовательский контекст фиксации, который будет помещен в журнал транзакций при фиксации на уровне 0.</span><span class="sxs-lookup"><span data-stu-id="c04be-117">This parameter sets a user specific commit context that will be placed in the transaction log on commit to level 0.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c04be-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c04be-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c04be-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="c04be-119">Reference</span></span>

[<span data-ttu-id="c04be-120">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="c04be-120">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
