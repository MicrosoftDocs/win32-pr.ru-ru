---
title: Метод Clone Иенумтфрендерингмаркуп
description: Метод Clone Иенумтфрендерингмаркуп создает копию объекта перечислителя.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Платформа текстовых служб метода клонирования
- Платформа текстовых служб метода клонирования, интерфейс Иенумтфрендерингмаркуп
- Платформа текстовых служб с интерфейсом Иенумтфрендерингмаркуп, метод Clone
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681644"
---
# <a name="ienumtfrenderingmarkupclone-method"></a>Метод Иенумтфрендерингмаркуп:: Clone

Метод **иенумтфрендерингмаркуп:: Clone** создает копию объекта перечислителя.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппенум* \[ заполняет\]
</dt> <dd>

\[\]указатель на интерфейс [иенумтфрендерингмаркуп](/windows/desktop/TSF/ienumtfrenderingmarkup) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Значение                                                                                        | Описание                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Метод успешно выполнен.<br/>          |
| <dl> <dt>**\_Ошибка E**</dt> </dl>       | Произошла неизвестная ошибка.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Один или несколько параметров недопустимы.<br/> |



 

## <a name="remarks"></a>Комментарии

> [!Note]  
> Этот метод в настоящее время не находится в файлах общедоступного заголовка. Чтобы использовать этот API, необходимо скомпилировать [прототип](prototypes.md)с помощью MIDL.

 

 

