---
description: Структура ЕКСПЕРТЕНУМИНФО предоставляет сведения о эксперте.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Структура ЕКСПЕРТЕНУМИНФО (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662206"
---
# <a name="expertenuminfo-structure"></a><span data-ttu-id="374a3-103">Структура ЕКСПЕРТЕНУМИНФО</span><span class="sxs-lookup"><span data-stu-id="374a3-103">EXPERTENUMINFO structure</span></span>

<span data-ttu-id="374a3-104">Структура **експертенуминфо** предоставляет сведения о эксперте.</span><span class="sxs-lookup"><span data-stu-id="374a3-104">The **EXPERTENUMINFO** structure provides information about the expert.</span></span> <span data-ttu-id="374a3-105">Сетевой монитор выделяет память для структуры и передает ее эксперту при вызове функции [**регистрации экспертов**](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="374a3-105">Network Monitor allocates memory for the structure, and passes it to the expert when it calls the [**Register Expert**](register-expert.md) function.</span></span> <span data-ttu-id="374a3-106">Когда эксперт получает структуру, он должен заполнить всю информацию, сетевой монитор запросы.</span><span class="sxs-lookup"><span data-stu-id="374a3-106">When the expert receives the structure, it must then fill-in all the information that Network Monitor requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="374a3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="374a3-107">Syntax</span></span>


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a><span data-ttu-id="374a3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="374a3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="374a3-109">**szName**</span><span class="sxs-lookup"><span data-stu-id="374a3-109">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-110">Имя эксперта.</span><span class="sxs-lookup"><span data-stu-id="374a3-110">Name of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="374a3-111">**сзвендор**</span><span class="sxs-lookup"><span data-stu-id="374a3-111">**szVendor**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-112">Имя поставщика, который создает эксперт.</span><span class="sxs-lookup"><span data-stu-id="374a3-112">Name of the vendor that creates the expert.</span></span>

</dd> <dt>

<span data-ttu-id="374a3-113">**сздескриптион**</span><span class="sxs-lookup"><span data-stu-id="374a3-113">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-114">Описание эксперта.</span><span class="sxs-lookup"><span data-stu-id="374a3-114">Description of the expert.</span></span> <span data-ttu-id="374a3-115">Значение элемента **сздескриптион** может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="374a3-115">The value of the **szDescription** member may be **NULL**.</span></span> <span data-ttu-id="374a3-116">Если имя слишком длинное, оно усекается в конфигурации средства просмотра по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="374a3-116">If the name is too long, it is truncated in the default viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="374a3-117">**Version**</span><span class="sxs-lookup"><span data-stu-id="374a3-117">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-118">Значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="374a3-118">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="374a3-119">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="374a3-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-120">Следующие флаги описывают эксперта.</span><span class="sxs-lookup"><span data-stu-id="374a3-120">The following flags describe the expert.</span></span>



| <span data-ttu-id="374a3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="374a3-121">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="374a3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="374a3-122">Meaning</span></span>                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <span data-ttu-id="374a3-123"><dt>**\_ \_ Настраиваемый флаг перечисления с \_ возможностью эксперта**</dt></span><span class="sxs-lookup"><span data-stu-id="374a3-123"><dt>**EXPERT\_ENUM\_FLAG\_CONFIGURABLE**</dt></span></span> </dl>                                          | <span data-ttu-id="374a3-124">Эксперт поддерживает вызовы метода [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="374a3-124">The expert supports calls to the [**Configure**](configure.md) method.</span></span> <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <span data-ttu-id="374a3-125"><dt>**\_средство просмотра флагов перечислений "Эксперт" \_ \_ \_ закрыто**</dt></span><span class="sxs-lookup"><span data-stu-id="374a3-125"><dt>**EXPERT\_ENUM\_FLAG\_VIEWER\_PRIVATE**</dt></span></span> </dl>                                   | <span data-ttu-id="374a3-126">Эксперту требуется частный (не общий) Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="374a3-126">The expert requires a private (non-shared) Event Viewer.</span></span> <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <span data-ttu-id="374a3-127"><dt>**\_флаг ПЕРЕЧИСЛЕНИЯ эксперта \_ \_ нет \_ средства просмотра**</dt></span><span class="sxs-lookup"><span data-stu-id="374a3-127"><dt>**EXPERT\_ENUM\_FLAG\_NO\_VIEWER**</dt></span></span> </dl>                                                  | <span data-ttu-id="374a3-128">Эксперт не отправляет уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="374a3-128">The expert does not send event notifications.</span></span> <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <span data-ttu-id="374a3-129"><dt>**\_флаг ПЕРЕЧИСЛЕНИЯ эксперта \_ \_ Добавить \_ меня \_ в \_ РМК \_ в \_ сводке**</dt></span><span class="sxs-lookup"><span data-stu-id="374a3-129"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_SUMMARY**</dt></span></span> </dl> | <span data-ttu-id="374a3-130">Когда фокус находится на панели сводки, эксперт отображается в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="374a3-130">When the focus is in the summary pane, the expert appears on the context menu.</span></span> <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <span data-ttu-id="374a3-131"><dt>**\_флаг ПЕРЕЧИСЛЕНИЯ эксперта \_ \_ Добавить \_ меня \_ в \_ РМК \_ \_ подробно**</dt></span><span class="sxs-lookup"><span data-stu-id="374a3-131"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_DETAIL**</dt></span></span> </dl>    | <span data-ttu-id="374a3-132">Когда фокус находится на панели подробностей, он отображается в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="374a3-132">When the focus is in the detail pane, the expert appears on the context menu.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="374a3-133">**хексперт**</span><span class="sxs-lookup"><span data-stu-id="374a3-133">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-134">Обрабатывайте эксперта.</span><span class="sxs-lookup"><span data-stu-id="374a3-134">Handle to the expert.</span></span> <span data-ttu-id="374a3-135">Если для регистрации эксперта используется структура **експертенуминфо** , параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="374a3-135">When the **EXPERTENUMINFO** structure is used to register an expert, the parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="374a3-136">**сздллнаме**</span><span class="sxs-lookup"><span data-stu-id="374a3-136">**szDllName**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-137">Закрытый член; не используйте.</span><span class="sxs-lookup"><span data-stu-id="374a3-137">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="374a3-138">**хмодуле**</span><span class="sxs-lookup"><span data-stu-id="374a3-138">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-139">Закрытый член; не используйте.</span><span class="sxs-lookup"><span data-stu-id="374a3-139">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="374a3-140">**прегистерпрок**</span><span class="sxs-lookup"><span data-stu-id="374a3-140">**pRegisterProc**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-141">Закрытый член; не используйте.</span><span class="sxs-lookup"><span data-stu-id="374a3-141">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="374a3-142">**пконфигпрок**</span><span class="sxs-lookup"><span data-stu-id="374a3-142">**pConfigProc**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-143">Закрытый член; не используйте.</span><span class="sxs-lookup"><span data-stu-id="374a3-143">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="374a3-144">**прунпрок**</span><span class="sxs-lookup"><span data-stu-id="374a3-144">**pRunProc**</span></span>
</dt> <dd>

<span data-ttu-id="374a3-145">Закрытый член; не используйте.</span><span class="sxs-lookup"><span data-stu-id="374a3-145">Private member; do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="374a3-146">Требования</span><span class="sxs-lookup"><span data-stu-id="374a3-146">Requirements</span></span>



| <span data-ttu-id="374a3-147">Требование</span><span class="sxs-lookup"><span data-stu-id="374a3-147">Requirement</span></span> | <span data-ttu-id="374a3-148">Значение</span><span class="sxs-lookup"><span data-stu-id="374a3-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="374a3-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="374a3-149">Minimum supported client</span></span><br/> | <span data-ttu-id="374a3-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="374a3-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="374a3-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="374a3-151">Minimum supported server</span></span><br/> | <span data-ttu-id="374a3-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="374a3-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="374a3-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="374a3-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="374a3-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="374a3-154"><dt>Netmon.h</dt></span></span> </dl> |



 

 




