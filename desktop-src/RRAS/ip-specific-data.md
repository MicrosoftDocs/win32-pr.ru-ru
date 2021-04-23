---
title: Структура IP_SPECIFIC_DATA (RTM. h)
description: Структура данных, относящаяся к конкретному IP-адресу, \_ содержит данные, относящиеся к IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- RAS структуры IP_SPECIFIC_DATA
- RAS — указатель структуры PIP_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136563"
---
# <a name="ip_specific_data-structure"></a><span data-ttu-id="27470-105">\_Структура данных для конкретного IP-адреса \_</span><span class="sxs-lookup"><span data-stu-id="27470-105">IP\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="27470-106">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="27470-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="27470-107">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="27470-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="27470-108">Структура **\_ данных, относящаяся** к конкретному IP-адресу, содержит данные, относящиеся к IP.</span><span class="sxs-lookup"><span data-stu-id="27470-108">The **IP\_SPECIFIC DATA** structure contains IP-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="27470-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27470-109">Syntax</span></span>


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="27470-110">Члены</span><span class="sxs-lookup"><span data-stu-id="27470-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="27470-111">**\_Тип ФСД**</span><span class="sxs-lookup"><span data-stu-id="27470-111">**FSD\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="27470-112">Указывает тип маршрута, как определено в [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="27470-112">Specifies the route type as defined in [RFC 1354](routing-protocols-request-for-comments.md).</span></span> <span data-ttu-id="27470-113">В следующей таблице показаны возможные значения для этого элемента.</span><span class="sxs-lookup"><span data-stu-id="27470-113">The following table shows the possible values for this member.</span></span>



| <span data-ttu-id="27470-114">Член</span><span class="sxs-lookup"><span data-stu-id="27470-114">Member</span></span>                                                                                               | <span data-ttu-id="27470-115">Значение</span><span class="sxs-lookup"><span data-stu-id="27470-115">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="27470-116"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="27470-116"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="27470-117">Тип маршрута не указан.</span><span class="sxs-lookup"><span data-stu-id="27470-117">The route type is not specified.</span></span> <span data-ttu-id="27470-118">Тип отличается от перечисленных здесь.</span><span class="sxs-lookup"><span data-stu-id="27470-118">The type is different from those listed here.</span></span><br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <span data-ttu-id="27470-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="27470-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="27470-120">Недопустимый маршрут.</span><span class="sxs-lookup"><span data-stu-id="27470-120">The route is invalid.</span></span> <span data-ttu-id="27470-121">Обычно это значение используется для аннулирования маршрута.</span><span class="sxs-lookup"><span data-stu-id="27470-121">Normally, this value is used to invalidate a route.</span></span> <span data-ttu-id="27470-122">Однако, поскольку недействительность не поддерживается диспетчером таблиц маршрутизации, маршрут по-прежнему учитывается в вычислениях наилучшего маршрута.</span><span class="sxs-lookup"><span data-stu-id="27470-122">However, since invalidation is not supported by the routing table manager, the route is still considered in best-route computations.</span></span> <span data-ttu-id="27470-123">Поэтому протоколы маршрутизации не должны использовать это значение.</span><span class="sxs-lookup"><span data-stu-id="27470-123">Therefore, routing protocols should not use this value.</span></span><br/> |
| <span id="3"></span><dl> <span data-ttu-id="27470-124"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="27470-124"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="27470-125">Маршрут является локальным маршрутом, то есть следующим прыжком является конечное назначение.</span><span class="sxs-lookup"><span data-stu-id="27470-125">The route is a local route, that is, the next hop is the final destination.</span></span><br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <span data-ttu-id="27470-126"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="27470-126"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="27470-127">Маршрут является удаленным маршрутом, т. е. следующий прыжок не является конечным назначением.</span><span class="sxs-lookup"><span data-stu-id="27470-127">The route is a remote route, that is, the next hop is not the final destination.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="27470-128">**\_Политика ФСД**</span><span class="sxs-lookup"><span data-stu-id="27470-128">**FSD\_Policy**</span></span>
</dt> <dd>

