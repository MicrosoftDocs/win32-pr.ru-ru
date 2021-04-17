---
title: Структура WMDM_PROP_VALUES_RANGE
description: '\_ \_ Структура диапазона значений Prop вмдм \_ описывает диапазон допустимых значений для конкретного свойства в определенной конфигурации свойства.'
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- WMDM_PROP_VALUES_RANGE структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694643"
---
# <a name="wmdm_prop_values_range-structure"></a>\_ \_ Структура диапазона значений Prop вмдм \_

Структура **\_ \_ \_ диапазона значений Prop вмдм** описывает диапазон допустимых значений для конкретного свойства в определенной конфигурации свойства.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a>Члены

<dl> <dt>

**rangeMin**
</dt> <dd>

Минимальное значение в диапазоне.

</dd> <dt>

**rangeMax**
</dt> <dd>

Максимальное значение в диапазоне.

</dd> <dt>

**ранжестеп**
</dt> <dd>

Размер шага, в котором допустимы значения, увеличивающиеся из минимального значения до максимального значения. Это позволяет указать дискретные допустимые значения в диапазоне.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта структура используется в структуре [**вмдм \_ prop \_**](wmdm-prop-desc.md) , чтобы описать диапазон допустимых значений. Диапазон допустимых значений применим, если выбрано перечисление \_ \_ \_ допустимых значений Prop enum вмдм \_ \_ из перечисления [**\_ \_ \_ допустимых \_ значений \_ Свойства вмдм enum Prop**](wmdm-enum-prop-valid-values-form.md) .

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

[**\_ \_ перечисление значений Prop вмдм \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





