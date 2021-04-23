---
title: Интерфейс Имсрдпклиенттранспортсеттингс
description: Управляет параметрами транспорта клиента для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов). | Интерфейс Имсрдпклиенттранспортсеттингс
ms.assetid: d2573727-1dcc-4d4d-af5c-038e9467ba84
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, описание
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec240d008ef2f9469fb67f4041cfb33c08383079
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684841"
---
# <a name="imsrdpclienttransportsettings-interface"></a><span data-ttu-id="478ed-106">Интерфейс Имсрдпклиенттранспортсеттингс</span><span class="sxs-lookup"><span data-stu-id="478ed-106">IMsRdpClientTransportSettings interface</span></span>

<span data-ttu-id="478ed-107">Управляет параметрами транспорта клиента для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="478ed-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="478ed-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="478ed-108">Members</span></span>

<span data-ttu-id="478ed-109">Интерфейс **имсрдпклиенттранспортсеттингс** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="478ed-109">The **IMsRdpClientTransportSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="478ed-110">**Имсрдпклиенттранспортсеттингс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="478ed-110">**IMsRdpClientTransportSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="478ed-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="478ed-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="478ed-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="478ed-112">Properties</span></span>

<span data-ttu-id="478ed-113">Интерфейс **имсрдпклиенттранспортсеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="478ed-113">The **IMsRdpClientTransportSettings** interface has these properties.</span></span>



| <span data-ttu-id="478ed-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="478ed-114">Property</span></span>                                                                                                          | <span data-ttu-id="478ed-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="478ed-115">Access type</span></span>           | <span data-ttu-id="478ed-116">Описание</span><span class="sxs-lookup"><span data-stu-id="478ed-116">Description</span></span>                                                 |
|:------------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------|
| [<span data-ttu-id="478ed-117">**гатевайкредссаурце**</span><span class="sxs-lookup"><span data-stu-id="478ed-117">**GatewayCredsSource**</span></span>](imsrdpclienttransportsettings-gatewaycredssource.md)<br/>                         | <span data-ttu-id="478ed-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="478ed-118">Read/write</span></span><br/> | <span data-ttu-id="478ed-119">Метод проверки подлинности сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="478ed-119">The RD Gateway server authentication method.</span></span><br/>     |
| [<span data-ttu-id="478ed-120">**гатевайдефаултусажемесод**</span><span class="sxs-lookup"><span data-stu-id="478ed-120">**GatewayDefaultUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewaydefaultusagemethod.md)<br/>           | <span data-ttu-id="478ed-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="478ed-121">Read-only</span></span><br/>  | <span data-ttu-id="478ed-122">Метод использования шлюза удаленных рабочих столов по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="478ed-122">The default RD Gateway usage method.</span></span><br/>             |
| [<span data-ttu-id="478ed-123">**гатевайхостнаме**</span><span class="sxs-lookup"><span data-stu-id="478ed-123">**GatewayHostname**</span></span>](imsrdpclienttransportsettings-gatewayhostname.md)<br/>                               | <span data-ttu-id="478ed-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="478ed-124">Read/write</span></span><br/> | <span data-ttu-id="478ed-125">Имя узла сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="478ed-125">Host name of the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="478ed-126">**гатевайиссуппортед**</span><span class="sxs-lookup"><span data-stu-id="478ed-126">**GatewayIsSupported**</span></span>](imsrdpclienttransportsettings-gatewayissupported.md)<br/>                         | <span data-ttu-id="478ed-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="478ed-127">Read-only</span></span><br/>  | <span data-ttu-id="478ed-128">Указывает, поддерживается ли шлюз удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="478ed-128">Indicates whether RD Gateway is supported.</span></span><br/>       |
| [<span data-ttu-id="478ed-129">**гатевайпрофилеусажемесод**</span><span class="sxs-lookup"><span data-stu-id="478ed-129">**GatewayProfileUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayprofileusagemethod.md)<br/>           | <span data-ttu-id="478ed-130">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="478ed-130">Read/write</span></span><br/> | <span data-ttu-id="478ed-131">Метод использования профиля шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="478ed-131">The RD Gateway profile usage method.</span></span><br/>             |
| [<span data-ttu-id="478ed-132">**гатевайусажемесод**</span><span class="sxs-lookup"><span data-stu-id="478ed-132">**GatewayUsageMethod**</span></span>](imsrdpclienttransportsettings-gatewayusagemethod.md)<br/>                         | <span data-ttu-id="478ed-133">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="478ed-133">Read/write</span></span><br/> | <span data-ttu-id="478ed-134">Метод использования сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="478ed-134">The RD Gateway server usage method.</span></span><br/>              |
| [<span data-ttu-id="478ed-135">**гатевайусерселектедкредссаурце**</span><span class="sxs-lookup"><span data-stu-id="478ed-135">**GatewayUserSelectedCredsSource**</span></span>](imsrdpclienttransportsettings-gatewayuserselectedcredssource.md)<br/> | <span data-ttu-id="478ed-136">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="478ed-136">Read/write</span></span><br/> | <span data-ttu-id="478ed-137">Указанный пользователем источник учетных данных шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="478ed-137">The user-specified RD Gateway credential source.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="478ed-138">Требования</span><span class="sxs-lookup"><span data-stu-id="478ed-138">Requirements</span></span>



| <span data-ttu-id="478ed-139">Требование</span><span class="sxs-lookup"><span data-stu-id="478ed-139">Requirement</span></span> | <span data-ttu-id="478ed-140">Значение</span><span class="sxs-lookup"><span data-stu-id="478ed-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="478ed-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="478ed-141">Minimum supported client</span></span><br/> | <span data-ttu-id="478ed-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="478ed-142">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="478ed-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="478ed-143">Minimum supported server</span></span><br/> | <span data-ttu-id="478ed-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="478ed-144">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="478ed-145">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="478ed-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="478ed-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="478ed-146"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="478ed-147">DLL</span><span class="sxs-lookup"><span data-stu-id="478ed-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="478ed-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="478ed-148"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="478ed-149">IID</span><span class="sxs-lookup"><span data-stu-id="478ed-149">IID</span></span><br/>                      | <span data-ttu-id="478ed-150">IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="478ed-150">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="478ed-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="478ed-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="478ed-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="478ed-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="478ed-153">Справочник по веб-подключение к удаленному рабочему столу</span><span class="sxs-lookup"><span data-stu-id="478ed-153">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="478ed-154">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="478ed-154">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

