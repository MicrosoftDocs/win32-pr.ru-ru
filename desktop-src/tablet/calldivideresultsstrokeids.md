---
description: Извлекает свойства идентификатора для объектов Иинкстрокедисп соответствующего слова, строки, абзаца или рисунка, определенных функцией анализа рукописного ввода.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: Функция Каллдивидересултсстрокеидс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 64b3e4180a34c45890408f8ba92cc79465fffa7f1028152e27f8d5c0aa40e3e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009134"
---
# <a name="calldivideresultsstrokeids-function"></a>Функция Каллдивидересултсстрокеидс

Извлекает свойства [**идентификатора**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) для объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) соответствующего слова, строки, абзаца или рисунка, определенных функцией анализа рукописного ввода.

Эта функция не предназначена для использования в коде приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдивидер* \[ окне\]
</dt> <dd>

Маркер объекта- [разделителя](the-divider-object.md) .

</dd> <dt>

*\[ авордстрокеидс \]* \[исходящий трафик\]
</dt> <dd>

Массив идентификаторов штрихов рукописного ввода в слове.

</dd> <dt>

*\[ алинестрокеидс \]* \[исходящий трафик\]
</dt> <dd>

Массив идентификаторов штриха для рукописного ввода в строке.

</dd> <dt>

*\[ апараграфстрокеидс \]* \[исходящий трафик\]
</dt> <dd>

Массив идентификаторов штрихов рукописного ввода в абзаце.

</dd> <dt>

*\[ адравингстрокеидс \]* \[исходящий трафик\]
</dt> <dd>

Массив идентификаторов штрихов рукописного ввода в документе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция может возвращать одно из этих значений.



| Код возврата                                                                                  | Описание                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Функция выполнена успешно.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *хдивидер* .<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Библиотека<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




