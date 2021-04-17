---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. LogFileSize'
title: Инстанцепараметерс. LogFileSize, свойство
TOCTitle: 'LogFileSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logfilesize(v=EXCHG.10)
ms:contentKeyID: 55103312
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogFileSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c141c76a92f49b4b5000cad65e302a7cf15d780f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702645"
---
# <a name="instanceparameterslogfilesize-property"></a><span data-ttu-id="b9110-103">Инстанцепараметерс. LogFileSize, свойство</span><span class="sxs-lookup"><span data-stu-id="b9110-103">InstanceParameters.LogFileSize property</span></span>

<span data-ttu-id="b9110-104">Возвращает или задает размер файлов журнала транзакций.</span><span class="sxs-lookup"><span data-stu-id="b9110-104">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="b9110-105">Этот параметр должен быть задан в единицах, равных 1024 байт (например, параметр 2048 будет предоставлять файлы журнала в 2 МБ).</span><span class="sxs-lookup"><span data-stu-id="b9110-105">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span>

<span data-ttu-id="b9110-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b9110-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b9110-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b9110-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9110-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9110-108">Syntax</span></span>

``` vb
'Declaration
Public Property LogFileSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogFileSize

instance.LogFileSize = value
```

``` csharp
public int LogFileSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b9110-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b9110-109">Property value</span></span>

<span data-ttu-id="b9110-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b9110-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b9110-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9110-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b9110-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="b9110-112">Reference</span></span>

[<span data-ttu-id="b9110-113">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="b9110-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="b9110-114">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="b9110-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="b9110-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b9110-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
