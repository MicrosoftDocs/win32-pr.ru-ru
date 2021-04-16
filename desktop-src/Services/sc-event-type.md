---
description: Указывает тип изменения состояния службы для мониторинга и создания отчетов.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: Перечисление SC_EVENT_TYPE (Винсвкп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664463"
---
# <a name="sc_event_type-enumeration"></a><span data-ttu-id="bbe9d-103">\_ \_ Перечисление типов событий SC</span><span class="sxs-lookup"><span data-stu-id="bbe9d-103">SC\_EVENT\_TYPE enumeration</span></span>

<span data-ttu-id="bbe9d-104">Указывает тип изменения состояния службы для мониторинга и создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="bbe9d-104">Indicates a type of service status change for monitoring and reporting.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbe9d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbe9d-105">Syntax</span></span>


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="bbe9d-106">Константы</span><span class="sxs-lookup"><span data-stu-id="bbe9d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bbe9d-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**\_ \_ изменение базы данных событий SC \_**</span><span class="sxs-lookup"><span data-stu-id="bbe9d-107"><span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**SC\_EVENT\_DATABASE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-108">Служба была добавлена или удалена.</span><span class="sxs-lookup"><span data-stu-id="bbe9d-108">A service has been added or deleted.</span></span> <span data-ttu-id="bbe9d-109">Параметр *хсервице* функции [**субскрибесервицечанженотификатионс**](subscribeservicechangenotifications.md) должен быть обработчиком SCM.</span><span class="sxs-lookup"><span data-stu-id="bbe9d-109">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the SCM.</span></span>

</dd> <dt>

<span data-ttu-id="bbe9d-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**\_ \_ изменение свойства события \_ SC**</span><span class="sxs-lookup"><span data-stu-id="bbe9d-110"><span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**SC\_EVENT\_PROPERTY\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-111">Одно или несколько свойств службы были обновлены.</span><span class="sxs-lookup"><span data-stu-id="bbe9d-111">One or more of service properties have been updated.</span></span> <span data-ttu-id="bbe9d-112">Параметр *хсервице* функции [**субскрибесервицечанженотификатионс**](subscribeservicechangenotifications.md) должен быть маркером службы.</span><span class="sxs-lookup"><span data-stu-id="bbe9d-112">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> <dt>

<span data-ttu-id="bbe9d-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**\_ \_ изменение состояния события \_ SC**</span><span class="sxs-lookup"><span data-stu-id="bbe9d-113"><span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**SC\_EVENT\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="bbe9d-114">Состояние службы изменилось.</span><span class="sxs-lookup"><span data-stu-id="bbe9d-114">The status of a service has changed.</span></span> <span data-ttu-id="bbe9d-115">Параметр *хсервице* функции [**субскрибесервицечанженотификатионс**](subscribeservicechangenotifications.md) должен быть маркером службы.</span><span class="sxs-lookup"><span data-stu-id="bbe9d-115">The *hService* parameter of the [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) function must be a handle to the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bbe9d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="bbe9d-116">Requirements</span></span>



| <span data-ttu-id="bbe9d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="bbe9d-117">Requirement</span></span> | <span data-ttu-id="bbe9d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bbe9d-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe9d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbe9d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bbe9d-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bbe9d-120">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="bbe9d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbe9d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bbe9d-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bbe9d-122">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="bbe9d-123">Header</span><span class="sxs-lookup"><span data-stu-id="bbe9d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbe9d-124"><dt>Винсвкп. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbe9d-124"><dt>Winsvcp.h</dt></span></span> </dl> |



 

 




