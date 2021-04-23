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
# <a name="image-file-machine-constants"></a><span data-ttu-id="3668a-103">Константы файлового компьютера образа</span><span class="sxs-lookup"><span data-stu-id="3668a-103">Image File Machine Constants</span></span>

<span data-ttu-id="3668a-104">Описывает возможные архитектуры компьютеров.</span><span class="sxs-lookup"><span data-stu-id="3668a-104">Describes possible machine architectures.</span></span> <span data-ttu-id="3668a-105">Используется в [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) и [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span><span class="sxs-lookup"><span data-stu-id="3668a-105">Used in [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) and [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).</span></span>

<dl> <dt>

<span data-ttu-id="3668a-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**\_неизвестный файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-106"><span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**IMAGE\_FILE\_MACHINE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-107">0</span><span class="sxs-lookup"><span data-stu-id="3668a-107">0</span></span>
</dt> <dt>



<span data-ttu-id="3668a-108">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="3668a-108">Unknown</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**\_ \_ \_ целевой узел ФАЙЛового компьютера образа \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-109"><span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**IMAGE\_FILE\_MACHINE\_TARGET\_HOST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="3668a-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="3668a-111">Взаимодействует с узлом, а не с WOW64 Guest</span><span class="sxs-lookup"><span data-stu-id="3668a-111">Interacts with the host and not a WOW64 guest</span></span>

> [!Note]  
> <span data-ttu-id="3668a-112">Эта константа доступна начиная с Windows 10, версии 1607 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="3668a-112">This constant is available starting with Windows 10, version 1607 and Windows Server 2016.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**\_Файл образа \_ Machine \_ i386**</span><span class="sxs-lookup"><span data-stu-id="3668a-113"><span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**IMAGE\_FILE\_MACHINE\_I386**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-114">0x014c</span><span class="sxs-lookup"><span data-stu-id="3668a-114">0x014c</span></span>
</dt> <dt>



<span data-ttu-id="3668a-115">Intel 386</span><span class="sxs-lookup"><span data-stu-id="3668a-115">Intel 386</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**\_R3000 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-116"><span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**IMAGE\_FILE\_MACHINE\_R3000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-117">0x0162</span><span class="sxs-lookup"><span data-stu-id="3668a-117">0x0162</span></span>
</dt> <dt>



<span data-ttu-id="3668a-118">MIPS с прямым порядком байтов, 0x160 с обратным порядком байтов</span><span class="sxs-lookup"><span data-stu-id="3668a-118">MIPS little-endian, 0x160 big-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**\_R4000 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-119"><span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**IMAGE\_FILE\_MACHINE\_R4000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-120">0x0166</span><span class="sxs-lookup"><span data-stu-id="3668a-120">0x0166</span></span>
</dt> <dt>



<span data-ttu-id="3668a-121">MIPS с прямым порядком байтов</span><span class="sxs-lookup"><span data-stu-id="3668a-121">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**\_R10000 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-122"><span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**IMAGE\_FILE\_MACHINE\_R10000**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-123">0x0168</span><span class="sxs-lookup"><span data-stu-id="3668a-123">0x0168</span></span>
</dt> <dt>



<span data-ttu-id="3668a-124">MIPS с прямым порядком байтов</span><span class="sxs-lookup"><span data-stu-id="3668a-124">MIPS little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**\_WCEMIPSV2 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-125"><span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**IMAGE\_FILE\_MACHINE\_WCEMIPSV2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-126">0x0169</span><span class="sxs-lookup"><span data-stu-id="3668a-126">0x0169</span></span>
</dt> <dt>



<span data-ttu-id="3668a-127">MIPS с прямым порядком байтов ВЦЕ v2</span><span class="sxs-lookup"><span data-stu-id="3668a-127">MIPS little-endian WCE v2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**Альфа-образ \_ файлового \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-128"><span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**IMAGE\_FILE\_MACHINE\_ALPHA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-129">0x0184</span><span class="sxs-lookup"><span data-stu-id="3668a-129">0x0184</span></span>
</dt> <dt>



<span data-ttu-id="3668a-130">Альфа-версия \_ AXP</span><span class="sxs-lookup"><span data-stu-id="3668a-130">Alpha\_AXP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**\_SH3 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-131"><span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**IMAGE\_FILE\_MACHINE\_SH3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-132">0x01a2</span><span class="sxs-lookup"><span data-stu-id="3668a-132">0x01a2</span></span>
</dt> <dt>



<span data-ttu-id="3668a-133">SH3 с прямым порядком байтов</span><span class="sxs-lookup"><span data-stu-id="3668a-133">SH3 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**\_SH3DSP файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-134"><span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**IMAGE\_FILE\_MACHINE\_SH3DSP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-135">0x01a3</span><span class="sxs-lookup"><span data-stu-id="3668a-135">0x01a3</span></span>
</dt> <dt>



<span data-ttu-id="3668a-136">SH3DSP</span><span class="sxs-lookup"><span data-stu-id="3668a-136">SH3DSP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**\_SH3E файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-137"><span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**IMAGE\_FILE\_MACHINE\_SH3E**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-138">0x01a4</span><span class="sxs-lookup"><span data-stu-id="3668a-138">0x01a4</span></span>
</dt> <dt>



<span data-ttu-id="3668a-139">SH3E с прямым порядком байтов</span><span class="sxs-lookup"><span data-stu-id="3668a-139">SH3E little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**\_SH4 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-140"><span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**IMAGE\_FILE\_MACHINE\_SH4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-141">0x01a6</span><span class="sxs-lookup"><span data-stu-id="3668a-141">0x01a6</span></span>
</dt> <dt>



<span data-ttu-id="3668a-142">SH4 с прямым порядком байтов</span><span class="sxs-lookup"><span data-stu-id="3668a-142">SH4 little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**\_SH5 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-143"><span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**IMAGE\_FILE\_MACHINE\_SH5**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-144">0x01a8</span><span class="sxs-lookup"><span data-stu-id="3668a-144">0x01a8</span></span>
</dt> <dt>



<span data-ttu-id="3668a-145">SH5</span><span class="sxs-lookup"><span data-stu-id="3668a-145">SH5</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**\_ARM для файлового \_ компьютера образа \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-146"><span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**IMAGE\_FILE\_MACHINE\_ARM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-147">0x01c0</span><span class="sxs-lookup"><span data-stu-id="3668a-147">0x01c0</span></span>
</dt> <dt>



<span data-ttu-id="3668a-148">Little-Endian ARM</span><span class="sxs-lookup"><span data-stu-id="3668a-148">ARM Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**\_ \_ бегунок файл образа компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-149"><span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**IMAGE\_FILE\_MACHINE\_THUMB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-150">0x01c2</span><span class="sxs-lookup"><span data-stu-id="3668a-150">0x01c2</span></span>
</dt> <dt>



<span data-ttu-id="3668a-151">РЫЧАГ Thumb/Thumb-2 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="3668a-151">ARM Thumb/Thumb-2 Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**\_армнт файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-152"><span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**IMAGE\_FILE\_MACHINE\_ARMNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-153">0x01c4</span><span class="sxs-lookup"><span data-stu-id="3668a-153">0x01c4</span></span>
</dt> <dt>



<span data-ttu-id="3668a-154">Little-Endianый бегунок ARM-2</span><span class="sxs-lookup"><span data-stu-id="3668a-154">ARM Thumb-2 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="3668a-155">Эта константа доступна начиная с Windows 7 и Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="3668a-155">This constant is available starting with Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**\_AM33 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-156"><span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**IMAGE\_FILE\_MACHINE\_AM33**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-157">0x01d3</span><span class="sxs-lookup"><span data-stu-id="3668a-157">0x01d3</span></span>
</dt> <dt>



<span data-ttu-id="3668a-158">TAM33BD</span><span class="sxs-lookup"><span data-stu-id="3668a-158">TAM33BD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**\_файл образа \_ машины \_ POWERPC**</span><span class="sxs-lookup"><span data-stu-id="3668a-159"><span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**IMAGE\_FILE\_MACHINE\_POWERPC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-160">0x01F0</span><span class="sxs-lookup"><span data-stu-id="3668a-160">0x01F0</span></span>
</dt> <dt>



<span data-ttu-id="3668a-161">Little-Endian IBM PowerPC</span><span class="sxs-lookup"><span data-stu-id="3668a-161">IBM PowerPC Little-Endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**\_поверпкфп файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-162"><span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**IMAGE\_FILE\_MACHINE\_POWERPCFP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-163">0x01f1</span><span class="sxs-lookup"><span data-stu-id="3668a-163">0x01f1</span></span>
</dt> <dt>



<span data-ttu-id="3668a-164">поверпкфп</span><span class="sxs-lookup"><span data-stu-id="3668a-164">POWERPCFP</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**\_Файл образа \_ Machine \_ ia64**</span><span class="sxs-lookup"><span data-stu-id="3668a-165"><span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**IMAGE\_FILE\_MACHINE\_IA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-166">0x0200</span><span class="sxs-lookup"><span data-stu-id="3668a-166">0x0200</span></span>
</dt> <dt>



<span data-ttu-id="3668a-167">Intel 64</span><span class="sxs-lookup"><span data-stu-id="3668a-167">Intel 64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**\_MIPS16 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-168"><span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**IMAGE\_FILE\_MACHINE\_MIPS16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-169">0x0266</span><span class="sxs-lookup"><span data-stu-id="3668a-169">0x0266</span></span>
</dt> <dt>



<span data-ttu-id="3668a-170">MIPS</span><span class="sxs-lookup"><span data-stu-id="3668a-170">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**\_ALPHA64 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-171"><span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**IMAGE\_FILE\_MACHINE\_ALPHA64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-172">0x0284</span><span class="sxs-lookup"><span data-stu-id="3668a-172">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="3668a-173">ALPHA64</span><span class="sxs-lookup"><span data-stu-id="3668a-173">ALPHA64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**\_мипсфпу файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-174"><span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-175">0x0366</span><span class="sxs-lookup"><span data-stu-id="3668a-175">0x0366</span></span>
</dt> <dt>



<span data-ttu-id="3668a-176">MIPS</span><span class="sxs-lookup"><span data-stu-id="3668a-176">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**\_MIPSFPU16 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-177"><span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**IMAGE\_FILE\_MACHINE\_MIPSFPU16**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-178">0x0466</span><span class="sxs-lookup"><span data-stu-id="3668a-178">0x0466</span></span>
</dt> <dt>



<span data-ttu-id="3668a-179">MIPS</span><span class="sxs-lookup"><span data-stu-id="3668a-179">MIPS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**\_AXP64 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-180"><span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**IMAGE\_FILE\_MACHINE\_AXP64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-181">0x0284</span><span class="sxs-lookup"><span data-stu-id="3668a-181">0x0284</span></span>
</dt> <dt>



<span data-ttu-id="3668a-182">AXP64</span><span class="sxs-lookup"><span data-stu-id="3668a-182">AXP64</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**\_трикоре файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-183"><span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**IMAGE\_FILE\_MACHINE\_TRICORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-184">0x0520</span><span class="sxs-lookup"><span data-stu-id="3668a-184">0x0520</span></span>
</dt> <dt>



<span data-ttu-id="3668a-185">инфинеон</span><span class="sxs-lookup"><span data-stu-id="3668a-185">Infineon</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**\_CEF файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-186"><span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**IMAGE\_FILE\_MACHINE\_CEF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-187">0x0CEF</span><span class="sxs-lookup"><span data-stu-id="3668a-187">0x0CEF</span></span>
</dt> <dt>



<span data-ttu-id="3668a-188">CEF</span><span class="sxs-lookup"><span data-stu-id="3668a-188">CEF</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**\_ебк файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-189"><span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**IMAGE\_FILE\_MACHINE\_EBC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-190">0x0EBC</span><span class="sxs-lookup"><span data-stu-id="3668a-190">0x0EBC</span></span>
</dt> <dt>



<span data-ttu-id="3668a-191">Код байта EFI</span><span class="sxs-lookup"><span data-stu-id="3668a-191">EFI Byte Code</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**Файл образа на \_ \_ машине \_ AMD64**</span><span class="sxs-lookup"><span data-stu-id="3668a-192"><span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**IMAGE\_FILE\_MACHINE\_AMD64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-193">0x8664</span><span class="sxs-lookup"><span data-stu-id="3668a-193">0x8664</span></span>
</dt> <dt>



<span data-ttu-id="3668a-194">AMD64 (K8)</span><span class="sxs-lookup"><span data-stu-id="3668a-194">AMD64 (K8)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**\_M32R файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-195"><span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**IMAGE\_FILE\_MACHINE\_M32R**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-196">0x9041</span><span class="sxs-lookup"><span data-stu-id="3668a-196">0x9041</span></span>
</dt> <dt>



<span data-ttu-id="3668a-197">M32R с прямым порядком байтов</span><span class="sxs-lookup"><span data-stu-id="3668a-197">M32R little-endian</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**\_ARM64 файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-198"><span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**IMAGE\_FILE\_MACHINE\_ARM64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-199">0xAA64</span><span class="sxs-lookup"><span data-stu-id="3668a-199">0xAA64</span></span>
</dt> <dt>



<span data-ttu-id="3668a-200">ARM64 Little-Endian</span><span class="sxs-lookup"><span data-stu-id="3668a-200">ARM64 Little-Endian</span></span>

> [!Note]  
> <span data-ttu-id="3668a-201">Эта константа доступна начиная с Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="3668a-201">This constant is available starting with Windows 8.1 and Windows Server 2012 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="3668a-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**\_CEE файл образа \_ компьютера \_**</span><span class="sxs-lookup"><span data-stu-id="3668a-202"><span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**IMAGE\_FILE\_MACHINE\_CEE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3668a-203">0xC0EE</span><span class="sxs-lookup"><span data-stu-id="3668a-203">0xC0EE</span></span>
</dt> <dt>



<span data-ttu-id="3668a-204">CEE</span><span class="sxs-lookup"><span data-stu-id="3668a-204">CEE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3668a-205">Требования</span><span class="sxs-lookup"><span data-stu-id="3668a-205">Requirements</span></span>



| <span data-ttu-id="3668a-206">Требование</span><span class="sxs-lookup"><span data-stu-id="3668a-206">Requirement</span></span> | <span data-ttu-id="3668a-207">Значение</span><span class="sxs-lookup"><span data-stu-id="3668a-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3668a-208">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3668a-208">Minimum supported client</span></span><br/> | <span data-ttu-id="3668a-209">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3668a-209">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3668a-210">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3668a-210">Minimum supported server</span></span><br/> | <span data-ttu-id="3668a-211">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3668a-211">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3668a-212">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3668a-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="3668a-213"><dt>Файл Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="3668a-213"><dt>Winnt.h</dt></span></span> </dl> |



 

 




