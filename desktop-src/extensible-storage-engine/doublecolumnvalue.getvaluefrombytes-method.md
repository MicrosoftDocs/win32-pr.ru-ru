---
description: 'Дополнительные сведения о методе: Даублеколумнвалуе. Жетвалуефромбитес'
title: Даублеколумнвалуе. Жетвалуефромбитес, метод
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.DoubleColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.doublecolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55107244
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DoubleColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DoubleColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 209f573862a257e587a26c1957e80e46f3190616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719432"
---
# <a name="doublecolumnvaluegetvaluefrombytes-method"></a><span data-ttu-id="427e4-103">Даублеколумнвалуе. Жетвалуефромбитес, метод</span><span class="sxs-lookup"><span data-stu-id="427e4-103">DoubleColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="427e4-104">Данные, полученные из ESENT, декодируются и задают значение в объекте Колумнвалуе.</span><span class="sxs-lookup"><span data-stu-id="427e4-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="427e4-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="427e4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="427e4-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="427e4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="427e4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="427e4-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a><span data-ttu-id="427e4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="427e4-108">Parameters</span></span>

  - <span data-ttu-id="427e4-109">значение</span><span class="sxs-lookup"><span data-stu-id="427e4-109">value</span></span>  
    <span data-ttu-id="427e4-110">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="427e4-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="427e4-111">Массив байтов.</span><span class="sxs-lookup"><span data-stu-id="427e4-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="427e4-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="427e4-112">startIndex</span></span>  
    <span data-ttu-id="427e4-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="427e4-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="427e4-114">Начальная позицией в байтах.</span><span class="sxs-lookup"><span data-stu-id="427e4-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="427e4-115">count</span><span class="sxs-lookup"><span data-stu-id="427e4-115">count</span></span>  
    <span data-ttu-id="427e4-116">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="427e4-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="427e4-117">Число байтов для декодирования.</span><span class="sxs-lookup"><span data-stu-id="427e4-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="427e4-118">Err</span><span class="sxs-lookup"><span data-stu-id="427e4-118">err</span></span>  
    <span data-ttu-id="427e4-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="427e4-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="427e4-120">Ошибка, возвращенная из ESENT.</span><span class="sxs-lookup"><span data-stu-id="427e4-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="427e4-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="427e4-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="427e4-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="427e4-122">Reference</span></span>

[<span data-ttu-id="427e4-123">Класс Даублеколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="427e4-123">DoubleColumnValue class</span></span>](./doublecolumnvalue-class.md)

[<span data-ttu-id="427e4-124">Элементы Даублеколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="427e4-124">DoubleColumnValue members</span></span>](./doublecolumnvalue-members.md)

[<span data-ttu-id="427e4-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="427e4-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
