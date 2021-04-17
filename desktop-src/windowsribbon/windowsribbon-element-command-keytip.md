---
title: Свойство Command. keytip
description: Представляет keytip для элемента управления.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Лента Windows для свойства Command. keytip
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701083"
---
# <a name="commandkeytip-property"></a>Свойство Command. keytip

Представляет keytip для элемента управления.

## <a name="usage"></a>Использование

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                   | Описание                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**Строка**](windowsribbon-element-string.md)<br/> | Может выполняться не более одного раза<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Комментарии

Необязательный элемент.

Может встречаться не более одного раза для каждого элемента [**Command**](windowsribbon-element-command.md) .

**Command. KeyTip** может содержать значение типа *xs: String* , ограниченное любой последовательностью символов Юникода, включая пробелы.

**Команда. KeyTip** может начинаться с числа, только если оно связано с элементом управления на [вкладке](windowsribbon-controls-tab.md) или на [панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md).

Чтобы отобразить ключевые подсказки, допустимые для текущего состояния ленты, нажмите и удерживайте клавишу ALT. На следующем снимке экрана показан первоначальный или первый уровень, которые отображаются в Microsoft Paint для Windows 7. После выбора KeyTip первого уровня отображаются только подсказки для второго уровня.

![ключевые подсказки первого уровня в Microsoft Paint для Windows 7](images/properties/ui-pkey-label-keytips.png)

**Command. KeyTip** выступает в качестве сочетания клавиш для команды, если эта команда не предоставлена через пункт меню. В этом случае платформа игнорирует значение **Command. KeyTip** и вместо этого использует символ, предшествующий амперсанду, указанный параметром [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или [ \_ \_ подписью PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md). Если амперсанд не указан с помощью **команды Command. лабелтитле** или \_ метки PKEY пользовательского интерфейса \_ , то KeyTip или сочетания клавиш не предоставляются.

Если для **Command. KeyTip** не указано значение, требуется дочерний элемент [**String**](windowsribbon-element-string.md) .

> [!Note]  
> Если **Command. KeyTip** содержит как значение, так и дочерний элемент [**String**](windowsribbon-element-string.md) , то приоритет имеет **строка** .

 

По умолчанию платформа использует следующие буквы для автоматического создания подсказок:

-   **F** назначается [меню приложение](windowsribbon-controls-applicationmenu.md).
-   **Y** назначается любой команде, не имеющей KeyTip, указанной приложением.
-   **Z** назначается каждому элементу управления [группы](windowsribbon-controls-group.md) и не может быть настроено. Группа KeyTip отображается, только если [**скалингполици**](windowsribbon-element-scalingpolicy.md) элемента управления указывает параметр размера **всплывающего окна** . Дополнительные сведения см. в разделе [Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md).

> [!Note]  
> Ни одна из этих букв не зарезервирована платформой. Каждый из них может быть назначен одной или нескольким командам по мере необходимости.

 

Платформа разрешает конфликты KeyTip следующими способами:

-   Если один или несколько элементов управления ["Вкладка"](windowsribbon-controls-tab.md) связаны с одним и тем же KeyTip, к каждому keytipу добавляется число, начиная с 1 и последовательно увеличивая (2, 3,...) для каждого элемента управления в порядке объявления. Если любому элементу управления вкладки назначена буква F как KeyTip, [меню приложения](windowsribbon-controls-applicationmenu.md) назначается F1 с остальными подклавишами, скорректированными согласно описанию.
-   При сопоставлении с одним элементом управления на [вкладке](windowsribbon-controls-tab.md)KeyTip F допустим как для элемента управления, так и для [меню приложения](windowsribbon-controls-applicationmenu.md). Меню приложения по умолчанию KeyTip не изменяется, но для элемента управления на активной вкладке приоритет передается.
-   Если один или несколько элементов управления на [вкладке](windowsribbon-controls-tab.md) связаны с одним и тем же KeyTip, платформа автоматически переопределяет ключевые подсказки этих элементов управления, как описано выше.

> [!Note]  
> Небольшая разновидность цвета текста используется для выделения рефакторинга подсказок в стандартной реализации ленты. Для нестандартной реализации ленты, в которой настроен цвет ленты, это поведение платформы переопределяется и все подсказки отображаются с тем же цветом текста. Дополнительные сведения см. в разделе [Настройка цветов ленты](ribbon-color.md).

 

Максимальная длина не ограничена.

## <a name="examples"></a>Примеры

В следующем примере показана разметка для элемента [**Command**](windowsribbon-element-command.md) с объявлением **Command. KeyTip** .


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[UI \_ PKEY \_ keytip](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





