---
title: Класс MDM_EnterpriseDataProtection_Settings01
description: Класс MDM \_ ентерприседатапротектион \_ Settings01 используется для настройки параметров Windows Information Protection (WIP) (прежнее название — защита корпоративных данных).
ms.assetid: 7537f548-85fb-46b4-ab94-c9dcf2bf1447
keywords:
- Класс MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01 класс, описание
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection_Settings01
- MDM_EnterpriseDataProtection_Settings01.InstanceID
- MDM_EnterpriseDataProtection_Settings01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ef063a1a8d72666dc44a2276bcecfb7d420c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491958"
---
# <a name="mdm_enterprisedataprotection_settings01-class"></a><span data-ttu-id="75d0d-105">\_Класс MDM ентерприседатапротектион \_ Settings01</span><span class="sxs-lookup"><span data-stu-id="75d0d-105">MDM\_EnterpriseDataProtection\_Settings01 class</span></span>

<span data-ttu-id="75d0d-106">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="75d0d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="75d0d-107">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="75d0d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="75d0d-108">Класс **MDM \_ ентерприседатапротектион \_ Settings01** используется для настройки параметров Windows Information Protection (WIP) (прежнее название — защита корпоративных данных).</span><span class="sxs-lookup"><span data-stu-id="75d0d-108">The **MDM\_EnterpriseDataProtection\_Settings01** class is used to configure Windows Information Protection (WIP) (formerly known as Enterprise Data Protection) specific settings.</span></span> <span data-ttu-id="75d0d-109">Дополнительные сведения о WIP см. в статье [Защита корпоративных данных с помощью защиты корпоративных данных (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span><span class="sxs-lookup"><span data-stu-id="75d0d-109">For more information about WIP, see [Protect your enterprise data using enterprise data protection (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).</span></span>

<span data-ttu-id="75d0d-110">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="75d0d-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d0d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75d0d-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection_Settings01
{
  string InstanceID;
  string ParentID;
  sint32 EDPEnforcementLevel;
  string EnterpriseProtectedDomainNames;
  sint32 AllowUserDecryption;
  string DataRecoveryCertificate;
  sint32 RevokeOnUnenroll;
  string SMBAutoEncryptedFileExtensions;
  sint32 AllowAzureRMSForEDP;
  string RMSTemplateIDForEDP;
  sint32 EDPShowIcons;
};
```

## <a name="members"></a><span data-ttu-id="75d0d-112">Члены</span><span class="sxs-lookup"><span data-stu-id="75d0d-112">Members</span></span>

<span data-ttu-id="75d0d-113">Класс **MDM \_ ентерприседатапротектион \_ Settings01** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="75d0d-113">The **MDM\_EnterpriseDataProtection\_Settings01** class has these types of members:</span></span>

-   [<span data-ttu-id="75d0d-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="75d0d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75d0d-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="75d0d-115">Properties</span></span>

<span data-ttu-id="75d0d-116">Класс **MDM \_ ентерприседатапротектион \_ Settings01** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="75d0d-116">The **MDM\_EnterpriseDataProtection\_Settings01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="75d0d-117">алловазурермсфоредп</span><span class="sxs-lookup"><span data-stu-id="75d0d-117">AllowAzureRMSForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowazurermsforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-118">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="75d0d-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75d0d-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75d0d-120">алловусердекриптион</span><span class="sxs-lookup"><span data-stu-id="75d0d-120">AllowUserDecryption</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-allowuserdecryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-121">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="75d0d-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-122">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75d0d-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75d0d-123">датарековерицертификате</span><span class="sxs-lookup"><span data-stu-id="75d0d-123">DataRecoveryCertificate</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-datarecoverycertificate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75d0d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75d0d-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-126">Квалификаторы: **октетстринг**</span><span class="sxs-lookup"><span data-stu-id="75d0d-126">Qualifiers: **Octetstring**</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75d0d-127">едпенфорцементлевел</span><span class="sxs-lookup"><span data-stu-id="75d0d-127">EDPEnforcementLevel</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpenforcementlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-128">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="75d0d-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75d0d-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75d0d-130">едпшовиконс</span><span class="sxs-lookup"><span data-stu-id="75d0d-130">EDPShowIcons</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-edpshowicons)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-131">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="75d0d-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75d0d-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75d0d-133">ентерприсепротектеддомаиннамес</span><span class="sxs-lookup"><span data-stu-id="75d0d-133">EnterpriseProtectedDomainNames</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-enterpriseprotecteddomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75d0d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75d0d-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="75d0d-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="75d0d-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75d0d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="75d0d-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-139">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="75d0d-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="75d0d-140">Определяет имя родительского узла.</span><span class="sxs-lookup"><span data-stu-id="75d0d-140">Identifies the name of the parent node.</span></span> <span data-ttu-id="75d0d-141">Для этого класса строка имеет значение "Settings".</span><span class="sxs-lookup"><span data-stu-id="75d0d-141">For this class, the string is "Settings".</span></span>

</dd> <dt>

<span data-ttu-id="75d0d-142">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="75d0d-142">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75d0d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="75d0d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-145">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="75d0d-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="75d0d-146">Описывает полный путь к родительскому узлу.</span><span class="sxs-lookup"><span data-stu-id="75d0d-146">Describes the full path to the parent node.</span></span> <span data-ttu-id="75d0d-147">Для этого класса строка имеет значение "./вендор/мсфт/ентерприседатапротектион"</span><span class="sxs-lookup"><span data-stu-id="75d0d-147">For this class, the string is "./Vendor/MSFT/EnterpriseDataProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="75d0d-148">ревокеонуненролл</span><span class="sxs-lookup"><span data-stu-id="75d0d-148">RevokeOnUnenroll</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-revokeonunenroll)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-149">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="75d0d-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75d0d-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75d0d-151">рмстемплатеидфоредп</span><span class="sxs-lookup"><span data-stu-id="75d0d-151">RMSTemplateIDForEDP</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-rmstemplateidforedp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75d0d-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75d0d-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75d0d-154">смбаутоенкриптедфиликстенсионс</span><span class="sxs-lookup"><span data-stu-id="75d0d-154">SMBAutoEncryptedFileExtensions</span></span>](/windows/client-management/mdm/enterprisedataprotection-csp#settings-smbautoencryptedfileextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75d0d-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75d0d-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75d0d-156">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75d0d-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75d0d-157">Требования</span><span class="sxs-lookup"><span data-stu-id="75d0d-157">Requirements</span></span>



| <span data-ttu-id="75d0d-158">Требование</span><span class="sxs-lookup"><span data-stu-id="75d0d-158">Requirement</span></span> | <span data-ttu-id="75d0d-159">Значение</span><span class="sxs-lookup"><span data-stu-id="75d0d-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d0d-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75d0d-160">Minimum supported client</span></span><br/> | <span data-ttu-id="75d0d-161">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="75d0d-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="75d0d-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75d0d-162">Minimum supported server</span></span><br/> | <span data-ttu-id="75d0d-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="75d0d-163">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="75d0d-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="75d0d-164">Namespace</span></span><br/>                | <span data-ttu-id="75d0d-165">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="75d0d-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="75d0d-166">MOF</span><span class="sxs-lookup"><span data-stu-id="75d0d-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75d0d-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75d0d-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="75d0d-168">DLL</span><span class="sxs-lookup"><span data-stu-id="75d0d-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d0d-169"><dt>MOF \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d0d-169"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

