---
title: Перечисление Вмусбдевицеклассенум (Впккоминтерфацес. h)
description: Указывает класс USB-устройства.
ms.assetid: 3f5044ea-f7a4-4524-bfb8-55db22732f81
keywords:
- Перечисление Вмусбдевицеклассенум Virtual PC
topic_type:
- apiref
api_name:
- VMUSBDeviceClassEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70335ae083ac2a80717ae64cc8c76f0aff9e791b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136714"
---
# <a name="vmusbdeviceclassenum-enumeration"></a><span data-ttu-id="b95e0-104">Перечисление Вмусбдевицеклассенум</span><span class="sxs-lookup"><span data-stu-id="b95e0-104">VMUSBDeviceClassEnum enumeration</span></span>

<span data-ttu-id="b95e0-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b95e0-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b95e0-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b95e0-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b95e0-107">Указывает класс USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="b95e0-107">Specifies the USB device class.</span></span>

## <a name="syntax"></a><span data-ttu-id="b95e0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b95e0-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUSBDeviceClass_InterfaceDescriptor  = 0x00,
  vmUSBDeviceClass_Audio                = 0x01,
  vmUSBDeviceClass_Communication        = 0x02,
  vmUSBDeviceClass_HID                  = 0x03,
  vmUSBDeviceClass_Physical             = 0x05,
  vmUSBDeviceClass_Image                = 0x06,
  vmUSBDeviceClass_Printer              = 0x07,
  vmUSBDeviceClass_MassStorage          = 0x08,
  vmUSBDeviceClass_Hub                  = 0x09,
  vmUSBDeviceClass_CDCData              = 0x0A,
  vmUSBDeviceClass_SmartCard            = 0x0B,
  vmUSBDeviceClass_ContentSecurity      = 0x0D,
  vmUSBDeviceClass_Video                = 0x0E,
  vmUSBDeviceClass_PersonalHealthcare   = 0x0F,
  vmUSBDeviceClass_DiagnosticDevice     = 0xDC,
  vmUSBDeviceClass_WirelessController   = 0xE0,
  vmUSBDeviceClass_Miscellaneous        = 0xEF,
  vmUSBDeviceClass_ApplicationSpecific  = 0xFE,
  vmUSBDeviceClass_VendorSpecific       = 0xFF
} VMUSBDeviceClassEnum;
```



## <a name="constants"></a><span data-ttu-id="b95e0-109">Константы</span><span class="sxs-lookup"><span data-stu-id="b95e0-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b95e0-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**Вмусбдевицекласс \_ интерфацедескриптор**</span><span class="sxs-lookup"><span data-stu-id="b95e0-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmUSBDeviceClass\_InterfaceDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-111">Неопознанное устройство.</span><span class="sxs-lookup"><span data-stu-id="b95e0-111">An unidentified device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**Вмусбдевицекласс \_ аудио**</span><span class="sxs-lookup"><span data-stu-id="b95e0-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmUSBDeviceClass\_Audio**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-113">Звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="b95e0-113">Audio device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**Вмусбдевицекласс \_ связь**</span><span class="sxs-lookup"><span data-stu-id="b95e0-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**vmUSBDeviceClass\_Communication**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-115">Коммуникационное устройство.</span><span class="sxs-lookup"><span data-stu-id="b95e0-115">Communication device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**Вмусбдевицекласс \_ HID**</span><span class="sxs-lookup"><span data-stu-id="b95e0-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmUSBDeviceClass\_HID**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-117">Устройство HID.</span><span class="sxs-lookup"><span data-stu-id="b95e0-117">HID device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**Вмусбдевицекласс \_ физическая**</span><span class="sxs-lookup"><span data-stu-id="b95e0-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass\_Physical**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-119">Устройство физического датчика.</span><span class="sxs-lookup"><span data-stu-id="b95e0-119">Physical sensory device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**\_изображение вмусбдевицекласс**</span><span class="sxs-lookup"><span data-stu-id="b95e0-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**vmUSBDeviceClass\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-121">Устройство сканирования или работы с образами.</span><span class="sxs-lookup"><span data-stu-id="b95e0-121">Scanning or imaging device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**\_принтер вмусбдевицекласс**</span><span class="sxs-lookup"><span data-stu-id="b95e0-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**vmUSBDeviceClass\_Printer**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-123">Устройство принтера.</span><span class="sxs-lookup"><span data-stu-id="b95e0-123">Printer device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**Вмусбдевицекласс \_ массстораже**</span><span class="sxs-lookup"><span data-stu-id="b95e0-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmUSBDeviceClass\_MassStorage**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-125">Запоминающее устройство.</span><span class="sxs-lookup"><span data-stu-id="b95e0-125">Mass storage device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**\_центр вмусбдевицекласс**</span><span class="sxs-lookup"><span data-stu-id="b95e0-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**vmUSBDeviceClass\_Hub**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-127">Устройство концентратора.</span><span class="sxs-lookup"><span data-stu-id="b95e0-127">Hub device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**Вмусбдевицекласс \_ кдкдата**</span><span class="sxs-lookup"><span data-stu-id="b95e0-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmUSBDeviceClass\_CDCData**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-129">Устройство данных CDC.</span><span class="sxs-lookup"><span data-stu-id="b95e0-129">CDC data device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**\_смарт-карта вмусбдевицекласс**</span><span class="sxs-lookup"><span data-stu-id="b95e0-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**vmUSBDeviceClass\_SmartCard**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-131">Устройство смарт-карт.</span><span class="sxs-lookup"><span data-stu-id="b95e0-131">Smart card device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**Вмусбдевицекласс \_ контентсекурити**</span><span class="sxs-lookup"><span data-stu-id="b95e0-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmUSBDeviceClass\_ContentSecurity**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-133">Устройство безопасности содержимого.</span><span class="sxs-lookup"><span data-stu-id="b95e0-133">Content security device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**\_видео вмусбдевицекласс**</span><span class="sxs-lookup"><span data-stu-id="b95e0-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**vmUSBDeviceClass\_Video**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-135">Видеоустройство.</span><span class="sxs-lookup"><span data-stu-id="b95e0-135">Video device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**Вмусбдевицекласс \_ персоналхеалскаре**</span><span class="sxs-lookup"><span data-stu-id="b95e0-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmUSBDeviceClass\_PersonalHealthcare**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-137">Устройство здравоохранения.</span><span class="sxs-lookup"><span data-stu-id="b95e0-137">Health care device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**Вмусбдевицекласс \_ диагностикдевице**</span><span class="sxs-lookup"><span data-stu-id="b95e0-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmUSBDeviceClass\_DiagnosticDevice**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-139">Диагностическое устройство.</span><span class="sxs-lookup"><span data-stu-id="b95e0-139">Diagnostic device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**Вмусбдевицекласс \_ вирелессконтроллер**</span><span class="sxs-lookup"><span data-stu-id="b95e0-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmUSBDeviceClass\_WirelessController**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-141">Беспроводное устройство.</span><span class="sxs-lookup"><span data-stu-id="b95e0-141">Wireless device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**Вмусбдевицекласс \_ Прочее**</span><span class="sxs-lookup"><span data-stu-id="b95e0-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmUSBDeviceClass\_Miscellaneous**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-143">Другое устройство.</span><span class="sxs-lookup"><span data-stu-id="b95e0-143">Miscellaneous device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**Вмусбдевицекласс \_ аппликатионспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="b95e0-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmUSBDeviceClass\_ApplicationSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-145">Устройство, зависящее от приложения.</span><span class="sxs-lookup"><span data-stu-id="b95e0-145">Application-specific device.</span></span>

</dd> <dt>

<span data-ttu-id="b95e0-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**Вмусбдевицекласс \_ вендорспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="b95e0-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmUSBDeviceClass\_VendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="b95e0-147">Устройство, относящееся к конкретному поставщику.</span><span class="sxs-lookup"><span data-stu-id="b95e0-147">Vendor-specific device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b95e0-148">Требования</span><span class="sxs-lookup"><span data-stu-id="b95e0-148">Requirements</span></span>



| <span data-ttu-id="b95e0-149">Требование</span><span class="sxs-lookup"><span data-stu-id="b95e0-149">Requirement</span></span> | <span data-ttu-id="b95e0-150">Значение</span><span class="sxs-lookup"><span data-stu-id="b95e0-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b95e0-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b95e0-151">Minimum supported client</span></span><br/> | <span data-ttu-id="b95e0-152">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b95e0-152">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b95e0-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b95e0-153">Minimum supported server</span></span><br/> | <span data-ttu-id="b95e0-154">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b95e0-154">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b95e0-155">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b95e0-155">End of client support</span></span><br/>    | <span data-ttu-id="b95e0-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b95e0-156">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b95e0-157">Продукт</span><span class="sxs-lookup"><span data-stu-id="b95e0-157">Product</span></span><br/>                  | <span data-ttu-id="b95e0-158">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b95e0-158">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b95e0-159">Header</span><span class="sxs-lookup"><span data-stu-id="b95e0-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="b95e0-160"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b95e0-160"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b95e0-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b95e0-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b95e0-162">**Ивмусбдевице::D Евицекласс**</span><span class="sxs-lookup"><span data-stu-id="b95e0-162">**IVMUSBDevice::DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)
</dt> </dl>

 

