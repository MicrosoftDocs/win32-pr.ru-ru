---
description: '\_Класс NIC хвконфиг является классом типа событий для событий конфигурации сетевых интерфейсных карт. Следующий синтаксис упрощен из MOF-кода.'
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: Класс HWConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: df3897c67ed65eeec5ace49dac1088ca35223a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081374"
---
# <a name="hwconfig_nic-class"></a><span data-ttu-id="30483-104">\_Класс сетевого адаптера хвконфиг</span><span class="sxs-lookup"><span data-stu-id="30483-104">HWConfig\_NIC class</span></span>

<span data-ttu-id="30483-105">Класс **\_ NIC хвконфиг** является классом типа событий для событий конфигурации сетевых интерфейсных карт.</span><span class="sxs-lookup"><span data-stu-id="30483-105">The **HWConfig\_NIC** class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="30483-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="30483-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="30483-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30483-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a><span data-ttu-id="30483-108">Участники</span><span class="sxs-lookup"><span data-stu-id="30483-108">Members</span></span>

<span data-ttu-id="30483-109">Класс **\_ сетевого адаптера хвконфиг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="30483-109">The **HWConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="30483-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="30483-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30483-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="30483-111">Properties</span></span>

<span data-ttu-id="30483-112">Класс **\_ сетевого адаптера хвконфиг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="30483-112">The **HWConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30483-113">NICName</span><span class="sxs-lookup"><span data-stu-id="30483-113">NICName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30483-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="30483-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30483-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="30483-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30483-116">Квалификаторы: Вмидатаид (1), Стрингтерминатион ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="30483-116">Qualifiers: WmiDataId(1), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="30483-117">Имя сетевой карты.</span><span class="sxs-lookup"><span data-stu-id="30483-117">Name of the network interface card.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30483-118">Требования</span><span class="sxs-lookup"><span data-stu-id="30483-118">Requirements</span></span>



| <span data-ttu-id="30483-119">Требование</span><span class="sxs-lookup"><span data-stu-id="30483-119">Requirement</span></span> | <span data-ttu-id="30483-120">Значение</span><span class="sxs-lookup"><span data-stu-id="30483-120">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="30483-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30483-121">Minimum supported client</span></span><br/> | <span data-ttu-id="30483-122">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="30483-122">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="30483-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30483-123">Minimum supported server</span></span><br/> | <span data-ttu-id="30483-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="30483-124">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="30483-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30483-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30483-126">**хвконфиг**</span><span class="sxs-lookup"><span data-stu-id="30483-126">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




