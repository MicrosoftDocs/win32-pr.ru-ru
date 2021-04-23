---
description: 'Дополнительные сведения о свойстве: SystemParameters. Енаблевиевкаче'
title: SystemParameters. Енаблевиевкаче, свойство
TOCTitle: 'EnableViewCache property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableViewCache
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableviewcache(v=EXCHG.10)
ms:contentKeyID: 55104120
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableViewCache
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableViewCache
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableViewCache
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableViewCache
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b22808109b8fd69df18b9a6ae98de17a814b5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272984"
---
# <a name="systemparametersenableviewcache-property"></a><span data-ttu-id="9f129-103">SystemParameters. Енаблевиевкаче, свойство</span><span class="sxs-lookup"><span data-stu-id="9f129-103">SystemParameters.EnableViewCache property</span></span>

<span data-ttu-id="9f129-104">Возвращает или задает значение, указывающее, следует ли ядру СУБД использовать файловый ввод-вывод, размещенный в памяти, для файлов базы данных.</span><span class="sxs-lookup"><span data-stu-id="9f129-104">Gets or sets a value indicating whether the database engine should use memory mapped file I/O for database files.</span></span>

<span data-ttu-id="9f129-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f129-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9f129-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9f129-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f129-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f129-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EnableViewCache As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableViewCache

SystemParameters.EnableViewCache = value
```

``` csharp
public static bool EnableViewCache { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="9f129-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9f129-108">Property value</span></span>

<span data-ttu-id="9f129-109">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="9f129-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9f129-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f129-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f129-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="9f129-111">Reference</span></span>

[<span data-ttu-id="9f129-112">SystemParameters - класс</span><span class="sxs-lookup"><span data-stu-id="9f129-112">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="9f129-113">Элементы SystemParameters</span><span class="sxs-lookup"><span data-stu-id="9f129-113">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="9f129-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9f129-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
