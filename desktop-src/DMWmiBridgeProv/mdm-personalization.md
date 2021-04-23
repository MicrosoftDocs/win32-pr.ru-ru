---
title: Класс MDM_Personalization
description: '\_Класс персонализации MDM используется для задания экрана блокировки и фоновых изображений рабочего стола. Установка этих политик также не позволяет пользователю изменять образ.'
ms.assetid: 99b60767-b321-4ec6-9802-76221d26c830
keywords:
- Класс MDM_Personalization
- MDM_Personalization класс, описание
topic_type:
- apiref
api_name:
- MDM_Personalization
- MDM_Personalization.InstanceID
- MDM_Personalization.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78986422cce15d750e1ae678aef352bbb369bfc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988460"
---
# <a name="mdm_personalization-class"></a><span data-ttu-id="7f82f-106">\_Класс персонализации MDM</span><span class="sxs-lookup"><span data-stu-id="7f82f-106">MDM\_Personalization class</span></span>

<span data-ttu-id="7f82f-107">\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском.</span><span class="sxs-lookup"><span data-stu-id="7f82f-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7f82f-108">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]</span><span class="sxs-lookup"><span data-stu-id="7f82f-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7f82f-109">\_Класс персонализации MDM используется для задания экрана блокировки и фоновых изображений рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="7f82f-109">The MDM\_Personalization class is used to set the lock screen and desktop background images.</span></span> <span data-ttu-id="7f82f-110">Установка этих политик также не позволяет пользователю изменять образ.</span><span class="sxs-lookup"><span data-stu-id="7f82f-110">Setting these policies also prevents the user from changing the image.</span></span>

<span data-ttu-id="7f82f-111">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7f82f-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f82f-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f82f-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Personalization
{
  string InstanceID;
  string ParentID;
  string DesktopImageUrl;
  sint32 DesktopImageStatus;
  string LockScreenImageUrl;
  sint32 LockScreenImageStatus;
};
```

## <a name="members"></a><span data-ttu-id="7f82f-113">Члены</span><span class="sxs-lookup"><span data-stu-id="7f82f-113">Members</span></span>

<span data-ttu-id="7f82f-114">Класс **\_ персонализации MDM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7f82f-114">The **MDM\_Personalization** class has these types of members:</span></span>

-   [<span data-ttu-id="7f82f-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="7f82f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7f82f-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="7f82f-116">Properties</span></span>

<span data-ttu-id="7f82f-117">Класс **\_ персонализации MDM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7f82f-117">The **MDM\_Personalization** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7f82f-118">десктопимажестатус</span><span class="sxs-lookup"><span data-stu-id="7f82f-118">DesktopImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#desktopimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f82f-119">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7f82f-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f82f-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7f82f-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7f82f-121">DesktopImageUrl</span><span class="sxs-lookup"><span data-stu-id="7f82f-121">DesktopImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#desktopimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f82f-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f82f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f82f-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7f82f-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f82f-124">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7f82f-124">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f82f-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f82f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f82f-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f82f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f82f-127">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7f82f-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7f82f-128">локкскринимажестатус</span><span class="sxs-lookup"><span data-stu-id="7f82f-128">LockScreenImageStatus</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimagestatus)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f82f-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7f82f-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f82f-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7f82f-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7f82f-131">LockScreenImageUrl</span><span class="sxs-lookup"><span data-stu-id="7f82f-131">LockScreenImageUrl</span></span>](/windows/client-management/mdm/personalization-csp#lockscreenimageurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f82f-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f82f-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f82f-133">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7f82f-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f82f-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7f82f-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f82f-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7f82f-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f82f-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f82f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f82f-137">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7f82f-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f82f-138">Требования</span><span class="sxs-lookup"><span data-stu-id="7f82f-138">Requirements</span></span>



| <span data-ttu-id="7f82f-139">Требование</span><span class="sxs-lookup"><span data-stu-id="7f82f-139">Requirement</span></span> | <span data-ttu-id="7f82f-140">Значение</span><span class="sxs-lookup"><span data-stu-id="7f82f-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f82f-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f82f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7f82f-142">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7f82f-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7f82f-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f82f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7f82f-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7f82f-144">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="7f82f-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7f82f-145">Namespace</span></span><br/>                | <span data-ttu-id="7f82f-146">Корневой \\ CIMV2 \\ MDM \\ дммап</span><span class="sxs-lookup"><span data-stu-id="7f82f-146">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="7f82f-147">MOF</span><span class="sxs-lookup"><span data-stu-id="7f82f-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f82f-148"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f82f-148"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f82f-149">DLL</span><span class="sxs-lookup"><span data-stu-id="7f82f-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f82f-150"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f82f-150"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

