---
description: 'Дополнительные сведения о: JET_RETINFO. Метод Контентекуалс'
title: JET_RETINFO. Метод Контентекуалс
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals(Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103869
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bac25d8184b1dd62e8c622cbdd79df42d4996314
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810517"
---
# <a name="jet_retinfocontentequals-method"></a><span data-ttu-id="a09f7-103">JET_RETINFO. Метод Контентекуалс</span><span class="sxs-lookup"><span data-stu-id="a09f7-103">JET_RETINFO.ContentEquals method</span></span>

<span data-ttu-id="a09f7-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="a09f7-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="a09f7-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a09f7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a09f7-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a09f7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a09f7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a09f7-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_RETINFO _
) As Boolean
'Usage
Dim instance As JET_RETINFO
Dim other As JET_RETINFO
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_RETINFO other
)
```

#### <a name="parameters"></a><span data-ttu-id="a09f7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a09f7-108">Parameters</span></span>

  - <span data-ttu-id="a09f7-109">др.</span><span class="sxs-lookup"><span data-stu-id="a09f7-109">other</span></span>  
    <span data-ttu-id="a09f7-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="a09f7-110">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="a09f7-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="a09f7-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a09f7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a09f7-112">Return value</span></span>

<span data-ttu-id="a09f7-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a09f7-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a09f7-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="a09f7-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="a09f7-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="a09f7-115">Implements</span></span>

[<span data-ttu-id="a09f7-116">Иконтентекуатабле \<T\> . Контентекуалс (T)</span><span class="sxs-lookup"><span data-stu-id="a09f7-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="a09f7-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a09f7-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a09f7-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="a09f7-118">Reference</span></span>

[<span data-ttu-id="a09f7-119">Класс JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="a09f7-119">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="a09f7-120">Элементы JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="a09f7-120">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="a09f7-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a09f7-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
