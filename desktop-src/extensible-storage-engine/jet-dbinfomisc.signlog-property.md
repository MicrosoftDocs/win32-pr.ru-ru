---
description: 'Дополнительные сведения о свойстве: JET_DBINFOMISC. Сигнлог'
title: Свойство JET_DBINFOMISC. Сигнлог
TOCTitle: 'signLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.signlog(v=EXCHG.10)
ms:contentKeyID: 39511875
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.signLog
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_signLog
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_signLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d75fed42b966cafe159f224667d0d30a85cc1a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143621"
---
# <a name="jet_dbinfomiscsignlog-property"></a><span data-ttu-id="8f8f3-103">Свойство JET_DBINFOMISC. Сигнлог</span><span class="sxs-lookup"><span data-stu-id="8f8f3-103">JET_DBINFOMISC.signLog property</span></span>

<span data-ttu-id="8f8f3-104">Возвращает подпись файла журнала, используемого для изменения базы данных.</span><span class="sxs-lookup"><span data-stu-id="8f8f3-104">Gets the logfile signature of logs used to modify the database.</span></span>

<span data-ttu-id="8f8f3-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8f8f3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8f8f3-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8f8f3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8f8f3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8f8f3-107">Syntax</span></span>

``` vb
'Declaration
Public Property signLog As JET_SIGNATURE
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_SIGNATURE

value = instance.signLog
```

``` csharp
public JET_SIGNATURE signLog { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="8f8f3-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8f8f3-108">Property value</span></span>

<span data-ttu-id="8f8f3-109">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="8f8f3-109">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8f8f3-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8f8f3-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8f8f3-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="8f8f3-111">Reference</span></span>

[<span data-ttu-id="8f8f3-112">Класс JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="8f8f3-112">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="8f8f3-113">Элементы JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="8f8f3-113">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="8f8f3-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8f8f3-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
