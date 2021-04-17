---
title: Клоседкаптион. Самифиленаме
description: Свойство Самифиленаме указывает или получает имя файла, содержащего сведения, необходимые для закрытого субтитров.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- Проигрыватель Windows Media Клоседкаптион. Самифиленаме
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIFileName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bd748076eec80b5b7d97e7c041f454c4f9193f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694874"
---
# <a name="closedcaptionsamifilename"></a>Клоседкаптион. Самифиленаме

Свойство **самифиленаме** указывает или получает имя файла, содержащего сведения, необходимые для закрытого субтитров.

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи.

## <a name="remarks"></a>Комментарии

Синхронизированный доступный файл обмена мультимедийными данными (SAMI) должен использовать расширение имени файла. SMI или Sami.

Если не указать значение для **самифиленаме**, это свойство получает строку, содержащую имя файла или URL-адрес, связанный с текущим элементом мультимедиа. Такая ассоциация может возникнуть, когда файл SAMI указывается с помощью параметра URL-адреса *Sami* или автоматически, если имя файла Sami совпадает с именем файла цифрового носителя (за исключением расширения имени файла). Если с текущим носителем не связан файл SAMI, это свойство получает пустую строку ("").

После указания значения для **самифиленаме** это значение сохраняется до тех пор, пока не будет указано новое значение (или до открытия нового элемента мультимедиа с помощью параметра *Sami* URL). Поэтому перед воспроизведением каждого нового элемента мультимедиа необходимо указать новое значение для этого свойства. Таким образом, новое значение для **самифиленаме** вступит в силу при открытии следующего элемента мультимедиа (или *проигрывателя*.**** вызывается Close). Указание нового значения для **самифиленаме** не влияет на текущий носитель.

Чтобы проигрыватель Windows Media возвращался с помощью файла SAMI, связанного с определенным элементом мультимедиа, перед воспроизведением следующего элемента мультимедиа укажите значение **самифиленаме** , равное пустой строке ("").

**Проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.

## <a name="examples"></a>Примеры

В следующих трех примерах JScript используется *клоседкаптион*. **Самифиленаме** , чтобы указать имя текстового файла с закрытым заголовком. Объект **Player** создан с идентификатором "Player".


```JScript
// Display the closed captions from a website.
Player.closedCaption.SAMIFileName="https://www.proseware.com/ccsample.smi";

// Display the closed captions from a local network.
// You must add an escape sequence of a backslash for every original backslash.
Player.closedCaption.SAMIFileName="\\\\yourservername\\Public\\ccsample.smi";

// Display the closed captions from a file on a local drive.
// Be sure to add the appropriate escape sequences.
Player.closedCaption.SAMIFileName="C:\\WMSDK\\WMPSDK9\\samples\\media\\ccsample.smi";

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Объект Клоседкаптион**](closedcaption-object.md)
</dt> <dt>

[**Player. закрыть**](player-close.md)
</dt> </dl>

 

 





