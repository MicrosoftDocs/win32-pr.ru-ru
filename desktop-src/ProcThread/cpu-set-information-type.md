---
description: Представляет тип сведений в \_ \_ структуре сведений о наборе ЦП системы \_ .
ms.assetid: B42CB8E8-0010-4B11-AB0D-6D196DCCC90A
title: Перечисление CPU_SET_INFORMATION_TYPE (Процесссреадапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPU_SET_INFORMATION_TYPE
api_type:
- HeaderDef
api_location:
- Processthreadapi.h
ms.openlocfilehash: 0283275856e8e68bf983aaeb9a7660a5a0a6bf59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673773"
---
# <a name="cpu_set_information_type-enumeration"></a><span data-ttu-id="fece3-103">\_ \_ Перечисление типов сведений о НАБОРе ЦП \_</span><span class="sxs-lookup"><span data-stu-id="fece3-103">CPU\_SET\_INFORMATION\_TYPE enumeration</span></span>

<span data-ttu-id="fece3-104">Представляет тип сведений в структуре [**\_ \_ \_ сведений о наборе ЦП системы**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) .</span><span class="sxs-lookup"><span data-stu-id="fece3-104">Represents the type of information in the [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fece3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fece3-105">Syntax</span></span>


```C++
typedef enum _CPU_SET_INFORMATION_TYPE { 
  CpuSetInformation
} CPU_SET_INFORMATION_TYPE, *PCPU_SET_INFORMATION_TYPE;
```



## <a name="constants"></a><span data-ttu-id="fece3-106">Константы</span><span class="sxs-lookup"><span data-stu-id="fece3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fece3-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**кпусетинформатион**</span><span class="sxs-lookup"><span data-stu-id="fece3-107"><span id="CpuSetInformation"></span><span id="cpusetinformation"></span><span id="CPUSETINFORMATION"></span>**CpuSetInformation**</span></span>
</dt> <dd>

<span data-ttu-id="fece3-108">Структура содержит сведения о наборе ЦП.</span><span class="sxs-lookup"><span data-stu-id="fece3-108">The structure contains CPU Set information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fece3-109">Требования</span><span class="sxs-lookup"><span data-stu-id="fece3-109">Requirements</span></span>



| <span data-ttu-id="fece3-110">Требование</span><span class="sxs-lookup"><span data-stu-id="fece3-110">Requirement</span></span> | <span data-ttu-id="fece3-111">Значение</span><span class="sxs-lookup"><span data-stu-id="fece3-111">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fece3-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fece3-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fece3-113">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fece3-113">Windows 10 \[desktop apps only\]</span></span><br/>                                                                       |
| <span data-ttu-id="fece3-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fece3-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fece3-115">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="fece3-115">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fece3-116">Header</span><span class="sxs-lookup"><span data-stu-id="fece3-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="fece3-117"><dt>Процесссреадсапи. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fece3-117"><dt>Processthreadsapi.h (include Windows.h)</dt></span></span> </dl> |



 

 




