---
title: Интерфейс IMsRdpClientNonScriptable6
description: Предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса IMsRdpClientNonScriptable5.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable6
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable6, описание
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "104416361"
---
# <a name="imsrdpclientnonscriptable6-interface"></a><span data-ttu-id="ec8c3-106">Интерфейс IMsRdpClientNonScriptable6</span><span class="sxs-lookup"><span data-stu-id="ec8c3-106">IMsRdpClientNonScriptable6 interface</span></span>

<span data-ttu-id="ec8c3-107">Предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="ec8c3-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="ec8c3-108">Является производным от интерфейса [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) .</span><span class="sxs-lookup"><span data-stu-id="ec8c3-108">Derives from the [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) interface.</span></span> <span data-ttu-id="ec8c3-109">Доступ к методам этого интерфейса возможен только через таблицу vtable; они недоступны для использования в сценариях клиентов.</span><span class="sxs-lookup"><span data-stu-id="ec8c3-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="ec8c3-110">Экземпляр этого интерфейса получен путем вызова [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для объекта [**имстскакс**](imstscax-interface.md) , передавая **IID \_ IMsRdpClientNonScriptable6**.</span><span class="sxs-lookup"><span data-stu-id="ec8c3-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable6**.</span></span>

## <a name="members"></a><span data-ttu-id="ec8c3-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="ec8c3-111">Members</span></span>

<span data-ttu-id="ec8c3-112">Интерфейс **IMsRdpClientNonScriptable6** наследует от [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="ec8c3-112">The **IMsRdpClientNonScriptable6** interface inherits from [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="ec8c3-113">**IMsRdpClientNonScriptable6** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ec8c3-113">**IMsRdpClientNonScriptable6** also has these types of members:</span></span>

- [<span data-ttu-id="ec8c3-114">Методы</span><span class="sxs-lookup"><span data-stu-id="ec8c3-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ec8c3-115">Методы</span><span class="sxs-lookup"><span data-stu-id="ec8c3-115">Methods</span></span>

<span data-ttu-id="ec8c3-116">Интерфейс **IMsRdpClientNonScriptable6** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ec8c3-116">The **IMsRdpClientNonScriptable6** interface has these methods.</span></span>


| <span data-ttu-id="ec8c3-117">Метод</span><span class="sxs-lookup"><span data-stu-id="ec8c3-117">Method</span></span>            | <span data-ttu-id="ec8c3-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ec8c3-118">Description</span></span>                   |
|:-----------------------------|:-----------------|
| [<span data-ttu-id="ec8c3-119">**SendLocation2D**</span><span class="sxs-lookup"><span data-stu-id="ec8c3-119">**SendLocation2D**</span></span>](imsrdpclientnonscriptable6-sendlocation2d.md)     |  <span data-ttu-id="ec8c3-120">Отправляет на сервер значение широты и долготы, благодаря чему географическое расположение клиента может быть отражено в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="ec8c3-120">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                   |
| [<span data-ttu-id="ec8c3-121">**SendLocation3D**</span><span class="sxs-lookup"><span data-stu-id="ec8c3-121">**SendLocation3D**</span></span>](imsrdpclientnonscriptable6-sendlocation3d.md)     | <span data-ttu-id="ec8c3-122">Отправляет на сервер значение широты, долготы и высоты, чтобы географическое расположение клиента можно было отражать в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="ec8c3-122">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                 |

## <a name="requirements"></a><span data-ttu-id="ec8c3-123">Требования</span><span class="sxs-lookup"><span data-stu-id="ec8c3-123">Requirements</span></span>

| <span data-ttu-id="ec8c3-124">Требование</span><span class="sxs-lookup"><span data-stu-id="ec8c3-124">Requirement</span></span> | <span data-ttu-id="ec8c3-125">Значение</span><span class="sxs-lookup"><span data-stu-id="ec8c3-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="ec8c3-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec8c3-126">Minimum supported client</span></span>| <span data-ttu-id="ec8c3-127">Windows 10, версия 1709 (сборка 16299)</span><span class="sxs-lookup"><span data-stu-id="ec8c3-127">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="ec8c3-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ec8c3-128">Type library</span></span>            | <span data-ttu-id="ec8c3-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ec8c3-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="ec8c3-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ec8c3-130">DLL</span></span>                  | <span data-ttu-id="ec8c3-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ec8c3-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="ec8c3-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="ec8c3-132">CLSID</span></span>                    | <span data-ttu-id="ec8c3-133">\_MSRDPCLIENT12 CLSID определен как 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="ec8c3-133">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="ec8c3-134">\_MSRDPCLIENT12NOTSAFEFORSCRIPTING CLSID определен как 3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="ec8c3-134">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="ec8c3-135">\_MSRDPCLIENT11 CLSID определен как 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="ec8c3-135">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="ec8c3-136">\_MSRDPCLIENT11NOTSAFEFORSCRIPTING CLSID определен как 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="ec8c3-136">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="ec8c3-137">IID</span><span class="sxs-lookup"><span data-stu-id="ec8c3-137">IID</span></span>                      | <span data-ttu-id="ec8c3-138">IID \_ IMsRdpClientNonScriptable6 определен как 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="ec8c3-138">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="ec8c3-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec8c3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec8c3-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="ec8c3-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>
