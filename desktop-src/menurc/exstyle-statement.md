---
title: ОПЕРАТОРЕ EXSTYLE, инструкция
description: Определяет расширенные стили окна для диалогового окна. В определении ресурса инструкция ОПЕРАТОРЕ EXSTYLE помещается с необязательными инструкциями перед началом тела определения ресурса.
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- Меню инструкций ОПЕРАТОРЕ EXSTYLE и другие ресурсы
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487620"
---
# <a name="exstyle-statement"></a>ОПЕРАТОРЕ EXSTYLE, инструкция

Определяет расширенные стили окна для диалогового окна. В определении ресурса инструкция **операторе EXSTYLE** помещается с необязательными инструкциями перед началом тела определения ресурса.

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*Расширенный стиль*
</dt> <dd>

Расширенный стиль окна для диалогового окна или элемента управления. Список расширенных стилей окон см. в разделе [**Расширенные стили окон**](/windows/desktop/winmsg/extended-window-styles).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Для элементов управления расширенные стили задаются после параметра *Style* в операторе Control Resource-Definition. Дополнительные сведения см. в описании инструкции Resource-Definition для отдельного элемента управления.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Accelerator**](accelerators-resource.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**Откроется**](dialog-resource.md)
</dt> <dt>

[**МЕНЮ**](menu-resource.md)
</dt> <dt>

[**ПОДСКАЗКИ**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[Определяемый пользователем ресурс](user-defined-resource.md)
</dt> </dl>

 

 