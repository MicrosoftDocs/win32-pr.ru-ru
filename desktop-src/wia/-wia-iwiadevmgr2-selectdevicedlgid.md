---
description: 'Метод IWiaDevMgr2:: Селектдевицедлгид — отображает диалоговое окно, позволяющее пользователю выбрать устройство для получения образа.'
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
ms.openlocfilehash: a4279bef86d761ed0eb7d90ad3b8dee46e0f17f4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106822"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a><span data-ttu-id="01d20-103">Метод IWiaDevMgr2:: Селектдевицедлгид</span><span class="sxs-lookup"><span data-stu-id="01d20-103">IWiaDevMgr2::SelectDeviceDlgID method</span></span>

<span data-ttu-id="01d20-104">Отображает диалоговое окно, позволяющее пользователю выбрать аппаратное устройство для получения образа.</span><span class="sxs-lookup"><span data-stu-id="01d20-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d20-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01d20-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="01d20-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01d20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01d20-107">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01d20-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d20-108">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="01d20-108">Type: **HWND**</span></span>

<span data-ttu-id="01d20-109">Указывает родительское окно диалогового окна **Выбор устройства** .</span><span class="sxs-lookup"><span data-stu-id="01d20-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="01d20-110">*лдевицетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01d20-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d20-111">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="01d20-111">Type: **LONG**</span></span>

<span data-ttu-id="01d20-112">Указывает тип устройства WIA 2,0 для использования.</span><span class="sxs-lookup"><span data-stu-id="01d20-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="01d20-113">Список возможных значений см. в разделе [описатели типа устройства WIA](-wia-wia-device-type-specifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="01d20-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="01d20-114">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01d20-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01d20-115">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="01d20-115">Type: **LONG**</span></span>

<span data-ttu-id="01d20-116">Задает поведение диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="01d20-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="01d20-117">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="01d20-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="01d20-118"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="01d20-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="01d20-119">Использовать поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="01d20-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="01d20-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ устройство не \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="01d20-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="01d20-121">Отображает диалоговое окно, несмотря на то, что имеется только одно соответствующее устройство.</span><span class="sxs-lookup"><span data-stu-id="01d20-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="01d20-122">*пбстрдевицеид* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="01d20-122">*pbstrDeviceID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="01d20-123">Тип: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="01d20-123">Type: **BSTR\***</span></span>

<span data-ttu-id="01d20-124">Указатель на строку, которая получает строку идентификатора устройства.</span><span class="sxs-lookup"><span data-stu-id="01d20-124">Pointer to a string that receives the identifier string of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01d20-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01d20-125">Return value</span></span>

<span data-ttu-id="01d20-126">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="01d20-126">Type: **HRESULT**</span></span>

<span data-ttu-id="01d20-127">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="01d20-127">This method can return one of these values.</span></span>



| <span data-ttu-id="01d20-128">Код возврата</span><span class="sxs-lookup"><span data-stu-id="01d20-128">Return code</span></span>                                                                                                  | <span data-ttu-id="01d20-129">Описание</span><span class="sxs-lookup"><span data-stu-id="01d20-129">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="01d20-130"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="01d20-130"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="01d20-131">Устройство успешно выбрано.</span><span class="sxs-lookup"><span data-stu-id="01d20-131">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="01d20-132"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="01d20-132"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="01d20-133">Пользователь отменил это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="01d20-133">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="01d20-134"><dt>**WIA \_ S \_ нет \_ \_ доступных устройств**</dt></span><span class="sxs-lookup"><span data-stu-id="01d20-134"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="01d20-135">Нет аппаратных устройств WIA 2,0, соответствующих спецификациям, указанным в параметре *лдевицетипе* .</span><span class="sxs-lookup"><span data-stu-id="01d20-135">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="01d20-136">Remarks</span><span class="sxs-lookup"><span data-stu-id="01d20-136">Remarks</span></span>

<span data-ttu-id="01d20-137">Этот метод создает и отображает диалоговое окно **Выбор устройства** , чтобы пользователь мог выбрать устройство WIA 2,0 для получения образа.</span><span class="sxs-lookup"><span data-stu-id="01d20-137">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="01d20-138">Если устройство успешно выбрано, метод **IWiaDevMgr2:: селектдевицедлгид** передает свою строку идентификатора приложению через его параметр *пбстрдевицеид* .</span><span class="sxs-lookup"><span data-stu-id="01d20-138">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlgID** method passes its identifier string to the application through its *pbstrDeviceID* parameter.</span></span>

<span data-ttu-id="01d20-139">Приложение может ограничить устройства, отображаемые пользователю, определенными типами, указав типы устройств с помощью параметра *лдевицетипе* .</span><span class="sxs-lookup"><span data-stu-id="01d20-139">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="01d20-140">Если спецификация соответствует только одному устройству, **IWiaDevMgr2:: селектдевицедлгид** не отображает диалоговое окно " **Выбор устройства** ".</span><span class="sxs-lookup"><span data-stu-id="01d20-140">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlgID** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="01d20-141">Вместо этого он передает в приложение строку идентификатора устройства без отображения диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="01d20-141">Instead it passes the device's identifier string to the application without displaying the dialog box.</span></span> <span data-ttu-id="01d20-142">Вы можете переопределить это поведение и принудительно вызвать **IWiaDevMgr2:: селектдевицедлгид** , чтобы отобразить диалоговое окно, передав WIA \_ SELECT \_ Device не Default в \_ качестве значения параметра *лфлагс* .</span><span class="sxs-lookup"><span data-stu-id="01d20-142">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlgID** to display the dialog box by passing WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="01d20-143">Если спецификация соответствует более чем одному устройству WIA 2,0, все соответствующие устройства отображаются в диалоговом окне Селектдевице, чтобы пользователь мог выбрать одно из них.</span><span class="sxs-lookup"><span data-stu-id="01d20-143">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the SelectDevice dialog box so the user may choose one.</span></span>

> [!Note]  
> <span data-ttu-id="01d20-144">Рекомендуется, чтобы приложения были доступны для выбора устройств и изображений с помощью пункта меню **с именем сканер** в меню **файл** .</span><span class="sxs-lookup"><span data-stu-id="01d20-144">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="01d20-145">Требования</span><span class="sxs-lookup"><span data-stu-id="01d20-145">Requirements</span></span>



| <span data-ttu-id="01d20-146">Требование</span><span class="sxs-lookup"><span data-stu-id="01d20-146">Requirement</span></span> | <span data-ttu-id="01d20-147">Значение</span><span class="sxs-lookup"><span data-stu-id="01d20-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01d20-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="01d20-148">Minimum supported client</span></span><br/> | <span data-ttu-id="01d20-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="01d20-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="01d20-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="01d20-150">Minimum supported server</span></span><br/> | <span data-ttu-id="01d20-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="01d20-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="01d20-152">Header</span><span class="sxs-lookup"><span data-stu-id="01d20-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="01d20-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="01d20-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="01d20-154">IDL</span><span class="sxs-lookup"><span data-stu-id="01d20-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01d20-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01d20-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 




