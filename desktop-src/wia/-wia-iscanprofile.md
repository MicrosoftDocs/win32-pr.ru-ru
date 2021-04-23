---
description: Интерфейс Исканпрофиле представляет один профиль сканирования и позволяет приложениям устанавливать и получать свойства профиля.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Интерфейс Исканпрофиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702226"
---
# <a name="iscanprofile-interface"></a><span data-ttu-id="eea2b-103">Интерфейс Исканпрофиле</span><span class="sxs-lookup"><span data-stu-id="eea2b-103">IScanProfile interface</span></span>

<span data-ttu-id="eea2b-104">Интерфейс **исканпрофиле** представляет один профиль сканирования и позволяет приложениям устанавливать и получать свойства профиля.</span><span class="sxs-lookup"><span data-stu-id="eea2b-104">The **IScanProfile** interface represents a single scan profile and enables applications to set and get the properties of the profile.</span></span>

## <a name="members"></a><span data-ttu-id="eea2b-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="eea2b-105">Members</span></span>

<span data-ttu-id="eea2b-106">Интерфейс **исканпрофиле** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="eea2b-106">The **IScanProfile** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="eea2b-107">**Исканпрофиле** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="eea2b-107">**IScanProfile** also has these types of members:</span></span>

-   [<span data-ttu-id="eea2b-108">Методы</span><span class="sxs-lookup"><span data-stu-id="eea2b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eea2b-109">Методы</span><span class="sxs-lookup"><span data-stu-id="eea2b-109">Methods</span></span>

<span data-ttu-id="eea2b-110">Интерфейс **исканпрофиле** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="eea2b-110">The **IScanProfile** interface has these methods.</span></span>



| <span data-ttu-id="eea2b-111">Метод</span><span class="sxs-lookup"><span data-stu-id="eea2b-111">Method</span></span>                                                     | <span data-ttu-id="eea2b-112">Описание</span><span class="sxs-lookup"><span data-stu-id="eea2b-112">Description</span></span>                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eea2b-113">**жеталлпропидс**</span><span class="sxs-lookup"><span data-stu-id="eea2b-113">**GetAllPropIDs**</span></span>](-wia-iscanprofile-getallpropids.md)   | <span data-ttu-id="eea2b-114">Возвращает все доступные идентификаторы свойств в профиле.</span><span class="sxs-lookup"><span data-stu-id="eea2b-114">Gets all available property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eea2b-115">**GetDeviceID**</span><span class="sxs-lookup"><span data-stu-id="eea2b-115">**GetDeviceID**</span></span>](-wia-iscanprofile-getdeviceid.md)       | <span data-ttu-id="eea2b-116">Возвращает идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="eea2b-116">Returns the ID of the device.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="eea2b-117">**GetGUID**</span><span class="sxs-lookup"><span data-stu-id="eea2b-117">**GetGUID**</span></span>](-wia-iscanprofile-getguid.md)               | <span data-ttu-id="eea2b-118">Возвращает идентификатор GUID профиля.</span><span class="sxs-lookup"><span data-stu-id="eea2b-118">Returns the GUID of the profile.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="eea2b-119">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="eea2b-119">**GetItem**</span></span>](-wia-iscanprofile-getitem.md)               | <span data-ttu-id="eea2b-120">Возвращает идентификатор GUID категории элемента WIA 2,0, с которым связан профиль.</span><span class="sxs-lookup"><span data-stu-id="eea2b-120">Gets the GUID of the category of the WIA 2.0 item that the profile is associated with.</span></span><br/>                                                   |
| [<span data-ttu-id="eea2b-121">**GetName**</span><span class="sxs-lookup"><span data-stu-id="eea2b-121">**GetName**</span></span>](-wia-iscanprofile-getname.md)               | <span data-ttu-id="eea2b-122">Возвращает понятное имя профиля.</span><span class="sxs-lookup"><span data-stu-id="eea2b-122">Gets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="eea2b-123">**жетнумпропидс**</span><span class="sxs-lookup"><span data-stu-id="eea2b-123">**GetNumPropIDS**</span></span>](-wia-iscanprofile-getnumpropids.md)   | <span data-ttu-id="eea2b-124">Возвращает число идентификаторов свойств в профиле.</span><span class="sxs-lookup"><span data-stu-id="eea2b-124">Gets the number of property IDs in a profile.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eea2b-125">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="eea2b-125">**GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)       | <span data-ttu-id="eea2b-126">Возвращает значение указанных дочерних свойств в `<Properties>` элементе профиля сканирования.</span><span class="sxs-lookup"><span data-stu-id="eea2b-126">Gets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="eea2b-127">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="eea2b-127">**IsDefault**</span></span>](-wia-iscanprofile-isdefault.md)           | <span data-ttu-id="eea2b-128">Возвращает значение, указывающее, является ли профиль профилем сканирования по умолчанию для связанного устройства [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="eea2b-128">Gets a value that indicates whether the profile is the default scan profile of an associated [**IWiaItem2**](-wia-iwiaitem2.md) device.</span></span><br/> |
| [<span data-ttu-id="eea2b-129">**RemoveProperty**</span><span class="sxs-lookup"><span data-stu-id="eea2b-129">**RemoveProperty**</span></span>](-wia-iscanprofile-removeproperty.md) | <span data-ttu-id="eea2b-130">Удаляет указанный список дочерних свойств `<Properties>` элемента профиля сканирования.</span><span class="sxs-lookup"><span data-stu-id="eea2b-130">Removes a specified list of child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |
| [<span data-ttu-id="eea2b-131">**Сохранить**</span><span class="sxs-lookup"><span data-stu-id="eea2b-131">**Save**</span></span>](-wia-iscanprofile-save.md)                     | <span data-ttu-id="eea2b-132">Сохраняет изменения профиля на диск.</span><span class="sxs-lookup"><span data-stu-id="eea2b-132">Saves changes to a profile to disk.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="eea2b-133">**сетитем**</span><span class="sxs-lookup"><span data-stu-id="eea2b-133">**SetItem**</span></span>](-wia-iscanprofile-setitem.md)               | <span data-ttu-id="eea2b-134">Задает идентификатор GUID категории элемента WIA 2,0, с которым связан профиль.</span><span class="sxs-lookup"><span data-stu-id="eea2b-134">Sets the GUID of the category of WIA 2.0 item that the profile is associated with.</span></span><br/>                                                       |
| [<span data-ttu-id="eea2b-135">**SetName**</span><span class="sxs-lookup"><span data-stu-id="eea2b-135">**SetName**</span></span>](-wia-iscanprofile-setname.md)               | <span data-ttu-id="eea2b-136">Задает понятное имя профиля.</span><span class="sxs-lookup"><span data-stu-id="eea2b-136">Sets the friendly name of the profile.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="eea2b-137">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="eea2b-137">**SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)       | <span data-ttu-id="eea2b-138">Задает значение указанных дочерних свойств в `<Properties>` элементе профиля сканирования.</span><span class="sxs-lookup"><span data-stu-id="eea2b-138">Sets the value of specified child properties in the `<Properties>` element of a scan profile.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="eea2b-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eea2b-139">Remarks</span></span>

