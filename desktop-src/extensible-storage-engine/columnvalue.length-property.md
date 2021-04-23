---
description: Дополнительные сведения о свойстве Колумнвалуе. length
title: Колумнвалуе. length, свойство
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55101208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Length
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c64e2b8e7b25be5b33d64591e16b982604e2fee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703389"
---
# <a name="columnvaluelength-property"></a><span data-ttu-id="ec0ce-103">Колумнвалуе. length, свойство</span><span class="sxs-lookup"><span data-stu-id="ec0ce-103">ColumnValue.Length property</span></span>

<span data-ttu-id="ec0ce-104">Возвращает длину в байтах значения столбца, равного нулю, если столбец имеет значение null, в противном случае он соответствует размеру для столбцов фиксированного размера и представляет фактическую длину байт для столбцов переменного размера (т. е. двоичного и строкового).</span><span class="sxs-lookup"><span data-stu-id="ec0ce-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the Size for fixed-size columns and represent the actual value byte length for variable sized columns (i.e. binary and string).</span></span> <span data-ttu-id="ec0ce-105">Для строк длина определяется в предположении 2 байта на символ.</span><span class="sxs-lookup"><span data-stu-id="ec0ce-105">For strings the length is determined in assumption two bytes per character.</span></span>

<span data-ttu-id="ec0ce-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ec0ce-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ec0ce-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ec0ce-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ec0ce-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec0ce-108">Syntax</span></span>

``` vb
'Declaration
Public MustOverride ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public abstract int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="ec0ce-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ec0ce-109">Property value</span></span>

<span data-ttu-id="ec0ce-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ec0ce-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="ec0ce-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec0ce-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ec0ce-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="ec0ce-112">Reference</span></span>

[<span data-ttu-id="ec0ce-113">Класс Колумнвалуе</span><span class="sxs-lookup"><span data-stu-id="ec0ce-113">ColumnValue class</span></span>](./columnvalue-class.md)

[<span data-ttu-id="ec0ce-114">Элементы Колумнвалуе</span><span class="sxs-lookup"><span data-stu-id="ec0ce-114">ColumnValue members</span></span>](./columnvalue-members.md)

[<span data-ttu-id="ec0ce-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ec0ce-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
