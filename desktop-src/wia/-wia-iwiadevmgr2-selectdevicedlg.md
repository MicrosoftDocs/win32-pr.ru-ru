---
description: 'Метод IWiaDevMgr2:: Селектдевицедлг — отображает диалоговое окно, позволяющее пользователю выбрать устройство для получения образа.'
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'Метод IWiaDevMgr2:: Селектдевицедлг (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 60ec24f264b8fe0424f17fc32deaf803e55c3346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091262"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a><span data-ttu-id="4b292-103">Метод IWiaDevMgr2:: Селектдевицедлг</span><span class="sxs-lookup"><span data-stu-id="4b292-103">IWiaDevMgr2::SelectDeviceDlg method</span></span>

<span data-ttu-id="4b292-104">Отображает диалоговое окно, позволяющее пользователю выбрать аппаратное устройство для получения образа.</span><span class="sxs-lookup"><span data-stu-id="4b292-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b292-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b292-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a><span data-ttu-id="4b292-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b292-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b292-107">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b292-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b292-108">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="4b292-108">Type: **HWND**</span></span>

<span data-ttu-id="4b292-109">Указывает родительское окно диалогового окна **Выбор устройства** .</span><span class="sxs-lookup"><span data-stu-id="4b292-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4b292-110">*лдевицетипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b292-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b292-111">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="4b292-111">Type: **LONG**</span></span>

<span data-ttu-id="4b292-112">Указывает тип устройства WIA 2,0 для использования.</span><span class="sxs-lookup"><span data-stu-id="4b292-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="4b292-113">Список возможных значений см. в разделе [описатели типа устройства WIA](-wia-wia-device-type-specifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="4b292-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="4b292-114">*лфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b292-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b292-115">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="4b292-115">Type: **LONG**</span></span>

<span data-ttu-id="4b292-116">Задает поведение диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4b292-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="4b292-117">Значение может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="4b292-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="4b292-118"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="4b292-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="4b292-119">Использовать поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4b292-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="4b292-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ SELECT \_ устройство не \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="4b292-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="4b292-121">Отображает диалоговое окно, несмотря на то, что имеется только одно соответствующее устройство.</span><span class="sxs-lookup"><span data-stu-id="4b292-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4b292-122">*пбстрдевицеид* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4b292-122">*pbstrDeviceID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b292-123">Тип: **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="4b292-123">Type: **BSTR\***</span></span>

<span data-ttu-id="4b292-124">В выходных данных получает строку, которая содержит строку идентификатора устройства.</span><span class="sxs-lookup"><span data-stu-id="4b292-124">On output, receives a string which contains the device's identifier string.</span></span> <span data-ttu-id="4b292-125">В поле входные данные передайте адрес указателя, если эти сведения необходимы, или **значение NULL** , если это не требуется.</span><span class="sxs-lookup"><span data-stu-id="4b292-125">On input, pass the address of a pointer if this information is needed, or **NULL** if it is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="4b292-126">*ппитемрут* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4b292-126">*ppItemRoot* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4b292-127">Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4b292-127">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="4b292-128">Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) корневого элемента иерархического дерева, представляющего выбранное устройство WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="4b292-128">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the hierarchical tree that represents the selected WIA 2.0 device.</span></span> <span data-ttu-id="4b292-129">Если устройство не найдено, оно получает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4b292-129">If no device is found, it receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b292-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b292-130">Return value</span></span>

<span data-ttu-id="4b292-131">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4b292-131">Type: **HRESULT**</span></span>

<span data-ttu-id="4b292-132">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="4b292-132">This method can return one of these values.</span></span>



| <span data-ttu-id="4b292-133">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4b292-133">Return code</span></span>                                                                                                  | <span data-ttu-id="4b292-134">Описание</span><span class="sxs-lookup"><span data-stu-id="4b292-134">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b292-135"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4b292-135"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="4b292-136">Устройство успешно выбрано.</span><span class="sxs-lookup"><span data-stu-id="4b292-136">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="4b292-137"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4b292-137"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="4b292-138">Пользователь отменил это диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4b292-138">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="4b292-139"><dt>**WIA \_ S \_ нет \_ \_ доступных устройств**</dt></span><span class="sxs-lookup"><span data-stu-id="4b292-139"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="4b292-140">Нет аппаратных устройств WIA 2,0, соответствующих спецификациям, указанным в параметре *лдевицетипе* .</span><span class="sxs-lookup"><span data-stu-id="4b292-140">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b292-141">Remarks</span><span class="sxs-lookup"><span data-stu-id="4b292-141">Remarks</span></span>

