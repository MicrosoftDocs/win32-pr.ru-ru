---
description: 'Дополнительные сведения о: JET_COLUMNCREATE. Метод Контентекуалс'
title: JET_COLUMNCREATE. Метод Контентекуалс
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103471
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: db39608007705284b4690893cb6e3196dca8dc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156903"
---
# <a name="jet_columncreatecontentequals-method"></a><span data-ttu-id="0afdc-103">JET_COLUMNCREATE. Метод Контентекуалс</span><span class="sxs-lookup"><span data-stu-id="0afdc-103">JET_COLUMNCREATE.ContentEquals method</span></span>

<span data-ttu-id="0afdc-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="0afdc-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="0afdc-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0afdc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0afdc-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0afdc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0afdc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0afdc-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_COLUMNCREATE _
) As Boolean
'Usage
Dim instance As JET_COLUMNCREATE
Dim other As JET_COLUMNCREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_COLUMNCREATE other
)
```

#### <a name="parameters"></a><span data-ttu-id="0afdc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0afdc-108">Parameters</span></span>

  - <span data-ttu-id="0afdc-109">др.</span><span class="sxs-lookup"><span data-stu-id="0afdc-109">other</span></span>  
    <span data-ttu-id="0afdc-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNCREATE](./jet-columncreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="0afdc-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE](./jet-columncreate-class.md)</span></span>  
    
    <span data-ttu-id="0afdc-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="0afdc-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0afdc-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0afdc-112">Return value</span></span>

<span data-ttu-id="0afdc-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="0afdc-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="0afdc-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="0afdc-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="0afdc-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="0afdc-115">Implements</span></span>

[<span data-ttu-id="0afdc-116">Иконтентекуатабле \<T\> . Контентекуалс (T)</span><span class="sxs-lookup"><span data-stu-id="0afdc-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="0afdc-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0afdc-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0afdc-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="0afdc-118">Reference</span></span>

[<span data-ttu-id="0afdc-119">Класс JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="0afdc-119">JET_COLUMNCREATE class</span></span>](./jet-columncreate-class.md)

[<span data-ttu-id="0afdc-120">Элементы JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="0afdc-120">JET_COLUMNCREATE members</span></span>](./jet-columncreate-members.md)

[<span data-ttu-id="0afdc-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0afdc-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
