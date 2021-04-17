---
title: Интерфейс IMsRdpClientAdvancedSettings4
description: Управляет дополнительными параметрами клиента. Является производным от интерфейса IMsRdpClientAdvancedSettings3.
ms.assetid: cb1785d6-1f94-4423-bdda-0e3e4e9b8641
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, описание
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d840206a139e3c3272551eab6a187a7b18416e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415464"
---
# <a name="imsrdpclientadvancedsettings4-interface"></a><span data-ttu-id="f2bd9-106">Интерфейс IMsRdpClientAdvancedSettings4</span><span class="sxs-lookup"><span data-stu-id="f2bd9-106">IMsRdpClientAdvancedSettings4 interface</span></span>

<span data-ttu-id="f2bd9-107">Управляет дополнительными параметрами клиента.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-107">Manages advanced client settings.</span></span> <span data-ttu-id="f2bd9-108">Является производным от интерфейса [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="f2bd9-108">Derives from the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="f2bd9-109">Этот интерфейс включает методы для получения и задания дополнительных (необязательных) свойств для удаленный рабочий стол элемента управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="f2bd9-110">Чтобы получить экземпляр этого интерфейса, используйте свойство [**имстскакс:: адванцедсеттингс**](imstscax-advancedsettings.md) для получения указателя на интерфейс [**имстскадванцедсеттингс**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="f2bd9-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="f2bd9-111">Затем вызовите [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в указателе **имстскадванцедсеттингс** и передайте **IID \_ IMsRdpClientAdvancedSettings4** в **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings4** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="f2bd9-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="f2bd9-112">Members</span></span>

<span data-ttu-id="f2bd9-113">Интерфейс **IMsRdpClientAdvancedSettings4** наследует от [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span><span class="sxs-lookup"><span data-stu-id="f2bd9-113">The **IMsRdpClientAdvancedSettings4** interface inherits from [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span></span> <span data-ttu-id="f2bd9-114">**IMsRdpClientAdvancedSettings4** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f2bd9-114">**IMsRdpClientAdvancedSettings4** also has these types of members:</span></span>

-   [<span data-ttu-id="f2bd9-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2bd9-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2bd9-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2bd9-116">Properties</span></span>

<span data-ttu-id="f2bd9-117">Интерфейс **IMsRdpClientAdvancedSettings4** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-117">The **IMsRdpClientAdvancedSettings4** interface has these properties.</span></span>



| <span data-ttu-id="f2bd9-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="f2bd9-118">Property</span></span>                                                                                    | <span data-ttu-id="f2bd9-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="f2bd9-119">Access type</span></span>           | <span data-ttu-id="f2bd9-120">Описание</span><span class="sxs-lookup"><span data-stu-id="f2bd9-120">Description</span></span>                                                              |
|:--------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="f2bd9-121">**аусентикатионлевел**</span><span class="sxs-lookup"><span data-stu-id="f2bd9-121">**AuthenticationLevel**</span></span>](imsrdpclientadvancedsettings4-authenticationlevel.md)<br/> | <span data-ttu-id="f2bd9-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="f2bd9-122">Read/write</span></span><br/> | <span data-ttu-id="f2bd9-123">Указывает уровень проверки подлинности, используемый для соединения.</span><span class="sxs-lookup"><span data-stu-id="f2bd9-123">Specifies the authentication level to use for the connection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f2bd9-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f2bd9-124">Remarks</span></span>

<span data-ttu-id="f2bd9-125">Этот интерфейс расширен следующими интерфейсами, при этом каждый новый интерфейс наследует все методы и свойства предыдущих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="f2bd9-125">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="f2bd9-126">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f2bd9-126">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="f2bd9-127">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f2bd9-127">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="f2bd9-128">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f2bd9-128">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="f2bd9-129">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f2bd9-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2bd9-130">Требования</span><span class="sxs-lookup"><span data-stu-id="f2bd9-130">Requirements</span></span>



| <span data-ttu-id="f2bd9-131">Требование</span><span class="sxs-lookup"><span data-stu-id="f2bd9-131">Requirement</span></span> | <span data-ttu-id="f2bd9-132">Значение</span><span class="sxs-lookup"><span data-stu-id="f2bd9-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2bd9-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2bd9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f2bd9-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2bd9-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="f2bd9-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2bd9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f2bd9-136">Windows Server 2008, Windows Server 2008 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="f2bd9-136">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="f2bd9-137">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="f2bd9-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2bd9-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2bd9-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="f2bd9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f2bd9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2bd9-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2bd9-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="f2bd9-141">IID</span><span class="sxs-lookup"><span data-stu-id="f2bd9-141">IID</span></span><br/>                      | <span data-ttu-id="f2bd9-142">IID \_ IMsRdpClientAdvancedSettings4 определяется как FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="f2bd9-142">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2bd9-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2bd9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2bd9-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f2bd9-144">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="f2bd9-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f2bd9-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f2bd9-146">**имсрдпклиентадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f2bd9-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f2bd9-147">**имстскадванцедсеттингс**</span><span class="sxs-lookup"><span data-stu-id="f2bd9-147">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f2bd9-148">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="f2bd9-148">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

