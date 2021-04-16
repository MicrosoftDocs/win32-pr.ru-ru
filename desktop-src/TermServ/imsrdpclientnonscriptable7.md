---
title: Интерфейс IMsRdpClientNonScriptable7
description: Предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX. Является производным от интерфейса IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable7
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable7, описание
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "105719222"
---
# <a name="imsrdpclientnonscriptable7-interface"></a><span data-ttu-id="3dec1-106">Интерфейс IMsRdpClientNonScriptable7</span><span class="sxs-lookup"><span data-stu-id="3dec1-106">IMsRdpClientNonScriptable7 interface</span></span>

<span data-ttu-id="3dec1-107">Предоставляет доступ к необрабатываемым свойствам удаленного сеанса клиента на удаленный рабочий стол элементе управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="3dec1-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="3dec1-108">Является производным от интерфейса [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) .</span><span class="sxs-lookup"><span data-stu-id="3dec1-108">Derives from the [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) interface.</span></span> <span data-ttu-id="3dec1-109">Доступ к методам этого интерфейса возможен только через таблицу vtable; они недоступны для использования в сценариях клиентов.</span><span class="sxs-lookup"><span data-stu-id="3dec1-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="3dec1-110">Экземпляр этого интерфейса получен путем вызова [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для объекта [**имстскакс**](imstscax-interface.md) , передавая **IID \_ IMsRdpClientNonScriptable7**.</span><span class="sxs-lookup"><span data-stu-id="3dec1-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable7**.</span></span>

## <a name="members"></a><span data-ttu-id="3dec1-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="3dec1-111">Members</span></span>

<span data-ttu-id="3dec1-112">Интерфейс **IMsRdpClientNonScriptable7** наследует от [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="3dec1-112">The **IMsRdpClientNonScriptable7** interface inherits from [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="3dec1-113">**IMsRdpClientNonScriptable7** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3dec1-113">**IMsRdpClientNonScriptable7** also has these types of members:</span></span>

- [<span data-ttu-id="3dec1-114">Методы</span><span class="sxs-lookup"><span data-stu-id="3dec1-114">Methods</span></span>](#methods)
- [<span data-ttu-id="3dec1-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="3dec1-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3dec1-116">Методы</span><span class="sxs-lookup"><span data-stu-id="3dec1-116">Methods</span></span>

<span data-ttu-id="3dec1-117">Интерфейс **IMsRdpClientNonScriptable7** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3dec1-117">The **IMsRdpClientNonScriptable7** interface has these methods.</span></span>


| <span data-ttu-id="3dec1-118">Метод</span><span class="sxs-lookup"><span data-stu-id="3dec1-118">Method</span></span>            | <span data-ttu-id="3dec1-119">Описание</span><span class="sxs-lookup"><span data-stu-id="3dec1-119">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="3dec1-120">**дисабледпикурсорскалингфорпроцесс**</span><span class="sxs-lookup"><span data-stu-id="3dec1-120">**DisableDpiCursorScalingForProcess**</span></span>](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  <span data-ttu-id="3dec1-121">Отключает локальное масштабирование курсора мыши, полученного от сервера, обеспечивая правильную визуализацию формы курсора без изменения.</span><span class="sxs-lookup"><span data-stu-id="3dec1-121">Disables local scaling of the mouse cursor received from the server, ensuring that the cursor shape is rendered correctly without modification.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="3dec1-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="3dec1-122">Properties</span></span>

<span data-ttu-id="3dec1-123">Интерфейс **IMsRdpClientNonScriptable7** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3dec1-123">The **IMsRdpClientNonScriptable7** interface has these properties.</span></span>

| <span data-ttu-id="3dec1-124">Свойство</span><span class="sxs-lookup"><span data-stu-id="3dec1-124">Property</span></span>         | <span data-ttu-id="3dec1-125">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="3dec1-125">Access type</span></span>           | <span data-ttu-id="3dec1-126">Описание</span><span class="sxs-lookup"><span data-stu-id="3dec1-126">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="3dec1-127">**камераредирконфигколлектион**</span><span class="sxs-lookup"><span data-stu-id="3dec1-127">**CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | <span data-ttu-id="3dec1-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3dec1-128">Read-only</span></span> |  <span data-ttu-id="3dec1-129">Возвращает коллекцию камер (и связанных конфигураций), доступных для перенаправления.</span><span class="sxs-lookup"><span data-stu-id="3dec1-129">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>   |
| [<span data-ttu-id="3dec1-130">**Буфер обмена**</span><span class="sxs-lookup"><span data-stu-id="3dec1-130">**Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)                       | <span data-ttu-id="3dec1-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3dec1-131">Read-only</span></span> |    <span data-ttu-id="3dec1-132">Возвращает контроллер буфера обмена, используемый для синхронизации локальных и удаленных буферов обмена, если включена ручная синхронизация буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="3dec1-132">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="3dec1-133">Требования</span><span class="sxs-lookup"><span data-stu-id="3dec1-133">Requirements</span></span>

| <span data-ttu-id="3dec1-134">Требование</span><span class="sxs-lookup"><span data-stu-id="3dec1-134">Requirement</span></span> | <span data-ttu-id="3dec1-135">Значение</span><span class="sxs-lookup"><span data-stu-id="3dec1-135">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="3dec1-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dec1-136">Minimum supported client</span></span>| <span data-ttu-id="3dec1-137">Windows 10, версия 1803 (сборка 17134)</span><span class="sxs-lookup"><span data-stu-id="3dec1-137">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="3dec1-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3dec1-138">Type library</span></span>            | <span data-ttu-id="3dec1-139">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="3dec1-139">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="3dec1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3dec1-140">DLL</span></span>                  | <span data-ttu-id="3dec1-141">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="3dec1-141">MsTscAx.dll</span></span>     |
| <span data-ttu-id="3dec1-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="3dec1-142">CLSID</span></span>                    | <span data-ttu-id="3dec1-143">\_MSRDPCLIENT12 CLSID определен как 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="3dec1-143">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="3dec1-144">\_MSRDPCLIENT12NOTSAFEFORSCRIPTING CLSID определен как 3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="3dec1-144">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="3dec1-145">\_MSRDPCLIENT11 CLSID определен как 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="3dec1-145">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="3dec1-146">\_MSRDPCLIENT11NOTSAFEFORSCRIPTING CLSID определен как 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="3dec1-146">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="3dec1-147">IID</span><span class="sxs-lookup"><span data-stu-id="3dec1-147">IID</span></span>                      | <span data-ttu-id="3dec1-148">IID \_ IMsRdpClientNonScriptable7 определен как 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="3dec1-148">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>            |

## <a name="see-also"></a><span data-ttu-id="3dec1-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dec1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dec1-150">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="3dec1-150">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
