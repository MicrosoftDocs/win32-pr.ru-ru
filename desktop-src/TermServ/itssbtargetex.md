---
title: Интерфейс Итссбтаржетекс
description: Отображает свойства, в которых хранятся сведения о конфигурации и состоянии целевого объекта.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов интерфейса Итссбтаржетекс
- Службы удаленных рабочих столов интерфейса Итссбтаржетекс, описание
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d53d126d9419f87d91b027b0d69847f67de84be6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989316"
---
# <a name="itssbtargetex-interface"></a><span data-ttu-id="86162-105">Интерфейс Итссбтаржетекс</span><span class="sxs-lookup"><span data-stu-id="86162-105">ITsSbTargetEx interface</span></span>

<span data-ttu-id="86162-106">Отображает свойства, в которых хранятся сведения о конфигурации и состоянии целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="86162-106">Exposes properties that store configuration and state information about a target.</span></span>

<span data-ttu-id="86162-107">Этот интерфейс доступен только в Windows Server 2012 R2 с установленным [KB3091411](https://support.microsoft.com/kb/3091411) .</span><span class="sxs-lookup"><span data-stu-id="86162-107">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="86162-108">Свойство [**таржетлоад**](itssbtarget-targetload.md) интерфейса [**итссбтаржет**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) доступно начиная с Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="86162-108">The [**TargetLoad**](itssbtarget-targetload.md) property of the [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) interface is available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="86162-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="86162-109">Members</span></span>

<span data-ttu-id="86162-110">Интерфейс **итссбтаржетекс** наследует от [**итссбтаржет**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span><span class="sxs-lookup"><span data-stu-id="86162-110">The **ITsSbTargetEx** interface inherits from [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget).</span></span> <span data-ttu-id="86162-111">**Итссбтаржетекс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="86162-111">**ITsSbTargetEx** also has these types of members:</span></span>

-   [<span data-ttu-id="86162-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="86162-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="86162-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="86162-113">Properties</span></span>

<span data-ttu-id="86162-114">Интерфейс **итссбтаржетекс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="86162-114">The **ITsSbTargetEx** interface has these properties.</span></span>



| <span data-ttu-id="86162-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="86162-115">Property</span></span>                                                                      | <span data-ttu-id="86162-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="86162-116">Access type</span></span>           | <span data-ttu-id="86162-117">Описание</span><span class="sxs-lookup"><span data-stu-id="86162-117">Description</span></span>                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86162-118">**EnvironmentName**</span><span class="sxs-lookup"><span data-stu-id="86162-118">**EnvironmentName**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | <span data-ttu-id="86162-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="86162-119">Read/write</span></span><br/> | <span data-ttu-id="86162-120">Возвращает или задает имя среды, связанной с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="86162-120">Retrieves or specifies the name of the environment associated with the target.</span></span><br/> |
| [<span data-ttu-id="86162-121">**фармнаме**</span><span class="sxs-lookup"><span data-stu-id="86162-121">**FarmName**</span></span>](itssbtarget-farmname.md)<br/>                           | <span data-ttu-id="86162-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="86162-122">Read/write</span></span><br/> | <span data-ttu-id="86162-123">Указывает или получает имя фермы, к которой присоединен этот целевой объект.</span><span class="sxs-lookup"><span data-stu-id="86162-123">Specifies or retrieves the name of the farm to which this target is joined.</span></span><br/>    |
| [<span data-ttu-id="86162-124">**IpAddresses**</span><span class="sxs-lookup"><span data-stu-id="86162-124">**IpAddresses**</span></span>](itssbtarget-ipaddresses.md)<br/>                     | <span data-ttu-id="86162-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="86162-125">Read/write</span></span><br/> | <span data-ttu-id="86162-126">Возвращает или задает внешние IP-адреса целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="86162-126">Retrieves or specifies the external IP addresses of the target.</span></span><br/>                |
| [<span data-ttu-id="86162-127">**нумпендингконнектионс**</span><span class="sxs-lookup"><span data-stu-id="86162-127">**NumPendingConnections**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | <span data-ttu-id="86162-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="86162-128">Read-only</span></span><br/>  | <span data-ttu-id="86162-129">Возвращает число ожидающих пользовательских соединений для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="86162-129">Retrieves the number of pending user connections for the target.</span></span><br/>               |
| [<span data-ttu-id="86162-130">**нумсессионс**</span><span class="sxs-lookup"><span data-stu-id="86162-130">**NumSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | <span data-ttu-id="86162-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="86162-131">Read-only</span></span><br/>  | <span data-ttu-id="86162-132">Возвращает число сеансов, обслуживаемых брокером для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="86162-132">Retrieves the number of sessions maintained by broker for the target.</span></span><br/>          |
| [<span data-ttu-id="86162-133">**таржетфкдн**</span><span class="sxs-lookup"><span data-stu-id="86162-133">**TargetFQDN**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | <span data-ttu-id="86162-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="86162-134">Read/write</span></span><br/> | <span data-ttu-id="86162-135">Указывает или получает полное доменное имя целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="86162-135">Specifies or retrieves the fully qualified domain name of the target.</span></span><br/>          |
| <span data-ttu-id="86162-136">[**таржетлоад**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="86162-136">[**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))</span></span><br/>                     | <span data-ttu-id="86162-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="86162-137">Read-only</span></span><br/>  | <span data-ttu-id="86162-138">Извлекает относительную нагрузку на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="86162-138">Retrieves the relative load on a target.</span></span><br/>                                       |
| [<span data-ttu-id="86162-139">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="86162-139">**TargetName**</span></span>](itssbtarget-targetname.md)<br/>                       | <span data-ttu-id="86162-140">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="86162-140">Read/write</span></span><br/> | <span data-ttu-id="86162-141">Указывает или получает имя целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="86162-141">Specifies or retrieves the name of the target.</span></span><br/>                                 |
| [<span data-ttu-id="86162-142">**таржетнетбиос**</span><span class="sxs-lookup"><span data-stu-id="86162-142">**TargetNetbios**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | <span data-ttu-id="86162-143">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="86162-143">Read/write</span></span><br/> | <span data-ttu-id="86162-144">Указывает или получает NetBIOS-имя целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="86162-144">Specifies or retrieves the NetBIOS name of the target.</span></span><br/>                         |
| [<span data-ttu-id="86162-145">**таржетпропертисет**</span><span class="sxs-lookup"><span data-stu-id="86162-145">**TargetPropertySet**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | <span data-ttu-id="86162-146">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="86162-146">Read/write</span></span><br/> | <span data-ttu-id="86162-147">Указывает или получает набор свойств для целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="86162-147">Specifies or retrieves the property set for the target.</span></span><br/>                        |
| [<span data-ttu-id="86162-148">**таржетстате**</span><span class="sxs-lookup"><span data-stu-id="86162-148">**TargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | <span data-ttu-id="86162-149">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="86162-149">Read/write</span></span><br/> | <span data-ttu-id="86162-150">Указывает или получает целевое состояние.</span><span class="sxs-lookup"><span data-stu-id="86162-150">Specifies or retrieves the target state.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="86162-151">Требования</span><span class="sxs-lookup"><span data-stu-id="86162-151">Requirements</span></span>



| <span data-ttu-id="86162-152">Требование</span><span class="sxs-lookup"><span data-stu-id="86162-152">Requirement</span></span> | <span data-ttu-id="86162-153">Значение</span><span class="sxs-lookup"><span data-stu-id="86162-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="86162-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="86162-154">Minimum supported client</span></span><br/> | <span data-ttu-id="86162-155">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="86162-155">None supported</span></span><br/>                                                        |
| <span data-ttu-id="86162-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="86162-156">Minimum supported server</span></span><br/> | <span data-ttu-id="86162-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="86162-157">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="86162-158">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="86162-158">End of server support</span></span><br/>    | <span data-ttu-id="86162-159">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="86162-159">Windows Server 2012 R2</span></span><br/>                                                |
| <span data-ttu-id="86162-160">IID</span><span class="sxs-lookup"><span data-stu-id="86162-160">IID</span></span><br/>                      | <span data-ttu-id="86162-161">IID \_ итссбтаржетекс определен как 74f99987-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="86162-161">IID\_ITsSbTargetEx is defined as 74f99987-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86162-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="86162-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86162-163">**итссбтаржет**</span><span class="sxs-lookup"><span data-stu-id="86162-163">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[<span data-ttu-id="86162-164">Интерфейсы виртуализации удаленный рабочий стол</span><span class="sxs-lookup"><span data-stu-id="86162-164">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

