---
description: 'Дополнительные сведения о свойстве: SystemParameters. Енаблеадванцед'
title: SystemParameters. Енаблеадванцед, свойство
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e311685bf5ef436be11d4593523aceee73b955b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712725"
---
# <a name="systemparametersenableadvanced-property"></a><span data-ttu-id="22e5e-103">SystemParameters. Енаблеадванцед, свойство</span><span class="sxs-lookup"><span data-stu-id="22e5e-103">SystemParameters.EnableAdvanced property</span></span>

<span data-ttu-id="22e5e-104">Возвращает или задает значение, указывающее, принимает ли ядро СУБД изменения, внесенные в подмножество системных параметров, или отклоняет их.</span><span class="sxs-lookup"><span data-stu-id="22e5e-104">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="22e5e-105">Этот параметр используется вместе с [конфигурацией](./systemparameters.configuration-property.md) , чтобы предотвратить установку некоторых параметров системы из значений по умолчанию выбранной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="22e5e-105">This parameter is used in conjunction with [Configuration](./systemparameters.configuration-property.md) to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="22e5e-106">Поддерживается в Windows Vista и выше.</span><span class="sxs-lookup"><span data-stu-id="22e5e-106">Supported on Windows Vista and up.</span></span> <span data-ttu-id="22e5e-107">Игнорируется в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="22e5e-107">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="22e5e-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="22e5e-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="22e5e-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="22e5e-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="22e5e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22e5e-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="22e5e-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="22e5e-111">Property value</span></span>

<span data-ttu-id="22e5e-112">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="22e5e-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="22e5e-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22e5e-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="22e5e-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="22e5e-114">Reference</span></span>

[<span data-ttu-id="22e5e-115">SystemParameters - класс</span><span class="sxs-lookup"><span data-stu-id="22e5e-115">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="22e5e-116">Элементы SystemParameters</span><span class="sxs-lookup"><span data-stu-id="22e5e-116">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="22e5e-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="22e5e-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
