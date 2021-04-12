---
description: 'Дополнительные сведения о свойстве: JET_INDEXCREATE. Сзкэй'
title: Свойство JET_INDEXCREATE. Сзкэй
TOCTitle: 'szKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.szkey(v=EXCHG.10)
ms:contentKeyID: 55103656
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86ade65ee28eef6314d31653772b0c22657476d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348802"
---
# <a name="jet_indexcreateszkey-property"></a><span data-ttu-id="8818a-103">Свойство JET_INDEXCREATE. Сзкэй</span><span class="sxs-lookup"><span data-stu-id="8818a-103">JET_INDEXCREATE.szKey property</span></span>

<span data-ttu-id="8818a-104">Возвращает или задает описание ключа индекса.</span><span class="sxs-lookup"><span data-stu-id="8818a-104">Gets or sets the description of the index key.</span></span> <span data-ttu-id="8818a-105">Это строка токенов с разделителями null, заканчивающаяся символом двойной точности null.</span><span class="sxs-lookup"><span data-stu-id="8818a-105">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="8818a-106">Каждый токен имеет вид \[ "направление- \] \[ имя столбца \] ", где "направление" — "+" или "-".</span><span class="sxs-lookup"><span data-stu-id="8818a-106">Each token is of the form \[direction-specifier\]\[column-name\], where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="8818a-107">Например, Сзкэй "+ ABC \\ 0-DEF \\ 0 + GHI \\ 0" будет индексировать три столбца "ABC" (в порядке возрастания), "def" (в убывающем порядке) и "GHI" (в возрастающем порядке).</span><span class="sxs-lookup"><span data-stu-id="8818a-107">for example, a szKey of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span>

<span data-ttu-id="8818a-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8818a-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8818a-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8818a-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8818a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8818a-110">Syntax</span></span>

``` vb
'Declaration
Public Property szKey As String
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As String

value = instance.szKey

instance.szKey = value
```

``` csharp
public string szKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="8818a-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8818a-111">Property value</span></span>

<span data-ttu-id="8818a-112">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8818a-112">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8818a-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8818a-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8818a-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="8818a-114">Reference</span></span>

[<span data-ttu-id="8818a-115">Класс JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="8818a-115">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="8818a-116">Элементы JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="8818a-116">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="8818a-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8818a-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
