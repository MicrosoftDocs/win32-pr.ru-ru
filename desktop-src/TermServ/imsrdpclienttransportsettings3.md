---
title: Интерфейс IMsRdpClientTransportSettings3
description: Определяет дополнительные свойства для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов). | Интерфейс IMsRdpClientTransportSettings3
ms.assetid: c0bdfe23-9a26-4feb-b9b7-e52f04f23aa1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings3, описание
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7498db4b39a4ad0e89761cbec439895e4e9a152
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914372"
---
# <a name="imsrdpclienttransportsettings3-interface"></a><span data-ttu-id="7f382-106">Интерфейс IMsRdpClientTransportSettings3</span><span class="sxs-lookup"><span data-stu-id="7f382-106">IMsRdpClientTransportSettings3 interface</span></span>

<span data-ttu-id="7f382-107">Определяет дополнительные свойства для сервера шлюза удаленный рабочий стол (шлюза удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="7f382-107">Defines additional properties for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="members"></a><span data-ttu-id="7f382-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="7f382-108">Members</span></span>

<span data-ttu-id="7f382-109">Интерфейс **IMsRdpClientTransportSettings3** наследует от [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="7f382-109">The **IMsRdpClientTransportSettings3** interface inherits from [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).</span></span> <span data-ttu-id="7f382-110">**IMsRdpClientTransportSettings3** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7f382-110">**IMsRdpClientTransportSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="7f382-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7f382-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7f382-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7f382-112">Properties</span></span>

<span data-ttu-id="7f382-113">Интерфейс **IMsRdpClientTransportSettings3** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7f382-113">The **IMsRdpClientTransportSettings3** interface has these properties.</span></span>



| <span data-ttu-id="7f382-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="7f382-114">Property</span></span>                                                                                                           | <span data-ttu-id="7f382-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="7f382-115">Access type</span></span>           | <span data-ttu-id="7f382-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7f382-116">Description</span></span>                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f382-117">**гатевайаускукиесервераддр**</span><span class="sxs-lookup"><span data-stu-id="7f382-117">**GatewayAuthCookieServerAddr**</span></span>](imsrdpclienttransportsettings3-gatewayauthcookieserveraddr.md)<br/>       | <span data-ttu-id="7f382-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7f382-118">Read/write</span></span><br/> | <span data-ttu-id="7f382-119">Адрес сервера для проверки подлинности на основе файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="7f382-119">The server address for cookie-based authentication.</span></span><br/>                                                                                       |
| [<span data-ttu-id="7f382-120">**гатевайауслогинпаже**</span><span class="sxs-lookup"><span data-stu-id="7f382-120">**GatewayAuthLoginPage**</span></span>](imsrdpclienttransportsettings3-gatewayauthloginpage.md)<br/>                     | <span data-ttu-id="7f382-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7f382-121">Read/write</span></span><br/> | <span data-ttu-id="7f382-122">Адрес веб-страницы входа, используемой для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="7f382-122">The address of the login webpage to use to authenticate a user.</span></span><br/>                                                                           |
| [<span data-ttu-id="7f382-123">**гатевайкредсаурцекукие**</span><span class="sxs-lookup"><span data-stu-id="7f382-123">**GatewayCredSourceCookie**</span></span>](imsrdpclienttransportsettings3-gatewaycredsourcecookie.md)<br/>               | <span data-ttu-id="7f382-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7f382-124">Read/write</span></span><br/> | <span data-ttu-id="7f382-125">Указывает, является ли источник учетных данных основанным на файлах cookie.</span><span class="sxs-lookup"><span data-stu-id="7f382-125">Specifies if the credential source is cookie based.</span></span><br/>                                                                                       |
| [<span data-ttu-id="7f382-126">**гатевайенкриптедаускукие**</span><span class="sxs-lookup"><span data-stu-id="7f382-126">**GatewayEncryptedAuthCookie**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md)<br/>         | <span data-ttu-id="7f382-127">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7f382-127">Read/write</span></span><br/> | <span data-ttu-id="7f382-128">Зашифрованный файл cookie проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="7f382-128">The encrypted authentication cookie.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="7f382-129">**гатевайенкриптедаускукиесизе**</span><span class="sxs-lookup"><span data-stu-id="7f382-129">**GatewayEncryptedAuthCookieSize**</span></span>](imsrdpclienttransportsettings3-gatewayencryptedauthcookiesize.md)<br/> | <span data-ttu-id="7f382-130">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7f382-130">Read/write</span></span><br/> | <span data-ttu-id="7f382-131">Размер (в символах) свойства [**гатевайенкриптедаускукие**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) .</span><span class="sxs-lookup"><span data-stu-id="7f382-131">The size, in characters, of the [**GatewayEncryptedAuthCookie**](imsrdpclienttransportsettings3-gatewayencryptedauthcookie.md) property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7f382-132">Требования</span><span class="sxs-lookup"><span data-stu-id="7f382-132">Requirements</span></span>



| <span data-ttu-id="7f382-133">Требование</span><span class="sxs-lookup"><span data-stu-id="7f382-133">Requirement</span></span> | <span data-ttu-id="7f382-134">Значение</span><span class="sxs-lookup"><span data-stu-id="7f382-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f382-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f382-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7f382-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f382-136">Windows 7</span></span><br/>                                                                              |
| <span data-ttu-id="7f382-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f382-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7f382-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f382-138">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="7f382-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7f382-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="7f382-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f382-140"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="7f382-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7f382-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f382-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f382-142"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="7f382-143">IID</span><span class="sxs-lookup"><span data-stu-id="7f382-143">IID</span></span><br/>                      | <span data-ttu-id="7f382-144">IID \_ IMsRdpClientTransportSettings3 определен как 3D5B21AC-748D-41DE-8F30-E15169586BD4</span><span class="sxs-lookup"><span data-stu-id="7f382-144">IID\_IMsRdpClientTransportSettings3 is defined as 3D5B21AC-748D-41DE-8F30-E15169586BD4</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f382-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f382-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f382-146">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="7f382-146">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





