---
description: Представляет один заголовок \_ объекта CIM дисплайконтроллер.
ms.assetid: 2bb034d9-d1df-4cc8-a6a8-b6ad7289f582
title: Класс CIM_VideoHead
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHead
- CIM_VideoHead.CurrentBitsPerPixel
- CIM_VideoHead.CurrentHorizontalResolution
- CIM_VideoHead.CurrentVerticalResolution
- CIM_VideoHead.MaxRefreshRate
- CIM_VideoHead.MinRefreshRate
- CIM_VideoHead.CurrentRefreshRate
- CIM_VideoHead.CurrentScanMode
- CIM_VideoHead.OtherCurrentScanMode
- CIM_VideoHead.CurrentNumberOfRows
- CIM_VideoHead.CurrentNumberOfColumns
- CIM_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9576f3b1e9e1c6279067e7ddc8878fdb33ef62e2aea917937d50358069ef38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427674"
---
# <a name="cim_videohead-class"></a>\_Класс CIM видеохеад

Представляет один заголовок объекта [**CIM \_ дисплайконтроллер**](cim-displaycontroller.md) .

## <a name="syntax"></a>Синтаксис

``` syntax
[Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHead : CIM_LogicalDevice
{
  uint32 CurrentBitsPerPixel;
  uint32 CurrentHorizontalResolution;
  uint32 CurrentVerticalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 CurrentRefreshRate;
  uint16 CurrentScanMode;
  string OtherCurrentScanMode;
  uint32 CurrentNumberOfRows;
  uint32 CurrentNumberOfColumns;
  uint64 CurrentNumberOfColors;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ видеохеад** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ видеохеад** имеет следующие свойства.

<dl> <dt>

**куррентбитсперпиксел**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BITS"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,12 "), **Пунит** (" бит ")
</dt> </dl>

Число битов, используемых для вывода каждого пикселя.

</dd> <dt>

**курренсоризонталресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,11 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ видеохеадресолутион. хоризонталресолутион "), **Пунит** (" пиксель ")
</dt> </dl>

Текущее число точек по горизонтали.

</dd> <dt>

**куррентнумберофколорс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ видеохеадресолутион. нумберофколорс")
</dt> </dl>

Число цветов, поддерживаемое в текущем разрешении.

</dd> <dt>

**куррентнумберофколумнс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 004,14 ")
</dt> </dl>

Если в символьном режиме, число столбцов для контроллера экрана; в противном случае — "0".

</dd> <dt>

**куррентнумберофровс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 004,13 ")
</dt> </dl>

Если в символьном режиме, число строк для контроллера экрана; в противном случае — "0".

</dd> <dt>

**куррентрефрешрате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Герц"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,15 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ видеохеадресолутион. рефрешрате "), **Пунит** (" Герц ")
</dt> </dl>

Текущая частота обновления контроллера экрана в герцах.

</dd> <dt>

**куррентсканмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Video \| 004,8 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ видеохеад**.**Осеркуррентсканмоде**, CIM \_ Видеохеадресолутион. сканмоде ")
</dt> </dl>

Текущий режим просмотра контроллера экрана.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Не поддерживается** (2)


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

**Операция без чередования** (3)


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

**Операция чередования** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**куррентвертикалресолутион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,10 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ видеохеадресолутион. вертикалресолутион "), **Пунит** (" пиксель ")
</dt> </dl>

Текущее число пикселей по вертикали.

</dd> <dt>

**максрефрешрате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Герц"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,5 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ видеохеадресолутион. максрефрешрате "), **Пунит** (" Герц ")
</dt> </dl>

Максимальная частота обновления контроллера экрана в герцах.

</dd> <dt>

**минрефрешрате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Герц"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Video \| 004,4 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ видеохеадресолутион. минрефрешрате "), **Пунит** (" Герц ")
</dt> </dl>

Минимальная частота обновления контроллера экрана в герцах.

</dd> <dt>

**осеркуррентсканмоде**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ видеохеад**.**Куррентсканмоде**, CIM \_ Видеохеадресолутион. осерсканмоде ")
</dt> </dl>

Описание текущего режима сканирования, если свойство **куррентсканмоде** имеет значение "1" (другое).

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Модель \_ CIM**](cim-logicaldevice.md)
</dt> </dl>

 

