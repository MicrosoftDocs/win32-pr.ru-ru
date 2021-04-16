---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Макстемпораритаблес'
title: Инстанцепараметерс. Макстемпораритаблес, свойство
TOCTitle: 'MaxTemporaryTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtemporarytables(v=EXCHG.10)
ms:contentKeyID: 55103560
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTemporaryTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5802e512a4ea6a4916ae54c24357dbdad057540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712453"
---
# <a name="instanceparametersmaxtemporarytables-property"></a><span data-ttu-id="529d5-103">Инстанцепараметерс. Макстемпораритаблес, свойство</span><span class="sxs-lookup"><span data-stu-id="529d5-103">InstanceParameters.MaxTemporaryTables property</span></span>

<span data-ttu-id="529d5-104">Возвращает или задает количество временных ресурсов таблицы для использования экземпляром.</span><span class="sxs-lookup"><span data-stu-id="529d5-104">Gets or sets the number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="529d5-105">Этот параметр влияет на количество временных таблиц, которые можно использовать одновременно.</span><span class="sxs-lookup"><span data-stu-id="529d5-105">This setting will affect how many temporary tables can be used at the same time.</span></span> <span data-ttu-id="529d5-106">Если этот системный параметр имеет значение 0, то временная база данных не будет создана и любое действие, требующее использования временной базы данных, завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="529d5-106">If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="529d5-107">Этот параметр может быть полезен, чтобы избежать операций ввода-вывода, необходимых для создания временной базы данных, если известно, что она не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="529d5-107">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="529d5-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="529d5-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="529d5-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="529d5-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="529d5-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="529d5-110">Syntax</span></span>

``` vb
'Declaration
Public Property MaxTemporaryTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTemporaryTables

instance.MaxTemporaryTables = value
```

``` csharp
public int MaxTemporaryTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="529d5-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="529d5-111">Property value</span></span>

<span data-ttu-id="529d5-112">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="529d5-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="remarks"></a><span data-ttu-id="529d5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="529d5-113">Remarks</span></span>

<span data-ttu-id="529d5-114">Для использования временной таблицы также требуется ресурс курсора.</span><span class="sxs-lookup"><span data-stu-id="529d5-114">The use of a temporary table also requires a cursor resource.</span></span>

## <a name="see-also"></a><span data-ttu-id="529d5-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="529d5-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="529d5-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="529d5-116">Reference</span></span>

[<span data-ttu-id="529d5-117">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="529d5-117">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="529d5-118">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="529d5-118">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="529d5-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="529d5-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
