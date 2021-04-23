---
title: Структура ГУЕСТОСВЕРСИОНИНФОЕКС (Впккоминтерфацес. h)
description: Содержит сведения о версии операционной системы для гостевой операционной системы.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- Структура ГУЕСТОСВЕРСИОНИНФОЕКС Virtual PC
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136298"
---
# <a name="guestosversioninfoex-structure"></a><span data-ttu-id="644d0-104">Структура ГУЕСТОСВЕРСИОНИНФОЕКС</span><span class="sxs-lookup"><span data-stu-id="644d0-104">GUESTOSVERSIONINFOEX structure</span></span>

<span data-ttu-id="644d0-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="644d0-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="644d0-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="644d0-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="644d0-107">Содержит сведения о версии операционной системы для гостевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="644d0-107">Contains operating system version information for the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="644d0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="644d0-108">Syntax</span></span>


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a><span data-ttu-id="644d0-109">Члены</span><span class="sxs-lookup"><span data-stu-id="644d0-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="644d0-110">**двосверсионинфосизе**</span><span class="sxs-lookup"><span data-stu-id="644d0-110">**dwOSVersionInfoSize**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-111">Размер этой структуры данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="644d0-111">The size of this data structure, in bytes.</span></span> <span data-ttu-id="644d0-112">Присвойте этому элементу значение `sizeof(GUESTOSVERSIONINFOEX)` .</span><span class="sxs-lookup"><span data-stu-id="644d0-112">Set this member to `sizeof(GUESTOSVERSIONINFOEX)`.</span></span>

</dd> <dt>

<span data-ttu-id="644d0-113">**двмажорверсион**</span><span class="sxs-lookup"><span data-stu-id="644d0-113">**dwMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-114">Основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="644d0-114">The major version number.</span></span>

</dd> <dt>

<span data-ttu-id="644d0-115">**двминорверсион**</span><span class="sxs-lookup"><span data-stu-id="644d0-115">**dwMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-116">Дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="644d0-116">The minor version number.</span></span>

</dd> <dt>

<span data-ttu-id="644d0-117">**двбуилднумбер**</span><span class="sxs-lookup"><span data-stu-id="644d0-117">**dwBuildNumber**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-118">Номер построения.</span><span class="sxs-lookup"><span data-stu-id="644d0-118">The build number.</span></span>

</dd> <dt>

<span data-ttu-id="644d0-119">**двплатформид**</span><span class="sxs-lookup"><span data-stu-id="644d0-119">**dwPlatformId**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-120">Платформа операционной системы.</span><span class="sxs-lookup"><span data-stu-id="644d0-120">The operating system platform.</span></span> <span data-ttu-id="644d0-121">Этот член может быть **\_ платформой версии \_ Win32 \_ NT** (2).</span><span class="sxs-lookup"><span data-stu-id="644d0-121">This member can be **VER\_PLATFORM\_WIN32\_NT** (2).</span></span>

</dd> <dt>

<span data-ttu-id="644d0-122">**сзксдверсион**</span><span class="sxs-lookup"><span data-stu-id="644d0-122">**szCSDVersion**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-123">Строка, завершающаяся нулем, например "пакет обновления 3", которая указывает на последний установленный в системе пакет обновления.</span><span class="sxs-lookup"><span data-stu-id="644d0-123">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="644d0-124">Если пакет обновления не установлен, строка пуста.</span><span class="sxs-lookup"><span data-stu-id="644d0-124">If no Service Pack has been installed, the string is empty.</span></span>

</dd> <dt>

