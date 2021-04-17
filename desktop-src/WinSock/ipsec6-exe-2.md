---
description: Настройка политик IPSec и сопоставлений безопасности для IPv6 выполняется с Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711028"
---
# <a name="ipsec6exe"></a><span data-ttu-id="22bf0-103">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="22bf0-103">Ipsec6.exe</span></span>

<span data-ttu-id="22bf0-104">Настройка политик IPSec и сопоставлений безопасности для IPv6 выполняется с Ipsec6.exe.</span><span class="sxs-lookup"><span data-stu-id="22bf0-104">Configuration of IPSec policies and security associations for IPv6 is done with Ipsec6.exe.</span></span> <span data-ttu-id="22bf0-105">Ниже приведены Ipsec6.exe подкоманды.</span><span class="sxs-lookup"><span data-stu-id="22bf0-105">The following are Ipsec6.exe subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="22bf0-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 SP \[** _Интерфейс_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="22bf0-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 sp \[**_Interface_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="22bf0-107">Отображает активные политики безопасности.</span><span class="sxs-lookup"><span data-stu-id="22bf0-107">Displays active security policies.</span></span> <span data-ttu-id="22bf0-108">Кроме того, отображает активные политики безопасности для определенного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="22bf0-108">Alternately, displays active security policies for a specific interface.</span></span>

</dd> <dt>

<span data-ttu-id="22bf0-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 SA**</span><span class="sxs-lookup"><span data-stu-id="22bf0-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 sa**</span></span>
</dt> <dd>

<span data-ttu-id="22bf0-110">Отображает активные сопоставления безопасности.</span><span class="sxs-lookup"><span data-stu-id="22bf0-110">Displays active security associations.</span></span>

</dd> <dt>

<span data-ttu-id="22bf0-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[** _Имя файла (без расширения)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="22bf0-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="22bf0-112">Создает файлы, используемые для настройки политик безопасности и сопоставлений безопасности.</span><span class="sxs-lookup"><span data-stu-id="22bf0-112">Creates files used to configure security policy and security associations.</span></span> <span data-ttu-id="22bf0-113">Создает *файл filename*. SPD для политик безопасности и *filename*. sad для сопоставлений безопасности.</span><span class="sxs-lookup"><span data-stu-id="22bf0-113">Creates *FileName*.spd for security policies and *FileName*.sad for security associations.</span></span> <span data-ttu-id="22bf0-114">Используйте созданные файлы в качестве шаблонов для настройки политик безопасности или сопоставлений безопасности.</span><span class="sxs-lookup"><span data-stu-id="22bf0-114">Use the created files as templates to configure security policies or security associations.</span></span> <span data-ttu-id="22bf0-115">Файлы можно изменить в текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="22bf0-115">The files can be modified with a text editor.</span></span> <span data-ttu-id="22bf0-116">Чтобы вызвать конфигурацию, содержащуюся в файлах SPD и SAD, используйте команду **ipsec6** .</span><span class="sxs-lookup"><span data-stu-id="22bf0-116">To invoke the configuration contained in the SPD and SAD files, use the **ipsec6 a** command.</span></span>

</dd> <dt>

<span data-ttu-id="22bf0-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 a \[** _Имя файла (без расширения)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="22bf0-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 a \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="22bf0-118">Добавляет политики *безопасности в файле filename.* SPD и сопоставления безопасности в файле *filename*. sad в список активных политик безопасности и сопоставлений безопасности.</span><span class="sxs-lookup"><span data-stu-id="22bf0-118">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations.</span></span>

</dd> <dt>

<span data-ttu-id="22bf0-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[**  *_\] \[_* _Имя файла политики (без расширения)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="22bf0-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[**_Policy_*_\] \[_*_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="22bf0-120">Добавляет политики безопасности в *файл* filename. SPD и сопоставления безопасности в файле *filename*. sad в список активных политик безопасности и сопоставлений безопасности, на которые ссылается номер политики.</span><span class="sxs-lookup"><span data-stu-id="22bf0-120">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations as referenced by policy number.</span></span>

</dd> <dt>

<span data-ttu-id="22bf0-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[ Type = SP SA \] \[** _индекснумбер_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="22bf0-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[type = sp sa\] \[**_IndexNumber_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="22bf0-122">Удаляет политики безопасности или сопоставления безопасности из списка активных политик безопасности и сопоставлений безопасности, которые указываются по номеру индекса (отображается с помощью **ipsec6 SP** или **ipsec6 SA**).</span><span class="sxs-lookup"><span data-stu-id="22bf0-122">Deletes security policies or security associations from the list of active security policies and security associations, as referenced by their index number (displayed with **ipsec6 sp** or **ipsec6 sa**).</span></span>

</dd> </dl>

 

 



