---
description: Создание нового дочернего элемента. Добавляет объекты IWiaItem2 в дерево IWiaItem2 устройства.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'Метод IWiaItem2:: Креатечилдитем (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e7d7215f528c36f6b4f5883be19d5d37c8b76d4d8ad9cacbcaa7a63397337c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965573"
---
# <a name="iwiaitem2createchilditem-method"></a>Метод IWiaItem2:: Креатечилдитем

Создание нового дочернего элемента. Добавляет объекты [**IWiaItem2**](-wia-iwiaitem2.md) в дерево **IWiaItem2** устройства.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*литемфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

Задает тип элемента WIA 2,0. См. раздел [**Флаги типа элемента WIA**](-wia-wia-item-type-flags.md).

</dd> <dt>

*лкреатионфлагс* \[ окне\]
</dt> <dd>

Тип: **Long**

Указывает, как создать новый элемент.

<dt>

<span id="0"></span>

<span id="0"></span>**0** (0)


</dt> <dd>

Задайте значения по умолчанию для свойств дочернего элемента.

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Копирование \_ \_ \_ Значения родительских свойств** (0x40000000)


</dt> <dd>

Скопируйте значения всех свойств чтения и записи из родительского объекта.

</dd> </dl> </dd> <dt>

*бстритемнаме* \[ окне\]
</dt> <dd>

Тип: **BSTR**

Указывает имя элемента. Это имя добавляется в конец имени родительского элемента для создания полного имени элемента.

</dd> <dt>

*ppIWiaItem2* \[ заполняет\]
</dt> <dd>

Тип: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Получает адрес указателя на интерфейс [**IWiaItem2**](-wia-iwiaitem2.md) , который задает метод **IWiaItem2:: креатечилдитем** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Некоторые аппаратные устройства WIA 2,0 позволяют приложениям создавать новые элементы в дереве [**IWiaItem2**](-wia-iwiaitem2.md) , представляющем устройство. Приложения должны протестировать устройства, чтобы узнать, поддерживают ли они эту возможность. Используйте интерфейс Иенумвиа \_ dev \_ CAP для перечисления возможностей текущего устройства.

Если устройство позволяет создавать новые элементы в дереве [**IWiaItem2**](-wia-iwiaitem2.md) , вызов **IWiaItem2:: креатечилдитем** создает новый объект **IWiaItem2** , являющийся дочерним по отношению к текущему узлу. Он передает указатель на новый узел приложению через параметр *ppIWiaItem2* . Приложения должны вызывать метод [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для указателей интерфейса, которые они получают с помощью параметра *ppIWiaItem2* .

Если *лкреатионфлагс* копирует \_ значения родительского \_ свойства \_ , а *Литемфлагс* равен нулю, функция возвращает E \_ INVALIDARG.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