<span data-ttu-id="27470-129">Задает набор условий, которые могут привести к выбору маршрута с несколькими путями.</span><span class="sxs-lookup"><span data-stu-id="27470-129">Specifies the set of conditions that would cause the selection of a multi-path route.</span></span> <span data-ttu-id="27470-130">Этот член обычно имеет формат IP-TOS.</span><span class="sxs-lookup"><span data-stu-id="27470-130">This member is typically in IP TOS format.</span></span> <span data-ttu-id="27470-131">Дополнительные сведения см. в [документе RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="27470-131">For more information, see [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="27470-132">**ФСД \_ некссопас**</span><span class="sxs-lookup"><span data-stu-id="27470-132">**FSD\_NextHopAS**</span></span>
</dt> <dd>

<span data-ttu-id="27470-133">Указывает номер автономной системы следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="27470-133">Specifies the autonomous system number of the next hop.</span></span>

</dd> <dt>

<span data-ttu-id="27470-134">**\_Приоритет ФСД**</span><span class="sxs-lookup"><span data-stu-id="27470-134">**FSD\_Priority**</span></span>
</dt> <dd>

<span data-ttu-id="27470-135">Задает значение метрики.</span><span class="sxs-lookup"><span data-stu-id="27470-135">Specifies a metric value.</span></span> <span data-ttu-id="27470-136">Диспетчер таблиц маршрутизации использует это значение для сравнения записи маршрута с записями маршрутов, полученными от других протоколов маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="27470-136">The routing table manager uses this value to compare this route entry to route entries obtained from other routing protocols.</span></span> <span data-ttu-id="27470-137">Значение этого элемента задается диспетчером таблиц маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="27470-137">The value of this member is set by the routing table manager.</span></span>

</dd> <dt>

<span data-ttu-id="27470-138">**\_Метрика ФСД**</span><span class="sxs-lookup"><span data-stu-id="27470-138">**FSD\_Metric**</span></span>
</dt> <dd>

<span data-ttu-id="27470-139">Задает значение метрики.</span><span class="sxs-lookup"><span data-stu-id="27470-139">Specifies a metric value.</span></span> <span data-ttu-id="27470-140">Диспетчер таблиц маршрутизации использует это значение для сравнения записи маршрута с другими записями маршрутов, полученными от того же протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="27470-140">The routing table manager uses this value to compare this route entry to other route entries obtained from the same routing protocol.</span></span> <span data-ttu-id="27470-141">Значение этого элемента задается протоколом маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="27470-141">The value of this member is set by the routing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="27470-142">**ФСД \_ метрика1**</span><span class="sxs-lookup"><span data-stu-id="27470-142">**FSD\_Metric1**</span></span>
</dt> <dd>

<span data-ttu-id="27470-143">Указывает значение метрики, зависящее от протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="27470-143">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="27470-144">Это значение метрики описано в [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="27470-144">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="27470-145">**ФСД \_ Metric2**</span><span class="sxs-lookup"><span data-stu-id="27470-145">**FSD\_Metric2**</span></span>
</dt> <dd>

<span data-ttu-id="27470-146">Указывает значение метрики, зависящее от протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="27470-146">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="27470-147">Это значение метрики описано в [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="27470-147">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="27470-148">**ФСД \_ Metric3**</span><span class="sxs-lookup"><span data-stu-id="27470-148">**FSD\_Metric3**</span></span>
</dt> <dd>

<span data-ttu-id="27470-149">Указывает значение метрики, зависящее от протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="27470-149">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="27470-150">Это значение метрики описано в [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="27470-150">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="27470-151">**ФСД \_ Metric4**</span><span class="sxs-lookup"><span data-stu-id="27470-151">**FSD\_Metric4**</span></span>
</dt> <dd>

<span data-ttu-id="27470-152">Указывает значение метрики, зависящее от протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="27470-152">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="27470-153">Это значение метрики описано в [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="27470-153">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="27470-154">**ФСД \_ метрика5**</span><span class="sxs-lookup"><span data-stu-id="27470-154">**FSD\_Metric5**</span></span>
</dt> <dd>

<span data-ttu-id="27470-155">Указывает значение метрики, зависящее от протокола маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="27470-155">Specifies a routing-protocol-specific metric value.</span></span> <span data-ttu-id="27470-156">Это значение метрики описано в [RFC 1354](routing-protocols-request-for-comments.md).</span><span class="sxs-lookup"><span data-stu-id="27470-156">This metric value is documented in [RFC 1354](routing-protocols-request-for-comments.md).</span></span>

</dd> <dt>

<span data-ttu-id="27470-157">**\_Флаги ФСД**</span><span class="sxs-lookup"><span data-stu-id="27470-157">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="27470-158">Указывает, является ли маршрут допустимым.</span><span class="sxs-lookup"><span data-stu-id="27470-158">Specifies whether the route is valid.</span></span> <span data-ttu-id="27470-159">Протокол маршрутизации должен сначала снять эти флаги, а затем задать допустимый или недопустимый маршрут.</span><span class="sxs-lookup"><span data-stu-id="27470-159">The routing protocol should first clear these flags, then set the route as either valid or invalid.</span></span> <span data-ttu-id="27470-160">Для выполнения этих операций протокол маршрутизации должен использовать макросы **клеарраутефлагс ()**, **сетраутевалид ()** и **клеарраутевалид ()** .</span><span class="sxs-lookup"><span data-stu-id="27470-160">The routing protocol should use the macros **ClearRouteFlags()**, **SetRouteValid()**, and **ClearRouteValid()** to perform these operations.</span></span> <span data-ttu-id="27470-161">Эти макросы определены в RTM. h.</span><span class="sxs-lookup"><span data-stu-id="27470-161">These macros are defined in Rtm.h.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27470-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27470-162">Remarks</span></span>

<span data-ttu-id="27470-163">Диспетчер таблиц маршрутизации использует члены **\_ метрики** **ФСД \_ Priority** и ФСД для расчета наилучшего маршрута к определенной конечной сети.</span><span class="sxs-lookup"><span data-stu-id="27470-163">The routing table manager uses the **FSD\_Priority** and **FSD\_Metric** members to compute the best route to a particular destination network.</span></span>

<span data-ttu-id="27470-164">Члены **ФСД \_ метрики \[ 1-5 \]** предназначены для соответствия MIB II.</span><span class="sxs-lookup"><span data-stu-id="27470-164">The **FSD\_Metric\[1-5\]** members are for MIB II conformance.</span></span> <span data-ttu-id="27470-165">Агенты MIB II отображают только эти значения метрик.</span><span class="sxs-lookup"><span data-stu-id="27470-165">MIB II agents display only these metric values.</span></span> <span data-ttu-id="27470-166">Они не отображают значение метрики **\_ метрики ФСД** .</span><span class="sxs-lookup"><span data-stu-id="27470-166">They do not display the **FSD\_Metric** metric value.</span></span> <span data-ttu-id="27470-167">Чтобы отобразить **\_ метрику ФСД** , протокол маршрутизации также должен сохранить значение в одном из членов **ФСД \_ метрики \[ 1-5 \]** .</span><span class="sxs-lookup"><span data-stu-id="27470-167">To have the **FSD\_Metric** displayed, the routing protocol should also store the value in one of the **FSD\_Metric\[1-5\]** members.</span></span>

<span data-ttu-id="27470-168">Диспетчер таблиц маршрутизации не использует значения метрики в членах **\_ метрики ФСД \[ 1-5 \]** при вычислении наилучшего маршрута к целевой сети.</span><span class="sxs-lookup"><span data-stu-id="27470-168">The routing table manager does not use the metric values in the **FSD\_Metric\[1-5\]** members when computing the best route to a destination network.</span></span> <span data-ttu-id="27470-169">Поэтому протокол маршрутизации должен гарантировать, что элемент **\_ метрики ФСД** имеет соответствующее значение метрики.</span><span class="sxs-lookup"><span data-stu-id="27470-169">Therefore, the routing protocol should ensure that the **FSD\_Metric** member has an appropriate metric value.</span></span>

<span data-ttu-id="27470-170">Протокол маршрутизации может использовать **\_ Флаги ФСД** , чтобы пометить маршрут как недопустимый, если маршрут не должен использоваться другими протоколами маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="27470-170">A routing protocol could use the **FSD\_Flags** to mark a route as invalid, if the route should not be used by other routing protocols.</span></span>

## <a name="requirements"></a><span data-ttu-id="27470-171">Требования</span><span class="sxs-lookup"><span data-stu-id="27470-171">Requirements</span></span>



| <span data-ttu-id="27470-172">Требование</span><span class="sxs-lookup"><span data-stu-id="27470-172">Requirement</span></span> | <span data-ttu-id="27470-173">Значение</span><span class="sxs-lookup"><span data-stu-id="27470-173">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="27470-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27470-174">Minimum supported client</span></span><br/> | <span data-ttu-id="27470-175">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="27470-175">None supported</span></span><br/>                                                        |
| <span data-ttu-id="27470-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27470-176">Minimum supported server</span></span><br/> | <span data-ttu-id="27470-177">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="27470-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="27470-178">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="27470-178">End of server support</span></span><br/>    | <span data-ttu-id="27470-179">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="27470-179">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="27470-180">Header</span><span class="sxs-lookup"><span data-stu-id="27470-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="27470-181"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="27470-181"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27470-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27470-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27470-183">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="27470-183">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="27470-184">Структуры диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="27470-184">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="27470-185">**Окончательная версия \_ IP- \_ маршрута**</span><span class="sxs-lookup"><span data-stu-id="27470-185">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





