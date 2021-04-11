---
description: 'Дополнительные сведения о свойстве: JET_INSTANCE_INFO. Сзинстанценаме'
title: Свойство JET_INSTANCE_INFO. Сзинстанценаме
TOCTitle: 'szInstanceName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szInstanceName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.szinstancename(v=EXCHG.10)
ms:contentKeyID: 55103713
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szInstanceName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_szInstanceName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.set_szInstanceName
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.szInstanceName
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edaa331fce5564672ac844f6977ea5ae1688a38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265558"
---
# <a name="jet_instance_infoszinstancename-property"></a><span data-ttu-id="1ff9f-103">Свойство JET_INSTANCE_INFO. Сзинстанценаме</span><span class="sxs-lookup"><span data-stu-id="1ff9f-103">JET_INSTANCE_INFO.szInstanceName property</span></span>

<span data-ttu-id="1ff9f-104">Возвращает имя экземпляра базы данных.</span><span class="sxs-lookup"><span data-stu-id="1ff9f-104">Gets the name of the database instance.</span></span> <span data-ttu-id="1ff9f-105">Это значение может быть равно null, если у экземпляра нет имени.</span><span class="sxs-lookup"><span data-stu-id="1ff9f-105">This value can be null if the instance does not have a name.</span></span>

<span data-ttu-id="1ff9f-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ff9f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ff9f-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ff9f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff9f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ff9f-108">Syntax</span></span>

``` vb
'Declaration
Public Property szInstanceName As String
    Get
    Private Set
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As String

value = instance.szInstanceName
```

``` csharp
public string szInstanceName { get; private set; }
```

#### <a name="property-value"></a><span data-ttu-id="1ff9f-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1ff9f-109">Property value</span></span>

<span data-ttu-id="1ff9f-110">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1ff9f-110">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ff9f-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ff9f-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ff9f-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="1ff9f-112">Reference</span></span>

[<span data-ttu-id="1ff9f-113">Класс JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="1ff9f-113">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="1ff9f-114">Элементы JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="1ff9f-114">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="1ff9f-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1ff9f-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
