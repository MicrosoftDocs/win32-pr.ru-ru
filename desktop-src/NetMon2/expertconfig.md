---
description: Структура ЕКСПЕРТКОНФИГ содержит данные конфигурации эксперта. Эксперт накладывает элемент Равконфигдата на структуру, относящуюся к эксперту.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Структура ЕКСПЕРТКОНФИГ (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662207"
---
# <a name="expertconfig-structure"></a><span data-ttu-id="f673c-104">Структура ЕКСПЕРТКОНФИГ</span><span class="sxs-lookup"><span data-stu-id="f673c-104">EXPERTCONFIG structure</span></span>

<span data-ttu-id="f673c-105">Структура **експертконфиг** содержит данные конфигурации эксперта.</span><span class="sxs-lookup"><span data-stu-id="f673c-105">The **EXPERTCONFIG** structure contains the configuration data of the expert.</span></span> <span data-ttu-id="f673c-106">Эксперт накладывает элемент **равконфигдата** на структуру, относящуюся к эксперту.</span><span class="sxs-lookup"><span data-stu-id="f673c-106">The expert overlays the **RawConfigData** member with an expert-specific structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f673c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f673c-107">Syntax</span></span>


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a><span data-ttu-id="f673c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f673c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f673c-109">**равконфигленгс**</span><span class="sxs-lookup"><span data-stu-id="f673c-109">**RawConfigLength**</span></span>
</dt> <dd>

<span data-ttu-id="f673c-110">Общая длина структуры, включая четыре байта, используемые для элемента.</span><span class="sxs-lookup"><span data-stu-id="f673c-110">Total length of the structure, including the four bytes used for the member.</span></span> <span data-ttu-id="f673c-111">Сетевой монитор использует значение при сохранении структуры на диске и при чтении с диска.</span><span class="sxs-lookup"><span data-stu-id="f673c-111">Network Monitor uses the value when the structure is saved-to and read-from a disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="f673c-112">**равконфигдата**</span><span class="sxs-lookup"><span data-stu-id="f673c-112">**RawConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="f673c-113">Данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f673c-113">Configuration data.</span></span> <span data-ttu-id="f673c-114">Эксперт должен добавить данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="f673c-114">The expert must add the configuration data.</span></span> <span data-ttu-id="f673c-115">Например, предположим, что у вас есть структура данных, похожая на эту.</span><span class="sxs-lookup"><span data-stu-id="f673c-115">For example, suppose that you had a data structure that looked like this.</span></span>

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

<span data-ttu-id="f673c-116">Обратите внимание, что **равконфигленгс** обеспечивает правильную работу оверлея.</span><span class="sxs-lookup"><span data-stu-id="f673c-116">Note that **RawConfigLength** ensures that the overlay works correctly.</span></span> <span data-ttu-id="f673c-117">При использовании данных код может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f673c-117">When you use the data, your code might look like this:</span></span>

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f673c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f673c-118">Requirements</span></span>



| <span data-ttu-id="f673c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f673c-119">Requirement</span></span> | <span data-ttu-id="f673c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f673c-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f673c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f673c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f673c-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f673c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f673c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f673c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f673c-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f673c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f673c-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f673c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f673c-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f673c-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




