---
title: Ошибка. метод Help
description: Метод "Справка" открывает страницу веб-справки проигрывателя Windows Media для вывода дополнительных сведений о первой ошибке в очереди ошибок (нулевой индекс). | Ошибка. метод Help
ms.assetid: 79797b41-1d47-4347-aa47-c104f7f7fbaf
keywords:
- метод WebMethod проигрыватель Windows Media
- метод WebMethod Windows Media Player, класс Error
- Класс ошибок Windows Media Player, метод WebMethod
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
ms.openlocfilehash: 862376be956bc8b37a778f5c9d1d2238c876208d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698970"
---
# <a name="errorwebhelp-method"></a>Ошибка. метод Help

Метод " **Справка** " открывает страницу веб-справки проигрывателя Windows Media для вывода дополнительных сведений о первой ошибке в очереди ошибок (нулевой индекс).

## <a name="syntax"></a>Синтаксис


```JScript
Error.webHelp()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Страницы веб-справки всегда содержат последние и более подробные сведения об ошибках проигрывателя Windows Media. Этот метод автоматически передает другие сведения, необходимые для веб-справки, например используемую версию операционной системы.

Чтобы получить доступ к страницам веб-справки напрямую, используйте следующий код ошибки и ссылки центра поддержки.

-   [Сведения о коде ошибки проигрывателя Windows Media](https://support.microsoft.com/kb/886273)
-   [Центр решений проигрывателя Windows Media](https://support.microsoft.com/ph/7763#tab0)

**Проигрыватель Windows Media 10 Mobile:** Этот метод всегда выполняется, но не выполняет требуемую операцию.

## <a name="examples"></a>Примеры

В следующем примере создается элемент кнопки HTML, который запускает страницу веб-справки проигрывателя Microsoft Windows Media. Объект **Player** создан с идентификатором "Player".


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
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Error**](error-object.md)
</dt> </dl>

 

 





