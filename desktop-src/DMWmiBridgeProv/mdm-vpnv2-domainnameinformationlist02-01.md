---
title: Класс MDM_VPNv2_DomainNameInformationList02_01
description: Класс MDM \_ Поддержка vpnv2 \_ DomainNameInformationList02 \_ 01 описывает правила таблица политики разрешения имен (NRPT) для профиля VPN.
ms.assetid: ed6863aa-f85e-4f65-9312-ddf60a8c0d5a
keywords:
- Класс MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01 класс, описание
topic_type:
- apiref
api_name:
- MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01.InstanceID
- MDM_VPNv2_DomainNameInformationList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2fa2b6fd4216256a085caa23333bccc5f386d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989219"
---
# <a name="mdm_vpnv2_domainnameinformationlist02_01-class"></a><span data-ttu-id="79486-105">\_Класс MDM поддержка vpnv2 \_ DomainNameInformationList02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="79486-105">MDM\_VPNv2\_DomainNameInformationList02\_01 class</span></span>

<span data-ttu-id="79486-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="79486-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="79486-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="79486-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="79486-108">Класс **MDM \_ Поддержка vpnv2 \_ DomainNameInformationList02 \_ 01** описывает правила таблица политики разрешения имен (NRPT) для профиля VPN.</span><span class="sxs-lookup"><span data-stu-id="79486-108">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class describes the Name Resolution Policy Table (NRPT) rules for the VPN profile.</span></span>

<span data-ttu-id="79486-109">Таблица политики разрешения имен (NRPT) — это таблица пространств имен и соответствующие параметры, хранящиеся в реестре Windows, которые определяют поведение клиента DNS при выдаче запросов и обработке ответов.</span><span class="sxs-lookup"><span data-stu-id="79486-109">The Name Resolution Policy Table (NRPT) is a table of namespaces and corresponding settings stored in the Windows registry that determines the DNS client behavior when issuing queries and processing responses.</span></span> <span data-ttu-id="79486-110">Каждая строка в таблице NRPT представляет правило для части пространства имен, для которого DNS-клиент выдает запросы.</span><span class="sxs-lookup"><span data-stu-id="79486-110">Each row in the NRPT represents a rule for a portion of the namespace for which the DNS client issues queries.</span></span> <span data-ttu-id="79486-111">Перед выдачей запросов на разрешение имен DNS-клиент обращается к NRPT, чтобы определить, должны ли в запросе быть заданы дополнительные флаги.</span><span class="sxs-lookup"><span data-stu-id="79486-111">Before issuing name resolution queries, the DNS client consults the NRPT to determine if any additional flags must be set in the query.</span></span> <span data-ttu-id="79486-112">После получения ответа клиент снова обращается к NRPT для проверки каких либо специальных требований к обработке или политике.</span><span class="sxs-lookup"><span data-stu-id="79486-112">After receiving the response, the client again consults the NRPT to check for any special processing or policy requirements.</span></span> <span data-ttu-id="79486-113">В отсутствие NRPT клиент работает на основе DNS-серверов и суффиксов, установленных для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="79486-113">In the absence of the NRPT, the client operates based on the DNS servers and suffixes set on the interface.</span></span>

<span data-ttu-id="79486-114">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="79486-114">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="79486-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79486-115">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DomainNameInformationList02_01
{
  string InstanceID;
  string ParentID;
  string DomainName;
  string DomainNameType;
  string DnsServers;
  string WebProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="79486-116">Члены</span><span class="sxs-lookup"><span data-stu-id="79486-116">Members</span></span>

<span data-ttu-id="79486-117">Класс **MDM \_ Поддержка vpnv2 \_ DomainNameInformationList02 \_ 01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="79486-117">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="79486-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="79486-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79486-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="79486-119">Properties</span></span>

<span data-ttu-id="79486-120">Класс **MDM \_ Поддержка vpnv2 \_ DomainNameInformationList02 \_ 01** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="79486-120">The **MDM\_VPNv2\_DomainNameInformationList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="79486-121">DnsServers</span><span class="sxs-lookup"><span data-stu-id="79486-121">DnsServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-dnsservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="79486-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79486-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79486-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="79486-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="79486-124">Имя_домена</span><span class="sxs-lookup"><span data-stu-id="79486-124">DomainName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="79486-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79486-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79486-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="79486-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="79486-127">домаиннаметипе</span><span class="sxs-lookup"><span data-stu-id="79486-127">DomainNameType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainnametype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="79486-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79486-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79486-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="79486-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="79486-130">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="79486-130">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79486-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79486-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79486-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79486-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79486-133">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="79486-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="79486-134">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="79486-134">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="79486-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="79486-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79486-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79486-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79486-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="79486-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79486-138">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="79486-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="79486-139">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="79486-139">Describes the full path to the parent node.</span></span> <span data-ttu-id="79486-140">Для этого класса строка имеет значение "./Vendor/MSFT/VPNv2/*имя_профиля*"</span><span class="sxs-lookup"><span data-stu-id="79486-140">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="79486-141">вебпроксисерверс</span><span class="sxs-lookup"><span data-stu-id="79486-141">WebProxyServers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-webproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="79486-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="79486-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="79486-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="79486-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79486-144">Требования</span><span class="sxs-lookup"><span data-stu-id="79486-144">Requirements</span></span>



| <span data-ttu-id="79486-145">Требование</span><span class="sxs-lookup"><span data-stu-id="79486-145">Requirement</span></span> | <span data-ttu-id="79486-146">Значение</span><span class="sxs-lookup"><span data-stu-id="79486-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79486-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79486-147">Minimum supported client</span></span><br/> | <span data-ttu-id="79486-148">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="79486-148">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79486-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79486-149">Minimum supported server</span></span><br/> | <span data-ttu-id="79486-150">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="79486-150">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="79486-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="79486-151">Namespace</span></span><br/>                | <span data-ttu-id="79486-152">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="79486-152">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="79486-153">MOF</span><span class="sxs-lookup"><span data-stu-id="79486-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79486-154"><dt>Дмвмибриджепров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79486-154"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="79486-155">DLL</span><span class="sxs-lookup"><span data-stu-id="79486-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79486-156"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79486-156"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79486-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79486-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79486-158">Использование сценариев PowerShell с WMI Bridge Provider</span><span class="sxs-lookup"><span data-stu-id="79486-158">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

