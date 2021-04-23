---
description: Дополнительные сведения о методе API. Жетжетлс
title: API. Жетжетлс, метод
TOCTitle: 'JetGetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS@,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetls(v=EXCHG.10)
ms:contentKeyID: 55100734
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 611f92e21dad83121b4e4a6226838ac9ebce2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262976"
---
# <a name="apijetgetls-method"></a><span data-ttu-id="968e2-103">API. Жетжетлс, метод</span><span class="sxs-lookup"><span data-stu-id="968e2-103">Api.JetGetLS method</span></span>

<span data-ttu-id="968e2-104">Позволяет приложению извлекать контекстный маркер, известный как локальное хранилище, связанное с курсором, или с таблицей, связанной с этим курсором.</span><span class="sxs-lookup"><span data-stu-id="968e2-104">Enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="968e2-105">Этот обработчик контекста должен быть ранее задан с помощью [жетсетлс (JET_SESID, JET_TABLEID, JET_LS, лсгрбит)](./api.jetsetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="968e2-105">This context handle must have been previously set using [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span> <span data-ttu-id="968e2-106">Жетжетлс также можно использовать для одновременной выборки текущего контекста для курсора или таблицы и сброса дескриптора контекста.</span><span class="sxs-lookup"><span data-stu-id="968e2-106">JetGetLS can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="968e2-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="968e2-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="968e2-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="968e2-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="968e2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="968e2-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetGetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetGetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="968e2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="968e2-110">Parameters</span></span>

  - <span data-ttu-id="968e2-111">сесид</span><span class="sxs-lookup"><span data-stu-id="968e2-111">sesid</span></span>  
    <span data-ttu-id="968e2-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="968e2-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="968e2-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="968e2-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="968e2-114">TableID</span><span class="sxs-lookup"><span data-stu-id="968e2-114">tableid</span></span>  
    <span data-ttu-id="968e2-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="968e2-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="968e2-116">Используемый курсор.</span><span class="sxs-lookup"><span data-stu-id="968e2-116">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="968e2-117">ls</span><span class="sxs-lookup"><span data-stu-id="968e2-117">ls</span></span>  
    <span data-ttu-id="968e2-118">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="968e2-118">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="968e2-119">Возвращает полученный обработчик контекста.</span><span class="sxs-lookup"><span data-stu-id="968e2-119">Returns the retrieved context handle.</span></span>

<!-- end list -->

  - <span data-ttu-id="968e2-120">грбит</span><span class="sxs-lookup"><span data-stu-id="968e2-120">grbit</span></span>  
    <span data-ttu-id="968e2-121">Тип: [Microsoft. ISAM. ESENT. Interop. лсгрбит](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="968e2-121">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="968e2-122">Получение параметров.</span><span class="sxs-lookup"><span data-stu-id="968e2-122">Retrieve options.</span></span>

## <a name="see-also"></a><span data-ttu-id="968e2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="968e2-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="968e2-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="968e2-124">Reference</span></span>

[<span data-ttu-id="968e2-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="968e2-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="968e2-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="968e2-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="968e2-127">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="968e2-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
