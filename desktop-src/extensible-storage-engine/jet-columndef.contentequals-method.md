---
description: 'Дополнительные сведения о: JET_COLUMNDEF. Метод Контентекуалс'
title: JET_COLUMNDEF. Метод Контентекуалс
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals(Microsoft.Isam.Esent.Interop.JET_COLUMNDEF)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103479
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f4527edef1fd8567ec3f4973dddc67548e79946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155027"
---
# <a name="jet_columndefcontentequals-method"></a><span data-ttu-id="5e7c5-103">JET_COLUMNDEF. Метод Контентекуалс</span><span class="sxs-lookup"><span data-stu-id="5e7c5-103">JET_COLUMNDEF.ContentEquals method</span></span>

<span data-ttu-id="5e7c5-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="5e7c5-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="5e7c5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5e7c5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5e7c5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5e7c5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5e7c5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5e7c5-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_COLUMNDEF _
) As Boolean
'Usage
Dim instance As JET_COLUMNDEF
Dim other As JET_COLUMNDEF
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_COLUMNDEF other
)
```

#### <a name="parameters"></a><span data-ttu-id="5e7c5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e7c5-108">Parameters</span></span>

  - <span data-ttu-id="5e7c5-109">др.</span><span class="sxs-lookup"><span data-stu-id="5e7c5-109">other</span></span>  
    <span data-ttu-id="5e7c5-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="5e7c5-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="5e7c5-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="5e7c5-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5e7c5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5e7c5-112">Return value</span></span>

<span data-ttu-id="5e7c5-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="5e7c5-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="5e7c5-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="5e7c5-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="5e7c5-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="5e7c5-115">Implements</span></span>

[<span data-ttu-id="5e7c5-116">Иконтентекуатабле \<T\> . Контентекуалс (T)</span><span class="sxs-lookup"><span data-stu-id="5e7c5-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="5e7c5-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5e7c5-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5e7c5-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="5e7c5-118">Reference</span></span>

[<span data-ttu-id="5e7c5-119">Класс JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="5e7c5-119">JET_COLUMNDEF class</span></span>](./jet-columndef-class.md)

[<span data-ttu-id="5e7c5-120">Элементы JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="5e7c5-120">JET_COLUMNDEF members</span></span>](./jet-columndef-members.md)

[<span data-ttu-id="5e7c5-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5e7c5-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
