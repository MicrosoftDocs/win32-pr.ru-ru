---
title: Структура WMDM_PROP_DESC
description: Структура ВМДМ \_ prop \_ Structure описывает допустимые значения свойства в определенной конфигурации свойства.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- WMDM_PROP_DESC структура диспетчер устройств Windows Media
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad250745d51f00d3bb0492b6da8d3f9802bf87b78d65f4640324a68caa9ddf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903944"
---
# <a name="wmdm_prop_desc-structure"></a>\_Структура вмдм Prop \_

Структура **вмдм \_ prop \_** Structure описывает допустимые значения свойства в определенной конфигурации свойства.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a>Члены

<dl> <dt>

**пвсзпропнаме**
</dt> <dd>

Имя свойства. Приложение должно освободить эту память, когда она будет создана с ее помощью.

</dd> <dt>

**валидвалуесформ**
</dt> <dd>

[**\_ \_ \_ Допустимые \_ значения \_ свойства Prop enum вмдм формируют**](wmdm-enum-prop-valid-values-form.md) значение перечисления, описывающее тип значений, например диапазон или список. Значение этого перечисления определяет, какая переменная-член используется.

</dd> <dt>

**ValidValues**
</dt> <dd>

Содержит допустимые значения свойства в конфигурации конкретного свойства. Этот элемент содержит один из трех элементов: значение перечисления ВМДМ \_ Enum \_ prop \_ Допустимые \_ значения \_ any; элемент **валидвалуесранже** или элемент **енумератедвалидвалуес**. Значение или член обозначается **валидвалуесформ**.

<dl> <dt>

**валидвалуесранже**
</dt> <dd>

Структура [**\_ \_ \_ диапазона значений Prop вмдм**](wmdm-prop-values-range.md) , содержащая диапазон допустимых значений. Это происходит только в том случае, если для **валидвалуесформ** задано значение вмдм \_ Enum \_ PROPS \_ Range допустимые \_ значения \_ . См. заметки.

</dd> <dt>

**енумератедвалидвалуес**
</dt> <dd>

Структура [**\_ \_ \_ перечисления значений Prop вмдм**](wmdm-prop-values-enum.md) , содержащая перечислимый набор допустимых значений. Это происходит, только если для **валидвалуесформ** задано значение вмдм \_ Enum \_ prop \_ Values Valid \_ \_ . См. заметки.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Структура **вмдм \_ prop \_** содержит описание свойства, состоящее из имени свойства и его допустимых значений в конкретной конфигурации.

Вызывающий объект необходим для высвобождения памяти, используемой **валидвалуесранже** или **енумератедвалуес**. Пример того, как это сделать, см. в [**разделе \_ \_ функция форматирования вмдм**](wmdm-format-capability.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдм. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**IWMDMDevice3:: Жетформаткапабилити**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_ \_ \_ форма допустимых \_ значений \_ вмдм enum Prop**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**\_возможность форматирования \_ вмдм**](wmdm-format-capability.md)
</dt> <dt>

[**\_Конфигурация вмдм Prop \_**](wmdm-prop-config.md)
</dt> <dt>

[**\_ \_ перечисление значений Prop вмдм \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**\_ \_ диапазон значений Prop \_ вмдм**](wmdm-prop-values-range.md)
</dt> <dt>

[**Структуры**](structures.md)
</dt> </dl>

 

 





