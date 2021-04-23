---
description: 'Дополнительные сведения о методе: Колумнвалуе. Жетвалуефромбитес'
title: Колумнвалуе. Жетвалуефромбитес, метод
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55101191
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 448c0626c0e4cf91b266a6894a021789d52955b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703302"
---
# <a name="columnvaluegetvaluefrombytes-method"></a><span data-ttu-id="7dc2a-103">Колумнвалуе. Жетвалуефромбитес, метод</span><span class="sxs-lookup"><span data-stu-id="7dc2a-103">ColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="7dc2a-104">Данные, полученные из ESENT, декодируются и задают значение в объекте Колумнвалуе.</span><span class="sxs-lookup"><span data-stu-id="7dc2a-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="7dc2a-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7dc2a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7dc2a-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7dc2a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7dc2a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7dc2a-107">Syntax</span></span>

``` vb
'Declaration
Protected MustOverride Sub GetValueFromBytes ( _
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
protected abstract void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a><span data-ttu-id="7dc2a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7dc2a-108">Parameters</span></span>

  - <span data-ttu-id="7dc2a-109">значение</span><span class="sxs-lookup"><span data-stu-id="7dc2a-109">value</span></span>  
    <span data-ttu-id="7dc2a-110">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="7dc2a-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="7dc2a-111">Массив байтов.</span><span class="sxs-lookup"><span data-stu-id="7dc2a-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="7dc2a-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="7dc2a-112">startIndex</span></span>  
    <span data-ttu-id="7dc2a-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7dc2a-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7dc2a-114">Начальная позицией в байтах.</span><span class="sxs-lookup"><span data-stu-id="7dc2a-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="7dc2a-115">count</span><span class="sxs-lookup"><span data-stu-id="7dc2a-115">count</span></span>  
    <span data-ttu-id="7dc2a-116">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7dc2a-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7dc2a-117">Число байтов для декодирования.</span><span class="sxs-lookup"><span data-stu-id="7dc2a-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="7dc2a-118">Err</span><span class="sxs-lookup"><span data-stu-id="7dc2a-118">err</span></span>  
    <span data-ttu-id="7dc2a-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7dc2a-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7dc2a-120">Ошибка, возвращенная из ESENT.</span><span class="sxs-lookup"><span data-stu-id="7dc2a-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="7dc2a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7dc2a-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7dc2a-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="7dc2a-122">Reference</span></span>

[<span data-ttu-id="7dc2a-123">Класс Колумнвалуе</span><span class="sxs-lookup"><span data-stu-id="7dc2a-123">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="7dc2a-124">Элементы Колумнвалуе</span><span class="sxs-lookup"><span data-stu-id="7dc2a-124">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="7dc2a-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7dc2a-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
