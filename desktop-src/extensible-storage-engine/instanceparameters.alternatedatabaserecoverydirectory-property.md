---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Алтернатедатабасерековеридиректори'
title: Инстанцепараметерс. Алтернатедатабасерековеридиректори, свойство
TOCTitle: 'AlternateDatabaseRecoveryDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.alternatedatabaserecoverydirectory(v=EXCHG.10)
ms:contentKeyID: 55107440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_AlternateDatabaseRecoveryDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70e08c65027806990ab511ef8561b41551f0ac2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701725"
---
# <a name="instanceparametersalternatedatabaserecoverydirectory-property"></a><span data-ttu-id="177f1-103">Инстанцепараметерс. Алтернатедатабасерековеридиректори, свойство</span><span class="sxs-lookup"><span data-stu-id="177f1-103">InstanceParameters.AlternateDatabaseRecoveryDirectory property</span></span>

<span data-ttu-id="177f1-104">Возвращает или задает относительный или абсолютный путь к файловой системе папки, в которой восстановление после сбоя или операция восстановления могут найти базы данных, на которые имеются ссылки в журнале транзакций в указанной папке.</span><span class="sxs-lookup"><span data-stu-id="177f1-104">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span>

<span data-ttu-id="177f1-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="177f1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="177f1-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="177f1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="177f1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="177f1-107">Syntax</span></span>

``` vb
'Declaration
Public Property AlternateDatabaseRecoveryDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.AlternateDatabaseRecoveryDirectory

instance.AlternateDatabaseRecoveryDirectory = value
```

``` csharp
public string AlternateDatabaseRecoveryDirectory { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="177f1-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="177f1-108">Property value</span></span>

<span data-ttu-id="177f1-109">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="177f1-109">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="remarks"></a><span data-ttu-id="177f1-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="177f1-110">Remarks</span></span>

<span data-ttu-id="177f1-111">Этот параметр не учитывается в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="177f1-111">This parameter is ignored on Windows XP.</span></span>

## <a name="see-also"></a><span data-ttu-id="177f1-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="177f1-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="177f1-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="177f1-113">Reference</span></span>

[<span data-ttu-id="177f1-114">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="177f1-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="177f1-115">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="177f1-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="177f1-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="177f1-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
