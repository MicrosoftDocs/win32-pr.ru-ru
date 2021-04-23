---
title: Объединение Сохаттрибутевалуе (Наппротокол. h)
description: Определяет содержимое члена типа в структуре Сохаттрибуте.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- Сохаттрибутевалуе объединения NAP
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492333"
---
# <a name="sohattributevalue-union"></a><span data-ttu-id="c8b19-104">Объединение Сохаттрибутевалуе</span><span class="sxs-lookup"><span data-stu-id="c8b19-104">SoHAttributeValue union</span></span>

> [!Note]  
> <span data-ttu-id="c8b19-105">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="c8b19-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c8b19-106">Объединение **сохаттрибутевалуе** определяет содержимое члена **типа** в структуре [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .</span><span class="sxs-lookup"><span data-stu-id="c8b19-106">The **SoHAttributeValue** union defines the contents of the **type** member in a [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span> <span data-ttu-id="c8b19-107">Структура объединения **сохаттрибутевалуе** определяется [**сохаттрибутетипе**](sohattributetype-enum.md) , указанным в элементе **Type** структуры [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .</span><span class="sxs-lookup"><span data-stu-id="c8b19-107">The structure of the **SoHAttributeValue** union is determined by the [**SoHAttributeType**](sohattributetype-enum.md) specified in the **type** member of the [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b19-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8b19-108">Syntax</span></span>


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a><span data-ttu-id="c8b19-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c8b19-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="c8b19-110">**идвал**</span><span class="sxs-lookup"><span data-stu-id="c8b19-110">**idVal**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-111">**регистр (Сохаттрибутетипесистемхеалсид)**</span><span class="sxs-lookup"><span data-stu-id="c8b19-111">**case(sohAttributeTypeSystemHealthId)**</span></span>

<span data-ttu-id="c8b19-112">Уникальный [системхеалсентитид](nap-datatypes.md) , содержащий идентификатор агента работоспособности системы (SHA) или средство проверки работоспособности системы (SHV), в котором был создан этот пакет [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="c8b19-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the System Health Agent (SHA) or System Health Validator (SHV) that constructed this [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="c8b19-113">**v4AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="c8b19-113">**v4AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-114">**регистр (sohAttributeTypeIpv4FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="c8b19-114">**case(sohAttributeTypeIpv4FixupServers)**</span></span>

<span data-ttu-id="c8b19-115">IPv4-адреса серверов исправления, используемых системой защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="c8b19-115">The IPv4 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="c8b19-116">**count**</span><span class="sxs-lookup"><span data-stu-id="c8b19-116">**count**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-117">Число IPv4-адресов в члене **addresses** в диапазоне от 1 до [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8b19-117">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8b19-118">**Addresses**</span><span class="sxs-lookup"><span data-stu-id="c8b19-118">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-119">Массив структур [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) , содержащих IPv4-адреса.</span><span class="sxs-lookup"><span data-stu-id="c8b19-119">An array of [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c8b19-120">**v6AddressesVal**</span><span class="sxs-lookup"><span data-stu-id="c8b19-120">**v6AddressesVal**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-121">**регистр (sohAttributeTypeIpv6FixupServers)**</span><span class="sxs-lookup"><span data-stu-id="c8b19-121">**case(sohAttributeTypeIpv6FixupServers)**</span></span>

<span data-ttu-id="c8b19-122">IPv6-адреса серверов исправления, используемых системой защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="c8b19-122">The IPv6 addresses of the fix-up servers in use by the NAP system.</span></span>

<dl> <dt>

<span data-ttu-id="c8b19-123">**count**</span><span class="sxs-lookup"><span data-stu-id="c8b19-123">**count**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-124">Число IPv4-адресов в члене **addresses** в диапазоне от 1 до [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8b19-124">The number of IPv4 addresses in the **addresses** member in the range 1 to [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8b19-125">**Addresses**</span><span class="sxs-lookup"><span data-stu-id="c8b19-125">**addresses**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-126">Массив структур [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) , содержащих IPv4-адреса.</span><span class="sxs-lookup"><span data-stu-id="c8b19-126">An array of [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) structures that contain the IPv4 addresses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c8b19-127">**кодесвал**</span><span class="sxs-lookup"><span data-stu-id="c8b19-127">**codesVal**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-128">**Case (Сохаттрибутетипекомплианцересулткодес, Сохаттрибутетипирроркодес)**</span><span class="sxs-lookup"><span data-stu-id="c8b19-128">**case(sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**</span></span>

<span data-ttu-id="c8b19-129">Структура [**ресулткодес**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) , содержащая либо определенные приложением коды результатов соответствия констант клиента, либо [**ошибки NAP**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8b19-129">A [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) structure that contains either the application defined compliance result codes of the client or [**NAP error constants**](nap-error-constants.md).</span></span> <span data-ttu-id="c8b19-130">Пакет [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) должен содержать этот TLV или TLV **сохаттрибутетипефаилурекатегори** .</span><span class="sxs-lookup"><span data-stu-id="c8b19-130">An [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet must contain this TLV or the **sohAttributeTypeFailureCategory** TLV.</span></span>

</dd> <dt>

<span data-ttu-id="c8b19-131">**датетимевал**</span><span class="sxs-lookup"><span data-stu-id="c8b19-131">**dateTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-132">**Case (Сохаттрибутетипетимеофластупдате, Сохаттрибутетипесохженератионтиме)**</span><span class="sxs-lookup"><span data-stu-id="c8b19-132">**case(sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**</span></span>

<span data-ttu-id="c8b19-133">Структура [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) , которая содержит время последнего обновления [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) или время создания **состояния работоспособности** .</span><span class="sxs-lookup"><span data-stu-id="c8b19-133">A [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that contains the time of the last [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) update or the **SoH** generation time.</span></span>

</dd> <dt>

<span data-ttu-id="c8b19-134">**вендорспеЦификвал**</span><span class="sxs-lookup"><span data-stu-id="c8b19-134">**vendorSpecificVal**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-135">**регистр (СохаттрибутетипевендорспеЦифик)**</span><span class="sxs-lookup"><span data-stu-id="c8b19-135">**case(sohAttributeTypeVendorSpecific)**</span></span>

<span data-ttu-id="c8b19-136">Зависящие от приложения данные, определяемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="c8b19-136">Application-specific data that is defined by the vendor.</span></span>

<dl> <dt>

<span data-ttu-id="c8b19-137">**Поставщика**</span><span class="sxs-lookup"><span data-stu-id="c8b19-137">**vendorId**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-138">4-байтовый идентификатор, который определяет идентификатор пары SHA/SHV.</span><span class="sxs-lookup"><span data-stu-id="c8b19-138">A 4-byte identifier that defines the SHA/SHV pair ID.</span></span> <span data-ttu-id="c8b19-139">Первые 3 байта — это код SMI поставщика, назначенный IETF, а последний байт идентифицирует сам компонент.</span><span class="sxs-lookup"><span data-stu-id="c8b19-139">The first 3 bytes are the IETF-assigned SMI code of the vendor, and the last byte identifies the component itself.</span></span> <span data-ttu-id="c8b19-140">При реализации SHA или SHV не используйте значения ИДЕНТИФИКАТОРов, назначенные внутренним компонентам работоспособности системы Майкрософт на [**константах поставщика NAP**](nap-vendor-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8b19-140">When implementing a SHA or SHV, do not use the ID values assigned to internal Microsoft system health components on [**NAP vendor constants**](nap-vendor-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8b19-141">**size**</span><span class="sxs-lookup"><span data-stu-id="c8b19-141">**size**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-142">Размер (в байтах) данных поставщика в диапазоне от 0 до ([**макссохаттрибутесизе**](nap-type-constants.md) -4).</span><span class="sxs-lookup"><span data-stu-id="c8b19-142">The size, in bytes, of the vendor data in the range 0 to ([**maxSoHAttributeSize**](nap-type-constants.md) - 4).</span></span>

</dd> <dt>

<span data-ttu-id="c8b19-143">**вендорспеЦификдата**</span><span class="sxs-lookup"><span data-stu-id="c8b19-143">**vendorSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-144">Указатель на данные конкретного поставщика в сетевом порядке байтов.</span><span class="sxs-lookup"><span data-stu-id="c8b19-144">A pointer to the vendor specific data in network byte order.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c8b19-145">**uint8Val**</span><span class="sxs-lookup"><span data-stu-id="c8b19-145">**uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-146">**Case (Сохаттрибутетипехеалскласс, Сохаттрибутетипефаилурекатегори, Сохаттрибутетипикстендедисолатионстате)**</span><span class="sxs-lookup"><span data-stu-id="c8b19-146">**case(sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory,sohAttributeTypeExtendedIsolationState)**</span></span>

<span data-ttu-id="c8b19-147">Класс работоспособности, Категория сбоя или Расширенное состояние изоляции компонента NAP как значение [**хеалсклассвалуе**](healthclassvalue-enum.md) или [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) или структура [**исолатионинфоекс**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .</span><span class="sxs-lookup"><span data-stu-id="c8b19-147">The health class, failure category, or extended isolation state of a NAP component as either a [**HealthClassValue**](healthclassvalue-enum.md) or [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) value, or a [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c8b19-148">**октетстрингвал**</span><span class="sxs-lookup"><span data-stu-id="c8b19-148">**octetStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-149">**default**</span><span class="sxs-lookup"><span data-stu-id="c8b19-149">**default**</span></span>

<span data-ttu-id="c8b19-150">Следующие значения атрибутов являются строками октета:</span><span class="sxs-lookup"><span data-stu-id="c8b19-150">The following attributes' values are octet strings:</span></span>

-   <span data-ttu-id="c8b19-151">сохаттрибутетипесофтвареверсион</span><span class="sxs-lookup"><span data-stu-id="c8b19-151">sohAttributeTypeSoftwareVersion</span></span>
-   <span data-ttu-id="c8b19-152">сохаттрибутетипеклиентид</span><span class="sxs-lookup"><span data-stu-id="c8b19-152">sohAttributeTypeClientId</span></span>
-   <span data-ttu-id="c8b19-153">сохаттрибутетипепродуктнаме</span><span class="sxs-lookup"><span data-stu-id="c8b19-153">sohAttributeTypeProductName</span></span>
-   <span data-ttu-id="c8b19-154">сохаттрибутетипехеалсклассстатус</span><span class="sxs-lookup"><span data-stu-id="c8b19-154">sohAttributeTypeHealthClassStatus</span></span>

<span data-ttu-id="c8b19-155">Для прямой совместимости все нераспознанные атрибуты возвращаются в виде строк октета.</span><span class="sxs-lookup"><span data-stu-id="c8b19-155">For forward compatibility, all unrecognized attributes are returned as octet strings.</span></span> <span data-ttu-id="c8b19-156">**данные** должны быть в сетевом порядке байтов.</span><span class="sxs-lookup"><span data-stu-id="c8b19-156">**data** must be in network byte order.</span></span>

<dl> <dt>

<span data-ttu-id="c8b19-157">**size**</span><span class="sxs-lookup"><span data-stu-id="c8b19-157">**size**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-158">Размер (в байтах) **данных** в диапазоне от 0 до [**макссохаттрибутесизе**](nap-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c8b19-158">The size, in bytes, of **data** in the range 0 to [**maxSoHAttributeSize**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8b19-159">**data**</span><span class="sxs-lookup"><span data-stu-id="c8b19-159">**data**</span></span>
</dt> <dd>

<span data-ttu-id="c8b19-160">Указатель на значение строки октета.</span><span class="sxs-lookup"><span data-stu-id="c8b19-160">A pointer to the octet string value.</span></span>

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a><span data-ttu-id="c8b19-161">Структура фактических данных</span><span class="sxs-lookup"><span data-stu-id="c8b19-161">Actual data layout</span></span>

<span data-ttu-id="c8b19-162">Из-за природы среды публикации SDK объединения не представляются явно в блоках синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="c8b19-162">Due to the nature of the SDK publishing environment, unions are not clearly represented in syntax blocks.</span></span> <span data-ttu-id="c8b19-163">Ниже приведен фактический синтаксис из файла заголовка Наппротокол. h.</span><span class="sxs-lookup"><span data-stu-id="c8b19-163">Here is the actual syntax from the NapProtocol.h header file.</span></span>


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a><span data-ttu-id="c8b19-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8b19-164">Remarks</span></span>

<span data-ttu-id="c8b19-165">Эти типы атрибутов используются системой защиты доступа к сети:</span><span class="sxs-lookup"><span data-stu-id="c8b19-165">These attribute types are consumed by the NAP system:</span></span>

-   <span data-ttu-id="c8b19-166">сохаттрибутетипесистемхеалсид</span><span class="sxs-lookup"><span data-stu-id="c8b19-166">sohAttributeTypeSystemHealthId</span></span>
-   <span data-ttu-id="c8b19-167">sohAttributeTypeIpv4FixupServers</span><span class="sxs-lookup"><span data-stu-id="c8b19-167">sohAttributeTypeIpv4FixupServers</span></span>
-   <span data-ttu-id="c8b19-168">sohAttributeTypeIpv6FixupServers</span><span class="sxs-lookup"><span data-stu-id="c8b19-168">sohAttributeTypeIpv6FixupServers</span></span>
-   <span data-ttu-id="c8b19-169">сохаттрибутетипекомплианцересулткодес</span><span class="sxs-lookup"><span data-stu-id="c8b19-169">sohAttributeTypeComplianceResultCodes</span></span>
-   <span data-ttu-id="c8b19-170">сохаттрибутетипефаилурекатегори</span><span class="sxs-lookup"><span data-stu-id="c8b19-170">sohAttributeTypeFailureCategory</span></span>

<span data-ttu-id="c8b19-171">Остальные [**сохаттрибутетипес**](sohattributetype-enum.md) предназначены исключительно в качестве нормативных руководств по использованию SHA и SHV.</span><span class="sxs-lookup"><span data-stu-id="c8b19-171">The rest of the [**SoHAttributeTypes**](sohattributetype-enum.md) are meant purely as prescriptive guidance for usage by SHAs and SHVs.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8b19-172">Требования</span><span class="sxs-lookup"><span data-stu-id="c8b19-172">Requirements</span></span>



| <span data-ttu-id="c8b19-173">Требование</span><span class="sxs-lookup"><span data-stu-id="c8b19-173">Requirement</span></span> | <span data-ttu-id="c8b19-174">Значение</span><span class="sxs-lookup"><span data-stu-id="c8b19-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b19-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8b19-175">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b19-176">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8b19-176">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c8b19-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8b19-177">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b19-178">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c8b19-178">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c8b19-179">Header</span><span class="sxs-lookup"><span data-stu-id="c8b19-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8b19-180"><dt>Наппротокол. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8b19-180"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8b19-181">IDL</span><span class="sxs-lookup"><span data-stu-id="c8b19-181">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8b19-182"><dt>Наппротокол. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8b19-182"><dt>NapProtocol.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8b19-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8b19-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8b19-184">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="c8b19-184">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="c8b19-185">Структуры NAP</span><span class="sxs-lookup"><span data-stu-id="c8b19-185">NAP Structures</span></span>](nap-structures.md)
</dt> </dl>

 

