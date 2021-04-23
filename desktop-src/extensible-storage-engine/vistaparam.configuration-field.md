---
description: 'Дополнительные сведения о: VistaParam.Configполе фигурации'
title: VistaParam.Configполе фигурации (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b330afb7158c616ba7bb9683a7bbe226d8d63542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808422"
---
# <a name="vistaparamconfiguration-field"></a><span data-ttu-id="9a865-103">VistaParam.Configполе фигурации</span><span class="sxs-lookup"><span data-stu-id="9a865-103">VistaParam.Configuration field</span></span>

<span data-ttu-id="9a865-104">Этот параметр предоставляет несколько наборов значений по умолчанию для всего набора системных параметров.</span><span class="sxs-lookup"><span data-stu-id="9a865-104">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="9a865-105">Если для этого параметра задана определенная конфигурация, все значения системных параметров сбрасываются в значения по умолчанию для этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9a865-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="9a865-106">Если конфигурация задана для конкретного экземпляра, глобальные системные параметры не будут сбрасываться к значениям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9a865-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="9a865-107">Небольшая конфигурация (0). ядро СУБД оптимизировано для использования памяти.</span><span class="sxs-lookup"><span data-stu-id="9a865-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="9a865-108">Устаревшая конфигурация (1). в ядре СУБД установлены традиционные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9a865-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="9a865-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9a865-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="9a865-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9a865-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9a865-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a865-111">Syntax</span></span>

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a><span data-ttu-id="9a865-112">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a865-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9a865-113">Справочник</span><span class="sxs-lookup"><span data-stu-id="9a865-113">Reference</span></span>

[<span data-ttu-id="9a865-114">Класс Вистапарам</span><span class="sxs-lookup"><span data-stu-id="9a865-114">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="9a865-115">Элементы Вистапарам</span><span class="sxs-lookup"><span data-stu-id="9a865-115">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="9a865-116">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="9a865-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
