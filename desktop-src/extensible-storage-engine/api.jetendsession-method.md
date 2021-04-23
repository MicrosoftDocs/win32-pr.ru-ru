---
description: Дополнительные сведения о методе API. Жетендсессион
title: API. Жетендсессион, метод
TOCTitle: 'JetEndSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.EndSessionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendsession(v=EXCHG.10)
ms:contentKeyID: 55100690
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10412f6b01b14d63557bf024d65975c271bbe31b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540858"
---
# <a name="apijetendsession-method"></a><span data-ttu-id="1dffe-103">API. Жетендсессион, метод</span><span class="sxs-lookup"><span data-stu-id="1dffe-103">Api.JetEndSession method</span></span>

<span data-ttu-id="1dffe-104">Завершает сеанс.</span><span class="sxs-lookup"><span data-stu-id="1dffe-104">Ends a session.</span></span>

<span data-ttu-id="1dffe-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1dffe-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1dffe-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1dffe-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1dffe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dffe-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndSession ( _
    sesid As JET_SESID, _
    grbit As EndSessionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As EndSessionGrbitApi.JetEndSession(sesid, grbit)
```

``` csharp
public static void JetEndSession(
    JET_SESID sesid,
    EndSessionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1dffe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1dffe-108">Parameters</span></span>

  - <span data-ttu-id="1dffe-109">сесид</span><span class="sxs-lookup"><span data-stu-id="1dffe-109">sesid</span></span>  
    <span data-ttu-id="1dffe-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1dffe-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1dffe-111">Сеанс, который необходимо завершить.</span><span class="sxs-lookup"><span data-stu-id="1dffe-111">The session to end.</span></span>

<!-- end list -->

  - <span data-ttu-id="1dffe-112">грбит</span><span class="sxs-lookup"><span data-stu-id="1dffe-112">grbit</span></span>  
    <span data-ttu-id="1dffe-113">Тип: [Microsoft. ISAM. ESENT. Interop. ендсессионгрбит](./endsessiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1dffe-113">Type: [Microsoft.Isam.Esent.Interop.EndSessionGrbit](./endsessiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1dffe-114">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="1dffe-114">This parameter is not used.</span></span>

## <a name="see-also"></a><span data-ttu-id="1dffe-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1dffe-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1dffe-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="1dffe-116">Reference</span></span>

[<span data-ttu-id="1dffe-117">Класс API</span><span class="sxs-lookup"><span data-stu-id="1dffe-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1dffe-118">Члены API</span><span class="sxs-lookup"><span data-stu-id="1dffe-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1dffe-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1dffe-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
