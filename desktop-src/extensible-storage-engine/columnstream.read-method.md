---
description: 'Дополнительные сведения о методе: Колумнстреам. Read'
title: Колумнстреам. Read, метод
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e407a9069807d10eaabf4f7ac3fce3919576bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674245"
---
# <a name="columnstreamread-method"></a><span data-ttu-id="d65d9-103">Колумнстреам. Read, метод</span><span class="sxs-lookup"><span data-stu-id="d65d9-103">ColumnStream.Read method</span></span>

<span data-ttu-id="d65d9-104">Считывает последовательность байтов из текущего потока и перемещает позицию внутри потока на число считанных байтов.</span><span class="sxs-lookup"><span data-stu-id="d65d9-104">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span>

<span data-ttu-id="d65d9-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d65d9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d65d9-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d65d9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d65d9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d65d9-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="d65d9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d65d9-108">Parameters</span></span>

  - <span data-ttu-id="d65d9-109">buffer</span><span class="sxs-lookup"><span data-stu-id="d65d9-109">buffer</span></span>  
    <span data-ttu-id="d65d9-110">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="d65d9-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="d65d9-111">Буфер, в который производится чтение.</span><span class="sxs-lookup"><span data-stu-id="d65d9-111">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="d65d9-112">offset</span><span class="sxs-lookup"><span data-stu-id="d65d9-112">offset</span></span>  
    <span data-ttu-id="d65d9-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d65d9-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d65d9-114">Смещение в буфере для чтения.</span><span class="sxs-lookup"><span data-stu-id="d65d9-114">The offset in the buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="d65d9-115">count</span><span class="sxs-lookup"><span data-stu-id="d65d9-115">count</span></span>  
    <span data-ttu-id="d65d9-116">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d65d9-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d65d9-117">Количество байтов, чтение которых необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="d65d9-117">The number of bytes to read.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d65d9-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d65d9-118">Return value</span></span>

<span data-ttu-id="d65d9-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d65d9-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="d65d9-120">Число байтов, считанных в буфер.</span><span class="sxs-lookup"><span data-stu-id="d65d9-120">The number of bytes read into the buffer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d65d9-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d65d9-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d65d9-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="d65d9-122">Reference</span></span>

[<span data-ttu-id="d65d9-123">Класс Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="d65d9-123">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="d65d9-124">Элементы Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="d65d9-124">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="d65d9-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d65d9-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
