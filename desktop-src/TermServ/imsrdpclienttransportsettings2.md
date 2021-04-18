---
title: Интерфейс IMsRdpClientTransportSettings2
description: Управляет параметрами транспорта клиента для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов). | Интерфейс IMsRdpClientTransportSettings2
ms.assetid: 4f9f1905-2693-4666-9f6f-6e00b1eb6a0f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, описание
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f2f4887c6a4f55f3b9c97c389e9afd702d2ffab
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684854"
---
# <a name="imsrdpclienttransportsettings2-interface"></a><span data-ttu-id="4f760-106">Интерфейс IMsRdpClientTransportSettings2</span><span class="sxs-lookup"><span data-stu-id="4f760-106">IMsRdpClientTransportSettings2 interface</span></span>

<span data-ttu-id="4f760-107">Управляет параметрами транспорта клиента для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="4f760-107">Manages client transport settings for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="4f760-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="4f760-108">Members</span></span>

<span data-ttu-id="4f760-109">Интерфейс **IMsRdpClientTransportSettings2** наследует от [**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md).</span><span class="sxs-lookup"><span data-stu-id="4f760-109">The **IMsRdpClientTransportSettings2** interface inherits from [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md).</span></span> <span data-ttu-id="4f760-110">**IMsRdpClientTransportSettings2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4f760-110">**IMsRdpClientTransportSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="4f760-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="4f760-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f760-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4f760-112">Properties</span></span>

<span data-ttu-id="4f760-113">Интерфейс **IMsRdpClientTransportSettings2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4f760-113">The **IMsRdpClientTransportSettings2** interface has these properties.</span></span>



