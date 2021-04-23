---
description: Метод Жетпропбид объекта DeviceInfo использует идентификатор свойства устройства для возвращения его значения.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: DeviceInfo. Жетпропбид, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719517"
---
# <a name="deviceinfogetpropbyid-method"></a><span data-ttu-id="28fbe-103">DeviceInfo. Жетпропбид, метод</span><span class="sxs-lookup"><span data-stu-id="28fbe-103">DeviceInfo.GetPropById method</span></span>

<span data-ttu-id="28fbe-104">Метод **жетпропбид** объекта [**DeviceInfo**](-wia-deviceinfo.md) использует идентификатор свойства устройства для возвращения его значения.</span><span class="sxs-lookup"><span data-stu-id="28fbe-104">The **GetPropById** method of the [**DeviceInfo**](-wia-deviceinfo.md) object uses a device property's ID to return its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="28fbe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28fbe-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="28fbe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28fbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28fbe-107">*Идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="28fbe-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28fbe-108">Тип: **[виадевицеинфопропертид](-wia-wiadeviceinfopropertyid.md)**</span><span class="sxs-lookup"><span data-stu-id="28fbe-108">Type: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span></span>

<span data-ttu-id="28fbe-109">Указывает идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="28fbe-109">Specifies the ID of the property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28fbe-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28fbe-110">Return value</span></span>

<span data-ttu-id="28fbe-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="28fbe-111">Type: **VARIANT**</span></span>

<span data-ttu-id="28fbe-112">Этот метод возвращает значение свойства, заданного *идентификатором*.</span><span class="sxs-lookup"><span data-stu-id="28fbe-112">This method returns the value of the property specified by *Id*.</span></span>

## <a name="remarks"></a><span data-ttu-id="28fbe-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28fbe-113">Remarks</span></span>

<span data-ttu-id="28fbe-114">Используйте этот метод, чтобы найти значение свойства устройства по его ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="28fbe-114">Use this method to find the value of a device property from its ID.</span></span> <span data-ttu-id="28fbe-115">Список идентификаторов свойств см. в разделе [определения констант свойств WIA](-wia-wia-property-constant-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="28fbe-115">For a list of property IDs, see [WIA Property Constant Definitions](-wia-wia-property-constant-definitions.md).</span></span> <span data-ttu-id="28fbe-116">Сведения о свойствах получения образа Windows (WIA) см. в разделе [константы свойства WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="28fbe-116">For information about Windows Image Acquisition (WIA) properties themselves, see [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

<span data-ttu-id="28fbe-117">Для приложений Microsoft Visual Basic добавьте ссылку на "Библиотека типов приобретения образа Windows 1,01".</span><span class="sxs-lookup"><span data-stu-id="28fbe-117">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span> <span data-ttu-id="28fbe-118">Следующие константы, определенные в этом файле, допустимы для этого метода:</span><span class="sxs-lookup"><span data-stu-id="28fbe-118">This following constants defined in that file are valid for this method:</span></span>

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a><span data-ttu-id="28fbe-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="28fbe-119">Examples</span></span>

<span data-ttu-id="28fbe-120">В следующем примере демонстрируется использование метода **жетпропбид** для получения значения свойства.</span><span class="sxs-lookup"><span data-stu-id="28fbe-120">The following example demonstrates the use of the **GetPropById** method to retrieve a property value.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="28fbe-121">Требования</span><span class="sxs-lookup"><span data-stu-id="28fbe-121">Requirements</span></span>



| <span data-ttu-id="28fbe-122">Требование</span><span class="sxs-lookup"><span data-stu-id="28fbe-122">Requirement</span></span> | <span data-ttu-id="28fbe-123">Значение</span><span class="sxs-lookup"><span data-stu-id="28fbe-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28fbe-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28fbe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="28fbe-125">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="28fbe-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="28fbe-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28fbe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="28fbe-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="28fbe-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="28fbe-128">DLL</span><span class="sxs-lookup"><span data-stu-id="28fbe-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28fbe-129"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="28fbe-129"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




