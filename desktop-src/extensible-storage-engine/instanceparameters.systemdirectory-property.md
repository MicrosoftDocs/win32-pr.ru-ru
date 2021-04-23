---
description: 'Дополнительные сведения: InstanceParameters.Sysсвойство Темдиректори'
title: InstanceParameters.Sys, свойство Темдиректори
TOCTitle: 'SystemDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.systemdirectory(v=EXCHG.10)
ms:contentKeyID: 55103561
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_SystemDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.SystemDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_SystemDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c0478b4b9d626610549240d58f3289fc24d10aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713085"
---
# <a name="instanceparameterssystemdirectory-property"></a><span data-ttu-id="57e31-103">InstanceParameters.Sys, свойство Темдиректори</span><span class="sxs-lookup"><span data-stu-id="57e31-103">InstanceParameters.SystemDirectory property</span></span>

<span data-ttu-id="57e31-104">Возвращает или задает относительный или абсолютный путь файловой системы к папке, которая будет содержать файл контрольных точек для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="57e31-104">Gets or sets the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span>

<span data-ttu-id="57e31-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="57e31-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="57e31-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="57e31-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="57e31-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57e31-107">Syntax</span></span>

``` vb
'Declaration
Public Property SystemDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.SystemDirectory

instance.SystemDirectory = value
```

``` csharp
public string SystemDirectory { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="57e31-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="57e31-108">Property value</span></span>

<span data-ttu-id="57e31-109">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="57e31-109">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="57e31-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57e31-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="57e31-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="57e31-111">Reference</span></span>

[<span data-ttu-id="57e31-112">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="57e31-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="57e31-113">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="57e31-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="57e31-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="57e31-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
