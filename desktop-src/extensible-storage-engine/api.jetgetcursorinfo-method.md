---
description: Дополнительные сведения о методе API. Жетжеткурсоринфо
title: API. Жетжеткурсоринфо, метод
TOCTitle: 'JetGetCursorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcursorinfo(v=EXCHG.10)
ms:contentKeyID: 55100707
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7144283a062b0097d6866e74d1c263bb130c5e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072676"
---
# <a name="apijetgetcursorinfo-method"></a><span data-ttu-id="a0f41-103">API. Жетжеткурсоринфо, метод</span><span class="sxs-lookup"><span data-stu-id="a0f41-103">Api.JetGetCursorInfo method</span></span>

<span data-ttu-id="a0f41-104">Определить, будет ли обновление текущей записи курсора конфликтом записи в зависимости от текущего состояния обновления записи.</span><span class="sxs-lookup"><span data-stu-id="a0f41-104">Determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="a0f41-105">Возможно, конфликт записи будет возвращен, даже если Жетжеткурсоринфо возвращается успешно.</span><span class="sxs-lookup"><span data-stu-id="a0f41-105">It is possible that a write conflict will ultimately be returned even if JetGetCursorInfo returns successfully.</span></span> <span data-ttu-id="a0f41-106">так как другой сеанс может обновить запись, прежде чем текущий сеанс сможет обновить ту же запись.</span><span class="sxs-lookup"><span data-stu-id="a0f41-106">because another session may update the record before the current session is able to update the same record.</span></span>

<span data-ttu-id="a0f41-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a0f41-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a0f41-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a0f41-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f41-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0f41-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCursorInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetGetCursorInfo(sesid, tableid)
```

``` csharp
public static void JetGetCursorInfo(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="a0f41-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0f41-110">Parameters</span></span>

  - <span data-ttu-id="a0f41-111">сесид</span><span class="sxs-lookup"><span data-stu-id="a0f41-111">sesid</span></span>  
    <span data-ttu-id="a0f41-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a0f41-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a0f41-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="a0f41-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a0f41-114">TableID</span><span class="sxs-lookup"><span data-stu-id="a0f41-114">tableid</span></span>  
    <span data-ttu-id="a0f41-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a0f41-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a0f41-116">Курсор для проверки.</span><span class="sxs-lookup"><span data-stu-id="a0f41-116">The cursor to check.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0f41-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0f41-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0f41-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="a0f41-118">Reference</span></span>

[<span data-ttu-id="a0f41-119">Класс API</span><span class="sxs-lookup"><span data-stu-id="a0f41-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a0f41-120">Члены API</span><span class="sxs-lookup"><span data-stu-id="a0f41-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a0f41-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a0f41-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
