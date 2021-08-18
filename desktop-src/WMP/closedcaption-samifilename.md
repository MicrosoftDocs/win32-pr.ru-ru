---
title: Клоседкаптион. Самифиленаме
description: Свойство Самифиленаме указывает или получает имя файла, содержащего сведения, необходимые для закрытого субтитров.
ms.assetid: f2090500-6c9f-4d2d-9855-a9c193b00a41
keywords:
- клоседкаптион. самифиленаме проигрыватель Windows Media
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
ms.openlocfilehash: 22ba314208db3cb5529042011f269f026a4cf2bd4d4b01d1b8d64719b96a5f90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119515"
---
# <a name="closedcaptionsamifilename"></a>Клоседкаптион. Самифиленаме

Свойство **самифиленаме** указывает или получает имя файла, содержащего сведения, необходимые для закрытого субтитров.

``` syntax
player.closedCaption.SAMIFileName
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи.

## <a name="remarks"></a>Remarks

Синхронизированный доступный файл обмена мультимедийными данными (SAMI) должен использовать расширение имени файла. SMI или Sami.

Если не указать значение для **самифиленаме**, это свойство получает строку, содержащую имя файла или URL-адрес, связанный с текущим элементом мультимедиа. Такая ассоциация может возникнуть, когда файл SAMI указывается с помощью параметра URL-адреса *Sami* или автоматически, если имя файла Sami совпадает с именем файла цифрового носителя (за исключением расширения имени файла). Если с текущим носителем не связан файл SAMI, это свойство получает пустую строку ("").

После указания значения для **самифиленаме** это значение сохраняется до тех пор, пока не будет указано новое значение (или до открытия нового элемента мультимедиа с помощью параметра *Sami* URL). Поэтому перед воспроизведением каждого нового элемента мультимедиа необходимо указать новое значение для этого свойства. Таким образом, новое значение для **самифиленаме** вступит в силу при открытии следующего элемента мультимедиа (или *проигрывателя*.**** вызывается Close). Указание нового значения для **самифиленаме** не влияет на текущий носитель.

чтобы проигрыватель Windows Media вернуться к использованию файла SAMI, связанного с определенным элементом мультимедиа, перед воспроизведением следующего элемента мультимедиа укажите значение **самифиленаме** , равное пустой строке ("").

**проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.

## <a name="examples"></a>Примеры

в следующих трех примерах JScript используется *клоседкаптион*. **Самифиленаме** , чтобы указать имя текстового файла с закрытым заголовком. Объект **Player** создан с идентификатором "Player".


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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Объект Клоседкаптион**](closedcaption-object.md)
</dt> <dt>

[**Player. закрыть**](player-close.md)
</dt> </dl>

 

 





