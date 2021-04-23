---
title: Интерфейс Имстсксекуредсеттингс
description: Содержит методы для получения и задания свойств элемента управления удаленный рабочий стол ActiveX, которые ограничены конкретными зонами безопасности URL-адресов Internet Explorer. | Интерфейс Имстсксекуредсеттингс
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имстсксекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имстсксекуредсеттингс, описание
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684876"
---
# <a name="imstscsecuredsettings-interface"></a><span data-ttu-id="77b1b-106">Интерфейс Имстсксекуредсеттингс</span><span class="sxs-lookup"><span data-stu-id="77b1b-106">IMsTscSecuredSettings interface</span></span>

<span data-ttu-id="77b1b-107">Содержит методы для получения и задания свойств элемента управления удаленный рабочий стол ActiveX, которые ограничены конкретными зонами безопасности URL-адресов Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="77b1b-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="77b1b-108">К свойствам относятся те, которые задают режим клиентского элемента управления (полноэкранный режим или оконный режим) и программу, запускаемую при подключении к серверу узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="77b1b-108">Properties include those that specify the mode of the client control (full-screen mode or window mode) and the program to start upon connection to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="77b1b-109">Эти методы также доступны через интерфейс [**имсрдпклиентсекуредсеттингс**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="77b1b-109">These methods are also available through the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="77b1b-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="77b1b-110">Members</span></span>

<span data-ttu-id="77b1b-111">Интерфейс **имстсксекуредсеттингс** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="77b1b-111">The **IMsTscSecuredSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="77b1b-112">**Имстсксекуредсеттингс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="77b1b-112">**IMsTscSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="77b1b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="77b1b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77b1b-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="77b1b-114">Properties</span></span>

<span data-ttu-id="77b1b-115">Интерфейс **имстсксекуредсеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="77b1b-115">The **IMsTscSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="77b1b-116">Свойство</span><span class="sxs-lookup"><span data-stu-id="77b1b-116">Property</span></span>                                                              | <span data-ttu-id="77b1b-117">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="77b1b-117">Access type</span></span>           | <span data-ttu-id="77b1b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="77b1b-118">Description</span></span>                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="77b1b-119">**FullScreen**</span><span class="sxs-lookup"><span data-stu-id="77b1b-119">**FullScreen**</span></span>](imstscsecuredsettings-fullscreen.md)<br/>     | <span data-ttu-id="77b1b-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="77b1b-120">Read/write</span></span><br/> | <span data-ttu-id="77b1b-121">Полноэкранное состояние клиентского элемента управления.</span><span class="sxs-lookup"><span data-stu-id="77b1b-121">The full-screen state of the client control.</span></span><br/>                    |
| [<span data-ttu-id="77b1b-122">**стартпрограм**</span><span class="sxs-lookup"><span data-stu-id="77b1b-122">**StartProgram**</span></span>](imstscsecuredsettings-startprogram.md)<br/> | <span data-ttu-id="77b1b-123">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="77b1b-123">Read/write</span></span><br/> | <span data-ttu-id="77b1b-124">Программа, запускаемая на удаленном сервере при подключении.</span><span class="sxs-lookup"><span data-stu-id="77b1b-124">The program to be started on the remote server upon connection.</span></span><br/> |
| [<span data-ttu-id="77b1b-125">**WorkDir**</span><span class="sxs-lookup"><span data-stu-id="77b1b-125">**WorkDir**</span></span>](imstscsecuredsettings-workdir.md)<br/>           | <span data-ttu-id="77b1b-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="77b1b-126">Read/write</span></span><br/> | <span data-ttu-id="77b1b-127">Рабочий каталог запускаемой программы.</span><span class="sxs-lookup"><span data-stu-id="77b1b-127">The working directory of the start program.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="77b1b-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77b1b-128">Remarks</span></span>

<span data-ttu-id="77b1b-129">Дополнительные сведения о методах этого интерфейса см. в разделе [предоставление для безопасности клиента RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="77b1b-129">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="77b1b-130">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="77b1b-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77b1b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="77b1b-131">Requirements</span></span>



| <span data-ttu-id="77b1b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="77b1b-132">Requirement</span></span> | <span data-ttu-id="77b1b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="77b1b-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77b1b-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77b1b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="77b1b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77b1b-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="77b1b-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77b1b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="77b1b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77b1b-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="77b1b-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="77b1b-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="77b1b-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77b1b-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="77b1b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="77b1b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77b1b-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77b1b-141"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77b1b-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77b1b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b1b-143">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="77b1b-143">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="77b1b-144">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="77b1b-144">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

