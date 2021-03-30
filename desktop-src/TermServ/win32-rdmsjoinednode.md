---
title: Класс Win32_RDMSJoinedNode
description: Представляет узел сервера под управлением служб удаленный рабочий стол Management Services (RDMS).
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSJoinedNode службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSJoinedNode, описание
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414837"
---
# <a name="win32_rdmsjoinednode-class"></a><span data-ttu-id="62209-105">\_Класс Win32 рдмсжоинедноде</span><span class="sxs-lookup"><span data-stu-id="62209-105">Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="62209-106">Представляет узел сервера под управлением служб удаленный рабочий стол Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="62209-106">Represents a server node that is managed by Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="62209-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="62209-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62209-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62209-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a><span data-ttu-id="62209-109">Члены</span><span class="sxs-lookup"><span data-stu-id="62209-109">Members</span></span>

<span data-ttu-id="62209-110">Класс **Win32 \_ рдмсжоинедноде** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="62209-110">The **Win32\_RDMSJoinedNode** class has these types of members:</span></span>

-   [<span data-ttu-id="62209-111">Методы</span><span class="sxs-lookup"><span data-stu-id="62209-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="62209-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="62209-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="62209-113">Методы</span><span class="sxs-lookup"><span data-stu-id="62209-113">Methods</span></span>

<span data-ttu-id="62209-114">Класс **Win32 \_ рдмсжоинедноде** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="62209-114">The **Win32\_RDMSJoinedNode** class has these methods.</span></span>



| <span data-ttu-id="62209-115">Метод</span><span class="sxs-lookup"><span data-stu-id="62209-115">Method</span></span>                                                                | <span data-ttu-id="62209-116">Описание</span><span class="sxs-lookup"><span data-stu-id="62209-116">Description</span></span>                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62209-117">**жетжоинеднодекаунт**</span><span class="sxs-lookup"><span data-stu-id="62209-117">**GetJoinedNodeCount**</span></span>](win32-rdmsjoinednode-getjoinednodecount.md) | <span data-ttu-id="62209-118">**Windows server 2012 R2 и Windows server 2012:** Этот метод недоступен до выхода Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="62209-118">**Windows Server 2012 R2 and Windows Server 2012:** This method is unavailable prior to Windows Server 2016.</span></span><br/> <span data-ttu-id="62209-119">Возвращает число серверов, на которых установлена указанная роль.</span><span class="sxs-lookup"><span data-stu-id="62209-119">Gets the number of servers that have the specified role installed.</span></span><br/> |
| [<span data-ttu-id="62209-120">**Join**</span><span class="sxs-lookup"><span data-stu-id="62209-120">**Join**</span></span>](join-win32-rdmsjoinednode.md)                             | <span data-ttu-id="62209-121">Добавляет узел в RDMS.</span><span class="sxs-lookup"><span data-stu-id="62209-121">Adds a node to RDMS.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="62209-122">**Отсоединить**</span><span class="sxs-lookup"><span data-stu-id="62209-122">**Unjoin**</span></span>](unjoin-win32-rdmsjoinednode.md)                         | <span data-ttu-id="62209-123">Удаляет узел из RDMS.</span><span class="sxs-lookup"><span data-stu-id="62209-123">Removes a node from RDMS.</span></span><br/>                                                                                                                                                                  |



 

### <a name="properties"></a><span data-ttu-id="62209-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="62209-124">Properties</span></span>

