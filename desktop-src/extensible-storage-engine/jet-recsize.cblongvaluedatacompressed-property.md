---
description: 'Дополнительные сведения о свойстве: JET_RECSIZE. Кблонгвалуедатакомпрессед'
title: Свойство JET_RECSIZE. Кблонгвалуедатакомпрессед (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'cbLongValueDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cblongvaluedatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515830
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbLongValueDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbLongValueDataCompressed
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113bb741287e85ef6f7132cd299202a0b9c2af31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423653"
---
# <a name="jet_recsizecblongvaluedatacompressed-property"></a><span data-ttu-id="12493-103">Свойство JET_RECSIZE. Кблонгвалуедатакомпрессед</span><span class="sxs-lookup"><span data-stu-id="12493-103">JET_RECSIZE.cbLongValueDataCompressed property</span></span>

<span data-ttu-id="12493-104">Возвращает сжатый размер пользовательских данных в дереве длинных значений.</span><span class="sxs-lookup"><span data-stu-id="12493-104">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="12493-105">Это то же самое, что и [кблонгвалуедата](./jet-recsize.cblongvaluedata-property.md) , если не сжаты отдельные длинные значения.</span><span class="sxs-lookup"><span data-stu-id="12493-105">This is the same as [cbLongValueData](./jet-recsize.cblongvaluedata-property.md) if no separated long values are compressed.</span></span>

<span data-ttu-id="12493-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="12493-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="12493-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="12493-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="12493-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12493-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbLongValueDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbLongValueDataCompressed
```

``` csharp
public long cbLongValueDataCompressed { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="12493-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="12493-109">Property value</span></span>

<span data-ttu-id="12493-110">Тип: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="12493-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="12493-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12493-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="12493-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="12493-112">Reference</span></span>

[<span data-ttu-id="12493-113">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="12493-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="12493-114">Элементы JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="12493-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="12493-115">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="12493-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
