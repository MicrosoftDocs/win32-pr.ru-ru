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
ms.openlocfilehash: fa86add32d77a5b2838fc78eaf097c11b8a15db3f0fde9186f93046691ebc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926570"
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

### <a name="properties"></a>Элемент Property

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

 

 




