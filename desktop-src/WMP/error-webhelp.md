---
title: Ошибка. метод Help
description: метод веб-справки открывает страницу проигрыватель Windows Media Web help для вывода дополнительных сведений о первой ошибке в очереди ошибок (нулевой индекс). | Ошибка. метод Help
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- проигрыватель Windows Media метода "справка"
- метод проигрыватель Windows Media, класс ошибок
- класс Error проигрыватель Windows Media, метод webmethod
topic_type:
- apiref
api_name:
- Error.webHelp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fee647d8f3ddca89ed36c224caab05543715864347700d35ae8e80ee45078cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577878"
---
# <a name="errorwebhelp-method"></a>Ошибка. метод Help

метод веб- **справки** открывает страницу проигрыватель Windows Media Web help для вывода дополнительных сведений о первой ошибке в очереди ошибок (нулевой индекс).

## <a name="syntax"></a>Синтаксис


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

страницы веб-справки всегда содержат последние и более подробные сведения об ошибках проигрыватель Windows Media. Этот метод автоматически передает другие сведения, необходимые для веб-справки, например используемую версию операционной системы.

Чтобы получить доступ к страницам веб-справки напрямую, используйте следующий код ошибки и ссылки центра поддержки.

-   [проигрыватель Windows Media Сведения о коде ошибки](https://support.microsoft.com/kb/886273)
-   [проигрыватель Windows Media Центр решений](https://support.microsoft.com/ph/7763#tab0)

**проигрыватель Windows Media 10 Mobile:** Этот метод всегда выполняется, но не выполняет требуемую операцию.

## <a name="examples"></a>Примеры

в следующем примере создается элемент кнопки HTML, который запускает страницу веб-справки Microsoft проигрыватель Windows Media. Объект **Player** создан с идентификатором "Player".


```JScript
<INPUT TYPE = "BUTTON"  
       NAME = "WHBUTTON"  
       VALUE = "More Info"

OnClick = "Player.error.webHelp();

">

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Error**](error-object.md)
</dt> </dl>

 

 





