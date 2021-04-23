---
description: 'Дополнительные сведения о свойстве: SystemParameters. Качесиземакс'
title: SystemParameters. Качесиземакс, свойство
TOCTitle: 'CacheSizeMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesizemax(v=EXCHG.10)
ms:contentKeyID: 55104037
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7b03df288a0263cf6b79281f5ed79330dfd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272391"
---
# <a name="systemparameterscachesizemax-property"></a><span data-ttu-id="e0ce1-103">SystemParameters. Качесиземакс, свойство</span><span class="sxs-lookup"><span data-stu-id="e0ce1-103">SystemParameters.CacheSizeMax property</span></span>

<span data-ttu-id="e0ce1-104">Возвращает или задает максимальный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-104">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="e0ce1-105">Размер находится в страницах базы данных.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-105">The size is in database pages.</span></span> <span data-ttu-id="e0ce1-106">Если этот параметр оставлен со значением по умолчанию, максимальный размер кэша будет установлен в размер физической памяти при вызове Жетинит.</span><span class="sxs-lookup"><span data-stu-id="e0ce1-106">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span>

<span data-ttu-id="e0ce1-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e0ce1-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e0ce1-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e0ce1-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ce1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0ce1-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Property CacheSizeMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSizeMax

SystemParameters.CacheSizeMax = value
```

``` csharp
public static int CacheSizeMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e0ce1-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e0ce1-110">Property value</span></span>

<span data-ttu-id="e0ce1-111">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e0ce1-111">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e0ce1-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0ce1-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e0ce1-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="e0ce1-113">Reference</span></span>

[<span data-ttu-id="e0ce1-114">SystemParameters - класс</span><span class="sxs-lookup"><span data-stu-id="e0ce1-114">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="e0ce1-115">Элементы SystemParameters</span><span class="sxs-lookup"><span data-stu-id="e0ce1-115">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="e0ce1-116">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e0ce1-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