| <span data-ttu-id="4f760-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="4f760-114">Property</span></span>                                                                                                    | <span data-ttu-id="4f760-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="4f760-115">Access type</span></span>           | <span data-ttu-id="4f760-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4f760-116">Description</span></span>                                                                                       |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f760-117">**гатевайкредшаринг**</span><span class="sxs-lookup"><span data-stu-id="4f760-117">**GatewayCredSharing**</span></span>](imsrdpclienttransportsettings2-gatewaycredsharing.md)<br/>                  | <span data-ttu-id="4f760-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4f760-118">Read/write</span></span><br/> | <span data-ttu-id="4f760-119">Указывает, включен ли компонент единого входа для шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="4f760-119">Indicates whether the single sign-on feature for RD Gateway is enabled.</span></span><br/>                |
| [<span data-ttu-id="4f760-120">**гатевайдомаин**</span><span class="sxs-lookup"><span data-stu-id="4f760-120">**GatewayDomain**</span></span>](imsrdpclienttransportsettings2-gatewaydomain.md)<br/>                            | <span data-ttu-id="4f760-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4f760-121">Read/write</span></span><br/> | <span data-ttu-id="4f760-122">Имя домена, которое пользователь предоставляет для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="4f760-122">The domain name that a user provides to connect to the RD Gateway server.</span></span><br/>              |
| [<span data-ttu-id="4f760-123">**гатевайенкриптедотпкукие**</span><span class="sxs-lookup"><span data-stu-id="4f760-123">**GatewayEncryptedOtpCookie**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>     | <span data-ttu-id="4f760-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4f760-124">Read/write</span></span><br/> | <span data-ttu-id="4f760-125">Зашифрованный файл cookie OTP.</span><span class="sxs-lookup"><span data-stu-id="4f760-125">The encrypted OTP cookie.</span></span><br/>                                                              |
| [<span data-ttu-id="4f760-126">**гатевайенкриптедотпкукиесизе**</span><span class="sxs-lookup"><span data-stu-id="4f760-126">**GatewayEncryptedOtpCookieSize**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/> | <span data-ttu-id="4f760-127">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4f760-127">Read/write</span></span><br/> | <span data-ttu-id="4f760-128">Размер зашифрованного файла cookie OTP (в байтах).</span><span class="sxs-lookup"><span data-stu-id="4f760-128">The size, in bytes, of the encrypted OTP cookie.</span></span><br/>                                       |
| [<span data-ttu-id="4f760-129">**гатевайпассворд**</span><span class="sxs-lookup"><span data-stu-id="4f760-129">**GatewayPassword**</span></span>](imsrdpclienttransportsettings2-gatewaypassword.md)<br/>                        | <span data-ttu-id="4f760-130">Только на запись</span><span class="sxs-lookup"><span data-stu-id="4f760-130">Write-only</span></span><br/> | <span data-ttu-id="4f760-131">Пароль, предоставляемый пользователем для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="4f760-131">The password that a user provides to connect to the RD Gateway server.</span></span><br/>                 |
| [<span data-ttu-id="4f760-132">**гатевайпреаусрекуиремент**</span><span class="sxs-lookup"><span data-stu-id="4f760-132">**GatewayPreAuthRequirement**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthrequirement.md)<br/>    | <span data-ttu-id="4f760-133">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4f760-133">Read/write</span></span><br/> | <span data-ttu-id="4f760-134">Указывает, включена ли функция одноразового пароля для шлюза удаленных рабочих столов (OTP).</span><span class="sxs-lookup"><span data-stu-id="4f760-134">Indicates whether the RD Gateway one-time password (OTP) feature is enabled.</span></span><br/>           |
| [<span data-ttu-id="4f760-135">**гатевайпреауссервераддр**</span><span class="sxs-lookup"><span data-stu-id="4f760-135">**GatewayPreAuthServerAddr**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>      | <span data-ttu-id="4f760-136">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4f760-136">Read/write</span></span><br/> | <span data-ttu-id="4f760-137">Веб-адрес сервера предварительной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4f760-137">The web address of the pre-authentication server.</span></span><br/>                                      |
| [<span data-ttu-id="4f760-138">**гатевайсуппортурл**</span><span class="sxs-lookup"><span data-stu-id="4f760-138">**GatewaySupportUrl**</span></span>](imsrdpclienttransportsettings2-gatewaypreauthserveraddr.md)<br/>             | <span data-ttu-id="4f760-139">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4f760-139">Read/write</span></span><br/> | <span data-ttu-id="4f760-140">Веб-адрес сайта, который предоставляет техническую поддержку для сервера шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="4f760-140">The web address of the site that provides technical support for the RD Gateway server.</span></span><br/> |
| [<span data-ttu-id="4f760-141">**гатевайусернаме**</span><span class="sxs-lookup"><span data-stu-id="4f760-141">**GatewayUsername**</span></span>](imsrdpclienttransportsettings2-gatewayusername.md)<br/>                        | <span data-ttu-id="4f760-142">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="4f760-142">Read/write</span></span><br/> | <span data-ttu-id="4f760-143">Имя пользователя, которое предоставляет пользователь для подключения к серверу шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="4f760-143">The user name that a user provides to connect to the RD Gateway server.</span></span><br/>                |



 

## <a name="requirements"></a><span data-ttu-id="4f760-144">Требования</span><span class="sxs-lookup"><span data-stu-id="4f760-144">Requirements</span></span>



| <span data-ttu-id="4f760-145">Требование</span><span class="sxs-lookup"><span data-stu-id="4f760-145">Requirement</span></span> | <span data-ttu-id="4f760-146">Значение</span><span class="sxs-lookup"><span data-stu-id="4f760-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f760-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f760-147">Minimum supported client</span></span><br/> | <span data-ttu-id="4f760-148">Windows Vista с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="4f760-148">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="4f760-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f760-149">Minimum supported server</span></span><br/> | <span data-ttu-id="4f760-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f760-150">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="4f760-151">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4f760-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f760-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f760-152"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4f760-153">DLL</span><span class="sxs-lookup"><span data-stu-id="4f760-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f760-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f760-154"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4f760-155">IID</span><span class="sxs-lookup"><span data-stu-id="4f760-155">IID</span></span><br/>                      | <span data-ttu-id="4f760-156">IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="4f760-156">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f760-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f760-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f760-158">**имсрдпклиенттранспортсеттингс**</span><span class="sxs-lookup"><span data-stu-id="4f760-158">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





