---
description: Структура КОНФИГУРЕДЕКСПЕРТ связывает эксперт с данными конфигурации.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Структура КОНФИГУРЕДЕКСПЕРТ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264698"
---
# <a name="configuredexpert-structure"></a><span data-ttu-id="9669a-103">Структура КОНФИГУРЕДЕКСПЕРТ</span><span class="sxs-lookup"><span data-stu-id="9669a-103">CONFIGUREDEXPERT structure</span></span>

<span data-ttu-id="9669a-104">Структура **конфигуредексперт** связывает эксперт с данными конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9669a-104">The **CONFIGUREDEXPERT** structure associates an expert with its configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9669a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9669a-105">Syntax</span></span>


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a><span data-ttu-id="9669a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9669a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9669a-107">**хексперт**</span><span class="sxs-lookup"><span data-stu-id="9669a-107">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="9669a-108">Обрабатывайте эксперта.</span><span class="sxs-lookup"><span data-stu-id="9669a-108">Handle to an expert.</span></span>

</dd> <dt>

<span data-ttu-id="9669a-109">**StartupFlags**</span><span class="sxs-lookup"><span data-stu-id="9669a-109">**StartupFlags**</span></span>
</dt> <dd>

<span data-ttu-id="9669a-110">Значения флага запуска эксперта.</span><span class="sxs-lookup"><span data-stu-id="9669a-110">Startup flag values of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="9669a-111">**pConfig**</span><span class="sxs-lookup"><span data-stu-id="9669a-111">**pConfig**</span></span>
</dt> <dd>

<span data-ttu-id="9669a-112">Указатель на структуру [**експертконфиг**](expertconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="9669a-112">Pointer to an [**EXPERTCONFIG**](expertconfig.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9669a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9669a-113">Requirements</span></span>



| <span data-ttu-id="9669a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9669a-114">Requirement</span></span> | <span data-ttu-id="9669a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9669a-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9669a-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9669a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9669a-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9669a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9669a-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9669a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9669a-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9669a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9669a-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9669a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9669a-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9669a-121"><dt>Netmon.h</dt></span></span> </dl> |



 

 




