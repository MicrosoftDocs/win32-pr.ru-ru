---
description: 'Дополнительные сведения о: Иконтентекуатабле <T> . Метод Контентекуалс'
title: Иконтентекуатабле (T). Метод Контентекуалс
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals(`0)
ms:mtpsurl: https://msdn.microsoft.com/library/Hh538970(v=EXCHG.10)
ms:contentKeyID: 39509953
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3b06307f7c4ebc44242e02ee5ae99a182f9ab3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683082"
---
# <a name="icontentequatabletcontentequals-method"></a><span data-ttu-id="d6edd-103">Иконтентекуатабле \<T\> . Метод Контентекуалс</span><span class="sxs-lookup"><span data-stu-id="d6edd-103">IContentEquatable\<T\>.ContentEquals method</span></span>

<span data-ttu-id="d6edd-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="d6edd-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="d6edd-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6edd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d6edd-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d6edd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6edd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6edd-107">Syntax</span></span>

``` vb
'Declaration
Function ContentEquals ( _
    other As T _
) As Boolean
'Usage
Dim instance As IContentEquatable
Dim other As T
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
bool ContentEquals(
    T other
)
```

#### <a name="parameters"></a><span data-ttu-id="d6edd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6edd-108">Parameters</span></span>

  - <span data-ttu-id="d6edd-109">др.</span><span class="sxs-lookup"><span data-stu-id="d6edd-109">other</span></span>  
    <span data-ttu-id="d6edd-110">Тип: [T](./icontentequatable-t-interface.md)</span><span class="sxs-lookup"><span data-stu-id="d6edd-110">Type: [T](./icontentequatable-t-interface.md)</span></span>  
    
    <span data-ttu-id="d6edd-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="d6edd-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d6edd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6edd-112">Return value</span></span>

<span data-ttu-id="d6edd-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="d6edd-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="d6edd-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="d6edd-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6edd-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6edd-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6edd-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="d6edd-116">Reference</span></span>

[<span data-ttu-id="d6edd-117">\<T\>Интерфейс иконтентекуатабле</span><span class="sxs-lookup"><span data-stu-id="d6edd-117">IContentEquatable\<T\> interface</span></span>](./icontentequatable-t-interface.md)

[<span data-ttu-id="d6edd-118">\<T\>Элементы иконтентекуатабле</span><span class="sxs-lookup"><span data-stu-id="d6edd-118">IContentEquatable\<T\> members</span></span>](./icontentequatable-t-members.md)

[<span data-ttu-id="d6edd-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d6edd-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
