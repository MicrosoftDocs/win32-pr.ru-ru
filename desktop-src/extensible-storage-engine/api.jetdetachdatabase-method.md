---
description: Дополнительные сведения о методе API. Жетдетачдатабасе
title: API. Жетдетачдатабасе, метод
TOCTitle: 'JetDetachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100687
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8881021d619bac1dae83a4a001e6b88e94e57256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662251"
---
# <a name="apijetdetachdatabase-method"></a><span data-ttu-id="651cc-103">API. Жетдетачдатабасе, метод</span><span class="sxs-lookup"><span data-stu-id="651cc-103">Api.JetDetachDatabase method</span></span>

<span data-ttu-id="651cc-104">Освобождает файл базы данных, который был ранее присоединен к сеансу базы данных.</span><span class="sxs-lookup"><span data-stu-id="651cc-104">Releases a database file that was previously attached to a database session.</span></span>

<span data-ttu-id="651cc-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="651cc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="651cc-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="651cc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="651cc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="651cc-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDetachDatabase ( _
    sesid As JET_SESID, _
    database As String _
)
'Usage
Dim sesid As JET_SESID
Dim database As StringApi.JetDetachDatabase(sesid, database)
```

``` csharp
public static void JetDetachDatabase(
    JET_SESID sesid,
    string database
)
```

#### <a name="parameters"></a><span data-ttu-id="651cc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="651cc-108">Parameters</span></span>

  - <span data-ttu-id="651cc-109">сесид</span><span class="sxs-lookup"><span data-stu-id="651cc-109">sesid</span></span>  
    <span data-ttu-id="651cc-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="651cc-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="651cc-111">Используемый сеанс базы данных.</span><span class="sxs-lookup"><span data-stu-id="651cc-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="651cc-112">База данных</span><span class="sxs-lookup"><span data-stu-id="651cc-112">database</span></span>  
    <span data-ttu-id="651cc-113">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="651cc-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="651cc-114">База данных для отсоединения.</span><span class="sxs-lookup"><span data-stu-id="651cc-114">The database to detach.</span></span>

## <a name="see-also"></a><span data-ttu-id="651cc-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="651cc-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="651cc-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="651cc-116">Reference</span></span>

[<span data-ttu-id="651cc-117">Класс API</span><span class="sxs-lookup"><span data-stu-id="651cc-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="651cc-118">Члены API</span><span class="sxs-lookup"><span data-stu-id="651cc-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="651cc-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="651cc-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