<span data-ttu-id="62209-125">Класс **Win32 \_ рдмсжоинедноде** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="62209-125">The **Win32\_RDMSJoinedNode** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62209-126">**Полное доменное имя.**</span><span class="sxs-lookup"><span data-stu-id="62209-126">**FQDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62209-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62209-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62209-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62209-129">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="62209-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="62209-130">Возвращает полное доменное имя узла.</span><span class="sxs-lookup"><span data-stu-id="62209-130">Gets the fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="62209-131">**исгатевайцертификатеинсталлед**</span><span class="sxs-lookup"><span data-stu-id="62209-131">**IsGatewayCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-132">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62209-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62209-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62209-134">Возвращает и задает значение, указывающее, имеет ли сервер сертификат для проверки подлинности для подключений шлюза удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="62209-134">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop gateway connections.</span></span> <span data-ttu-id="62209-135">**Значение true** , если сертификат установлен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62209-135">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62209-136">**испублишингцертификатеинсталлед**</span><span class="sxs-lookup"><span data-stu-id="62209-136">**IsPublishingCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-137">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62209-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62209-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62209-139">Возвращает и задает значение, указывающее, имеет ли сервер сертификат для подписывания протокол удаленного рабочего стола файлов публикации.</span><span class="sxs-lookup"><span data-stu-id="62209-139">Gets and sets a value that indicates whether the server has a certificate to sign Remote Desktop Protocol publishing files.</span></span> <span data-ttu-id="62209-140">**Значение true** , если сертификат установлен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62209-140">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62209-141">**исрдкб**</span><span class="sxs-lookup"><span data-stu-id="62209-141">**IsRdcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62209-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62209-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62209-144">Возвращает и задает значение, указывающее, является ли сервер компонентом Service Broker подключение к удаленному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="62209-144">Gets and sets a value that indicates whether the server is Remote Desktop Connection Broker.</span></span> <span data-ttu-id="62209-145">**Значение true** , если сервер является компонентом подключение к удаленному рабочему столу Broker; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62209-145">**TRUE** if the server is a Remote Desktop Connection Broker; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62209-146">**исрдг**</span><span class="sxs-lookup"><span data-stu-id="62209-146">**IsRdg**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-147">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62209-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62209-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62209-149">Возвращает и задает значение, указывающее, является ли сервер сервером шлюза удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="62209-149">Gets and sets a value that indicates whether the server is Remote Desktop gateway server.</span></span> <span data-ttu-id="62209-150">**Значение true** , если сервер является сервером шлюза удаленный рабочий стол; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62209-150">**TRUE** if the server is a Remote Desktop gateway server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62209-151">**исрдлс**</span><span class="sxs-lookup"><span data-stu-id="62209-151">**IsRdls**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-152">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62209-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62209-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62209-154">Возвращает и задает значение, указывающее, является ли сервер сервером лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="62209-154">Gets and sets a value that indicates whether the server is Remote Desktop license server.</span></span> <span data-ttu-id="62209-155">**Значение true** , если сервер является сервером лицензирования удаленный рабочий стол; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62209-155">**TRUE** if the server is a Remote Desktop license server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62209-156">**исрдш**</span><span class="sxs-lookup"><span data-stu-id="62209-156">**IsRdsh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-157">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62209-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62209-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62209-159">Возвращает и задает значение, указывающее, является ли сервер сервером узла сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="62209-159">Gets and sets a value that indicates whether the server is Remote Desktop session host server.</span></span> <span data-ttu-id="62209-160">**Значение true** , если сервер является сервером узла сеансов удаленный рабочий стол; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62209-160">**TRUE** if the server is a Remote Desktop session host server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62209-161">**исрдвх**</span><span class="sxs-lookup"><span data-stu-id="62209-161">**IsRdvh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-162">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62209-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62209-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62209-164">Возвращает и задает значение, указывающее, является ли сервер узлом виртуализации удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="62209-164">Gets and sets a value that indicates whether the server is Remote Desktop virtualization host.</span></span> <span data-ttu-id="62209-165">**Значение true** , если сервер является узлом виртуализации удаленный рабочий стол; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62209-165">**TRUE** if the server is a Remote Desktop virtualization host; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62209-166">**исрдва**</span><span class="sxs-lookup"><span data-stu-id="62209-166">**IsRdwa**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-167">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62209-167">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62209-168">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-168">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62209-169">Возвращает и задает значение, указывающее, является ли сервер сервером веб-доступа удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="62209-169">Gets and sets a value that indicates whether the server is Remote Desktop web access server.</span></span> <span data-ttu-id="62209-170">**Значение true** , если сервер является сервером удаленный рабочий стол веб-доступ; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62209-170">**TRUE** if the server is a Remote Desktop Web Access server; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62209-171">**исредиректорцертификатеинсталлед**</span><span class="sxs-lookup"><span data-stu-id="62209-171">**IsRedirectorCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-172">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62209-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62209-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62209-174">Возвращает и задает значение, указывающее, имеет ли сервер сертификат для проверки подлинности при развертывании службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="62209-174">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Services deployment.</span></span> <span data-ttu-id="62209-175">**Значение true** , если сертификат установлен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62209-175">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62209-176">**исвебакцессцертификатеинсталлед**</span><span class="sxs-lookup"><span data-stu-id="62209-176">**IsWebAccessCertificateInstalled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-177">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62209-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62209-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="62209-179">Возвращает и задает значение, указывающее, имеет ли сервер сертификат для проверки подлинности удаленный рабочий стол Веб-доступ.</span><span class="sxs-lookup"><span data-stu-id="62209-179">Gets and sets a value that indicates whether the server has a certificate to perform authentication for Remote Desktop Web Access.</span></span> <span data-ttu-id="62209-180">**Значение true** , если сертификат установлен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="62209-180">**TRUE** if the certificate is installed; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62209-181">**OSVersion**</span><span class="sxs-lookup"><span data-stu-id="62209-181">**OSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62209-182">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="62209-183">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="62209-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="62209-184">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="62209-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="62209-185">Возвращает и задает версию операционных систем на узле.</span><span class="sxs-lookup"><span data-stu-id="62209-185">Gets and sets the version of the operating systems on the node.</span></span>

</dd> <dt>

<span data-ttu-id="62209-186">**SID**</span><span class="sxs-lookup"><span data-stu-id="62209-186">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62209-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62209-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62209-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62209-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62209-189">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="62209-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="62209-190">Возвращает идентификатор безопасности (SID) узла.</span><span class="sxs-lookup"><span data-stu-id="62209-190">Gets the security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62209-191">Требования</span><span class="sxs-lookup"><span data-stu-id="62209-191">Requirements</span></span>



| <span data-ttu-id="62209-192">Требование</span><span class="sxs-lookup"><span data-stu-id="62209-192">Requirement</span></span> | <span data-ttu-id="62209-193">Значение</span><span class="sxs-lookup"><span data-stu-id="62209-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="62209-194">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62209-194">Minimum supported client</span></span><br/> | <span data-ttu-id="62209-195">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="62209-195">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="62209-196">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62209-196">Minimum supported server</span></span><br/> | <span data-ttu-id="62209-197">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62209-197">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="62209-198">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62209-198">Namespace</span></span><br/>                | <span data-ttu-id="62209-199">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="62209-199">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="62209-200">MOF</span><span class="sxs-lookup"><span data-stu-id="62209-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62209-201"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62209-201"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="62209-202">DLL</span><span class="sxs-lookup"><span data-stu-id="62209-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62209-203"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62209-203"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="62209-204">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62209-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62209-205">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="62209-205">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

