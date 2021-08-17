---
description: Задает свойство LineHeight объекта Инкдивидер.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: Функция Сетлинехеигхт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 2c6a176b5878b7aaee4a0e51a5a366302b13a1a643453ad2c6d57e103362c4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966823"
---
# <a name="setlineheight-function"></a>Функция Сетлинехеигхт

Задает свойство [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) объекта [**инкдивидер**](inkdivider-class.md) .

Эта вспомогательная функция не предназначена для использования в коде приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдивидер* \[ окне\]
</dt> <dd>

Маркер объекта [**инкдивидер**](inkdivider-class.md) .

</dd> <dt>

*ллинехеигхт* \[ окне\]
</dt> <dd>

Свойство [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) объекта [**инкдивидер**](inkdivider-class.md) в единицах HIMETRIC.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция может возвращать одно из этих значений.



| Код возврата                                                                                  | Описание                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Функция выполнена успешно.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *пдивидер* .<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Библиотека<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 
