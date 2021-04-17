---
title: Перечисление WMDM_ENUM_PROP_VALID_VALUES_FORM
description: '\_ \_ Допустимые значения параметра prop enum вмдм \_ \_ \_ . тип перечисления содержит описание возможных форм допустимых значений для свойства.'
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- WMDM_ENUM_PROP_VALID_VALUES_FORM перечисление Windows Media диспетчер устройств
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694524"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a>\_ \_ \_ Перечисление допустимых \_ значений свойства Prop enum вмдм \_

**\_ \_ \_ Допустимые \_ значения \_ параметра prop enum вмдм** . тип перечисления содержит описание возможных форм допустимых значений для свойства.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**ВМДМ \_ Enum \_ prop \_ Допустимые \_ значения \_ ANY**
</dt> <dd>

Все значения допустимы.

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**\_ \_ \_ диапазон допустимых \_ значений Prop Enum \_ вмдм**
</dt> <dd>

Допустимые значения выражаются в виде диапазона. Подробные сведения см. в разделе [**Структура \_ \_ \_ диапазона значений свойств вмдм**](wmdm-prop-values-range.md) .

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**\_ \_ \_ перечисление допустимых \_ значений \_ вмдм enum Prop**
</dt> <dd>

Допустимые значения — перечислимый набор. Подробные сведения см. в описании [**\_ \_ \_ перечисления вмдм Prop Values**](wmdm-prop-values-enum.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется в [**структуре \_ вмдм \_ prop**](wmdm-prop-desc.md) , чтобы указать форму допустимых значений для свойства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3:: Жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_возможность форматирования \_ вмдм**](wmdm-format-capability.md)
</dt> <dt>

[**\_Конфигурация вмдм Prop \_**](wmdm-prop-config.md)
</dt> <dt>

[**ВМДМ \_ prop, \_ DESC**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ перечисление значений Prop вмдм \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_ \_ диапазон значений Prop \_ вмдм**](wmdm-prop-values-range.md)
</dt> </dl>

 

 





