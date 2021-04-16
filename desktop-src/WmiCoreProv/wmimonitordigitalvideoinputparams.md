---
description: Представляет входные параметры для цифрового видео.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: Класс Вмимонитордигиталвидеоинпутпарамс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a08e38a38bb5f5e8d539fabdf69c429c42f4b1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712530"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a>Класс Вмимонитордигиталвидеоинпутпарамс

**Вмимонитордигиталвидеоинпутпарамс** представляет входные параметры для цифрового видео. Данные в этом классе соответствуют данным в определении видеовходного видео по стандарту (E-EDID) расширенному расширенному отображению данных. Экземпляр этого класса доступен только в том случае, если свойство **видеоинпуттипе** класса [**Вмимониторбасикдисплайпарамс**](wmimonitorbasicdisplayparams.md) имеет значение Digital.

## <a name="syntax"></a>Синтаксис

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a>Члены

Класс **вмимонитордигиталвидеоинпутпарамс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **вмимонитордигиталвидеоинпутпарамс** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает активный монитор.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Имя конкретного экземпляра монитора.

</dd> <dt>

**IsDFP1xCompatible**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

VESA ДФП 1. x или совместимая. Если этот параметр задан, интерфейс имеет сигнал совместимости с цифровой плоской панелью VESA (ДФП) 1. x. Переход на более высокий уровень дифференциальной сигнализации (ТМДС) КРГБ, 1 пиксель/час, до 8 бит/цвет, наиболее значимый бит (сверху), с высоким уровнем серьезности, DE-активный.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсмониторкласс**](msmonitorclass.md)
</dt> </dl>

 

 




