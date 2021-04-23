---
description: 'Дополнительные сведения о свойстве: JET_COLUMNDEF. CP'
title: Свойство JET_COLUMNDEF. CP
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.cp(v=EXCHG.10)
ms:contentKeyID: 55103411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.get_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df383b212105a4b871f0c44d341d6113abf94d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155395"
---
# <a name="jet_columndefcp-property"></a><span data-ttu-id="c8689-103">Свойство JET_COLUMNDEF. CP</span><span class="sxs-lookup"><span data-stu-id="c8689-103">JET_COLUMNDEF.cp property</span></span>

<span data-ttu-id="c8689-104">Возвращает или задает кодовую страницу столбца.</span><span class="sxs-lookup"><span data-stu-id="c8689-104">Gets or sets code page of the column.</span></span> <span data-ttu-id="c8689-105">Это имеет смысл только для столбцов типа [Text](./jet-coltyp-enumeration.md) и [LongText](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="c8689-105">This is only meaningful for columns of type [Text](./jet-coltyp-enumeration.md) and [LongText](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="c8689-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c8689-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c8689-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c8689-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c8689-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8689-108">Syntax</span></span>

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Set
'Usage
Dim instance As JET_COLUMNDEF
Dim value As JET_CP

value = instance.cp

instance.cp = value
```

``` csharp
public JET_CP cp { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="c8689-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c8689-109">Property value</span></span>

<span data-ttu-id="c8689-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_CP](./jet-cp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c8689-110">Type: [Microsoft.Isam.Esent.Interop.JET_CP](./jet-cp-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c8689-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8689-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c8689-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="c8689-112">Reference</span></span>

[<span data-ttu-id="c8689-113">Класс JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="c8689-113">JET_COLUMNDEF class</span></span>](./jet-columndef-class.md)

[<span data-ttu-id="c8689-114">Элементы JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="c8689-114">JET_COLUMNDEF members</span></span>](./jet-columndef-members.md)

[<span data-ttu-id="c8689-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c8689-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