<span data-ttu-id="eea2b-140">У любого устройства [**IWiaItem2**](-wia-iwiaitem2.md) может быть профиль сканирования.</span><span class="sxs-lookup"><span data-stu-id="eea2b-140">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="eea2b-141">Однако **IWiaItem2** элементы типов \_ Категория WIA \_ Finished \_ File и WIA \_ Category \_ не могут иметь профили.</span><span class="sxs-lookup"><span data-stu-id="eea2b-141">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="eea2b-142">Если профиль сканирования сохранен с помощью метода [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) , он сохраняется как XML-файл в% UserProfile% \\ Application Data \\ \\ Center \\ усерсканпрофилес.</span><span class="sxs-lookup"><span data-stu-id="eea2b-142">If a scan profile is saved using the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method, it is stored as an XML file at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="eea2b-143">Чтобы создать экземпляр объекта **исканпрофиле** , используйте метод [**Исканпрофилемгр:: креатепрофиле**](-wia-iscanprofilemgr-createprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="eea2b-143">To create an instance of an **IScanProfile** object, use the [**IScanProfileMgr::CreateProfile**](-wia-iscanprofilemgr-createprofile.md) method.</span></span> <span data-ttu-id="eea2b-144">Чтобы получить ссылку на профиль сканирования, который уже был сохранен на диске, используйте метод [**исканпрофилемгр:: опенпрофиле**](-wia-iscanprofilemgr-openprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="eea2b-144">To get a reference to a scan profile that has already been saved to disk, use the [**IScanProfileMgr::OpenProfile**](-wia-iscanprofilemgr-openprofile.md) method.</span></span>

<span data-ttu-id="eea2b-145">Все профили сканирования имеют следующие элементы: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , и `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="eea2b-145">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="eea2b-146">Профиль по умолчанию для устройства также имеет `<Default>` элемент.</span><span class="sxs-lookup"><span data-stu-id="eea2b-146">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="eea2b-147">`<ProfileGUID>`Элементы и `<DeviceID>` не могут быть изменены после создания профиля.</span><span class="sxs-lookup"><span data-stu-id="eea2b-147">The `<ProfileGUID>` and `<DeviceID>` elements cannot be changed after the profile is created.</span></span> <span data-ttu-id="eea2b-148">Значения `<ProfileName>` элемента и `<WiaItem>` элемента можно изменить после создания профиля.</span><span class="sxs-lookup"><span data-stu-id="eea2b-148">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed after the profile is created.</span></span> <span data-ttu-id="eea2b-149">`<Default>`Элемент можно добавить или удалить.</span><span class="sxs-lookup"><span data-stu-id="eea2b-149">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="eea2b-150">Это можно сделать программно с помощью методов [**исканпрофиле:: SetName**](-wia-iscanprofile-setname.md), [**Исканпрофиле:: сетитем**](-wia-iscanprofile-setitem.md)и [**исканпрофилемгр:: сетдефаулт**](-wia-iscanprofilemgr-setdefault.md) .</span><span class="sxs-lookup"><span data-stu-id="eea2b-150">This can be done programatically with the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="eea2b-151">Эти свойства также могут быть изменены пользователями с помощью метода [**исканпрофилеуи:: сканпрофиледиалог**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="eea2b-151">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="eea2b-152">`<Properties>`Элемент содержит `<Property>` дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="eea2b-152">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="eea2b-153">Используйте их, чтобы добавить в профиль любое свойство элемента WIA 2,0 или устройства.</span><span class="sxs-lookup"><span data-stu-id="eea2b-153">Use these to add any WIA 2.0 item or device property to the profile.</span></span> <span data-ttu-id="eea2b-154">Вы также можете разработать собственные `<Property>` дочерние элементы приобретения Image.</span><span class="sxs-lookup"><span data-stu-id="eea2b-154">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="eea2b-155">Это делает схему профиля сканирования расширяемой.</span><span class="sxs-lookup"><span data-stu-id="eea2b-155">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="eea2b-156">(Дополнительные сведения о расширении схемы см. в разделе [Определение пользовательских свойств](-wia-defining-custom-properties.md), [**исканпрофиле::-Property**](-wia-iscanprofile-getproperty.md)и [**исканпрофиле:: SetProperty**](-wia-iscanprofile-setproperty.md).)</span><span class="sxs-lookup"><span data-stu-id="eea2b-156">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="eea2b-157">Требования</span><span class="sxs-lookup"><span data-stu-id="eea2b-157">Requirements</span></span>



| <span data-ttu-id="eea2b-158">Требование</span><span class="sxs-lookup"><span data-stu-id="eea2b-158">Requirement</span></span> | <span data-ttu-id="eea2b-159">Значение</span><span class="sxs-lookup"><span data-stu-id="eea2b-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eea2b-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eea2b-160">Minimum supported client</span></span><br/> | <span data-ttu-id="eea2b-161">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eea2b-161">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="eea2b-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eea2b-162">Minimum supported server</span></span><br/> | <span data-ttu-id="eea2b-163">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eea2b-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eea2b-164">IDL</span><span class="sxs-lookup"><span data-stu-id="eea2b-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eea2b-165"><dt>Сканпрофилес. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eea2b-165"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eea2b-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eea2b-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea2b-167">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="eea2b-167">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="eea2b-168">Схема профиля сканирования</span><span class="sxs-lookup"><span data-stu-id="eea2b-168">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