<span data-ttu-id="644d0-125">**всервицепаккмажор**</span><span class="sxs-lookup"><span data-stu-id="644d0-125">**wServicePackMajor**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-126">Основной номер версии последнего установленного пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="644d0-126">The major version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="644d0-127">**всервицепаккминор**</span><span class="sxs-lookup"><span data-stu-id="644d0-127">**wServicePackMinor**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-128">Дополнительный номер версии последнего установленного пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="644d0-128">The minor version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="644d0-129">**всуитемаск**</span><span class="sxs-lookup"><span data-stu-id="644d0-129">**wSuiteMask**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-130">Битовая маска, определяющая наборы продуктов, доступные в системе.</span><span class="sxs-lookup"><span data-stu-id="644d0-130">A bitmask that identifies the product suites available on the system.</span></span> <span data-ttu-id="644d0-131">Этот элемент может быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="644d0-131">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="644d0-132">Значение</span><span class="sxs-lookup"><span data-stu-id="644d0-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="644d0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="644d0-133">Meaning</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <span data-ttu-id="644d0-134"><dt>**Версия \_ НАБОР \_ BackOffice**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-134"><dt>**VER\_SUITE\_BACKOFFICE**</dt> <dt>0x00000004</dt></span></span> </dl>                                            | <span data-ttu-id="644d0-135">Компоненты Microsoft BackOffice установлены.</span><span class="sxs-lookup"><span data-stu-id="644d0-135">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <span data-ttu-id="644d0-136"><dt>**Версия \_ \_Колонка "набор**</dt> " <dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-136"><dt>**VER\_SUITE\_BLADE**</dt> <dt>0x00000400</dt></span></span> </dl>                                                           | <span data-ttu-id="644d0-137">Установлен выпуск Windows Server 2003, Web Edition.</span><span class="sxs-lookup"><span data-stu-id="644d0-137">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <span data-ttu-id="644d0-138"><dt>**Версия \_ НАБОР \_ вычислений для \_ сервера**</dt> <dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-138"><dt>**VER\_SUITE\_COMPUTE\_SERVER**</dt> <dt>0x00004000</dt></span></span> </dl>                               | <span data-ttu-id="644d0-139">Windows Server 2003, выпуски Compute Cluster Edition установлены.</span><span class="sxs-lookup"><span data-stu-id="644d0-139">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <span data-ttu-id="644d0-140"><dt>**Версия \_ 0x00000080 \_ центра данных набора**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="644d0-140"><dt>**VER\_SUITE\_DATACENTER**</dt> <dt>0x00000080</dt></span></span> </dl>                                            | <span data-ttu-id="644d0-141">Установлен Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition или Windows 2000 Datacenter Server.</span><span class="sxs-lookup"><span data-stu-id="644d0-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <span data-ttu-id="644d0-142"><dt>**Версия \_ Комплект \_ Enterprise**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-142"><dt>**VER\_SUITE\_ENTERPRISE**</dt> <dt>0x00000002</dt></span></span> </dl>                                            | <span data-ttu-id="644d0-143">Установлена операционная система Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition или Windows 2000 Advanced Server.</span><span class="sxs-lookup"><span data-stu-id="644d0-143">Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="644d0-144">Дополнительные сведения об этом битовом флаге см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="644d0-144">Refer to the Remarks section for more information about this bit flag.</span></span><br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <span data-ttu-id="644d0-145"><dt>**Версия \_ 0x00000040 \_ ЕМБЕДДЕДНТ Suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="644d0-145"><dt>**VER\_SUITE\_EMBEDDEDNT**</dt> <dt>0x00000040</dt></span></span> </dl>                                            | <span data-ttu-id="644d0-146">Установлена операционная система Windows XP Embedded.</span><span class="sxs-lookup"><span data-stu-id="644d0-146">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <span data-ttu-id="644d0-147"><dt>**Версия \_ \_Персональный**</dt> <dt>0x00000200</dt> Suite</span><span class="sxs-lookup"><span data-stu-id="644d0-147"><dt>**VER\_SUITE\_PERSONAL**</dt> <dt>0x00000200</dt></span></span> </dl>                                                  | <span data-ttu-id="644d0-148">Установлена ОС Windows Vista Home Premium, Windows Vista Домашняя базовая или Windows XP Home Edition.</span><span class="sxs-lookup"><span data-stu-id="644d0-148">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <span data-ttu-id="644d0-149"><dt>**Версия \_ 0x00000100 \_ СИНГЛЕУСЕРТС Suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="644d0-149"><dt>**VER\_SUITE\_SINGLEUSERTS**</dt> <dt>0x00000100</dt></span></span> </dl>                                      | <span data-ttu-id="644d0-150">Удаленный рабочий стол поддерживается, но поддерживается только один интерактивный сеанс.</span><span class="sxs-lookup"><span data-stu-id="644d0-150">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="644d0-151">Это значение задается, если система не работает в режиме сервера приложений.</span><span class="sxs-lookup"><span data-stu-id="644d0-151">This value is set unless the system is running in application server mode.</span></span><br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <span data-ttu-id="644d0-152"><dt>**Версия \_ НАБОР \_ смаллбусинесс**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-152"><dt>**VER\_SUITE\_SMALLBUSINESS**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="644d0-153">Microsoft Small Business Server был установлен в системе, но может быть обновлен до другой версии Windows.</span><span class="sxs-lookup"><span data-stu-id="644d0-153">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="644d0-154">Дополнительные сведения об этом битовом флаге см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="644d0-154">Refer to the Remarks section for more information about this bit flag.</span></span><br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <span data-ttu-id="644d0-155"><dt>**Версия \_ \_СМАЛЛБУСИНЕСС Suite \_ ограниченный**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-155"><dt>**VER\_SUITE\_SMALLBUSINESS\_RESTRICTED**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="644d0-156">Microsoft Small Business Server устанавливается с лицензией на клиентскую лицензию принудительно.</span><span class="sxs-lookup"><span data-stu-id="644d0-156">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="644d0-157">Дополнительные сведения об этом битовом флаге см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="644d0-157">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <span data-ttu-id="644d0-158"><dt>**Версия \_ 0x00002000 \_ \_ сервера хранилища Suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="644d0-158"><dt>**VER\_SUITE\_STORAGE\_SERVER**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="644d0-159">Установлен Windows Storage Server 2003 R2 или Windows Storage Server 2003.</span><span class="sxs-lookup"><span data-stu-id="644d0-159">Windows Storage Server 2003 R2 or Windows Storage Server 2003is installed.</span></span><br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <span data-ttu-id="644d0-160"><dt>**Версия \_ \_Терминальный пакет**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-160"><dt>**VER\_SUITE\_TERMINAL**</dt> <dt>0x00000010</dt></span></span> </dl>                                                  | <span data-ttu-id="644d0-161">Службы терминалов установлены.</span><span class="sxs-lookup"><span data-stu-id="644d0-161">Terminal Services is installed.</span></span> <span data-ttu-id="644d0-162">Это значение всегда задано.</span><span class="sxs-lookup"><span data-stu-id="644d0-162">This value is always set.</span></span><br/> <span data-ttu-id="644d0-163">Если **установлен \_ \_ терминал ver Suite** , но версия **ver \_ Suite \_ синглеусертс** не задана, система работает в режиме сервера приложений.</span><span class="sxs-lookup"><span data-stu-id="644d0-163">If **VER\_SUITE\_TERMINAL** is set but **VER\_SUITE\_SINGLEUSERTS** is not set, the system is running in application server mode.</span></span><br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <span data-ttu-id="644d0-164"><dt>**Версия \_ НАБОР \_ \_**</dt> , который является <dt>0x00008000ом</dt> сервера</span><span class="sxs-lookup"><span data-stu-id="644d0-164"><dt>**VER\_SUITE\_WH\_SERVER**</dt> <dt>0x00008000</dt></span></span> </dl>                                              | <span data-ttu-id="644d0-165">Установлен Windows Home Server.</span><span class="sxs-lookup"><span data-stu-id="644d0-165">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="644d0-166">**впродукттипе**</span><span class="sxs-lookup"><span data-stu-id="644d0-166">**wProductType**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-167">Дополнительные сведения о системе.</span><span class="sxs-lookup"><span data-stu-id="644d0-167">Any additional information about the system.</span></span> <span data-ttu-id="644d0-168">Этот элемент может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="644d0-168">This member can be one of the following values.</span></span>



