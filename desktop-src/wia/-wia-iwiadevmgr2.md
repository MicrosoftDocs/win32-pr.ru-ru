---
description: Интерфейс IWiaDevMgr2 используется для создания устройств получения изображений и управления ими, а также для регистрации событий устройств.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: Интерфейс IWiaDevMgr2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909864"
---
# <a name="iwiadevmgr2-interface"></a><span data-ttu-id="dd9a9-103">Интерфейс IWiaDevMgr2</span><span class="sxs-lookup"><span data-stu-id="dd9a9-103">IWiaDevMgr2 interface</span></span>

<span data-ttu-id="dd9a9-104">Интерфейс **IWiaDevMgr2** используется для создания устройств получения изображений и управления ими, а также для регистрации событий устройств.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-104">The **IWiaDevMgr2** interface is used to create and manage image acquisition devices and to register to receive device events.</span></span>

## <a name="members"></a><span data-ttu-id="dd9a9-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="dd9a9-105">Members</span></span>

<span data-ttu-id="dd9a9-106">Интерфейс **IWiaDevMgr2** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dd9a9-106">The **IWiaDevMgr2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dd9a9-107">**IWiaDevMgr2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dd9a9-107">**IWiaDevMgr2** also has these types of members:</span></span>

-   [<span data-ttu-id="dd9a9-108">Методы</span><span class="sxs-lookup"><span data-stu-id="dd9a9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dd9a9-109">Методы</span><span class="sxs-lookup"><span data-stu-id="dd9a9-109">Methods</span></span>

<span data-ttu-id="dd9a9-110">Интерфейс **IWiaDevMgr2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-110">The **IWiaDevMgr2** interface has these methods.</span></span>



| <span data-ttu-id="dd9a9-111">Метод</span><span class="sxs-lookup"><span data-stu-id="dd9a9-111">Method</span></span>                                                                                    | <span data-ttu-id="dd9a9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="dd9a9-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd9a9-113">**креатедевице**</span><span class="sxs-lookup"><span data-stu-id="dd9a9-113">**CreateDevice**</span></span>](-wia-iwiadevmgr2-createdevice.md)                                     | <span data-ttu-id="dd9a9-114">Создает иерархическое дерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) для устройства WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-114">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="dd9a9-115">**енумдевицеинфо**</span><span class="sxs-lookup"><span data-stu-id="dd9a9-115">**EnumDeviceInfo**</span></span>](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | <span data-ttu-id="dd9a9-116">Создает перечислитель сведений о свойстве для каждого доступного устройства WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-116">Creates an enumerator of property information for each available WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="dd9a9-117">**жетимажедлг**</span><span class="sxs-lookup"><span data-stu-id="dd9a9-117">**GetImageDlg**</span></span>](-wia-iwiadevmgr2-getimagedlg.md)                                       | <span data-ttu-id="dd9a9-118">Метод [**IWiaDevMgr2:: жетимажедлг**](-wia-iwiadevmgr2-getimagedlg.md) отображает одно или несколько диалоговых окон, которые позволяют пользователю получить изображение с устройства WIA 2,0 и записать образ в указанный файл.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-118">The [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method displays one or more dialog boxes that enable a user to acquire an image from a WIA 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="dd9a9-119">Этот метод расширяет функциональные возможности [**IWiaDevMgr2:: селектдевицедлг**](-wia-iwiadevmgr2-selectdevicedlg.md) для инкапсуляции получения образа в рамках одного вызова API.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-119">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span> <br/> |
| [<span data-ttu-id="dd9a9-120">**регистеревенткаллбаккклсид**</span><span class="sxs-lookup"><span data-stu-id="dd9a9-120">**RegisterEventCallbackCLSID**</span></span>](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | <span data-ttu-id="dd9a9-121">Метод [**IWiaDevMgr2:: регистеревенткаллбаккклсид**](-wia-iwiadevmgr2-registereventcallbackclsid.md) регистрирует приложение для получения событий, даже если приложение не работает.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-121">The [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) method registers an application to receive events even if the application is not running.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="dd9a9-122">**регистеревенткаллбаккинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="dd9a9-122">**RegisterEventCallbackInterface**</span></span>](-wia-iwiadevmgr2-registereventcallbackinterface.md) | <span data-ttu-id="dd9a9-123">Регистрирует выполняющееся приложение для уведомления о событии WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-123">Registers a running application for WIA 2.0 event notification.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="dd9a9-124">**регистеревенткаллбаккпрограм**</span><span class="sxs-lookup"><span data-stu-id="dd9a9-124">**RegisterEventCallbackProgram**</span></span>](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | <span data-ttu-id="dd9a9-125">Метод [**IWiaDevMgr2:: регистеревенткаллбаккпрограм**](-wia-iwiadevmgr2-registereventcallbackprogram.md) регистрирует приложение для получения событий устройства.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-125">The [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method registers an application to receive device events.</span></span> <span data-ttu-id="dd9a9-126">В основном он предоставляется для обеспечения обратной совместимости с приложениями, которые не были написаны для WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-126">It is primarily provided for backward compatibility with applications that were not written for WIA 2.0.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="dd9a9-127">**селектдевицедлг**</span><span class="sxs-lookup"><span data-stu-id="dd9a9-127">**SelectDeviceDlg**</span></span>](-wia-iwiadevmgr2-selectdevicedlg.md)                               | <span data-ttu-id="dd9a9-128">Отображает диалоговое окно, позволяющее пользователю выбрать аппаратное устройство для получения образа.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-128">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="dd9a9-129">**селектдевицедлгид**</span><span class="sxs-lookup"><span data-stu-id="dd9a9-129">**SelectDeviceDlgID**</span></span>](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | <span data-ttu-id="dd9a9-130">Отображает диалоговое окно, позволяющее пользователю выбрать аппаратное устройство для получения образа.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-130">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="dd9a9-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd9a9-131">Remarks</span></span>

<span data-ttu-id="dd9a9-132">Интерфейс **IWiaDevMgr2** , как и все интерфейсы модели компонентных объектов (com), наследует методы интерфейса [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dd9a9-132">The **IWiaDevMgr2** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="dd9a9-133">Методы IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd9a9-133">IUnknown Methods</span></span>                                        | <span data-ttu-id="dd9a9-134">Описание</span><span class="sxs-lookup"><span data-stu-id="dd9a9-134">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="dd9a9-135">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="dd9a9-135">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="dd9a9-136">Возвращает указатели на поддерживаемые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-136">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="dd9a9-137">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="dd9a9-137">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="dd9a9-138">Увеличивает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-138">Increments reference count.</span></span>               |
| [<span data-ttu-id="dd9a9-139">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="dd9a9-139">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="dd9a9-140">Уменьшает значение счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-140">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="dd9a9-141">Требования</span><span class="sxs-lookup"><span data-stu-id="dd9a9-141">Requirements</span></span>



| <span data-ttu-id="dd9a9-142">Требование</span><span class="sxs-lookup"><span data-stu-id="dd9a9-142">Requirement</span></span> | <span data-ttu-id="dd9a9-143">Значение</span><span class="sxs-lookup"><span data-stu-id="dd9a9-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd9a9-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd9a9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="dd9a9-145">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd9a9-145">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dd9a9-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd9a9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="dd9a9-147">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dd9a9-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dd9a9-148">Header</span><span class="sxs-lookup"><span data-stu-id="dd9a9-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd9a9-149"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd9a9-149"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd9a9-150">IDL</span><span class="sxs-lookup"><span data-stu-id="dd9a9-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd9a9-151"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd9a9-151"><dt>Wia.idl</dt></span></span> </dl> |



 

 
