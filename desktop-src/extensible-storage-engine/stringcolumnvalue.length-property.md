---
description: Дополнительные сведения о свойстве Стрингколумнвалуе. length
title: Стрингколумнвалуе. length, свойство
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55104090
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Length
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7313f66bd25653a66ebd8567a21c0ad5431ec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265713"
---
# <a name="stringcolumnvaluelength-property"></a><span data-ttu-id="99971-103">Стрингколумнвалуе. length, свойство</span><span class="sxs-lookup"><span data-stu-id="99971-103">StringColumnValue.Length property</span></span>

<span data-ttu-id="99971-104">Возвращает длину в байтах значения столбца, равного нулю, если столбец имеет значение null, в противном случае соответствует длине в байтах строкового значения.</span><span class="sxs-lookup"><span data-stu-id="99971-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the byte length of the string value.</span></span> <span data-ttu-id="99971-105">Длина байта определяется в соответствии с двумя байтами на символ.</span><span class="sxs-lookup"><span data-stu-id="99971-105">The byte length is determined in assumption of two bytes per character.</span></span>

<span data-ttu-id="99971-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="99971-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="99971-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="99971-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="99971-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99971-108">Syntax</span></span>

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As StringColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="99971-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="99971-109">Property value</span></span>

<span data-ttu-id="99971-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="99971-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="99971-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99971-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="99971-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="99971-112">Reference</span></span>

[<span data-ttu-id="99971-113">Класс Стрингколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="99971-113">StringColumnValue class</span></span>](./stringcolumnvalue-class.md)

[<span data-ttu-id="99971-114">Элементы Стрингколумнвалуе</span><span class="sxs-lookup"><span data-stu-id="99971-114">StringColumnValue members</span></span>](./stringcolumnvalue-members.md)

[<span data-ttu-id="99971-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="99971-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
