---
description: Интерфейс Исканпрофилемгр предоставляет методы для создания, открытия, удаления профилей сканирования и управления ими.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Интерфейс Исканпрофилемгр (Сканпрофилемгр. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 9f0762befdda272b91451dcca67c3f9560ad354e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662587"
---
# <a name="iscanprofilemgr-interface"></a><span data-ttu-id="97592-103">Интерфейс Исканпрофилемгр</span><span class="sxs-lookup"><span data-stu-id="97592-103">IScanProfileMgr interface</span></span>

<span data-ttu-id="97592-104">Интерфейс **исканпрофилемгр** предоставляет методы для создания, открытия, удаления профилей сканирования и управления ими.</span><span class="sxs-lookup"><span data-stu-id="97592-104">The **IScanProfileMgr** interface provides methods for creating, opening, deleting, and managing scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="97592-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="97592-105">Members</span></span>

<span data-ttu-id="97592-106">Интерфейс **исканпрофилемгр** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="97592-106">The **IScanProfileMgr** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="97592-107">**Исканпрофилемгр** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="97592-107">**IScanProfileMgr** also has these types of members:</span></span>

-   [<span data-ttu-id="97592-108">Методы</span><span class="sxs-lookup"><span data-stu-id="97592-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97592-109">Методы</span><span class="sxs-lookup"><span data-stu-id="97592-109">Methods</span></span>

<span data-ttu-id="97592-110">Интерфейс **исканпрофилемгр** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="97592-110">The **IScanProfileMgr** interface has these methods.</span></span>



| <span data-ttu-id="97592-111">Метод</span><span class="sxs-lookup"><span data-stu-id="97592-111">Method</span></span>                                                                              | <span data-ttu-id="97592-112">Описание</span><span class="sxs-lookup"><span data-stu-id="97592-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97592-113">**креатепрофиле**</span><span class="sxs-lookup"><span data-stu-id="97592-113">**CreateProfile**</span></span>](-wia-iscanprofilemgr-createprofile.md)                         | <span data-ttu-id="97592-114">Создает пустой профиль сканирования и связывает его с сканером или другим элементом WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="97592-114">Creates an empty scan profile and associates it with a scanner or other WIA 2.0 item.</span></span><br/>                       |
| [<span data-ttu-id="97592-115">**делетеаллпрофилес**</span><span class="sxs-lookup"><span data-stu-id="97592-115">**DeleteAllProfiles**</span></span>](-wia-iscanprofilemgr-deleteallprofiles.md)                 | <span data-ttu-id="97592-116">Удаляет все профили сканирования, связанные с указанным устройством.</span><span class="sxs-lookup"><span data-stu-id="97592-116">Deletes all the scan profiles associated with the specified device.</span></span><br/>                                         |
| [<span data-ttu-id="97592-117">**делетеаллпрофилесфорусер**</span><span class="sxs-lookup"><span data-stu-id="97592-117">**DeleteAllProfilesForUser**</span></span>](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | <span data-ttu-id="97592-118">Удаляет все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="97592-118">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span> <br/> |
| [<span data-ttu-id="97592-119">**делетепрофиле**</span><span class="sxs-lookup"><span data-stu-id="97592-119">**DeleteProfile**</span></span>](-wia-iscanprofilemgr-deleteprofile.md)                         | <span data-ttu-id="97592-120">Удаляет указанный профиль сканирования.</span><span class="sxs-lookup"><span data-stu-id="97592-120">Deletes the specified scan profile.</span></span><br/>                                                                         |
| [<span data-ttu-id="97592-121">**жетдефаултпрофиле**</span><span class="sxs-lookup"><span data-stu-id="97592-121">**GetDefaultProfile**</span></span>](-wia-iscanprofilemgr-getdefaultprofile.md)                 | <span data-ttu-id="97592-122">Возвращает профиль сканирования по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="97592-122">Gets the default scan profile.</span></span><br/>                                                                              |
| [<span data-ttu-id="97592-123">**жетнумпрофилес**</span><span class="sxs-lookup"><span data-stu-id="97592-123">**GetNumProfiles**</span></span>](-wia-iscanprofilemgr-getnumprofiles.md)                       | <span data-ttu-id="97592-124">Возвращает число профилей сканирования, созданных для пользователя в системе, в которой выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="97592-124">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span><br/> |
| [<span data-ttu-id="97592-125">**жетнумпрофилесфордевицеид**</span><span class="sxs-lookup"><span data-stu-id="97592-125">**GetNumProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | <span data-ttu-id="97592-126">Возвращает число профилей сканирования для устройства.</span><span class="sxs-lookup"><span data-stu-id="97592-126">Gets the number of scan profiles for the device.</span></span><br/>                                                            |
| [<span data-ttu-id="97592-127">**Профили профилирования**</span><span class="sxs-lookup"><span data-stu-id="97592-127">**GetProfiles**</span></span>](-wia-iscanprofilemgr-getprofiles.md)                             | <span data-ttu-id="97592-128">Получает все профили сканирования, доступные для пользователя в системе, в которой выполняется приложение.</span><span class="sxs-lookup"><span data-stu-id="97592-128">Gets all the scan profiles available for the user in the system that your application is running under.</span></span><br/>     |
| [<span data-ttu-id="97592-129">**жетпрофилесфордевицеид**</span><span class="sxs-lookup"><span data-stu-id="97592-129">**GetProfilesforDeviceID**</span></span>](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | <span data-ttu-id="97592-130">Возвращает все профили сканирования, связанные с устройством.</span><span class="sxs-lookup"><span data-stu-id="97592-130">Gets all the scan profiles associated with a device.</span></span><br/>                                                        |
| [<span data-ttu-id="97592-131">**опенпрофиле**</span><span class="sxs-lookup"><span data-stu-id="97592-131">**OpenProfile**</span></span>](-wia-iscanprofilemgr-openprofile.md)                             | <span data-ttu-id="97592-132">Открывает профиль сканирования, сохраненный на диске в виде XML-файла.</span><span class="sxs-lookup"><span data-stu-id="97592-132">Opens a scan profile that has been saved to disk as an XML file.</span></span><br/>                                            |
| [<span data-ttu-id="97592-133">**Обновить**</span><span class="sxs-lookup"><span data-stu-id="97592-133">**Refresh**</span></span>](-wia-iscanprofilemgr-refresh.md)                                     | <span data-ttu-id="97592-134">Повторно перечисляет все профили сканирования в системе.</span><span class="sxs-lookup"><span data-stu-id="97592-134">Re-enumerates all the scan profiles in the system.</span></span><br/>                                                          |
| [<span data-ttu-id="97592-135">**SetDefault**</span><span class="sxs-lookup"><span data-stu-id="97592-135">**SetDefault**</span></span>](-wia-iscanprofilemgr-setdefault.md)                               | <span data-ttu-id="97592-136">Задает указанный профиль сканирования в качестве профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="97592-136">Sets the specified scan profile as the default profile.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="97592-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97592-137">Remarks</span></span>

<span data-ttu-id="97592-138">Чтобы создать объект **исканпрофилемгр** , используйте метод [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) со следующими параметрами:</span><span class="sxs-lookup"><span data-stu-id="97592-138">To create an **IScanProfileMgr** object, use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method with the following parameters:</span></span>

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

<span data-ttu-id="97592-139">Если профиль сканирования сохранен с помощью метода [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) , он сохраняется как XML-файл в% UserProfile% \\ Application Data \\ \\ Center \\ усерсканпрофилес.</span><span class="sxs-lookup"><span data-stu-id="97592-139">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="97592-140">Требования</span><span class="sxs-lookup"><span data-stu-id="97592-140">Requirements</span></span>



| <span data-ttu-id="97592-141">Требование</span><span class="sxs-lookup"><span data-stu-id="97592-141">Requirement</span></span> | <span data-ttu-id="97592-142">Значение</span><span class="sxs-lookup"><span data-stu-id="97592-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="97592-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97592-143">Minimum supported client</span></span><br/> | <span data-ttu-id="97592-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97592-144">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="97592-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97592-145">Minimum supported server</span></span><br/> | <span data-ttu-id="97592-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97592-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97592-147">Header</span><span class="sxs-lookup"><span data-stu-id="97592-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="97592-148"><dt>Сканпрофилемгр. h</dt></span><span class="sxs-lookup"><span data-stu-id="97592-148"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="97592-149">IDL</span><span class="sxs-lookup"><span data-stu-id="97592-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97592-150"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97592-150"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97592-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97592-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97592-152">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="97592-152">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="97592-153">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="97592-153">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
