---
description: 'Дополнительные сведения о свойстве: JET_RECSIZE. Кбдатакомпрессед'
title: Свойство JET_RECSIZE. Кбдатакомпрессед (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cbdatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515358
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbDataCompressed
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 747c2f00077f6a9d13de059f742bacc9a7936d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808518"
---
# <a name="jet_recsizecbdatacompressed-property"></a><span data-ttu-id="869f2-103">Свойство JET_RECSIZE. Кбдатакомпрессед</span><span class="sxs-lookup"><span data-stu-id="869f2-103">JET_RECSIZE.cbDataCompressed property</span></span>

<span data-ttu-id="869f2-104">Возвращает сжатый размер данных пользователя в записи.</span><span class="sxs-lookup"><span data-stu-id="869f2-104">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="869f2-105">Это то же самое, что [cbData](./jet-recsize.cbdata-property.md) , если никакие внутренние значения long не сжимаются).</span><span class="sxs-lookup"><span data-stu-id="869f2-105">This is the same as [cbData](./jet-recsize.cbdata-property.md) if no intrinsic long-values are compressed).</span></span>

<span data-ttu-id="869f2-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="869f2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="869f2-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="869f2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="869f2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="869f2-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbDataCompressed
```

``` csharp
public long cbDataCompressed { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="869f2-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="869f2-109">Property value</span></span>

<span data-ttu-id="869f2-110">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="869f2-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="869f2-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="869f2-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="869f2-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="869f2-112">Reference</span></span>

[<span data-ttu-id="869f2-113">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="869f2-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="869f2-114">Элементы JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="869f2-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="869f2-115">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="869f2-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
