---
description: 'Дополнительные сведения о методе: Колумнстреам. Write'
title: Колумнстреам. Write, метод
TOCTitle: 'Write method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Write(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.write(v=EXCHG.10)
ms:contentKeyID: 55100987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77b62e7dd028da3452082c973690ce0c0210b438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081428"
---
# <a name="columnstreamwrite-method"></a><span data-ttu-id="3be70-103">Колумнстреам. Write, метод</span><span class="sxs-lookup"><span data-stu-id="3be70-103">ColumnStream.Write method</span></span>

<span data-ttu-id="3be70-104">Записывает последовательность байтов в текущий поток и перемещает текущую позицию внутри потока на число записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="3be70-104">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span>

<span data-ttu-id="3be70-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3be70-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3be70-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3be70-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3be70-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3be70-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Sub Write ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
)
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer

instance.Write(buffer, offset, count)
```

``` csharp
public override void Write(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="3be70-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3be70-108">Parameters</span></span>

  - <span data-ttu-id="3be70-109">buffer</span><span class="sxs-lookup"><span data-stu-id="3be70-109">buffer</span></span>  
    <span data-ttu-id="3be70-110">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="3be70-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="3be70-111">Буфер, из которого производится запись.</span><span class="sxs-lookup"><span data-stu-id="3be70-111">The buffer to write from.</span></span>

<!-- end list -->

  - <span data-ttu-id="3be70-112">offset</span><span class="sxs-lookup"><span data-stu-id="3be70-112">offset</span></span>  
    <span data-ttu-id="3be70-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3be70-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3be70-114">Смещение в буфере для записи.</span><span class="sxs-lookup"><span data-stu-id="3be70-114">The offset in the buffer to write.</span></span>

<!-- end list -->

  - <span data-ttu-id="3be70-115">count</span><span class="sxs-lookup"><span data-stu-id="3be70-115">count</span></span>  
    <span data-ttu-id="3be70-116">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3be70-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3be70-117">Количество записываемых байтов.</span><span class="sxs-lookup"><span data-stu-id="3be70-117">The number of bytes to write.</span></span>

## <a name="see-also"></a><span data-ttu-id="3be70-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3be70-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3be70-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="3be70-119">Reference</span></span>

[<span data-ttu-id="3be70-120">Класс Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="3be70-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="3be70-121">Элементы Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="3be70-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="3be70-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3be70-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
