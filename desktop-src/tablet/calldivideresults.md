---
description: Извлекает результаты анализа из объекта Инкдивидер.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: Функция Каллдивидересултс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143006"
---
# <a name="calldivideresults-function"></a>Функция Каллдивидересултс

Извлекает результаты анализа из объекта [**инкдивидер**](inkdivider-class.md) .

Эта функция не предназначена для использования в коде приложения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хдивидер* \[ окне\]
</dt> <dd>

Маркер объекта [**инкдивидер**](inkdivider-class.md) .

</dd> <dt>

*авордстрокеидс* \[ заполняет\]
</dt> <dd>

Массив идентификаторов, связанный со словом, которое передается в класс [**инкдивидер**](inkdivider-class.md) .

</dd> <dt>

*алинестрокеидс* \[ заполняет\]
</dt> <dd>

Массив свойств [**идентификатора**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) для объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , связанных со строкой, передаваемой в класс [**инкдивидер**](inkdivider-class.md) .

</dd> <dt>

*апараграфстрокеидс* \[ заполняет\]
</dt> <dd>

Массив свойств [**идентификатора**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) для объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , связанных с абзацем из класса [**инкдивидер**](inkdivider-class.md) .

</dd> <dt>

*адравингстрокеидс* \[ заполняет\]
</dt> <dd>

Массив свойств [**идентификатора**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) для объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , связанных с рисованием из класса [**инкдивидер**](inkdivider-class.md) .

</dd> <dt>

*пастрвордс* \[ заполняет\]
</dt> <dd>

Массив слов, возвращаемых из анализа рукописного ввода.

</dd> <dt>

*пастрлинес* \[ заполняет\]
</dt> <dd>

Массив строк, возвращенных из анализа рукописного ввода.

</dd> <dt>

*пастрпараграфс* \[ заполняет\]
</dt> <dd>

Массив абзацев, возвращенных из анализа рукописного ввода.

</dd> <dt>

*авордротатионцентеркс* \[ заполняет\]
</dt> <dd>

Массив центральных точек слов вдоль оси x из анализа рукописного ввода.

</dd> <dt>

*авордротатионцентери* \[ заполняет\]
</dt> <dd>

Массив центральных точек слов вдоль оси y из анализа рукописного ввода.

</dd> <dt>

*авордангле* \[ заполняет\]
</dt> <dd>

Массив, содержащий углы, на которые поворачиваются слова для получения лучших результатов анализа.

</dd> <dt>

*алинеротатионцентеркс* \[ заполняет\]
</dt> <dd>

Массив, содержащий центральные точки линий вдоль оси x.

</dd> <dt>

*алинеротатионцентери* \[ заполняет\]
</dt> <dd>

Массив, содержащий центральные точки линий вдоль оси y.

</dd> <dt>

*алинеангле* \[ заполняет\]
</dt> <dd>

Массив, содержащий углы, на которые поворачиваются линии для получения наилучших результатов анализа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Эта функция может возвращать одно из этих значений.



| Код возврата                                                                                   | Описание                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Функция выполнена успешно.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Недопустимый параметр *хдивидер* .<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Не удалось выделить достаточно памяти для хранения результатов.<br/> |



 

## <a name="remarks"></a>Комментарии

Чтобы избежать утечек памяти, необходимо освободить ресурсы для *пастрвордс*, *пастрлинес* и *пастрпараграфс*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                         |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Библиотека<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




