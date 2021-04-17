---
title: Интерфейс Имсрдпклиентсекуредсеттингс
description: Содержит методы для получения и задания свойств элемента управления удаленный рабочий стол ActiveX, которые ограничены конкретными зонами безопасности URL-адресов Internet Explorer. | Интерфейс Имсрдпклиентсекуредсеттингс
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентсекуредсеттингс, описание
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674617"
---
# <a name="imsrdpclientsecuredsettings-interface"></a><span data-ttu-id="e58d6-106">Интерфейс Имсрдпклиентсекуредсеттингс</span><span class="sxs-lookup"><span data-stu-id="e58d6-106">IMsRdpClientSecuredSettings interface</span></span>

<span data-ttu-id="e58d6-107">Содержит методы для получения и задания свойств элемента управления удаленный рабочий стол ActiveX, которые ограничены конкретными зонами безопасности URL-адресов Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e58d6-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="e58d6-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="e58d6-108">Members</span></span>

<span data-ttu-id="e58d6-109">Интерфейс **имсрдпклиентсекуредсеттингс** наследует от [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="e58d6-109">The **IMsRdpClientSecuredSettings** interface inherits from [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span> <span data-ttu-id="e58d6-110">**Имсрдпклиентсекуредсеттингс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e58d6-110">**IMsRdpClientSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="e58d6-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e58d6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e58d6-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e58d6-112">Properties</span></span>

<span data-ttu-id="e58d6-113">Интерфейс **имсрдпклиентсекуредсеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e58d6-113">The **IMsRdpClientSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="e58d6-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="e58d6-114">Property</span></span>                                                                                   | <span data-ttu-id="e58d6-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="e58d6-115">Access type</span></span>           | <span data-ttu-id="e58d6-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e58d6-116">Description</span></span>                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="e58d6-117">**аудиоредиректионмоде**</span><span class="sxs-lookup"><span data-stu-id="e58d6-117">**AudioRedirectionMode**</span></span>](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | <span data-ttu-id="e58d6-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e58d6-118">Read/write</span></span><br/> | <span data-ttu-id="e58d6-119">Параметры перенаправления звука.</span><span class="sxs-lookup"><span data-stu-id="e58d6-119">The audio redirection settings.</span></span><br/>    |
| [<span data-ttu-id="e58d6-120">**кэйбоардхукмоде**</span><span class="sxs-lookup"><span data-stu-id="e58d6-120">**KeyboardHookMode**</span></span>](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | <span data-ttu-id="e58d6-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e58d6-121">Read/write</span></span><br/> | <span data-ttu-id="e58d6-122">Параметры перенаправления клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="e58d6-122">The keyboard redirection settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e58d6-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e58d6-123">Remarks</span></span>

<span data-ttu-id="e58d6-124">Эти свойства не могут быть заданы при соединении элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e58d6-124">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="e58d6-125">Дополнительные сведения о методах этого интерфейса см. в разделе [предоставление для безопасности клиента RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="e58d6-125">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="e58d6-126">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e58d6-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e58d6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e58d6-127">Requirements</span></span>



| <span data-ttu-id="e58d6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e58d6-128">Requirement</span></span> | <span data-ttu-id="e58d6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e58d6-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e58d6-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e58d6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e58d6-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e58d6-131">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="e58d6-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e58d6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e58d6-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e58d6-133">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="e58d6-134">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e58d6-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="e58d6-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e58d6-135"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e58d6-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e58d6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e58d6-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e58d6-137"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="e58d6-138">IID</span><span class="sxs-lookup"><span data-stu-id="e58d6-138">IID</span></span><br/>                      | <span data-ttu-id="e58d6-139">IID \_ имсрдпклиентсекуредсеттингс определен как 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="e58d6-139">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e58d6-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e58d6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e58d6-141">**имстсксекуредсеттингс**</span><span class="sxs-lookup"><span data-stu-id="e58d6-141">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e58d6-142">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="e58d6-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