<span data-ttu-id="4b292-142">Этот метод создает и отображает диалоговое окно **Выбор устройства** , чтобы пользователь мог выбрать устройство WIA 2,0 для получения образа.</span><span class="sxs-lookup"><span data-stu-id="4b292-142">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="4b292-143">Если устройство успешно выбрано, метод **IWiaDevMgr2:: селектдевицедлг** создает иерархическое дерево объектов [**IWiaItem2**](-wia-iwiaitem2.md) для устройства.</span><span class="sxs-lookup"><span data-stu-id="4b292-143">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlg** method creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for the device.</span></span> <span data-ttu-id="4b292-144">Он сохраняет указатель на интерфейс **IWiaItem2** корневого элемента в параметре *ппитемрут*.</span><span class="sxs-lookup"><span data-stu-id="4b292-144">It stores a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span>

<span data-ttu-id="4b292-145">Приложение может ограничить устройства, отображаемые пользователю, определенными типами, указав типы устройств с помощью параметра *лдевицетипе* .</span><span class="sxs-lookup"><span data-stu-id="4b292-145">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="4b292-146">Если спецификация соответствует только одному устройству, **IWiaDevMgr2:: селектдевицедлг** не отображает диалоговое окно " **Выбор устройства** ".</span><span class="sxs-lookup"><span data-stu-id="4b292-146">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlg** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="4b292-147">Вместо этого он создает дерево [**IWiaItem2**](-wia-iwiaitem2.md) для устройства и сохраняет указатель на интерфейс **IWiaItem2** корневого элемента в параметре *ппитемрут*.</span><span class="sxs-lookup"><span data-stu-id="4b292-147">Instead it creates the [**IWiaItem2**](-wia-iwiaitem2.md) tree for the device and store a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span> <span data-ttu-id="4b292-148">Вы можете переопределить это поведение и принудительно вызвать **IWiaDevMgr2:: селектдевицедлг** , чтобы отобразить диалоговое окно, указав WIA \_ SELECT \_ Device не \_ по умолчанию в качестве значения параметра *лфлагс* .</span><span class="sxs-lookup"><span data-stu-id="4b292-148">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlg** to display the dialog box by specifying WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="4b292-149">Если спецификация соответствует более чем одному устройству WIA 2,0, все соответствующие устройства отображаются в диалоговом окне **Выбор устройства** , чтобы пользователь мог выбрать одно из них.</span><span class="sxs-lookup"><span data-stu-id="4b292-149">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the **Select Device** dialog box so the user may choose one.</span></span>

<span data-ttu-id="4b292-150">Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ппитемрут* .</span><span class="sxs-lookup"><span data-stu-id="4b292-150">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppItemRoot* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="4b292-151">Рекомендуется, чтобы приложения были доступны для выбора устройств и изображений с помощью пункта меню **с именем сканер** в меню **файл** .</span><span class="sxs-lookup"><span data-stu-id="4b292-151">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b292-152">Требования</span><span class="sxs-lookup"><span data-stu-id="4b292-152">Requirements</span></span>



| <span data-ttu-id="4b292-153">Требование</span><span class="sxs-lookup"><span data-stu-id="4b292-153">Requirement</span></span> | <span data-ttu-id="4b292-154">Значение</span><span class="sxs-lookup"><span data-stu-id="4b292-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4b292-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b292-155">Minimum supported client</span></span><br/> | <span data-ttu-id="4b292-156">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b292-156">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4b292-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b292-157">Minimum supported server</span></span><br/> | <span data-ttu-id="4b292-158">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b292-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4b292-159">Header</span><span class="sxs-lookup"><span data-stu-id="4b292-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b292-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b292-160"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b292-161">IDL</span><span class="sxs-lookup"><span data-stu-id="4b292-161">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b292-162"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b292-162"><dt>Wia.idl</dt></span></span> </dl> |



 

 
