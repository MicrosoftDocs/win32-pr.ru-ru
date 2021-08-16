---
description: Метод Жетпропбид объекта Item использует идентификатор свойства элемента для возвращения его значения.
ms.assetid: 00f7a91c-fd55-4016-a932-f710045a14b8
title: Item. Жетпропбид, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 5c8d5f68114f74505fce11ca8872370a802e31400159146d7030ec34339c7d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208378"
---
# <a name="itemgetpropbyid-method"></a>Item. Жетпропбид, метод

Метод **жетпропбид** объекта [**Item**](-wia-item.md) использует идентификатор свойства элемента для возвращения его значения.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Item.GetPropById(
  Id
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Идентификатор* \[ в\]
</dt> <dd>

Тип: **[виаитемпропертид](-wia-wiaitempropertyid.md)**

Указывает идентификатор свойства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **Variant**

Этот метод возвращает значение свойства, заданного *идентификатором*.

## <a name="remarks"></a>Remarks

Используйте этот метод, чтобы найти значение свойства элемента по его ИДЕНТИФИКАТОРу. Список идентификаторов свойств см. в разделе [определения констант свойств WIA](-wia-wia-property-constant-definitions.md). Сведения о самих свойствах см. в разделе [константы свойства WIA](-wia-wia-property-constants.md).

для приложений Microsoft Visual Basic добавьте ссылку на "Windows получения образа библиотеки типов 1,01". Следующие константы, определенные в этом файле, допустимы только для корневых элементов (элементов устройств):

``` syntax
const FirmwareVersion = 1026
const ConnectStatus = 1027
const DeviceTime = 1028
const PicturesTaken = 2050
const PicturesRemaining = 2051
const ExposureMode = 2052
const ExposureCompensation = 2053
const ExposureTime = 2054
const FNumber = 2055
const FlashMode = 2056
const FocusMode = 2057
const FocusManualDist = 2058
const ZoomPosition = 2059
const PanPosition = 2060
const TiltPostion = 2061
const TimerMode = 2062
const TimerValue = 2063
const PowerMode = 2064
const BatteryStatus = 2065
const Dimension = 2070
const HorizontalBedSize = 3074
const VerticalBedSize = 3075
const HorizontalSheetFeedSize = 3076
const VerticalSheetFeedSize = 3077
const SheetFeederRegistration = 3078
const HorizontalBedRegistration = 3079
const VerticalBedRegistraion = 3080
const PlatenColor = 3081
const PadColor = 3082
const FilterSelect = 3083
const DitherSelect = 3084
const DitherPatternData = 3085
const DocumentHandlingCapabilities = 3086
const DocumentHandlingStatus = 3087
const DocumentHandlingSelect = 3088
const DocumentHandlingCapacity = 3089
const HorizontalOpticalResolution = 3090
const VerticalOpticalResolution = 3091
const EndorserCharacters = 3092
const EndorserString = 3093
const ScanAheadPages = 3094
const MaxScanTime = 3095
const Pages = 3096
const PageSize = 3097
const PageWidth = 3098
const PageHeight = 3099
const Preview = 3100
const TransparencyAdapter = 3101
const TransparecnyAdapterSelect = 3102
```

## <a name="examples"></a>Примеры

В следующем примере демонстрируется использование метода **жетпропбид** для получения значения свойства.


```JScript
<SCRIPT LANGUAGE="VBScript">
const DeviceType = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
Dim objItem
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    objRootItem=objDeviceInfo.Create()
    objSelectedItems=objRootItem.GetItemsFromUI(0, 0)
    For Each objItem In objSelectedItem
    PropValue = objItem.GetPropById(DeviceType)
    Next
Next
</SCRIPT>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




