---
title: Функция Ртмблоккделетераутес (RTM. h)
description: Функция Ртмблоккделетераутес удаляет все маршруты в указанном подмножестве маршрутов в таблице.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- RAS функции Ртмблоккделетераутес
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491403"
---
# <a name="rtmblockdeleteroutes-function"></a><span data-ttu-id="b240e-104">Функция Ртмблоккделетераутес</span><span class="sxs-lookup"><span data-stu-id="b240e-104">RtmBlockDeleteRoutes function</span></span>

<span data-ttu-id="b240e-105">\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b240e-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="b240e-106">Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]</span><span class="sxs-lookup"><span data-stu-id="b240e-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="b240e-107">Функция **ртмблоккделетераутес** удаляет все маршруты в указанном подмножестве маршрутов в таблице.</span><span class="sxs-lookup"><span data-stu-id="b240e-107">The **RtmBlockDeleteRoutes** function deletes all routes in the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b240e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b240e-108">Syntax</span></span>


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="b240e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b240e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b240e-110">*Клиенсандле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b240e-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b240e-111">Обработчик, идентифицирующий клиента и, следовательно, протокол маршрутизации удаляемых маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b240e-111">Handle that identifies the client, and therefore the routing protocol, of the routes to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="b240e-112">*Енумератионфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b240e-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b240e-113">Указывает, какие маршруты следует перечислить.</span><span class="sxs-lookup"><span data-stu-id="b240e-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="b240e-114">Этот параметр ограничивает набор удаленных маршрутов подмножеством, определенным следующими флагами, и значениями в соответствующих элементах структуры, на которые указывает параметр *критериарауте* .</span><span class="sxs-lookup"><span data-stu-id="b240e-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="b240e-115">Флаги аналогичны параметрам, используемым в [**ртмкреатинумератионхандле**](rtmcreateenumerationhandle.md) , за исключением того, что RTM \_ только \_ лучшие \_ маршруты являются избыточными для **ртмблоккделетераутес**.</span><span class="sxs-lookup"><span data-stu-id="b240e-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) except that RTM\_ONLY\_BEST\_ROUTES is redundant for **RtmBlockDeleteRoutes**.</span></span> <span data-ttu-id="b240e-116">Наилучшее направление маршрута корректируется по мере удаления маршрутов, поэтому функция в конечном итоге удаляет все маршруты в подмножестве.</span><span class="sxs-lookup"><span data-stu-id="b240e-116">The best-route designation is adjusted as routes are deleted, so the function eventually deletes all the routes in the subset.</span></span>

</dd> <dt>

<span data-ttu-id="b240e-117">*Критериарауте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b240e-117">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b240e-118">Указатель на структуру маршрута для конкретного семейства протоколов ( [**RTM \_ - \_ маршрут IP**](rtm-ip-route.md) или [**\_ \_ маршрут RTM IPX**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="b240e-118">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="b240e-119">Значения элементов в этой структуре соответствуют флагам, заданным параметром *енумератионфлагс* .</span><span class="sxs-lookup"><span data-stu-id="b240e-119">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b240e-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b240e-120">Return value</span></span>

<span data-ttu-id="b240e-121">Если функция выполнена удачно, возвращается значение NO \_ Error.</span><span class="sxs-lookup"><span data-stu-id="b240e-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="b240e-122">Если функция завершается ошибкой, возвращаемое значение является одним из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="b240e-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="b240e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b240e-123">Value</span></span>                                                                                                       | <span data-ttu-id="b240e-124">Описание</span><span class="sxs-lookup"><span data-stu-id="b240e-124">Description</span></span>                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b240e-125"><dt>**ОШИБКИ \_ нет \_ маршрутов**</dt></span><span class="sxs-lookup"><span data-stu-id="b240e-125"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="b240e-126">Нет маршрутов с указанными критериями.</span><span class="sxs-lookup"><span data-stu-id="b240e-126">There are no routes that have the specified criteria.</span></span><br/>                                           |
| <dl> <span data-ttu-id="b240e-127"><dt>**Ошибка \_ недопустимого \_ маркера**</dt></span><span class="sxs-lookup"><span data-stu-id="b240e-127"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="b240e-128">Недопустимый параметр *клиенсандле* .</span><span class="sxs-lookup"><span data-stu-id="b240e-128">The *ClientHandle* parameter is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="b240e-129"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="b240e-129"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="b240e-130">Один или несколько входных параметров недопустимы, например, недопустимые флаги перечисления.</span><span class="sxs-lookup"><span data-stu-id="b240e-130">One or more of the input parameters is invalid, for example, the enumeration flags are invalid.</span></span><br/> |
| <dl> <span data-ttu-id="b240e-131"><dt>**\_нет \_ системных \_ ресурсов**</dt></span><span class="sxs-lookup"><span data-stu-id="b240e-131"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="b240e-132">Недостаточно ресурсов для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="b240e-132">There are insufficient resources to carry out the operation.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b240e-133"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="b240e-133"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="b240e-134">Недостаточно памяти для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="b240e-134">There is insufficient memory to carry out the operation.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="b240e-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b240e-135">Remarks</span></span>

<span data-ttu-id="b240e-136">Функция создает соответствующие сообщения уведомления для всех зарегистрированных клиентов, включая вызывающего.</span><span class="sxs-lookup"><span data-stu-id="b240e-136">The function generates appropriate notification messages to all registered clients including the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="b240e-137">Требования</span><span class="sxs-lookup"><span data-stu-id="b240e-137">Requirements</span></span>



| <span data-ttu-id="b240e-138">Требование</span><span class="sxs-lookup"><span data-stu-id="b240e-138">Requirement</span></span> | <span data-ttu-id="b240e-139">Значение</span><span class="sxs-lookup"><span data-stu-id="b240e-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b240e-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b240e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b240e-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b240e-141">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b240e-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b240e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b240e-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b240e-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b240e-144">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b240e-144">End of server support</span></span><br/>    | <span data-ttu-id="b240e-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b240e-145">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="b240e-146">Header</span><span class="sxs-lookup"><span data-stu-id="b240e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="b240e-147"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b240e-147"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="b240e-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b240e-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="b240e-149"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b240e-149"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="b240e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b240e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b240e-151"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b240e-151"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b240e-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b240e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b240e-153">Справочник по диспетчеру таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="b240e-153">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="b240e-154">Функции диспетчера таблиц маршрутизации версии 1</span><span class="sxs-lookup"><span data-stu-id="b240e-154">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="b240e-155">**ртмкреатинумератионхандле**</span><span class="sxs-lookup"><span data-stu-id="b240e-155">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="b240e-156">**ртмрегистерклиент**</span><span class="sxs-lookup"><span data-stu-id="b240e-156">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





