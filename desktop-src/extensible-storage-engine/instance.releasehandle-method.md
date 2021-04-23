---
description: Дополнительные сведения о методе instance. ReleaseHandle
title: Экземпляр. ReleaseHandle, метод
TOCTitle: 'ReleaseHandle method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.releasehandle(v=EXCHG.10)
ms:contentKeyID: 55103298
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance.ReleaseHandle
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fcac0fcbffc685fb91bd0c0bf2f97865540cb1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081204"
---
# <a name="instancereleasehandle-method"></a><span data-ttu-id="0bbaa-103">Экземпляр. ReleaseHandle, метод</span><span class="sxs-lookup"><span data-stu-id="0bbaa-103">Instance.ReleaseHandle method</span></span>

<span data-ttu-id="0bbaa-104">Освобождение маркера для этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0bbaa-104">Release the handle for this instance.</span></span>

<span data-ttu-id="0bbaa-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0bbaa-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0bbaa-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0bbaa-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0bbaa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bbaa-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Function ReleaseHandle As Boolean
'Usage
Dim returnValue As Boolean

returnValue = Me.ReleaseHandle()
```

``` csharp
protected override bool ReleaseHandle()
```

#### <a name="return-value"></a><span data-ttu-id="0bbaa-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bbaa-108">Return value</span></span>

<span data-ttu-id="0bbaa-109">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="0bbaa-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="0bbaa-110">Значение true, если можно освободить маркер.</span><span class="sxs-lookup"><span data-stu-id="0bbaa-110">True if the handle could be released.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0bbaa-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bbaa-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0bbaa-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="0bbaa-112">Reference</span></span>

[<span data-ttu-id="0bbaa-113">Класс экземпляра</span><span class="sxs-lookup"><span data-stu-id="0bbaa-113">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="0bbaa-114">Члены экземпляра</span><span class="sxs-lookup"><span data-stu-id="0bbaa-114">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="0bbaa-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0bbaa-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
