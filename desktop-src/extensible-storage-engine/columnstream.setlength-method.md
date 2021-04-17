---
description: 'Дополнительные сведения о методе: Колумнстреам. SetLength'
title: Колумнстреам. SetLength, метод
TOCTitle: 'SetLength method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.SetLength(System.Int64)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.setlength(v=EXCHG.10)
ms:contentKeyID: 55100986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.SetLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.SetLength
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fccf32d6494427811c3db8a2d2f4b71a2909a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702987"
---
# <a name="columnstreamsetlength-method"></a><span data-ttu-id="420d7-103">Колумнстреам. SetLength, метод</span><span class="sxs-lookup"><span data-stu-id="420d7-103">ColumnStream.SetLength method</span></span>

<span data-ttu-id="420d7-104">Задает длину потока.</span><span class="sxs-lookup"><span data-stu-id="420d7-104">Sets the length of the stream.</span></span>

<span data-ttu-id="420d7-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="420d7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="420d7-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="420d7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="420d7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="420d7-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Sub SetLength ( _
    value As Long _
)
'Usage
Dim instance As ColumnStream
Dim value As Long

instance.SetLength(value)
```

``` csharp
public override void SetLength(
    long value
)
```

#### <a name="parameters"></a><span data-ttu-id="420d7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="420d7-108">Parameters</span></span>

  - <span data-ttu-id="420d7-109">значение</span><span class="sxs-lookup"><span data-stu-id="420d7-109">value</span></span>  
    <span data-ttu-id="420d7-110">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="420d7-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="420d7-111">Требуемая длина в байтах.</span><span class="sxs-lookup"><span data-stu-id="420d7-111">The desired length, in bytes.</span></span>

## <a name="see-also"></a><span data-ttu-id="420d7-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="420d7-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="420d7-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="420d7-113">Reference</span></span>

[<span data-ttu-id="420d7-114">Класс Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="420d7-114">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="420d7-115">Элементы Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="420d7-115">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="420d7-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="420d7-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
