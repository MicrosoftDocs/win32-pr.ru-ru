---
description: Дополнительные сведения о методе API. Жетдупсессион
title: API. Жетдупсессион, метод
TOCTitle: 'JetDupSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupsession(v=EXCHG.10)
ms:contentKeyID: 55100689
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupSession
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9013c3c99c1d6c6067386038ec4a51f37f978650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144341"
---
# <a name="apijetdupsession-method"></a><span data-ttu-id="b5c4a-103">API. Жетдупсессион, метод</span><span class="sxs-lookup"><span data-stu-id="b5c4a-103">Api.JetDupSession method</span></span>

<span data-ttu-id="b5c4a-104">Инициализируйте новый сеанс ESE в том же экземпляре, что и заданный сесид.</span><span class="sxs-lookup"><span data-stu-id="b5c4a-104">Initialize a new ESE session in the same instance as the given sesid.</span></span>

<span data-ttu-id="b5c4a-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b5c4a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b5c4a-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b5c4a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c4a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5c4a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDupSession ( _
    sesid As JET_SESID, _
    <OutAttribute> ByRef newSesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESID
Dim newSesid As JET_SESIDApi.JetDupSession(sesid, newSesid)
```

``` csharp
public static void JetDupSession(
    JET_SESID sesid,
    out JET_SESID newSesid
)
```

#### <a name="parameters"></a><span data-ttu-id="b5c4a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5c4a-108">Parameters</span></span>

  - <span data-ttu-id="b5c4a-109">сесид</span><span class="sxs-lookup"><span data-stu-id="b5c4a-109">sesid</span></span>  
    <span data-ttu-id="b5c4a-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b5c4a-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b5c4a-111">Сеанс для дублирования.</span><span class="sxs-lookup"><span data-stu-id="b5c4a-111">The session to duplicate.</span></span>

<!-- end list -->

  - <span data-ttu-id="b5c4a-112">невсесид</span><span class="sxs-lookup"><span data-stu-id="b5c4a-112">newSesid</span></span>  
    <span data-ttu-id="b5c4a-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b5c4a-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b5c4a-114">Возвращает новый сеанс.</span><span class="sxs-lookup"><span data-stu-id="b5c4a-114">Returns the new session.</span></span>

## <a name="see-also"></a><span data-ttu-id="b5c4a-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5c4a-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b5c4a-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="b5c4a-116">Reference</span></span>

[<span data-ttu-id="b5c4a-117">Класс API</span><span class="sxs-lookup"><span data-stu-id="b5c4a-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b5c4a-118">Члены API</span><span class="sxs-lookup"><span data-stu-id="b5c4a-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b5c4a-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b5c4a-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
