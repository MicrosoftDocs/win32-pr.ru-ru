---
description: Описывает возможные архитектуры компьютеров.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Константы файлового компьютера образа (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542671"
---
# <a name="image-file-machine-constants"></a>Константы файлового компьютера образа

Описывает возможные архитектуры компьютеров. Используется в [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) и [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).

<dl> <dt>

<span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**\_неизвестный файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Неизвестно


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**\_ \_ \_ целевой узел ФАЙЛового компьютера образа \_**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Взаимодействует с узлом, а не с WOW64 Guest

> [!Note]  
> Эта константа доступна начиная с Windows 10, версии 1607 и Windows Server 2016.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**\_Файл образа \_ Machine \_ i386**
</dt> <dd> <dl> <dt>

0x014c
</dt> <dt>



Intel 386


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**\_R3000 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0162
</dt> <dt>



MIPS с прямым порядком байтов, 0x160 с обратным порядком байтов


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**\_R4000 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0166
</dt> <dt>



MIPS с прямым порядком байтов


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**\_R10000 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0168
</dt> <dt>



MIPS с прямым порядком байтов


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**\_WCEMIPSV2 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0169
</dt> <dt>



MIPS с прямым порядком байтов ВЦЕ v2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**Альфа-образ \_ файлового \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0184
</dt> <dt>



Альфа-версия \_ AXP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**\_SH3 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x01a2
</dt> <dt>



SH3 с прямым порядком байтов


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**\_SH3DSP файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x01a3
</dt> <dt>



SH3DSP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**\_SH3E файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x01a4
</dt> <dt>



SH3E с прямым порядком байтов


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**\_SH4 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x01a6
</dt> <dt>



SH4 с прямым порядком байтов


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**\_SH5 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x01a8
</dt> <dt>



SH5


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**\_ARM для файлового \_ компьютера образа \_**
</dt> <dd> <dl> <dt>

0x01c0
</dt> <dt>



Little-Endian ARM


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**\_ \_ бегунок файл образа компьютера \_**
</dt> <dd> <dl> <dt>

0x01c2
</dt> <dt>



РЫЧАГ Thumb/Thumb-2 Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**\_армнт файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x01c4
</dt> <dt>



Little-Endianый бегунок ARM-2

> [!Note]  
> Эта константа доступна начиная с Windows 7 и Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**\_AM33 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x01d3
</dt> <dt>



TAM33BD


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**\_файл образа \_ машины \_ POWERPC**
</dt> <dd> <dl> <dt>

0x01F0
</dt> <dt>



Little-Endian IBM PowerPC


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**\_поверпкфп файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x01f1
</dt> <dt>



поверпкфп


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**\_Файл образа \_ Machine \_ ia64**
</dt> <dd> <dl> <dt>

0x0200
</dt> <dt>



Intel 64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**\_MIPS16 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0266
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**\_ALPHA64 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



ALPHA64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**\_мипсфпу файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0366
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**\_MIPSFPU16 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0466
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**\_AXP64 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



AXP64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**\_трикоре файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0520
</dt> <dt>



инфинеон


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**\_CEF файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0CEF
</dt> <dt>



CEF


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**\_ебк файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x0EBC
</dt> <dt>



Код байта EFI


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**Файл образа на \_ \_ машине \_ AMD64**
</dt> <dd> <dl> <dt>

0x8664
</dt> <dt>



AMD64 (K8)


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**\_M32R файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0x9041
</dt> <dt>



M32R с прямым порядком байтов


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**\_ARM64 файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0xAA64
</dt> <dt>



ARM64 Little-Endian

> [!Note]  
> Эта константа доступна начиная с Windows 8.1 и Windows Server 2012 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**\_CEE файл образа \_ компьютера \_**
</dt> <dd> <dl> <dt>

0xC0EE
</dt> <dt>



CEE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Файл Winnt. h</dt> </dl> |



 

 




