---
description: 'Дополнительные сведения о методе: Windows7Api. Жетпререадкэйс (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, Пререадкэйсгрбит)'
title: Метод Windows7Api. Жетпререадкэйс (JET_SESID, JET_TABLEID, Byte [] [], Int32, Int32, Int32, Int32, Пререадкэйсгрбит) (Microsoft. ISAM. ESENT. Interop. Windows7)
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55104374
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a799c890887df730fdad97ad4d08fa500a6dd4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263370"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-int32-prereadkeysgrbit"></a><span data-ttu-id="bf180-103">Метод Windows7Api. жетпререадкэйс (JET_SESID, JET_TABLEID, Byte \[ \] \[ \] , Int32, Int32, Int32, Int32, пререадкэйсгрбит)</span><span class="sxs-lookup"><span data-stu-id="bf180-103">Windows7Api.JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte\[\]\[\], Int32 , Int32, Int32, Int32, PrereadKeysGrbit)</span></span>

<span data-ttu-id="bf180-104">Если записи с указанными ключами отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.</span><span class="sxs-lookup"><span data-stu-id="bf180-104">If the records with the specified keys are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="bf180-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bf180-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)</span></span>  
<span data-ttu-id="bf180-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bf180-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bf180-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf180-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyIndex As Integer, _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyIndex As Integer
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyIndex, keyCount, _
    keysPreread, grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyIndex,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="bf180-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf180-108">Parameters</span></span>

  - <span data-ttu-id="bf180-109">сесид</span><span class="sxs-lookup"><span data-stu-id="bf180-109">sesid</span></span>  
    <span data-ttu-id="bf180-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bf180-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bf180-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="bf180-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf180-112">TableID</span><span class="sxs-lookup"><span data-stu-id="bf180-112">tableid</span></span>  
    <span data-ttu-id="bf180-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bf180-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bf180-114">Таблица, для которой выдаются сведения о предчтении.</span><span class="sxs-lookup"><span data-stu-id="bf180-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf180-115">ключи</span><span class="sxs-lookup"><span data-stu-id="bf180-115">keys</span></span>  
    <span data-ttu-id="bf180-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="bf180-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="bf180-117">Ключи для чтения.</span><span class="sxs-lookup"><span data-stu-id="bf180-117">The keys to preread.</span></span> <span data-ttu-id="bf180-118">Ключи должны быть отсортированы.</span><span class="sxs-lookup"><span data-stu-id="bf180-118">The keys must be sorted.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf180-119">кэйленгсс</span><span class="sxs-lookup"><span data-stu-id="bf180-119">keyLengths</span></span>  
    <span data-ttu-id="bf180-120">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="bf180-120">Type: \[\]</span></span>  
    
    <span data-ttu-id="bf180-121">Длина ключей для чтения.</span><span class="sxs-lookup"><span data-stu-id="bf180-121">The lengths of the keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf180-122">keyIndex</span><span class="sxs-lookup"><span data-stu-id="bf180-122">keyIndex</span></span>  
    <span data-ttu-id="bf180-123">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bf180-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bf180-124">Индекс первого ключа в массиве ключей для чтения.</span><span class="sxs-lookup"><span data-stu-id="bf180-124">The index of the first key in the keys array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf180-125">кэйкаунт</span><span class="sxs-lookup"><span data-stu-id="bf180-125">keyCount</span></span>  
    <span data-ttu-id="bf180-126">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bf180-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bf180-127">Максимальное число ключей для чтения.</span><span class="sxs-lookup"><span data-stu-id="bf180-127">The maximum number of keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf180-128">кэйспререад</span><span class="sxs-lookup"><span data-stu-id="bf180-128">keysPreread</span></span>  
    <span data-ttu-id="bf180-129">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bf180-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bf180-130">Возвращает число ключей для фактического чтения.</span><span class="sxs-lookup"><span data-stu-id="bf180-130">Returns the number of keys to actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="bf180-131">грбит</span><span class="sxs-lookup"><span data-stu-id="bf180-131">grbit</span></span>  
    <span data-ttu-id="bf180-132">Тип: [Microsoft. ISAM. ESENT. Interop. Windows7. пререадкэйсгрбит](./prereadkeysgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="bf180-132">Type: [Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="bf180-133">Параметры для чтения.</span><span class="sxs-lookup"><span data-stu-id="bf180-133">Preread options.</span></span> <span data-ttu-id="bf180-134">Используется для указания направления выполнения перед чтением.</span><span class="sxs-lookup"><span data-stu-id="bf180-134">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf180-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf180-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bf180-136">Справочник</span><span class="sxs-lookup"><span data-stu-id="bf180-136">Reference</span></span>

[<span data-ttu-id="bf180-137">Класс Windows7Api</span><span class="sxs-lookup"><span data-stu-id="bf180-137">Windows7Api class</span></span>](./windows7api-class.md)

[<span data-ttu-id="bf180-138">Элементы Windows7Api</span><span class="sxs-lookup"><span data-stu-id="bf180-138">Windows7Api members</span></span>](./windows7api-members.md)

[<span data-ttu-id="bf180-139">Перегрузка Жетпререадкэйс</span><span class="sxs-lookup"><span data-stu-id="bf180-139">JetPrereadKeys overload</span></span>](./windows7api.jetprereadkeys-method.md)

[<span data-ttu-id="bf180-140">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows7</span><span class="sxs-lookup"><span data-stu-id="bf180-140">Microsoft.Isam.Esent.Interop.Windows7 namespace</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)
