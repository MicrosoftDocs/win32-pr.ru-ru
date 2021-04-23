---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Макстрансактионсизе'
title: Инстанцепараметерс. Макстрансактионсизе, свойство
TOCTitle: 'MaxTransactionSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtransactionsize(v=EXCHG.10)
ms:contentKeyID: 55103317
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTransactionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTransactionSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTransactionSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370d05364142a6fca7d84265dc8d29c7ab5c808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910503"
---
# <a name="instanceparametersmaxtransactionsize-property"></a><span data-ttu-id="37ad5-103">Инстанцепараметерс. Макстрансактионсизе, свойство</span><span class="sxs-lookup"><span data-stu-id="37ad5-103">InstanceParameters.MaxTransactionSize property</span></span>

<span data-ttu-id="37ad5-104">Возвращает или задает процентное значение хранилища версий, которое может использоваться самой старой транзакцией перед [версионстореаутофмемори](./jet-err-enumeration.md) (по умолчанию = 100).</span><span class="sxs-lookup"><span data-stu-id="37ad5-104">Gets or sets the percentage of version store that can be used by oldest transaction before [VersionStoreOutOfMemory](./jet-err-enumeration.md) (default = 100).</span></span>

<span data-ttu-id="37ad5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="37ad5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="37ad5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="37ad5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="37ad5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37ad5-107">Syntax</span></span>

``` vb
'Declaration
Public Property MaxTransactionSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTransactionSize

instance.MaxTransactionSize = value
```

``` csharp
public int MaxTransactionSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="37ad5-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="37ad5-108">Property value</span></span>

<span data-ttu-id="37ad5-109">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="37ad5-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="37ad5-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37ad5-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="37ad5-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="37ad5-111">Reference</span></span>

[<span data-ttu-id="37ad5-112">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="37ad5-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="37ad5-113">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="37ad5-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="37ad5-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="37ad5-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
