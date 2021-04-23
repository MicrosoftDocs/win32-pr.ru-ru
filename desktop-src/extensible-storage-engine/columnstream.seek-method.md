---
description: 'Дополнительные сведения о методе: Колумнстреам. Seek'
title: Колумнстреам. Seek, метод
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5489bb0ee9a4a1550166e14a945a2a6d58c45af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543439"
---
# <a name="columnstreamseek-method"></a><span data-ttu-id="2d67e-103">Колумнстреам. Seek, метод</span><span class="sxs-lookup"><span data-stu-id="2d67e-103">ColumnStream.Seek method</span></span>

<span data-ttu-id="2d67e-104">Задает позицию в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="2d67e-104">Sets the position in the current stream.</span></span>

<span data-ttu-id="2d67e-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2d67e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2d67e-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2d67e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2d67e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d67e-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a><span data-ttu-id="2d67e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d67e-108">Parameters</span></span>

  - <span data-ttu-id="2d67e-109">offset</span><span class="sxs-lookup"><span data-stu-id="2d67e-109">offset</span></span>  
    <span data-ttu-id="2d67e-110">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="2d67e-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="2d67e-111">Смещение в байтах относительно параметра origin.</span><span class="sxs-lookup"><span data-stu-id="2d67e-111">Byte offset relative to the origin parameter.</span></span>

<!-- end list -->

  - <span data-ttu-id="2d67e-112">Исходное подключение</span><span class="sxs-lookup"><span data-stu-id="2d67e-112">origin</span></span>  
    <span data-ttu-id="2d67e-113">Тип: [System. IO. SeekOrigin](/dotnet/api/system.io.seekorigin)</span><span class="sxs-lookup"><span data-stu-id="2d67e-113">Type: [System.IO.SeekOrigin](/dotnet/api/system.io.seekorigin)</span></span>  
    
    <span data-ttu-id="2d67e-114">Значение SeekOrigin, указывающее точку ссылки для новой позиции.</span><span class="sxs-lookup"><span data-stu-id="2d67e-114">A SeekOrigin indicating the reference point for the new position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2d67e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d67e-115">Return value</span></span>

<span data-ttu-id="2d67e-116">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="2d67e-116">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
<span data-ttu-id="2d67e-117">Новая позицией в текущем потоке.</span><span class="sxs-lookup"><span data-stu-id="2d67e-117">The new position in the current stream.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2d67e-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d67e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2d67e-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="2d67e-119">Reference</span></span>

[<span data-ttu-id="2d67e-120">Класс Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="2d67e-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="2d67e-121">Элементы Колумнстреам</span><span class="sxs-lookup"><span data-stu-id="2d67e-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="2d67e-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2d67e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
