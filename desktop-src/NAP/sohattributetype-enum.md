---
title: Перечисление Сохаттрибутетипе (Наппротокол. h)
description: Задает тип атрибута, хранящегося в объекте-длине типа атрибута (TLV).
ms.assetid: ba725bf1-1d0a-4489-b912-3e761557d772
keywords:
- Сохаттрибутетипе перечисление NAP
topic_type:
- apiref
api_name:
- SoHAttributeType
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db164bbedf2267aaa5941a21a56ccfd53e1e1646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340990"
---
# <a name="sohattributetype-enumeration"></a><span data-ttu-id="e065c-104">Перечисление Сохаттрибутетипе</span><span class="sxs-lookup"><span data-stu-id="e065c-104">SoHAttributeType enumeration</span></span>

> [!Note]  
> <span data-ttu-id="e065c-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="e065c-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e065c-106">Перечисление **сохаттрибутетипе** указывает тип атрибута, хранящегося в объекте-длине типа атрибута (TLV).</span><span class="sxs-lookup"><span data-stu-id="e065c-106">The **SoHAttributeType** enumeration specifies the type of attribute stored in the attribute type-length-value (TLV) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e065c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e065c-107">Syntax</span></span>


```C++
typedef enum tagSoHAttributeType { 
  sohAttributeTypeSystemHealthId          = 2,
  sohAttributeTypeIpv4FixupServers        = 3,
  sohAttributeTypeComplianceResultCodes   = 4,
  sohAttributeTypeTimeOfLastUpdate        = 5,
  sohAttributeTypeClientId                = 6,
  sohAttributeTypeVendorSpecific          = 7,
  sohAttributeTypeHealthClass             = 8,
  sohAttributeTypeSoftwareVersion         = 9,
  sohAttributeTypeProductName             = 10,
  sohAttributeTypeHealthClassStatus       = 11,
  sohAttributeTypeSoHGenerationTime       = 12,
  sohAttributeTypeErrorCodes              = 13,
  sohAttributeTypeFailureCategory         = 14,
  sohAttributeTypeIpv6FixupServers        = 15,
  sohAttributeTypeExtendedIsolationState  = 16
} SoHAttributeType;
```



## <a name="constants"></a><span data-ttu-id="e065c-108">Константы</span><span class="sxs-lookup"><span data-stu-id="e065c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e065c-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**сохаттрибутетипесистемхеалсид**</span><span class="sxs-lookup"><span data-stu-id="e065c-109"><span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohAttributeTypeSystemHealthId**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-110">Указывает тип атрибута "идентификатор работоспособности системы".</span><span class="sxs-lookup"><span data-stu-id="e065c-110">Specifies the system health ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span><span class="sxs-lookup"><span data-stu-id="e065c-111"><span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-112">Указывает тип атрибута сервера исправления IPv4.</span><span class="sxs-lookup"><span data-stu-id="e065c-112">Specifies the IPv4 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**сохаттрибутетипекомплианцересулткодес**</span><span class="sxs-lookup"><span data-stu-id="e065c-113"><span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohAttributeTypeComplianceResultCodes**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-114">Указывает тип атрибута кода результата соответствия.</span><span class="sxs-lookup"><span data-stu-id="e065c-114">Specifies the compliance result code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**сохаттрибутетипетимеофластупдате**</span><span class="sxs-lookup"><span data-stu-id="e065c-115"><span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohAttributeTypeTimeOfLastUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-116">Задает время последнего типа атрибута обновления.</span><span class="sxs-lookup"><span data-stu-id="e065c-116">Specifies the time of the last update attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**сохаттрибутетипеклиентид**</span><span class="sxs-lookup"><span data-stu-id="e065c-117"><span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohAttributeTypeClientId**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-118">Указывает тип атрибута идентификатора клиента.</span><span class="sxs-lookup"><span data-stu-id="e065c-118">Specifies the client ID attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**сохаттрибутетипевендорспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="e065c-119"><span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohAttributeTypeVendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-120">Указывает тип атрибута, зависящий от поставщика.</span><span class="sxs-lookup"><span data-stu-id="e065c-120">Specifies the vendor-specific attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**сохаттрибутетипехеалскласс**</span><span class="sxs-lookup"><span data-stu-id="e065c-121"><span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohAttributeTypeHealthClass**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-122">Указывает тип атрибута класса работоспособности.</span><span class="sxs-lookup"><span data-stu-id="e065c-122">Specifies the health class attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**сохаттрибутетипесофтвареверсион**</span><span class="sxs-lookup"><span data-stu-id="e065c-123"><span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohAttributeTypeSoftwareVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-124">Указывает тип атрибута версии программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e065c-124">Specifies the software version attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**сохаттрибутетипепродуктнаме**</span><span class="sxs-lookup"><span data-stu-id="e065c-125"><span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohAttributeTypeProductName**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-126">Указывает тип атрибута «Название продукта».</span><span class="sxs-lookup"><span data-stu-id="e065c-126">Specifies the product name attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**сохаттрибутетипехеалсклассстатус**</span><span class="sxs-lookup"><span data-stu-id="e065c-127"><span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohAttributeTypeHealthClassStatus**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-128">Указывает тип атрибута состояния класса работоспособности.</span><span class="sxs-lookup"><span data-stu-id="e065c-128">Specifies the health class status attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**сохаттрибутетипесохженератионтиме**</span><span class="sxs-lookup"><span data-stu-id="e065c-129"><span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohAttributeTypeSoHGenerationTime**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-130">Указывает время формирования инструкции типа атрибута работоспособности.</span><span class="sxs-lookup"><span data-stu-id="e065c-130">Specifies the generation time of the Statement of Health attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**сохаттрибутетипирроркодес**</span><span class="sxs-lookup"><span data-stu-id="e065c-131"><span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohAttributeTypeErrorCodes**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-132">Задает тип атрибута кода ошибки.</span><span class="sxs-lookup"><span data-stu-id="e065c-132">Specifies the error code attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**сохаттрибутетипефаилурекатегори**</span><span class="sxs-lookup"><span data-stu-id="e065c-133"><span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohAttributeTypeFailureCategory**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-134">Указывает тип атрибута категории сбоев.</span><span class="sxs-lookup"><span data-stu-id="e065c-134">Specifies the failure category attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span><span class="sxs-lookup"><span data-stu-id="e065c-135"><span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-136">Указывает тип атрибута сервера исправления IPv6.</span><span class="sxs-lookup"><span data-stu-id="e065c-136">Specifies the IPv6 fix-up server attribute type.</span></span>

