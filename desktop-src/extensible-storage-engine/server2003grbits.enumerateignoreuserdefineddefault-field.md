---
description: 'Дополнительные сведения о: Server2003Grbits. Енумератеигнореусердефинеддефаулт поле'
title: Поле Server2003Grbits. Енумератеигнореусердефинеддефаулт (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: EnumerateIgnoreUserDefinedDefault field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.enumerateignoreuserdefineddefault(v=EXCHG.10)
ms:contentKeyID: 55104099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 508565c518b67d31b0299014817b669f9484f743
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702345"
---
# <a name="server2003grbitsenumerateignoreuserdefineddefault-field"></a><span data-ttu-id="72d72-103">Server2003Grbits. Енумератеигнореусердефинеддефаулт, поле</span><span class="sxs-lookup"><span data-stu-id="72d72-103">Server2003Grbits.EnumerateIgnoreUserDefinedDefault field</span></span>

<span data-ttu-id="72d72-104">Если данный столбец отсутствует в записи и имеет определенное пользователем значение по умолчанию, значение столбца не будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="72d72-104">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="72d72-105">Этот параметр предотвратит вызов функции обратного вызова, которая будет вычислять определенное пользователем значение по умолчанию для столбца, при перечислении значений для этого столбца.</span><span class="sxs-lookup"><span data-stu-id="72d72-105">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span>

<span data-ttu-id="72d72-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="72d72-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="72d72-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="72d72-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="72d72-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72d72-108">Syntax</span></span>

``` vb
'Declaration
Public Const EnumerateIgnoreUserDefinedDefault As EnumerateColumnsGrbit
'Usage
Dim value As EnumerateColumnsGrbit

value = Server2003Grbits.EnumerateIgnoreUserDefinedDefault
```

``` csharp
public const EnumerateColumnsGrbit EnumerateIgnoreUserDefinedDefault
```

## <a name="remarks"></a><span data-ttu-id="72d72-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="72d72-109">Remarks</span></span>

<span data-ttu-id="72d72-110">Этот параметр доступен только для операционных систем Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="72d72-110">This option is only available for Windows Server 2003 SP1 and later operating systems.</span></span>

## <a name="see-also"></a><span data-ttu-id="72d72-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72d72-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="72d72-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="72d72-112">Reference</span></span>

[<span data-ttu-id="72d72-113">Класс Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="72d72-113">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="72d72-114">Элементы Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="72d72-114">Server2003Grbits members</span></span>](./server2003grbits-members.md)

[<span data-ttu-id="72d72-115">Пространство имен Microsoft. ISAM. ESENT. Interop. server2003</span><span class="sxs-lookup"><span data-stu-id="72d72-115">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
