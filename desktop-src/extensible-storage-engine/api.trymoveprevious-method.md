---
description: Дополнительные сведения о методе API. Тримовепревиаус
title: API. Тримовепревиаус, метод
TOCTitle: 'TryMovePrevious method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMovePrevious(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymoveprevious(v=EXCHG.10)
ms:contentKeyID: 55100940
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMovePrevious
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMovePrevious
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe512ac4443f670ac73964a422bd9606d903055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647303"
---
# <a name="apitrymoveprevious-method"></a><span data-ttu-id="3377b-103">API. Тримовепревиаус, метод</span><span class="sxs-lookup"><span data-stu-id="3377b-103">Api.TryMovePrevious method</span></span>

<span data-ttu-id="3377b-104">Попробуйте перейти к предыдущей записи в таблице.</span><span class="sxs-lookup"><span data-stu-id="3377b-104">Try to move to the previous record in the table.</span></span> <span data-ttu-id="3377b-105">Если Предыдущая запись отсутствует, возвращает значение false, если возникла другая ошибка, возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="3377b-105">If there is not a previous record this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="3377b-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3377b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3377b-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3377b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3377b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3377b-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMovePrevious ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMovePrevious(sesid, _
    tableid)
```

``` csharp
public static bool TryMovePrevious(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="3377b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3377b-109">Parameters</span></span>

  - <span data-ttu-id="3377b-110">сесид</span><span class="sxs-lookup"><span data-stu-id="3377b-110">sesid</span></span>  
    <span data-ttu-id="3377b-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3377b-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3377b-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="3377b-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3377b-113">TableID</span><span class="sxs-lookup"><span data-stu-id="3377b-113">tableid</span></span>  
    <span data-ttu-id="3377b-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3377b-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3377b-115">Курсор для позиции.</span><span class="sxs-lookup"><span data-stu-id="3377b-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="3377b-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3377b-116">Return value</span></span>

<span data-ttu-id="3377b-117">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="3377b-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="3377b-118">Значение true, если перемещение прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="3377b-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3377b-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3377b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3377b-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="3377b-120">Reference</span></span>

[<span data-ttu-id="3377b-121">Класс API</span><span class="sxs-lookup"><span data-stu-id="3377b-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3377b-122">Члены API</span><span class="sxs-lookup"><span data-stu-id="3377b-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3377b-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3377b-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
