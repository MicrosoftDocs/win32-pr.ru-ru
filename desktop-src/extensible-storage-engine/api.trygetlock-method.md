---
description: Дополнительные сведения о методе API. Трижетлокк
title: API. Трижетлокк, метод
TOCTitle: 'TryGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trygetlock(v=EXCHG.10)
ms:contentKeyID: 55100934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ecd4e0e66226d438b4e5a78b2397f5637154096
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272537"
---
# <a name="apitrygetlock-method"></a><span data-ttu-id="a7db0-103">API. Трижетлокк, метод</span><span class="sxs-lookup"><span data-stu-id="a7db0-103">Api.TryGetLock method</span></span>

<span data-ttu-id="a7db0-104">Явно Зарезервируйте возможность обновления строки, блокировки записи или явного запрета обновления строки любым другим сеансом, блокировка чтения.</span><span class="sxs-lookup"><span data-stu-id="a7db0-104">Explicitly reserve the ability to update a row, write lock, or to explicitly prevent a row from being updated by any other session, read lock.</span></span> <span data-ttu-id="a7db0-105">Обычно блокировки записи строк получаются неявно в результате обновления строк.</span><span class="sxs-lookup"><span data-stu-id="a7db0-105">Normally, row write locks are acquired implicitly as a result of updating rows.</span></span> <span data-ttu-id="a7db0-106">Блокировки чтения обычно не требуются из-за управления версиями записей.</span><span class="sxs-lookup"><span data-stu-id="a7db0-106">Read locks are usually not required because of record versioning.</span></span> <span data-ttu-id="a7db0-107">Однако в некоторых случаях транзакция может потребовать явно заблокировать строку для принудительного применения сериализации или убедиться, что дальнейшая операция будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="a7db0-107">However, in some cases a transaction may desire to explicitly lock a row to enforce serialization, or to ensure that a subsequent operation will succeed.</span></span>

<span data-ttu-id="a7db0-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a7db0-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a7db0-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a7db0-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a7db0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7db0-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbit
Dim returnValue As Boolean

returnValue = Api.TryGetLock(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TryGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="a7db0-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7db0-111">Parameters</span></span>

  - <span data-ttu-id="a7db0-112">сесид</span><span class="sxs-lookup"><span data-stu-id="a7db0-112">sesid</span></span>  
    <span data-ttu-id="a7db0-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a7db0-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a7db0-114">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="a7db0-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7db0-115">TableID</span><span class="sxs-lookup"><span data-stu-id="a7db0-115">tableid</span></span>  
    <span data-ttu-id="a7db0-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a7db0-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a7db0-117">Используемый курсор.</span><span class="sxs-lookup"><span data-stu-id="a7db0-117">The cursor to use.</span></span> <span data-ttu-id="a7db0-118">Для текущей записи будет получена блокировка.</span><span class="sxs-lookup"><span data-stu-id="a7db0-118">A lock will be acquired on the current record.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7db0-119">грбит</span><span class="sxs-lookup"><span data-stu-id="a7db0-119">grbit</span></span>  
    <span data-ttu-id="a7db0-120">Тип: [Microsoft. ISAM. ESENT. Interop. жетлоккгрбит](./getlockgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a7db0-120">Type: [Microsoft.Isam.Esent.Interop.GetLockGrbit](./getlockgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a7db0-121">Параметры блокировки. Используйте этот параметр, чтобы указать тип блокировки для получения.</span><span class="sxs-lookup"><span data-stu-id="a7db0-121">Lock options, use this to specify which type of lock to obtain.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a7db0-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7db0-122">Return value</span></span>

<span data-ttu-id="a7db0-123">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a7db0-123">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a7db0-124">Значение true, если блокировка получена; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="a7db0-124">True if the lock was obtained, false otherwise.</span></span> <span data-ttu-id="a7db0-125">Если обнаружена непредвиденная ошибка, возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="a7db0-125">An exception is thrown if an unexpected error is encountered.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a7db0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a7db0-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7db0-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="a7db0-127">Reference</span></span>

[<span data-ttu-id="a7db0-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="a7db0-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a7db0-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="a7db0-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a7db0-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a7db0-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
