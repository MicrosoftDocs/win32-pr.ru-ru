---
description: Таблица Мсишорткутпроперти позволяет установщику окон задавать свойства для ярлыков, которые также являются объектами оболочки Windows.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Таблица Мсишорткутпроперти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546423"
---
# <a name="msishortcutproperty-table"></a>Таблица Мсишорткутпроперти

Таблица Мсишорткутпроперти позволяет установщику окон задавать свойства для ярлыков, которые также являются объектами [оболочки Windows](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) . Начиная с Windows Vista и Windows Server 2008 оболочка Windows предоставляет интерфейс Ипропертисторе для объектов оболочки, таких как ярлыки. Пакет установщик Windows 5,0, выполняющийся в Windows Server 2008 R2 или Windows 7, может устанавливать эти свойства при установке ярлыка.

**[Установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается. Эта таблица доступна начиная с установщик Windows 5,0.

Таблица Мсишорткутпроперти содержит следующие столбцы.



| Столбец              | Type                         | Ключ | Допускает значения NULL |
|---------------------|------------------------------|-----|----------|
| мсишорткутпроперти | [Идентификатор](identifier.md) | Да   | Нет        |
| Сочетание клавиш\_          | [Идентификатор](identifier.md) | Нет   | Нет        |
| PropertyKey         | [Формате](formatted.md)   | Нет   | Нет        |
| пропвариантвалуе    | [Формате](formatted.md)   | Нет   | Нет        |



 

## <a name="columns"></a>Столбцы

<dl> <dt>

<span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>мсишорткутпроперти
</dt> <dd>

Уникальный идентификатор для этой строки таблицы Мсишорткутпроперти.

</dd> <dt>

<span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Сочетания\_
</dt> <dd>

Ключ в таблице [ярлыков](shortcut-table.md) , который определяет ярлык с набором свойств.

</dd> <dt>

<span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey
</dt> <dd>

Строковое значение, предоставляющее сведения для структуры [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . Сведения в этом поле должны ссылаться на каноническое имя свойства, зарегистрированное в системе свойств Windows. Дополнительные сведения о системе свойств Windows см. в разделе Общие сведения о [системе свойств](/previous-versions//bb776909(v=vs.85)).

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>пропвариантвалуе
</dt> <dd>

Строковое значение, предоставляющее сведения для структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

</dd> </dl>

Для ярлыка можно задать несколько свойств. Если одно и то же свойство задано несколько раз для одного и того же сочетания клавиш, оно устанавливается в неопределенном порядке.

Установщик Windows могут устанавливать свойства ярлыка только при установке или переустановке ярлыка. Исправление, которое не устанавливает уже установленный ярлык, не обновляет свойства ярлыка. Исправление может обновить свойства, включив в пакет исправлений таблицу [ярлыков](shortcut-table.md) и переустановив ярлык.

## <a name="remarks"></a>Комментарии

[Установщик Windows сообщение об ошибке](windows-installer-error-messages.md) 1946 возвращается в виде предупреждения, и установка будет продолжена, если установщик Windows не удается задать свойство ярлыка, указанное в таблице мсишорткутпроперти.

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
</dl>

 

 
