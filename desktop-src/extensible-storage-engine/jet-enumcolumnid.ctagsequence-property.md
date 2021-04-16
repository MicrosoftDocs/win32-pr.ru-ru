---
description: 'Дополнительные сведения о свойстве: JET_ENUMCOLUMNID. Ктагсекуенце'
title: Свойство JET_ENUMCOLUMNID. Ктагсекуенце
TOCTitle: 'ctagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid.ctagsequence(v=EXCHG.10)
ms:contentKeyID: 55107537
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.set_ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.ctagSequence
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID.get_ctagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e12c8c6a102cbb20862b3cc9859f7e632ade8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719338"
---
# <a name="jet_enumcolumnidctagsequence-property"></a><span data-ttu-id="61a95-103">Свойство JET_ENUMCOLUMNID. Ктагсекуенце</span><span class="sxs-lookup"><span data-stu-id="61a95-103">JET_ENUMCOLUMNID.ctagSequence property</span></span>

<span data-ttu-id="61a95-104">Возвращает или задает количество значений столбца (по одному индексу) для перечисления по указанному ИДЕНТИФИКАТОРу столбца.</span><span class="sxs-lookup"><span data-stu-id="61a95-104">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="61a95-105">Если Ктагсекуенце имеет значение 0 (ноль), то Ргтагсекуенце игнорируется и все значения столбцов для указанного идентификатора столбца будут перечислены.</span><span class="sxs-lookup"><span data-stu-id="61a95-105">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="61a95-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="61a95-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="61a95-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="61a95-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61a95-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61a95-108">Syntax</span></span>

``` vb
'Declaration
Public Property ctagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_ENUMCOLUMNID
Dim value As Integer

value = instance.ctagSequence

instance.ctagSequence = value
```

``` csharp
public int ctagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="61a95-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="61a95-109">Property value</span></span>

<span data-ttu-id="61a95-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="61a95-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="61a95-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61a95-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61a95-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="61a95-112">Reference</span></span>

[<span data-ttu-id="61a95-113">Класс JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="61a95-113">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="61a95-114">Элементы JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="61a95-114">JET_ENUMCOLUMNID members</span></span>](./jet-enumcolumnid-members.md)

[<span data-ttu-id="61a95-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="61a95-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
