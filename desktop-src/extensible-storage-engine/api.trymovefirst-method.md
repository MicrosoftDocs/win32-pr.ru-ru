---
description: Дополнительные сведения о методе API. Тримовефирст
title: API. Тримовефирст, метод
TOCTitle: 'TryMoveFirst method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveFirst(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovefirst(v=EXCHG.10)
ms:contentKeyID: 55100946
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveFirst
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveFirst
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624fba29ab6fe653b7af674e32b907ea3934d643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692106"
---
# <a name="apitrymovefirst-method"></a><span data-ttu-id="09513-103">API. Тримовефирст, метод</span><span class="sxs-lookup"><span data-stu-id="09513-103">Api.TryMoveFirst method</span></span>

<span data-ttu-id="09513-104">Попробуйте перейти к первой записи в таблице.</span><span class="sxs-lookup"><span data-stu-id="09513-104">Try to move to the first record in the table.</span></span> <span data-ttu-id="09513-105">Если таблица пуста, возвращает значение false, если возникла другая ошибка, возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="09513-105">If the table is empty this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="09513-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="09513-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="09513-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="09513-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="09513-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09513-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMoveFirst ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveFirst(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveFirst(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="09513-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="09513-109">Parameters</span></span>

  - <span data-ttu-id="09513-110">сесид</span><span class="sxs-lookup"><span data-stu-id="09513-110">sesid</span></span>  
    <span data-ttu-id="09513-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09513-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="09513-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="09513-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="09513-113">TableID</span><span class="sxs-lookup"><span data-stu-id="09513-113">tableid</span></span>  
    <span data-ttu-id="09513-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09513-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="09513-115">Курсор для позиции.</span><span class="sxs-lookup"><span data-stu-id="09513-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="09513-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09513-116">Return value</span></span>

<span data-ttu-id="09513-117">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="09513-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="09513-118">Значение true, если перемещение прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="09513-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="09513-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09513-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="09513-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="09513-120">Reference</span></span>

[<span data-ttu-id="09513-121">Класс API</span><span class="sxs-lookup"><span data-stu-id="09513-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="09513-122">Члены API</span><span class="sxs-lookup"><span data-stu-id="09513-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="09513-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="09513-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
