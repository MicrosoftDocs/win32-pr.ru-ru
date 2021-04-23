---
title: Структура IPX_SPECIFIC_DATA (RTM. h)
description: '\_Структура данных, относящаяся к IPX, \_ содержит данные, относящиеся к IPX.'
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- RAS структуры IPX_SPECIFIC_DATA
- RAS — указатель структуры PIPX_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988164"
---
# <a name="ipx_specific_data-structure"></a><span data-ttu-id="a300f-105">\_Структура данных, характерная для IPX \_</span><span class="sxs-lookup"><span data-stu-id="a300f-105">IPX\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="a300f-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a300f-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="a300f-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="a300f-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="a300f-108">Структура **\_ \_ данных, относящаяся к IPX** , содержит данные, относящиеся к IPX.</span><span class="sxs-lookup"><span data-stu-id="a300f-108">The **IPX\_SPECIFIC\_DATA** structure contains IPX-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a300f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a300f-109">Syntax</span></span>


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="a300f-110">Члены</span><span class="sxs-lookup"><span data-stu-id="a300f-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="a300f-111">**\_Флаги ФСД**</span><span class="sxs-lookup"><span data-stu-id="a300f-111">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a300f-112">Задает флаги, описывающие маршрут.</span><span class="sxs-lookup"><span data-stu-id="a300f-112">Specifies flags that describe the route.</span></span> <span data-ttu-id="a300f-113">В настоящее время этот элемент либо равен нулю, либо имеет следующее значение флага.</span><span class="sxs-lookup"><span data-stu-id="a300f-113">Currently, this member is either zero or the following flag value.</span></span>



| <span data-ttu-id="a300f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a300f-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="a300f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a300f-115">Meaning</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <span data-ttu-id="a300f-116"><dt>**Глобальный IPX- \_ \_ \_ маршрут глобальной сети \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a300f-116"><dt>**IPX\_GLOBAL\_CLIENT\_WAN\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="a300f-117">Указывает, что этот маршрут предназначен для глобальной сети, выделенной для всех клиентов глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="a300f-117">Specifies that this route is for the global network allocated for all WAN clients.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a300f-118">**ФСДое \_ TickCount**</span><span class="sxs-lookup"><span data-stu-id="a300f-118">**FSD\_TickCount**</span></span>
</dt> <dd>

<span data-ttu-id="a300f-119">Указывает число тактов, необходимое для достижения целевой сети.</span><span class="sxs-lookup"><span data-stu-id="a300f-119">Specifies the number of ticks it takes to reach the destination network.</span></span> <span data-ttu-id="a300f-120">Протоколы маршрутизации, отличные от RIP, должны преобразовывать свои метрики в такты.</span><span class="sxs-lookup"><span data-stu-id="a300f-120">Routing protocols other than RIP should convert their metrics into ticks.</span></span>

</dd> <dt>

<span data-ttu-id="a300f-121">**ФСД \_ хопкаунт**</span><span class="sxs-lookup"><span data-stu-id="a300f-121">**FSD\_HopCount**</span></span>
</dt> <dd>

<span data-ttu-id="a300f-122">Указывает число прыжков, связанное с маршрутом.</span><span class="sxs-lookup"><span data-stu-id="a300f-122">Specifies the hop count associated with the route.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a300f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a300f-123">Requirements</span></span>



| <span data-ttu-id="a300f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a300f-124">Requirement</span></span> | <span data-ttu-id="a300f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a300f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a300f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a300f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a300f-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a300f-127">None supported</span></span><br/>                                                        |
| <span data-ttu-id="a300f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a300f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a300f-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a300f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a300f-130">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a300f-130">End of server support</span></span><br/>    | <span data-ttu-id="a300f-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a300f-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="a300f-132">Header</span><span class="sxs-lookup"><span data-stu-id="a300f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a300f-133"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a300f-133"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a300f-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a300f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a300f-135">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="a300f-135">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="a300f-136">Структуры диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="a300f-136">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="a300f-137">**\_маршрут IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="a300f-137">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





