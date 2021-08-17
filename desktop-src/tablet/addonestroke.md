---
description: Добавляет новый объект Иинкстрокедисп в переданный объект Инкдивидер.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: Функция Аддонестроке
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 431043b261b3e6fa67e8c6c9e45df27bb6c252dfd92b18e0e4127d4795533c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857133"
---
# <a name="addonestroke-function"></a>Функция Аддонестроке

Добавляет новый объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) в переданный объект [**инкдивидер**](inkdivider-class.md) .

Эта функция не предназначена для использования в коде приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдивидер* \[ окне\]
</dt> <dd>

Маркер объекта [**инкдивидер**](inkdivider-class.md) .

</dd> <dt>

*строкеид* \[ окне\]
</dt> <dd>

[**Идентификатор**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , добавляемого в объект [**инкдивидер**](inkdivider-class.md) .

</dd> <dt>

*cPoints* \[ окне\]
</dt> <dd>

Число пакетов, составляющих новый объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

</dd> <dt>

*апоинтс* \[ окне\]
</dt> <dd>

Массив пакетов, составляющих объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) в *строкеид*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция может возвращать одно из этих значений.



| Код возврата                                                                                  | Описание                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Функция выполнена успешно.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Недопустимый параметр *хдивидер* .<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                         |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Библиотека<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