| <span data-ttu-id="644d0-169">Значение</span><span class="sxs-lookup"><span data-stu-id="644d0-169">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="644d0-170">Значение</span><span class="sxs-lookup"><span data-stu-id="644d0-170">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <span data-ttu-id="644d0-171"><dt>**Версия \_ \_ \_ Контроллер домена NT**</dt> <dt>0x0000002</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-171"><dt>**VER\_NT\_DOMAIN\_CONTROLLER**</dt> <dt>0x0000002</dt></span></span> </dl> | <span data-ttu-id="644d0-172">Система является контроллером домена, а операционной системой является Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="644d0-172">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <span data-ttu-id="644d0-173"><dt>**Версия \_ NT \_ Server**</dt> <dt>0x0000003</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-173"><dt>**VER\_NT\_SERVER**</dt> <dt>0x0000003</dt></span></span> </dl>                                   | <span data-ttu-id="644d0-174">Операционная система — Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="644d0-174">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="644d0-175">Обратите внимание, что сервер, который также является контроллером домена, сообщается как **\_ \_ \_ контроллер домена ver NT**, а не **\_ \_ сервер ver NT**.</span><span class="sxs-lookup"><span data-stu-id="644d0-175">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <span data-ttu-id="644d0-176"><dt>**Версия \_ \_Рабочая станция NT**</dt> <dt>0x0000001</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-176"><dt>**VER\_NT\_WORKSTATION**</dt> <dt>0x0000001</dt></span></span> </dl>                    | <span data-ttu-id="644d0-177">Операционная система — Windows 7, Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="644d0-177">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="644d0-178">**вресервед**</span><span class="sxs-lookup"><span data-stu-id="644d0-178">**wReserved**</span></span>
</dt> <dd>

<span data-ttu-id="644d0-179">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="644d0-179">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="644d0-180">Требования</span><span class="sxs-lookup"><span data-stu-id="644d0-180">Requirements</span></span>



| <span data-ttu-id="644d0-181">Требование</span><span class="sxs-lookup"><span data-stu-id="644d0-181">Requirement</span></span> | <span data-ttu-id="644d0-182">Значение</span><span class="sxs-lookup"><span data-stu-id="644d0-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="644d0-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="644d0-183">Minimum supported client</span></span><br/> | <span data-ttu-id="644d0-184">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="644d0-184">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="644d0-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="644d0-185">Minimum supported server</span></span><br/> | <span data-ttu-id="644d0-186">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="644d0-186">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="644d0-187">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="644d0-187">End of client support</span></span><br/>    | <span data-ttu-id="644d0-188">Windows 7</span><span class="sxs-lookup"><span data-stu-id="644d0-188">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="644d0-189">Продукт</span><span class="sxs-lookup"><span data-stu-id="644d0-189">Product</span></span><br/>                  | <span data-ttu-id="644d0-190">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="644d0-190">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="644d0-191">Header</span><span class="sxs-lookup"><span data-stu-id="644d0-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="644d0-192"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="644d0-192"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="644d0-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="644d0-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="644d0-194">**Ивмгуестос:: Жетосверсионинфо**</span><span class="sxs-lookup"><span data-stu-id="644d0-194">**IVMGuestOS::GetOsVersionInfo**</span></span>](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

