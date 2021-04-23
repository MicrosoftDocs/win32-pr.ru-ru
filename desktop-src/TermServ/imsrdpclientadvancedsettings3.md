---
title: Интерфейс IMsRdpClientAdvancedSettings3
description: Управляет дополнительными параметрами клиента. Является производным от интерфейса IMsRdpClientAdvancedSettings2.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760ae7d40742a800556b3d62bc5a1609b89c986b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802159"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a><span data-ttu-id="36dde-106">Интерфейс IMsRdpClientAdvancedSettings3</span><span class="sxs-lookup"><span data-stu-id="36dde-106">IMsRdpClientAdvancedSettings3 interface</span></span>

<span data-ttu-id="36dde-107">Управляет дополнительными параметрами клиента.</span><span class="sxs-lookup"><span data-stu-id="36dde-107">Manages advanced client settings.</span></span> <span data-ttu-id="36dde-108">Является производным от интерфейса [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="36dde-108">Derives from the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="36dde-109">Этот интерфейс включает методы для получения и задания дополнительных (необязательных) свойств для удаленный рабочий стол элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="36dde-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="36dde-110">Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="36dde-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="36dde-111">Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings3** в **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="36dde-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings3** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="36dde-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="36dde-112">Members</span></span>

<span data-ttu-id="36dde-113">Интерфейс **IMsRdpClientAdvancedSettings3** наследует от [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="36dde-113">The **IMsRdpClientAdvancedSettings3** interface inherits from [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span></span> <span data-ttu-id="36dde-114">**IMsRdpClientAdvancedSettings3** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="36dde-114">**IMsRdpClientAdvancedSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="36dde-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="36dde-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36dde-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="36dde-116">Properties</span></span>

<span data-ttu-id="36dde-117">Интерфейс **IMsRdpClientAdvancedSettings3** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="36dde-117">The **IMsRdpClientAdvancedSettings3** interface has these properties.</span></span>



| <span data-ttu-id="36dde-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="36dde-118">Property</span></span>                                                                                                            | <span data-ttu-id="36dde-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="36dde-119">Access type</span></span>           | <span data-ttu-id="36dde-120">Описание</span><span class="sxs-lookup"><span data-stu-id="36dde-120">Description</span></span>                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="36dde-121">**коннектионбаршовминимизебуттон**</span><span class="sxs-lookup"><span data-stu-id="36dde-121">**ConnectionBarShowMinimizeButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | <span data-ttu-id="36dde-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="36dde-122">Read/write</span></span><br/> | <span data-ttu-id="36dde-123">Указывает, отображать ли кнопку **сворачивания** на панели подключения.</span><span class="sxs-lookup"><span data-stu-id="36dde-123">Specifies whether to display the **Minimize** button on the connection bar.</span></span><br/> |
| [<span data-ttu-id="36dde-124">**коннектионбаршовресторебуттон**</span><span class="sxs-lookup"><span data-stu-id="36dde-124">**ConnectionBarShowRestoreButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | <span data-ttu-id="36dde-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="36dde-125">Read/write</span></span><br/> | <span data-ttu-id="36dde-126">Указывает, следует ли отображать кнопку **восстановить** на панели подключения.</span><span class="sxs-lookup"><span data-stu-id="36dde-126">Specifies whether to display the **Restore** button on the connection bar.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="36dde-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36dde-127">Remarks</span></span>

<span data-ttu-id="36dde-128">Этот интерфейс расширен следующими интерфейсами, при этом каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="36dde-128">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="36dde-129">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="36dde-129">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="36dde-130">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="36dde-130">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="36dde-131">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="36dde-131">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="36dde-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="36dde-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="36dde-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="36dde-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

<span data-ttu-id="36dde-134">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="36dde-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36dde-135">Требования</span><span class="sxs-lookup"><span data-stu-id="36dde-135">Requirements</span></span>



| <span data-ttu-id="36dde-136">Требование</span><span class="sxs-lookup"><span data-stu-id="36dde-136">Requirement</span></span> | <span data-ttu-id="36dde-137">Значение</span><span class="sxs-lookup"><span data-stu-id="36dde-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36dde-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36dde-138">Minimum supported client</span></span><br/> | <span data-ttu-id="36dde-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36dde-139">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="36dde-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36dde-140">Minimum supported server</span></span><br/> | <span data-ttu-id="36dde-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36dde-141">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="36dde-142">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="36dde-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="36dde-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36dde-143"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="36dde-144">DLL</span><span class="sxs-lookup"><span data-stu-id="36dde-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36dde-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36dde-145"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="36dde-146">IID</span><span class="sxs-lookup"><span data-stu-id="36dde-146">IID</span></span><br/>                      | <span data-ttu-id="36dde-147">IID \_ IMsRdpClientAdvancedSettings3 определен как 19cd856b-C542-4c53-ACee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="36dde-147">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36dde-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36dde-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36dde-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="36dde-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="36dde-150">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="36dde-150">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="36dde-151">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="36dde-151">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="36dde-152">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="36dde-152">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

