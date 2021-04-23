---
description: 'Дополнительные сведения о: <T> интерфейс иконтентекуатабле'
title: Интерфейс Иконтентекуатабле (T)
TOCTitle: IContentEquatable(T) interface
ms:assetid: T:Microsoft.Isam.Esent.Interop.IContentEquatable`1
ms:mtpsurl: https://msdn.microsoft.com/library/Hh578046(v=EXCHG.10)
ms:contentKeyID: 39511318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02e237714f020f5bafa3ce8b7465f1c8e2615c01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662691"
---
# <a name="icontentequatablet-interface"></a><span data-ttu-id="0a2de-103">\<T\>Интерфейс иконтентекуатабле</span><span class="sxs-lookup"><span data-stu-id="0a2de-103">IContentEquatable\<T\> interface</span></span>

<span data-ttu-id="0a2de-104">Интерфейс для объектов, содержимое которых может быть сравнено друг с другом.</span><span class="sxs-lookup"><span data-stu-id="0a2de-104">Interface for objects that can have their contents compared against each other.</span></span> <span data-ttu-id="0a2de-105">Он должен использоваться для сравнения на равенство изменяемых ссылочных объектов, если переопределение Equals () и GetHashCode () не является хорошей идеей.</span><span class="sxs-lookup"><span data-stu-id="0a2de-105">This should be used for equality comparisons on mutable reference objects where overriding Equals() and GetHashCode() isn't a good idea.</span></span>

<span data-ttu-id="0a2de-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0a2de-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0a2de-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0a2de-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0a2de-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a2de-108">Syntax</span></span>

``` vb
'Declaration
Public Interface IContentEquatable(Of T)
'Usage
Dim instance As IContentEquatable(Of T)
```

``` csharp
public interface IContentEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="0a2de-109">Параметры типа</span><span class="sxs-lookup"><span data-stu-id="0a2de-109">Type parameters</span></span>

  - <span data-ttu-id="0a2de-110">T</span><span class="sxs-lookup"><span data-stu-id="0a2de-110">T</span></span>  
    <span data-ttu-id="0a2de-111">Тип объектов для комапре.</span><span class="sxs-lookup"><span data-stu-id="0a2de-111">The type of objects to comapre.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a2de-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a2de-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0a2de-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="0a2de-113">Reference</span></span>

[<span data-ttu-id="0a2de-114">\<T\>Элементы иконтентекуатабле</span><span class="sxs-lookup"><span data-stu-id="0a2de-114">IContentEquatable\<T\> members</span></span>](./icontentequatable-t-members.md)

[<span data-ttu-id="0a2de-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0a2de-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
