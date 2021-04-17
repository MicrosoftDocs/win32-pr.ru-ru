---
title: Структура WMDM_PROP_VALUES_ENUM
description: '\_ \_ Структура перечисления значений Prop вмдм \_ содержит перечислимый набор допустимых значений для конкретного свойства в определенной конфигурации свойства.'
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- WMDM_PROP_VALUES_ENUM структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694644"
---
# <a name="wmdm_prop_values_enum-structure"></a>\_ \_ Структура перечисления значений Prop вмдм \_

Структура **\_ \_ \_ перечисления значений Prop вмдм** содержит перечислимый набор допустимых значений для конкретного свойства в определенной конфигурации свойства.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a>Члены

<dl> <dt>

**ценумвалуес**
</dt> <dd>

Число перечисляемых значений.

</dd> <dt>

**пвалуес**
</dt> <dd>

Указатель на массив значений. Размер массива равен значению параметра **ценумвалуес**.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура используется в структуре **вмдм \_ prop \_** Structure для описания перечислимого набора допустимых значений. Перечислимый набор допустимых значений применим, если выбрано перечисление \_ \_ \_ допустимых значений Prop enum вмдм \_ \_ из перечисления **\_ \_ \_ допустимых \_ значений \_ Свойства вмдм enum Prop** .

Вызывающий объект необходим для высвобождения памяти, используемой **пвалуес**. Пример того, как это сделать, см. в [**разделе \_ \_ функция форматирования вмдм**](wmdm-format-capability.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IWMDMDevice3:: Жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_ \_ \_ форма допустимых \_ значений \_ вмдм enum Prop**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**\_возможность форматирования \_ вмдм**](wmdm-format-capability.md)
</dt> <dt>

[**\_Конфигурация вмдм Prop \_**](wmdm-prop-config.md)
</dt> <dt>

[**ВМДМ \_ prop, \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ диапазон значений Prop \_ вмдм**](wmdm-prop-values-range.md)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





