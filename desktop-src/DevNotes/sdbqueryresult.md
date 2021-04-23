---
description: Содержит результаты запроса к базе данных оболочек для соответствующего исполняемого файла.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: Структура СДБКУЕРИРЕСУЛТ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990469"
---
# <a name="sdbqueryresult-structure"></a><span data-ttu-id="e9229-103">Структура СДБКУЕРИРЕСУЛТ</span><span class="sxs-lookup"><span data-stu-id="e9229-103">SDBQUERYRESULT structure</span></span>

<span data-ttu-id="e9229-104">Содержит результаты запроса к базе данных оболочек для соответствующего исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="e9229-104">Contains the results from querying the shim database for a matching executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9229-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9229-105">Syntax</span></span>


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a><span data-ttu-id="e9229-106">Члены</span><span class="sxs-lookup"><span data-stu-id="e9229-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9229-107">**атрексес**</span><span class="sxs-lookup"><span data-stu-id="e9229-107">**atrExes**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-108">Значения **тагреф** для соответствующих исполняемых файлов.</span><span class="sxs-lookup"><span data-stu-id="e9229-108">The **TAGREF** values of the matching executable files.</span></span> <span data-ttu-id="e9229-109">Обратите внимание, что **SDB \_ Max \_ exe** определяется как 16.</span><span class="sxs-lookup"><span data-stu-id="e9229-109">Note that **SDB\_MAX\_EXES** is defined as 16.</span></span>

</dd> <dt>

<span data-ttu-id="e9229-110">**адвексефлагс**</span><span class="sxs-lookup"><span data-stu-id="e9229-110">**adwExeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-111">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e9229-111">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e9229-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ оболочку совместимости** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="e9229-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e9229-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Шимрег \_ APPHELP \_ NOUI)** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="e9229-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Шимрег \_ APPHELP \_ Cancel** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="e9229-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="e9229-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ слой** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="e9229-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ драйвер** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="e9229-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="e9229-119">**атрлайерс**</span><span class="sxs-lookup"><span data-stu-id="e9229-119">**atrLayers**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-120">Значения **тагреф** соответствующих слоев.</span><span class="sxs-lookup"><span data-stu-id="e9229-120">The **TAGREF** values of the matching layers.</span></span> <span data-ttu-id="e9229-121">Обратите внимание, что **SDB \_ Max \_ слоев** определяется как 8.</span><span class="sxs-lookup"><span data-stu-id="e9229-121">Note that **SDB\_MAX\_LAYERS** is defined as 8.</span></span>

</dd> <dt>

<span data-ttu-id="e9229-122">**двлайерфлагс**</span><span class="sxs-lookup"><span data-stu-id="e9229-122">**dwLayerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-123">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e9229-123">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e9229-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ оболочку совместимости** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="e9229-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e9229-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Шимрег \_ APPHELP \_ NOUI)** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="e9229-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Шимрег \_ APPHELP \_ Cancel** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="e9229-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="e9229-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ слой** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="e9229-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ драйвер** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="e9229-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="e9229-131">**трапфелп**</span><span class="sxs-lookup"><span data-stu-id="e9229-131">**trApphelp**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-132">Значение **тагреф** сообщения AppHelp соответствующего исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="e9229-132">The **TAGREF** value of the apphelp message of the corresponding executable.</span></span>

</dd> <dt>

<span data-ttu-id="e9229-133">**двексекаунт**</span><span class="sxs-lookup"><span data-stu-id="e9229-133">**dwExeCount**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-134">Число элементов в **атрексес**.</span><span class="sxs-lookup"><span data-stu-id="e9229-134">The number of elements in **atrExes**.</span></span>

</dd> <dt>

<span data-ttu-id="e9229-135">**двлайеркаунт**</span><span class="sxs-lookup"><span data-stu-id="e9229-135">**dwLayerCount**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-136">Число элементов в **атрлайерс**.</span><span class="sxs-lookup"><span data-stu-id="e9229-136">The number of elements in **atrLayers**.</span></span>

</dd> <dt>

<span data-ttu-id="e9229-137">**guidID**</span><span class="sxs-lookup"><span data-stu-id="e9229-137">**guidID**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-138">Идентификатор GUID последнего исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="e9229-138">The GUID of the last executable file.</span></span>

</dd> <dt>

<span data-ttu-id="e9229-139">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="e9229-139">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-140">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e9229-140">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e9229-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ оболочку совместимости** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="e9229-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="e9229-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Шимрег \_ APPHELP \_ NOUI)** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="e9229-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Шимрег \_ APPHELP \_ Cancel** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="e9229-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="e9229-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ слой** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="e9229-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="e9229-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ драйвер** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="e9229-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="e9229-148">**двкустомсдбмап**</span><span class="sxs-lookup"><span data-stu-id="e9229-148">**dwCustomSDBMap**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-149">Схема пользовательских баз данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="e9229-149">A map of the custom shim databases.</span></span> <span data-ttu-id="e9229-150">Соответствующие биты задаются, если **рггуиддб** является допустимым.</span><span class="sxs-lookup"><span data-stu-id="e9229-150">The corresponding bits are set if **rgGuidDB** is valid.</span></span>

</dd> <dt>

<span data-ttu-id="e9229-151">**рггуиддб**</span><span class="sxs-lookup"><span data-stu-id="e9229-151">**rgGuidDB**</span></span>
</dt> <dd>

<span data-ttu-id="e9229-152">Идентификаторы GUID баз данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="e9229-152">The GUIDs of the shim databases.</span></span> <span data-ttu-id="e9229-153">Обратите внимание, что **SDB \_ Max \_ сдбс** определяется как 16.</span><span class="sxs-lookup"><span data-stu-id="e9229-153">Note that **SDB\_MAX\_SDBS** is defined as 16.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9229-154">Требования</span><span class="sxs-lookup"><span data-stu-id="e9229-154">Requirements</span></span>



| <span data-ttu-id="e9229-155">Требование</span><span class="sxs-lookup"><span data-stu-id="e9229-155">Requirement</span></span> | <span data-ttu-id="e9229-156">Значение</span><span class="sxs-lookup"><span data-stu-id="e9229-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e9229-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9229-157">Minimum supported client</span></span><br/> | <span data-ttu-id="e9229-158">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9229-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e9229-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9229-159">Minimum supported server</span></span><br/> | <span data-ttu-id="e9229-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9229-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9229-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9229-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9229-162">**сдбжетматчинжексе**</span><span class="sxs-lookup"><span data-stu-id="e9229-162">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> </dl>

 

 