</dd> <dt>

<span data-ttu-id="e065c-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**сохаттрибутетипикстендедисолатионстате**</span><span class="sxs-lookup"><span data-stu-id="e065c-137"><span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohAttributeTypeExtendedIsolationState**</span></span>
</dt> <dd>

<span data-ttu-id="e065c-138">Задает расширенный тип атрибута состояния изоляции.</span><span class="sxs-lookup"><span data-stu-id="e065c-138">Specifies the extended isolation state attribute type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e065c-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e065c-139">Remarks</span></span>

<span data-ttu-id="e065c-140">Структура [**сохаттрибутевалуе**](sohattributevalue-union.md) определяет значения атрибутов, соответствующие каждому типу атрибута.</span><span class="sxs-lookup"><span data-stu-id="e065c-140">The [**SoHAttributeValue**](sohattributevalue-union.md) structure defines the attribute values that correspond to each attribute type.</span></span>

<span data-ttu-id="e065c-141">Эти типы атрибутов используются системой защиты доступа к сети:</span><span class="sxs-lookup"><span data-stu-id="e065c-141">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="e065c-142">сохаттрибутетипесистемхеалсид</span><span class="sxs-lookup"><span data-stu-id="e065c-142">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="e065c-143">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="e065c-143">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="e065c-144">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="e065c-144">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="e065c-145">сохаттрибутетипекомплианцересулткодес</span><span class="sxs-lookup"><span data-stu-id="e065c-145">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="e065c-146">сохаттрибутетипефаилурекатегори</span><span class="sxs-lookup"><span data-stu-id="e065c-146">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="e065c-147">Остальные типы предназначены только для помощи SHA и SHV.</span><span class="sxs-lookup"><span data-stu-id="e065c-147">The rest of the types are only intended to guide the usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="e065c-148">Требования</span><span class="sxs-lookup"><span data-stu-id="e065c-148">Requirements</span></span>



| <span data-ttu-id="e065c-149">Требование</span><span class="sxs-lookup"><span data-stu-id="e065c-149">Requirement</span></span> | <span data-ttu-id="e065c-150">Значение</span><span class="sxs-lookup"><span data-stu-id="e065c-150">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e065c-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e065c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e065c-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e065c-152">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e065c-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e065c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e065c-154">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e065c-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e065c-155">Header</span><span class="sxs-lookup"><span data-stu-id="e065c-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="e065c-156"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="e065c-156"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="e065c-157">IDL</span><span class="sxs-lookup"><span data-stu-id="e065c-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e065c-158"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e065c-158"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e065c-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e065c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e065c-160">**сохаттрибутевалуе**</span><span class="sxs-lookup"><span data-stu-id="e065c-160">**SoHAttributeValue**</span></span>](sohattributevalue-union.md)
</dt> <dt>

[<span data-ttu-id="e065c-161">**сохаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="e065c-161">**SoHAttribute**</span></span>](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[<span data-ttu-id="e065c-162">**Состояния**</span><span class="sxs-lookup"><span data-stu-id="e065c-162">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[<span data-ttu-id="e065c-163">**инапсохконструктор**</span><span class="sxs-lookup"><span data-stu-id="e065c-163">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> <dt>

[<span data-ttu-id="e065c-164">**инапсохпроцессор**</span><span class="sxs-lookup"><span data-stu-id="e065c-164">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





