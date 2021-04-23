---
description: 'Дополнительные сведения: SystemParameters.Configсвойство фигурации'
title: SystemParameters.Config, свойство фигурации
TOCTitle: 'Configuration property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.configuration(v=EXCHG.10)
ms:contentKeyID: 55104117
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.set_Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.get_Configuration
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5eaa387f63df1dd91641ff38f2a6f6450629fe99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910220"
---
# <a name="systemparametersconfiguration-property"></a><span data-ttu-id="0fc32-103">SystemParameters.Config, свойство фигурации</span><span class="sxs-lookup"><span data-stu-id="0fc32-103">SystemParameters.Configuration property</span></span>

<span data-ttu-id="0fc32-104">Возвращает или задает значение, указывающее значения по умолчанию для всего набора системных параметров.</span><span class="sxs-lookup"><span data-stu-id="0fc32-104">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="0fc32-105">Если для этого параметра задана определенная конфигурация, все значения системных параметров сбрасываются в значения по умолчанию для этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="0fc32-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="0fc32-106">Если конфигурация задана для конкретного экземпляра, глобальные системные параметры не будут сбрасываться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0fc32-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="0fc32-107">Небольшая конфигурация (0). ядро СУБД оптимизировано для использования памяти.</span><span class="sxs-lookup"><span data-stu-id="0fc32-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="0fc32-108">Устаревшая конфигурация (1). в ядре СУБД установлены традиционные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0fc32-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="0fc32-109">Поддерживается в Windows Vista и выше.</span><span class="sxs-lookup"><span data-stu-id="0fc32-109">Supported on Windows Vista and up.</span></span> <span data-ttu-id="0fc32-110">Игнорируется в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0fc32-110">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="0fc32-111">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0fc32-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0fc32-112">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0fc32-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0fc32-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fc32-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property Configuration As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.Configuration

SystemParameters.Configuration = value
```

``` csharp
public static int Configuration { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="0fc32-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0fc32-114">Property value</span></span>

<span data-ttu-id="0fc32-115">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0fc32-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0fc32-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fc32-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0fc32-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="0fc32-117">Reference</span></span>

[<span data-ttu-id="0fc32-118">SystemParameters - класс</span><span class="sxs-lookup"><span data-stu-id="0fc32-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="0fc32-119">Элементы SystemParameters</span><span class="sxs-lookup"><span data-stu-id="0fc32-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="0fc32-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0fc32-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
