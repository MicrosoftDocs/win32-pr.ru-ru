---
description: Дополнительные сведения о методе API. Жетресеттаблесекуентиал
title: API. Жетресеттаблесекуентиал, метод
TOCTitle: 'JetResetTableSequential method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetresettablesequential(v=EXCHG.10)
ms:contentKeyID: 55100789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetResetTableSequential
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b45ca118894015df7cda56201733cdaad9b88d69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272538"
---
# <a name="apijetresettablesequential-method"></a><span data-ttu-id="db3ea-103">API. Жетресеттаблесекуентиал, метод</span><span class="sxs-lookup"><span data-stu-id="db3ea-103">Api.JetResetTableSequential method</span></span>

<span data-ttu-id="db3ea-104">Уведомляет ядро СУБД о том, что приложение больше не просматривает весь индекс, на котором расположен курсор.</span><span class="sxs-lookup"><span data-stu-id="db3ea-104">Notifies the database engine that the application is no longer scanning the entire index the cursor is positioned on.</span></span> <span data-ttu-id="db3ea-105">Этот вызов обращается к отправке уведомления, отправленного [жетсеттаблесекуентиал (JET_SESID, JET_TABLEID, сеттаблесекуентиалгрбит)](./api.jetsettablesequential-method.md).</span><span class="sxs-lookup"><span data-stu-id="db3ea-105">This call reverses a notification sent by [JetSetTableSequential(JET_SESID, JET_TABLEID, SetTableSequentialGrbit)](./api.jetsettablesequential-method.md).</span></span>

<span data-ttu-id="db3ea-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db3ea-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="db3ea-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="db3ea-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db3ea-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db3ea-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetResetTableSequential ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As ResetTableSequentialGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As ResetTableSequentialGrbitApi.JetResetTableSequential(sesid, _
    tableid, grbit)
```

``` csharp
public static void JetResetTableSequential(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ResetTableSequentialGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="db3ea-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="db3ea-109">Parameters</span></span>

  - <span data-ttu-id="db3ea-110">сесид</span><span class="sxs-lookup"><span data-stu-id="db3ea-110">sesid</span></span>  
    <span data-ttu-id="db3ea-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db3ea-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="db3ea-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="db3ea-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="db3ea-113">TableID</span><span class="sxs-lookup"><span data-stu-id="db3ea-113">tableid</span></span>  
    <span data-ttu-id="db3ea-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db3ea-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="db3ea-115">Курсор, обращающийся к данным.</span><span class="sxs-lookup"><span data-stu-id="db3ea-115">The cursor that was accessing the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="db3ea-116">грбит</span><span class="sxs-lookup"><span data-stu-id="db3ea-116">grbit</span></span>  
    <span data-ttu-id="db3ea-117">Тип: [Microsoft. ISAM. ESENT. Interop. ресеттаблесекуентиалгрбит](./resettablesequentialgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="db3ea-117">Type: [Microsoft.Isam.Esent.Interop.ResetTableSequentialGrbit](./resettablesequentialgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="db3ea-118">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="db3ea-118">Reserved for future use.</span></span>

## <a name="see-also"></a><span data-ttu-id="db3ea-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db3ea-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db3ea-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="db3ea-120">Reference</span></span>

[<span data-ttu-id="db3ea-121">Класс API</span><span class="sxs-lookup"><span data-stu-id="db3ea-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="db3ea-122">Члены API</span><span class="sxs-lookup"><span data-stu-id="db3ea-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="db3ea-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="db3ea-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
