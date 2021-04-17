---
description: 'Дополнительные сведения: метод API. Жетсетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Сетколумнгрбит, JET_SETINFO)'
title: Метод API. Жетсетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Сетколумнгрбит, JET_SETINFO)
TOCTitle: JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnGrbit,Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumn(v=EXCHG.10)
ms:contentKeyID: 55100804
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5afebba00c784abf5bf71ac0f524376bd0f3b066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713016"
---
# <a name="apijetsetcolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-setcolumngrbit-jet_setinfo"></a><span data-ttu-id="8bf7a-103">Метод API. Жетсетколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Сетколумнгрбит, JET_SETINFO)</span><span class="sxs-lookup"><span data-stu-id="8bf7a-103">Api.JetSetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, SetColumnGrbit, JET_SETINFO)</span></span>

<span data-ttu-id="8bf7a-104">Функция Жетсетколумн изменяет значение одного столбца в изменяемой записи, которое вставляется, или обновляет текущую запись.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-104">The JetSetColumn function modifies a single column value in a modified record to be inserted or to update the current record.</span></span> <span data-ttu-id="8bf7a-105">Он может перезаписать существующее значение, добавить новое значение в последовательность значений в столбце с несколькими значениями, удалить значение из последовательности значений в многозначном столбце или обновить все или часть длинного значения (столбец типа [LongText](./jet-coltyp-enumeration.md) или [лонгбинари](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="8bf7a-105">It can overwrite an existing value, add a new value to a sequence of values in a multi-valued column, remove a value from a sequence of values in a multi-valued column, or update all or part of a long value (a column of type [LongText](./jet-coltyp-enumeration.md) or [LongBinary](./jet-coltyp-enumeration.md)).</span></span>

<span data-ttu-id="8bf7a-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8bf7a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8bf7a-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8bf7a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf7a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bf7a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnGrbit, _
    setinfo As JET_SETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnGrbit
Dim setinfo As JET_SETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumn(sesid, _
    tableid, columnid, data, dataSize, _
    grbit, setinfo)
```

``` csharp
public static JET_wrn JetSetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    SetColumnGrbit grbit,
    JET_SETINFO setinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="8bf7a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8bf7a-109">Parameters</span></span>

  - <span data-ttu-id="8bf7a-110">сесид</span><span class="sxs-lookup"><span data-stu-id="8bf7a-110">sesid</span></span>  
    <span data-ttu-id="8bf7a-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8bf7a-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8bf7a-112">Сеанс, который выполняет обновление.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-112">The session which is performing the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="8bf7a-113">TableID</span><span class="sxs-lookup"><span data-stu-id="8bf7a-113">tableid</span></span>  
    <span data-ttu-id="8bf7a-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8bf7a-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8bf7a-115">Обновляемый курсор.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-115">The cursor to update.</span></span> <span data-ttu-id="8bf7a-116">Необходимо подготовить обновление.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="8bf7a-117">columnid</span><span class="sxs-lookup"><span data-stu-id="8bf7a-117">columnid</span></span>  
    <span data-ttu-id="8bf7a-118">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8bf7a-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="8bf7a-119">Устанавливаемое значение columnid.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-119">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="8bf7a-120">.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-120">data</span></span>  
    <span data-ttu-id="8bf7a-121">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="8bf7a-121">Type: \[\]</span></span>  
    
    <span data-ttu-id="8bf7a-122">Задаваемые данные.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-122">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="8bf7a-123">dataSize</span><span class="sxs-lookup"><span data-stu-id="8bf7a-123">dataSize</span></span>  
    <span data-ttu-id="8bf7a-124">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8bf7a-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="8bf7a-125">Размер устанавливаемых данных.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-125">The size of data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="8bf7a-126">грбит</span><span class="sxs-lookup"><span data-stu-id="8bf7a-126">grbit</span></span>  
    <span data-ttu-id="8bf7a-127">Тип: [Microsoft. ISAM. ESENT. Interop. сетколумнгрбит](./setcolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8bf7a-127">Type: [Microsoft.Isam.Esent.Interop.SetColumnGrbit](./setcolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8bf7a-128">Параметры Сетколумн.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-128">SetColumn options.</span></span>

<!-- end list -->

  - <span data-ttu-id="8bf7a-129">сетинфо</span><span class="sxs-lookup"><span data-stu-id="8bf7a-129">setinfo</span></span>  
    <span data-ttu-id="8bf7a-130">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SETINFO](./jet-setinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="8bf7a-130">Type: [Microsoft.Isam.Esent.Interop.JET_SETINFO](./jet-setinfo-class.md)</span></span>  
    
    <span data-ttu-id="8bf7a-131">Используется для указания итаг или смещения длинного значения.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-131">Used to specify itag or long-value offset.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8bf7a-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8bf7a-132">Return value</span></span>

<span data-ttu-id="8bf7a-133">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8bf7a-133">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="8bf7a-134">Код предупреждения.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-134">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="8bf7a-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8bf7a-135">Remarks</span></span>

<span data-ttu-id="8bf7a-136">Методы Сетколумн предоставляют переопределяемые типы данных, которые могут быть более эффективными.</span><span class="sxs-lookup"><span data-stu-id="8bf7a-136">The SetColumn methods provide datatype-specific overrides which may be more efficient.</span></span>

## <a name="see-also"></a><span data-ttu-id="8bf7a-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bf7a-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8bf7a-138">Справочник</span><span class="sxs-lookup"><span data-stu-id="8bf7a-138">Reference</span></span>

[<span data-ttu-id="8bf7a-139">Класс API</span><span class="sxs-lookup"><span data-stu-id="8bf7a-139">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8bf7a-140">Члены API</span><span class="sxs-lookup"><span data-stu-id="8bf7a-140">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8bf7a-141">Перегрузка Жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="8bf7a-141">JetSetColumn overload</span></span>](./api.jetsetcolumn-method.md)

[<span data-ttu-id="8bf7a-142">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8bf7a-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
