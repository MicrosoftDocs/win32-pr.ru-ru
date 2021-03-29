---
description: 'Дополнительные сведения о: Server2003Param. Алтернатедатабасерековерипас поле'
title: Поле Server2003Param. Алтернатедатабасерековерипас (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: AlternateDatabaseRecoveryPath field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003param.alternatedatabaserecoverypath(v=EXCHG.10)
ms:contentKeyID: 55104217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 770ac27596b4385d0012cb65847754b4deb7e9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647209"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a><span data-ttu-id="a6e08-103">Server2003Param. Алтернатедатабасерековерипас, поле</span><span class="sxs-lookup"><span data-stu-id="a6e08-103">Server2003Param.AlternateDatabaseRecoveryPath field</span></span>

<span data-ttu-id="a6e08-104">Полный путь к каждой базе данных сохраняется в журналах транзакций во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a6e08-104">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="a6e08-105">Обычно эти базы данных должны оставаться в исходном расположении для правильной работы воспроизведения транзакций.</span><span class="sxs-lookup"><span data-stu-id="a6e08-105">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="a6e08-106">Этот параметр можно использовать для принудительного восстановления после сбоя или операции восстановления, чтобы найти базы данных, упоминаемые в журнале транзакций в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="a6e08-106">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<span data-ttu-id="a6e08-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a6e08-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="a6e08-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a6e08-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a6e08-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6e08-109">Syntax</span></span>

``` vb
'Declaration
Public Const AlternateDatabaseRecoveryPath As JET_param
'Usage
Dim value As JET_param

value = Server2003Param.AlternateDatabaseRecoveryPath
```

``` csharp
public const JET_param AlternateDatabaseRecoveryPath
```

## <a name="see-also"></a><span data-ttu-id="a6e08-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6e08-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a6e08-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="a6e08-111">Reference</span></span>

[<span data-ttu-id="a6e08-112">Класс Server2003Param</span><span class="sxs-lookup"><span data-stu-id="a6e08-112">Server2003Param class</span></span>](./server2003param-class.md)

[<span data-ttu-id="a6e08-113">Элементы Server2003Param</span><span class="sxs-lookup"><span data-stu-id="a6e08-113">Server2003Param members</span></span>](./server2003param-members.md)

[<span data-ttu-id="a6e08-114">Пространство имен Microsoft. ISAM. ESENT. Interop. server2003</span><span class="sxs-lookup"><span data-stu-id="a6e08-114">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
