---
title: Интерфейс IMsRdpClientAdvancedSettings6
description: Отображает свойства, управляющие дополнительными параметрами элементов управления ActiveX.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681939"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a><span data-ttu-id="c92d1-105">Интерфейс IMsRdpClientAdvancedSettings6</span><span class="sxs-lookup"><span data-stu-id="c92d1-105">IMsRdpClientAdvancedSettings6 interface</span></span>

<span data-ttu-id="c92d1-106">Отображает свойства, управляющие дополнительными параметрами элементов управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="c92d1-106">Exposes properties that manage advanced ActiveX control settings.</span></span> <span data-ttu-id="c92d1-107">Интерфейс **IMsRdpClientAdvancedSettings6** является производным от интерфейса [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="c92d1-107">The **IMsRdpClientAdvancedSettings6** interface is derived from the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="c92d1-108">Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="c92d1-108">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="c92d1-109">Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings6** в **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="c92d1-109">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings6** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="c92d1-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="c92d1-110">Members</span></span>

<span data-ttu-id="c92d1-111">Интерфейс **IMsRdpClientAdvancedSettings6** наследует от [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span><span class="sxs-lookup"><span data-stu-id="c92d1-111">The **IMsRdpClientAdvancedSettings6** interface inherits from [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span></span> <span data-ttu-id="c92d1-112">**IMsRdpClientAdvancedSettings6** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c92d1-112">**IMsRdpClientAdvancedSettings6** also has these types of members:</span></span>

-   [<span data-ttu-id="c92d1-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c92d1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c92d1-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c92d1-114">Properties</span></span>

<span data-ttu-id="c92d1-115">Интерфейс **IMsRdpClientAdvancedSettings6** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c92d1-115">The **IMsRdpClientAdvancedSettings6** interface has these properties.</span></span>



| <span data-ttu-id="c92d1-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="c92d1-116">Property</span></span>                                                                                                  | <span data-ttu-id="c92d1-117">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="c92d1-117">Access type</span></span>           | <span data-ttu-id="c92d1-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c92d1-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c92d1-119">**аусентикатионсервицекласс**</span><span class="sxs-lookup"><span data-stu-id="c92d1-119">**AuthenticationServiceClass**</span></span>](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | <span data-ttu-id="c92d1-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c92d1-120">Read/write</span></span><br/> | <span data-ttu-id="c92d1-121">Указывает имя участника-службы (SPN), используемое для проверки подлинности на сервере.</span><span class="sxs-lookup"><span data-stu-id="c92d1-121">Specifies the service principal name (SPN) to use for authentication to the server.</span></span><br/>                                     |
| [<span data-ttu-id="c92d1-122">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="c92d1-122">**AuthenticationType**</span></span>](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | <span data-ttu-id="c92d1-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="c92d1-123">Read-only</span></span><br/>  | <span data-ttu-id="c92d1-124">Указывает тип проверки подлинности, используемый для этого соединения.</span><span class="sxs-lookup"><span data-stu-id="c92d1-124">Specifies the type of authentication used for this connection.</span></span><br/>                                                          |
| [<span data-ttu-id="c92d1-125">**коннекттоадминистерсервер**</span><span class="sxs-lookup"><span data-stu-id="c92d1-125">**ConnectToAdministerServer**</span></span>](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | <span data-ttu-id="c92d1-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c92d1-126">Read/write</span></span><br/> | <span data-ttu-id="c92d1-127">Возвращает или задает значение, указывающее, должен ли элемент управления ActiveX пытаться подключиться к серверу для административных целей.</span><span class="sxs-lookup"><span data-stu-id="c92d1-127">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span><br/> |
| [<span data-ttu-id="c92d1-128">**енаблекредсспсуппорт**</span><span class="sxs-lookup"><span data-stu-id="c92d1-128">**EnableCredSspSupport**</span></span>](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | <span data-ttu-id="c92d1-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c92d1-129">Read/write</span></span><br/> | <span data-ttu-id="c92d1-130">Указывает, включен ли поставщик службы безопасности учетных данных (CredSSP) для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="c92d1-130">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span><br/>                    |
| [<span data-ttu-id="c92d1-131">**хоткэйфокусрелеаселефт**</span><span class="sxs-lookup"><span data-stu-id="c92d1-131">**HotKeyFocusReleaseLeft**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | <span data-ttu-id="c92d1-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c92d1-132">Read/write</span></span><br/> | <span data-ttu-id="c92d1-133">Задает код виртуального ключа, добавляемый в сочетание клавиш CTRL + ALT для определения замены с помощью сочетания клавиш CTRL + ALT + стрелка влево.</span><span class="sxs-lookup"><span data-stu-id="c92d1-133">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+LEFT ARROW.</span></span><br/>          |
| [<span data-ttu-id="c92d1-134">**хоткэйфокусрелеасеригхт**</span><span class="sxs-lookup"><span data-stu-id="c92d1-134">**HotKeyFocusReleaseRight**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | <span data-ttu-id="c92d1-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c92d1-135">Read/write</span></span><br/> | <span data-ttu-id="c92d1-136">Указывает код виртуального ключа, добавляемый в сочетание клавиш CTRL + ALT для определения замены с помощью сочетания клавиш CTRL + ALT + стрелка вправо.</span><span class="sxs-lookup"><span data-stu-id="c92d1-136">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+RIGHT ARROW.</span></span><br/>         |
| [<span data-ttu-id="c92d1-137">**пкб**</span><span class="sxs-lookup"><span data-stu-id="c92d1-137">**PCB**</span></span>](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | <span data-ttu-id="c92d1-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c92d1-138">Read/write</span></span><br/> | <span data-ttu-id="c92d1-139">Задает параметр предварительного подключения BLOB-объекта (ПКБ), используемый перед подключением для передачи на сервер.</span><span class="sxs-lookup"><span data-stu-id="c92d1-139">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/>               |
| [<span data-ttu-id="c92d1-140">**релативемаусемоде**</span><span class="sxs-lookup"><span data-stu-id="c92d1-140">**RelativeMouseMode**</span></span>](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | <span data-ttu-id="c92d1-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c92d1-141">Read/write</span></span><br/> | <span data-ttu-id="c92d1-142">Указывает, следует ли использовать относительный режим для мыши.</span><span class="sxs-lookup"><span data-stu-id="c92d1-142">Specifies whether the mouse should use relative mode.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="c92d1-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c92d1-143">Remarks</span></span>

<span data-ttu-id="c92d1-144">Этот интерфейс расширен интерфейсом [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) , который наследует все методы и свойства предыдущих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="c92d1-144">This interface has been extended by the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface, inheriting all the methods and properties of the previous interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="c92d1-145">Требования</span><span class="sxs-lookup"><span data-stu-id="c92d1-145">Requirements</span></span>



| <span data-ttu-id="c92d1-146">Требование</span><span class="sxs-lookup"><span data-stu-id="c92d1-146">Requirement</span></span> | <span data-ttu-id="c92d1-147">Значение</span><span class="sxs-lookup"><span data-stu-id="c92d1-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c92d1-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c92d1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c92d1-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c92d1-149">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="c92d1-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c92d1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c92d1-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c92d1-151">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="c92d1-152">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="c92d1-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="c92d1-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c92d1-153"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c92d1-154">DLL</span><span class="sxs-lookup"><span data-stu-id="c92d1-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c92d1-155"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c92d1-155"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c92d1-156">IID</span><span class="sxs-lookup"><span data-stu-id="c92d1-156">IID</span></span><br/>                      | <span data-ttu-id="c92d1-157">IID \_ IMsRdpClientAdvancedSettings6 определен как 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="c92d1-157">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c92d1-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c92d1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c92d1-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c92d1-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c92d1-160">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c92d1-160">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c92d1-161">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c92d1-161">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="c92d1-162">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c92d1-162">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c92d1-163">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="c92d1-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c92d1-164">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="c92d1-164">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

