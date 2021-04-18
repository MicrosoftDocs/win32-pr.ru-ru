---
description: Содержит сведения о данных AppHelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: Структура APPHELP_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655659"
---
# <a name="apphelp_data-structure"></a><span data-ttu-id="92763-103">\_Структура данных APPHELP</span><span class="sxs-lookup"><span data-stu-id="92763-103">APPHELP\_DATA structure</span></span>

<span data-ttu-id="92763-104">Содержит сведения о данных AppHelp.</span><span class="sxs-lookup"><span data-stu-id="92763-104">Contains Apphelp data information.</span></span>

## <a name="syntax"></a><span data-ttu-id="92763-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92763-105">Syntax</span></span>


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a><span data-ttu-id="92763-106">Члены</span><span class="sxs-lookup"><span data-stu-id="92763-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="92763-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="92763-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="92763-108">Этот параметр может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="92763-108">This parameter can be one of more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="92763-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ оболочку совместимости** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="92763-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="92763-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="92763-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="92763-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**Шимрег \_ APPHELP \_ NOUI)** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="92763-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="92763-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**Шимрег \_ APPHELP \_ Cancel** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="92763-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="92763-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="92763-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="92763-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ слой** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="92763-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="92763-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**Шимрег \_ ОТКЛЮЧИТЬ \_ драйвер** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="92763-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="92763-116">**двсеверити**</span><span class="sxs-lookup"><span data-stu-id="92763-116">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="92763-117">Этот параметр может иметь значение "тип" \_ None (0).</span><span class="sxs-lookup"><span data-stu-id="92763-117">This parameter can be APPTYPE\_NONE (0).</span></span>

</dd> <dt>

<span data-ttu-id="92763-118">**двхтмлхелпид**</span><span class="sxs-lookup"><span data-stu-id="92763-118">**dwHTMLHelpID**</span></span>
</dt> <dd>

<span data-ttu-id="92763-119">Идентификатор HTML Help.</span><span class="sxs-lookup"><span data-stu-id="92763-119">The HTML Help identifier.</span></span>

</dd> <dt>

<span data-ttu-id="92763-120">**сзаппнаме**</span><span class="sxs-lookup"><span data-stu-id="92763-120">**szAppName**</span></span>
</dt> <dd>

<span data-ttu-id="92763-121">Имя приложения.</span><span class="sxs-lookup"><span data-stu-id="92763-121">The application name.</span></span>

</dd> <dt>

<span data-ttu-id="92763-122">**трексе**</span><span class="sxs-lookup"><span data-stu-id="92763-122">**trExe**</span></span>
</dt> <dd>

<span data-ttu-id="92763-123">[**Тагреф**](tagref.md) соответствующего исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="92763-123">The [**TAGREF**](tagref.md) of the corresponding executable file.</span></span>

</dd> <dt>

<span data-ttu-id="92763-124">**сзурл**</span><span class="sxs-lookup"><span data-stu-id="92763-124">**szURL**</span></span>
</dt> <dd>

<span data-ttu-id="92763-125">URL-адрес для ссылки AppHelp Online.</span><span class="sxs-lookup"><span data-stu-id="92763-125">The URL for Apphelp online link.</span></span>

</dd> <dt>

<span data-ttu-id="92763-126">**сзлинк**</span><span class="sxs-lookup"><span data-stu-id="92763-126">**szLink**</span></span>
</dt> <dd>

<span data-ttu-id="92763-127">Текст ссылки для **сзурл**.</span><span class="sxs-lookup"><span data-stu-id="92763-127">The link text for **szURL**.</span></span>

</dd> <dt>

<span data-ttu-id="92763-128">**сзапптитле**</span><span class="sxs-lookup"><span data-stu-id="92763-128">**szAppTitle**</span></span>
</dt> <dd>

<span data-ttu-id="92763-129">Заголовок сообщения AppHelp.</span><span class="sxs-lookup"><span data-stu-id="92763-129">The title for the Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="92763-130">**сзконтакт**</span><span class="sxs-lookup"><span data-stu-id="92763-130">**szContact**</span></span>
</dt> <dd>

<span data-ttu-id="92763-131">Контактные данные поставщика.</span><span class="sxs-lookup"><span data-stu-id="92763-131">The vendor contact information.</span></span>

</dd> <dt>

<span data-ttu-id="92763-132">**сздетаилс**</span><span class="sxs-lookup"><span data-stu-id="92763-132">**szDetails**</span></span>
</dt> <dd>

<span data-ttu-id="92763-133">Подробное сообщение AppHelp.</span><span class="sxs-lookup"><span data-stu-id="92763-133">The detailed Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="92763-134">**двдата**</span><span class="sxs-lookup"><span data-stu-id="92763-134">**dwData**</span></span>
</dt> <dd>

<span data-ttu-id="92763-135">Определяемые пользователем данные, управляемые приложением.</span><span class="sxs-lookup"><span data-stu-id="92763-135">User-defined data managed by the application.</span></span>

</dd> <dt>

<span data-ttu-id="92763-136">**бспентри**</span><span class="sxs-lookup"><span data-stu-id="92763-136">**bSPEntry**</span></span>
</dt> <dd>

<span data-ttu-id="92763-137">Этот член имеет **значение true** , если эта запись находится в базе данных пакета обновления, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="92763-137">This member is **TRUE** if this entry is in the service pack database and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92763-138">Требования</span><span class="sxs-lookup"><span data-stu-id="92763-138">Requirements</span></span>



| <span data-ttu-id="92763-139">Требование</span><span class="sxs-lookup"><span data-stu-id="92763-139">Requirement</span></span> | <span data-ttu-id="92763-140">Значение</span><span class="sxs-lookup"><span data-stu-id="92763-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="92763-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92763-141">Minimum supported client</span></span><br/> | <span data-ttu-id="92763-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92763-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="92763-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92763-143">Minimum supported server</span></span><br/> | <span data-ttu-id="92763-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92763-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92763-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92763-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92763-146">**сдбреадапфелпдетаилсдата**</span><span class="sxs-lookup"><span data-stu-id="92763-146">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




