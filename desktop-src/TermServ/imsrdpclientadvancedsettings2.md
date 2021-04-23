---
title: Интерфейс IMsRdpClientAdvancedSettings2
description: Управляет дополнительными параметрами клиента. Является производным от интерфейса Имсрдпклиентадванцедсеттингс.
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d7f9ad9b93c0f3cd1d62fdbbaddf4faa55ad9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340875"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a><span data-ttu-id="be6e2-106">Интерфейс IMsRdpClientAdvancedSettings2</span><span class="sxs-lookup"><span data-stu-id="be6e2-106">IMsRdpClientAdvancedSettings2 interface</span></span>

<span data-ttu-id="be6e2-107">Управляет дополнительными параметрами клиента.</span><span class="sxs-lookup"><span data-stu-id="be6e2-107">Manages advanced client settings.</span></span> <span data-ttu-id="be6e2-108">Является производным от интерфейса [**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="be6e2-108">Derives from the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="be6e2-109">Этот интерфейс включает методы для получения и задания дополнительных (необязательных) свойств для удаленный рабочий стол элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="be6e2-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="be6e2-110">Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="be6e2-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="be6e2-111">Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings2** в **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="be6e2-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings2** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="be6e2-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="be6e2-112">Members</span></span>

<span data-ttu-id="be6e2-113">Интерфейс **IMsRdpClientAdvancedSettings2** наследует от [**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="be6e2-113">The **IMsRdpClientAdvancedSettings2** interface inherits from [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span></span> <span data-ttu-id="be6e2-114">**IMsRdpClientAdvancedSettings2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be6e2-114">**IMsRdpClientAdvancedSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="be6e2-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="be6e2-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be6e2-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="be6e2-116">Properties</span></span>

<span data-ttu-id="be6e2-117">Интерфейс **IMsRdpClientAdvancedSettings2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be6e2-117">The **IMsRdpClientAdvancedSettings2** interface has these properties.</span></span>



| <span data-ttu-id="be6e2-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="be6e2-118">Property</span></span>                                                                                      | <span data-ttu-id="be6e2-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="be6e2-119">Access type</span></span>           | <span data-ttu-id="be6e2-120">Описание</span><span class="sxs-lookup"><span data-stu-id="be6e2-120">Description</span></span>                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be6e2-121">**канаутореконнект**</span><span class="sxs-lookup"><span data-stu-id="be6e2-121">**CanAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | <span data-ttu-id="be6e2-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="be6e2-122">Read-only</span></span><br/>  | <span data-ttu-id="be6e2-123">Указывает, может ли клиентский элемент управления автоматически подключаться к текущему сеансу в случае отключения от сети.</span><span class="sxs-lookup"><span data-stu-id="be6e2-123">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span><br/>    |
| [<span data-ttu-id="be6e2-124">**енаблеаутореконнект**</span><span class="sxs-lookup"><span data-stu-id="be6e2-124">**EnableAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | <span data-ttu-id="be6e2-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="be6e2-125">Read/write</span></span><br/> | <span data-ttu-id="be6e2-126">Указывает, следует ли включить клиентский элемент управления для автоматического подключения к сеансу в случае отключения от сети.</span><span class="sxs-lookup"><span data-stu-id="be6e2-126">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span><br/>            |
| [<span data-ttu-id="be6e2-127">**максреконнектаттемптс**</span><span class="sxs-lookup"><span data-stu-id="be6e2-127">**MaxReconnectAttempts**</span></span>](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | <span data-ttu-id="be6e2-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="be6e2-128">Read/write</span></span><br/> | <span data-ttu-id="be6e2-129">Указывает количество повторных попыток подключения во время автоматического повторного подключения.</span><span class="sxs-lookup"><span data-stu-id="be6e2-129">Specifies the number of times to try to reconnect during automatic reconnection.</span></span> <span data-ttu-id="be6e2-130">Допустимые значения этого свойства: от 0 до 200 включительно.</span><span class="sxs-lookup"><span data-stu-id="be6e2-130">The valid values of this property are 0 to 200 inclusive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="be6e2-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be6e2-131">Remarks</span></span>

<span data-ttu-id="be6e2-132">Этот интерфейс расширен следующими интерфейсами, при этом каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="be6e2-132">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="be6e2-133">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="be6e2-133">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
-   [<span data-ttu-id="be6e2-134">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="be6e2-134">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="be6e2-135">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="be6e2-135">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="be6e2-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="be6e2-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="be6e2-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="be6e2-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="be6e2-138">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="be6e2-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be6e2-139">Требования</span><span class="sxs-lookup"><span data-stu-id="be6e2-139">Requirements</span></span>



| <span data-ttu-id="be6e2-140">Требование</span><span class="sxs-lookup"><span data-stu-id="be6e2-140">Requirement</span></span> | <span data-ttu-id="be6e2-141">Значение</span><span class="sxs-lookup"><span data-stu-id="be6e2-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be6e2-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be6e2-142">Minimum supported client</span></span><br/> | <span data-ttu-id="be6e2-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be6e2-143">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="be6e2-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be6e2-144">Minimum supported server</span></span><br/> | <span data-ttu-id="be6e2-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be6e2-145">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="be6e2-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="be6e2-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="be6e2-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be6e2-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="be6e2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="be6e2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be6e2-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be6e2-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="be6e2-150">IID</span><span class="sxs-lookup"><span data-stu-id="be6e2-150">IID</span></span><br/>                      | <span data-ttu-id="be6e2-151">IID \_ IMsRdpClientAdvancedSettings2 определен как 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="be6e2-151">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be6e2-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be6e2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6e2-153">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="be6e2-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="be6e2-154">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="be6e2-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="be6e2-155">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="be6e2-155">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

