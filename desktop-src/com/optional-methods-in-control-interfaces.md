---
title: Необязательные методы в интерфейсах управления
description: Необязательные методы в интерфейсах управления
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92303b9e4e6a5edd295d0895a9121eee70ea05ae2a8967a9346ea26b153e8b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859294"
---
# <a name="optional-methods-in-control-interfaces"></a>Необязательные методы в интерфейсах управления

Реализация интерфейса не обязательно означает реализацию всех методов этого интерфейса для выполнения каких-либо дополнительных действий, чем возврат E \_ нотимпл или S \_ OK соответственно. В следующей таблице приведены методы интерфейсов, перечисленных в разделе [Поддержка интерфейса —](what-support-for-an-interface-means.md) это тема, которую элемент управления может реализовать таким образом. Если интерфейс поддерживается, любой метод, не указанный здесь, должен быть полностью реализован.



| Метод интерфейса IOleControl                                                                                                   | Примечания                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**Жетконтролинфо**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo), [ **OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | Обязателен для элементов управления с назначенными клавишами.<br/>                              |
| [**Метод интерфейса IOleControl:: Онамбиентпропертичанже**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | Обязателен для элементов управления, использующих внешние свойства.<br/>                 |
| [**Метод интерфейса IOleControl:: FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | См. раздел [замораживание события](event-freezing.md)<br/>                            |
| иолеобжект                                                                                                    |                                                                                |
| [**сетмоникер**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | Обязательно, если элемент управления не помечен с помощью ОЛЕМИСК \_ кантлинкинсиде<br/> |
| [**Моникер**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | Обязательно, если элемент управления не помечен с помощью ОЛЕМИСК \_ кантлинкинсиде<br/> |
| [**инитфромдата**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | Необязательный<br/>                                                            |
| [**жетклипбоарддата**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | Необязательный<br/>                                                            |
| [**сетекстент**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | Обязательно только для \_ содержимого дваспект<br/>                                |
| [**Расширение**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | Обязательно только для \_ содержимого дваспект<br/>                                |
| [**сетколорсчеме**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | Необязательный<br/>                                                            |
| [**доверб**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | См. Примечание 1<br/>                                                          |
| иолеинплацеобжект                                                                                             |                                                                                |
| [**контекстсенситивехелп**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Необязательный<br/>                                                            |
| [**реактиватеандундо**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | Необязательный<br/>                                                            |
| Метода IOleInPlaceActiveObject                                                                                       |                                                                                |
| [**контекстсенситивехелп**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | Необязательный<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**Freeze**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | Необязательный<br/>                                                            |
| [**Освободить**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | Необязательный<br/>                                                            |
| [**Натенок**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | Необязательный<br/>                                                            |
| IPersistStream, Иперсистстреаминит, Иперсистмемори                                                            |                                                                                |
| [**жетсиземакс**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | См. примечание 2<br/>                                                          |



 

1.  Элемент управления со страницами свойств должен поддерживать [**иолеобжект::D оверб**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) для \_ свойств олеиверб и \_ основных глаголов олеиверб. Элемент управления, который может быть активным, должен поддерживать **доверб** для \_ команды олеиверб инплацеактивате. Элемент управления, который может быть активным UI, также должен поддерживать **доверб** для \_ команды олеиверб уиактивате.
2.  Если элемент управления поддерживает [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) или [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) и может возвращать точное значение, это следует сделать.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Элементы управления](controls.md)
</dt> </dl>

 

 





