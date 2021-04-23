---
description: Отображает диалоговое окно, позволяющее пользователю выбрать аппаратное устройство для получения образа.
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'Метод IWiaDevMgr2:: Селектдевицедлгид (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bad749eb48e72b362070ea4951d4e9eac380e737
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701683"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a><span data-ttu-id="a6ddc-103">Метод IWiaDevMgr2:: Селектдевицедлгид</span><span class="sxs-lookup"><span data-stu-id="a6ddc-103">IWiaDevMgr2::SelectDeviceDlgID method</span></span>

<span data-ttu-id="a6ddc-104">Отображает диалоговое окно, позволяющее пользователю выбрать аппаратное устройство для получения образа.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ddc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6ddc-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="a6ddc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6ddc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ddc-107">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a6ddc-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ddc-108">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="a6ddc-108">Type: **HWND**</span></span>

<span data-ttu-id="a6ddc-109">Указывает родительское окно диалогового окна **Выбор устройства** .</span><span class="sxs-lookup"><span data-stu-id="a6ddc-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="a6ddc-110">*лдевицетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a6ddc-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ddc-111">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="a6ddc-111">Type: **LONG**</span></span>

<span data-ttu-id="a6ddc-112">Указывает тип устройства WIA 2,0 для использования.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="a6ddc-113">Список возможных значений см. в разделе [описатели типа устройства WIA](-wia-wia-device-type-specifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="a6ddc-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="a6ddc-114">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a6ddc-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ddc-115">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="a6ddc-115">Type: **LONG**</span></span>

<span data-ttu-id="a6ddc-116">Задает поведение диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="a6ddc-117">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a6ddc-118"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="a6ddc-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a6ddc-119">Использовать поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="a6ddc-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ устройство не \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="a6ddc-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="a6ddc-121">Отображает диалоговое окно, несмотря на то, что имеется только одно соответствующее устройство.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a6ddc-122">*пбстрдевицеид* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a6ddc-122">*pbstrDeviceID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ddc-123">Тип: \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="a6ddc-123">Type: \**BSTR\** _</span></span>

<span data-ttu-id="a6ddc-124">Указатель на строку, которая получает строку идентификатора устройства.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-124">Pointer to a string that receives the identifier string of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6ddc-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6ddc-125">Return value</span></span>

<span data-ttu-id="a6ddc-126">Тип: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a6ddc-126">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a6ddc-127">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-127">This method can return one of these values.</span></span>



| <span data-ttu-id="a6ddc-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a6ddc-128">Return code</span></span>                                                                                                  | <span data-ttu-id="a6ddc-129">Описание</span><span class="sxs-lookup"><span data-stu-id="a6ddc-129">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6ddc-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ddc-130"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="a6ddc-131">Устройство успешно выбрано.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-131">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="a6ddc-132"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ddc-132"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="a6ddc-133">Пользователь отменил это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-133">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="a6ddc-134"><dt>**WIA \_ S \_ нет \_ \_ доступных устройств**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ddc-134"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="a6ddc-135">Нет аппаратных устройств WIA 2,0, соответствующих спецификациям, указанным в параметре *лдевицетипе* .</span><span class="sxs-lookup"><span data-stu-id="a6ddc-135">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6ddc-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6ddc-136">Remarks</span></span>

<span data-ttu-id="a6ddc-137">Этот метод создает и отображает диалоговое окно **Выбор устройства** , чтобы пользователь мог выбрать устройство WIA 2,0 для получения образа.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-137">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="a6ddc-138">Если устройство успешно выбрано, метод **IWiaDevMgr2:: селектдевицедлгид** передает свою строку идентификатора приложению через его параметр *пбстрдевицеид* .</span><span class="sxs-lookup"><span data-stu-id="a6ddc-138">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlgID** method passes its identifier string to the application through its *pbstrDeviceID* parameter.</span></span>

<span data-ttu-id="a6ddc-139">Приложение может ограничить устройства, отображаемые пользователю, определенными типами, указав типы устройств с помощью параметра *лдевицетипе* .</span><span class="sxs-lookup"><span data-stu-id="a6ddc-139">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="a6ddc-140">Если спецификация соответствует только одному устройству, **IWiaDevMgr2:: селектдевицедлгид** не отображает диалоговое окно " **Выбор устройства** ".</span><span class="sxs-lookup"><span data-stu-id="a6ddc-140">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlgID** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="a6ddc-141">Вместо этого он передает в приложение строку идентификатора устройства без отображения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-141">Instead it passes the device's identifier string to the application without displaying the dialog box.</span></span> <span data-ttu-id="a6ddc-142">Вы можете переопределить это поведение и принудительно вызвать **IWiaDevMgr2:: селектдевицедлгид** , чтобы отобразить диалоговое окно, передав WIA \_ SELECT \_ Device не Default в \_ качестве значения параметра *лфлагс* .</span><span class="sxs-lookup"><span data-stu-id="a6ddc-142">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlgID** to display the dialog box by passing WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="a6ddc-143">Если спецификация соответствует более чем одному устройству WIA 2,0, все соответствующие устройства отображаются в диалоговом окне Селектдевице, чтобы пользователь мог выбрать одно из них.</span><span class="sxs-lookup"><span data-stu-id="a6ddc-143">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the SelectDevice dialog box so the user may choose one.</span></span>

> [!Note]  
> <span data-ttu-id="a6ddc-144">Рекомендуется, чтобы приложения были доступны для выбора устройств и изображений с помощью пункта меню **с именем сканер** в меню **файл** .</span><span class="sxs-lookup"><span data-stu-id="a6ddc-144">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a6ddc-145">Требования</span><span class="sxs-lookup"><span data-stu-id="a6ddc-145">Requirements</span></span>



| <span data-ttu-id="a6ddc-146">Требование</span><span class="sxs-lookup"><span data-stu-id="a6ddc-146">Requirement</span></span> | <span data-ttu-id="a6ddc-147">Значение</span><span class="sxs-lookup"><span data-stu-id="a6ddc-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ddc-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6ddc-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ddc-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6ddc-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a6ddc-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6ddc-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ddc-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6ddc-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a6ddc-152">Header</span><span class="sxs-lookup"><span data-stu-id="a6ddc-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ddc-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6ddc-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6ddc-154">IDL</span><span class="sxs-lookup"><span data-stu-id="a6ddc-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6ddc-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6ddc-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 




