---
description: Дополнительные сведения о методе API. Жетсетлс
title: API. Жетсетлс, метод
TOCTitle: 'JetSetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetls(v=EXCHG.10)
ms:contentKeyID: 55100808
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d11d0790bb1d9340c427fd1b836d927527c6ca63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266217"
---
# <a name="apijetsetls-method"></a><span data-ttu-id="bfa66-103">API. Жетсетлс, метод</span><span class="sxs-lookup"><span data-stu-id="bfa66-103">Api.JetSetLS method</span></span>

<span data-ttu-id="bfa66-104">Позволяет приложению связать описатель контекста, известный как локальное хранилище, с курсором или с таблицей, связанной с этим курсором.</span><span class="sxs-lookup"><span data-stu-id="bfa66-104">Enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="bfa66-105">Этот обработчик контекста может использоваться приложением для хранения вспомогательных данных, связанных с курсором или таблицей.</span><span class="sxs-lookup"><span data-stu-id="bfa66-105">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="bfa66-106">После этого приложение будет уведомлено с помощью обратного вызова времени выполнения, когда должен быть освобожден обработчик контекста.</span><span class="sxs-lookup"><span data-stu-id="bfa66-106">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="bfa66-107">Это дает возможность связать динамически выделенное состояние с курсором или таблицей.</span><span class="sxs-lookup"><span data-stu-id="bfa66-107">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="bfa66-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bfa66-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bfa66-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bfa66-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa66-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfa66-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetSetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetSetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="bfa66-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfa66-111">Parameters</span></span>

  - <span data-ttu-id="bfa66-112">сесид</span><span class="sxs-lookup"><span data-stu-id="bfa66-112">sesid</span></span>  
    <span data-ttu-id="bfa66-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bfa66-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bfa66-114">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="bfa66-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bfa66-115">TableID</span><span class="sxs-lookup"><span data-stu-id="bfa66-115">tableid</span></span>  
    <span data-ttu-id="bfa66-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bfa66-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bfa66-117">Используемый курсор.</span><span class="sxs-lookup"><span data-stu-id="bfa66-117">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bfa66-118">ls</span><span class="sxs-lookup"><span data-stu-id="bfa66-118">ls</span></span>  
    <span data-ttu-id="bfa66-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bfa66-119">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="bfa66-120">Контекстный обработчик, связываемый с сеансом или курсором.</span><span class="sxs-lookup"><span data-stu-id="bfa66-120">The context handle to be associated with the session or cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="bfa66-121">грбит</span><span class="sxs-lookup"><span data-stu-id="bfa66-121">grbit</span></span>  
    <span data-ttu-id="bfa66-122">Тип: [Microsoft. ISAM. ESENT. Interop. лсгрбит](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bfa66-122">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="bfa66-123">Задайте параметры.</span><span class="sxs-lookup"><span data-stu-id="bfa66-123">Set options.</span></span>

## <a name="see-also"></a><span data-ttu-id="bfa66-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfa66-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bfa66-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="bfa66-125">Reference</span></span>

[<span data-ttu-id="bfa66-126">Класс API</span><span class="sxs-lookup"><span data-stu-id="bfa66-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bfa66-127">Члены API</span><span class="sxs-lookup"><span data-stu-id="bfa66-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bfa66-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bfa66-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
