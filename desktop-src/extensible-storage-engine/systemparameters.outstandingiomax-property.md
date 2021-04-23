---
description: 'Дополнительные сведения о свойстве: SystemParameters. Аутстандингиомакс'
title: SystemParameters. Аутстандингиомакс, свойство
TOCTitle: 'OutstandingIOMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.outstandingiomax(v=EXCHG.10)
ms:contentKeyID: 55104045
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.set_OutstandingIOMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7faf7af3aec16bc81fada5c8742b4c60595bedad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545738"
---
# <a name="systemparametersoutstandingiomax-property"></a><span data-ttu-id="114da-103">SystemParameters. Аутстандингиомакс, свойство</span><span class="sxs-lookup"><span data-stu-id="114da-103">SystemParameters.OutstandingIOMax property</span></span>

<span data-ttu-id="114da-104">Этот параметр определяет, сколько операций ввода-вывода в файле базы данных может быть помещено в очередь на диск в операционной системе узла.</span><span class="sxs-lookup"><span data-stu-id="114da-104">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="114da-105">Большее значение этого параметра может значительно помочь в производительности большого приложения базы данных.</span><span class="sxs-lookup"><span data-stu-id="114da-105">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="114da-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="114da-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="114da-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="114da-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="114da-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="114da-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property OutstandingIOMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.OutstandingIOMax

SystemParameters.OutstandingIOMax = value
```

``` csharp
public static int OutstandingIOMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="114da-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="114da-109">Property value</span></span>

<span data-ttu-id="114da-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="114da-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="114da-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="114da-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="114da-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="114da-112">Reference</span></span>

[<span data-ttu-id="114da-113">SystemParameters - класс</span><span class="sxs-lookup"><span data-stu-id="114da-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="114da-114">Элементы SystemParameters</span><span class="sxs-lookup"><span data-stu-id="114da-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="114da-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="114da-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
