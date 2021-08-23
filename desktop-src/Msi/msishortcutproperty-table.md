---
description: таблица мсишорткутпроперти позволяет установщику окон задавать свойства для ярлыков, которые также Windows объекты оболочки.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Таблица Мсишорткутпроперти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7cf51d8016cdc87008a6cc9a20daee1f35131af7ea0f5827c67da7f45a6e46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944431"
---
# <a name="msishortcutproperty-table"></a>Таблица Мсишорткутпроперти

таблица мсишорткутпроперти позволяет установщику окон задавать свойства для ярлыков, которые также [Windows объекты оболочки](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) . начиная с Windows Vista и Windows Server 2008 оболочка Windows предоставляет интерфейс ипропертисторе для объектов оболочки, таких как ярлыки. пакет установщик Windows 5,0, выполняющийся на Windows Server 2008 R2 или Windows 7, может задавать эти свойства при установке ярлыка.

**[установщик Windows 4,5 или более ранней версии](not-supported-in-windows-installer-4-5.md):** Не поддерживается. эта таблица доступна начиная с установщик Windows 5,0.

Таблица Мсишорткутпроперти содержит следующие столбцы.



| Столбец              | Type                         | Ключ | Допускает значения NULL |
|---------------------|------------------------------|-----|----------|
| мсишорткутпроперти | [Идентификатор](identifier.md) | Д   | Нет        |
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

Строковое значение, предоставляющее сведения для структуры [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . сведения в этом поле должны ссылаться на каноническое имя свойства, зарегистрированного в системе свойств Windows. дополнительные сведения о системе свойств Windows см. в разделе общие сведения о [системе свойств](/previous-versions//bb776909(v=vs.85)).

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>пропвариантвалуе
</dt> <dd>

Строковое значение, предоставляющее сведения для структуры [**пропвариант**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

</dd> </dl>

Для ярлыка можно задать несколько свойств. Если одно и то же свойство задано несколько раз для одного и того же сочетания клавиш, оно устанавливается в неопределенном порядке.

Windows Установщик может устанавливать свойства ярлыка только при установке или переустановке ярлыка. Исправление, которое не устанавливает уже установленный ярлык, не обновляет свойства ярлыка. Исправление может обновить свойства, включив в пакет исправлений таблицу [ярлыков](shortcut-table.md) и переустановив ярлык.

## <a name="remarks"></a>Remarks

[установщик Windows сообщение об ошибке](windows-installer-error-messages.md) 1946 возвращается в виде предупреждения, и установка будет продолжена, если установщик Windows не удается задать свойство ярлыка, указанное в таблице мсишорткутпроперти.

## <a name="validation"></a>Проверка

<dl>

[ICE03](ice03.md)  
</dl>

 

 
