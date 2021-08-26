---
description: реализовано оболочкой, чтобы помочь сценариям и разработчикам Microsoft Visual Basic использовать некоторые функции, доступные в оболочке. Объект Шеллуихелпер не имеет свойств или событий. Для добавления элементов в оболочку предоставляются методы.
title: Объект Шеллуихелпер (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9fffebc8-29b9-4064-b60c-c8c63690a79e
ms.openlocfilehash: f254bd218024b3d1df15a826da701b1f010ae616
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473330"
---
# <a name="shelluihelper-object"></a>Объект Шеллуихелпер

реализовано оболочкой, чтобы помочь сценариям и разработчикам Microsoft Visual Basic использовать некоторые функции, доступные в оболочке. Объект **шеллуихелпер** не имеет свойств или событий. Для добавления элементов в оболочку предоставляются методы.

## <a name="members"></a>Элементы

Объект **шеллуихелпер** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Объект **шеллуихелпер** содержит эти методы.




| Метод | Описание | 
|--------|-------------|
| <a href="shelluihelper-addchannel.md"><strong>аддчаннел</strong></a> | Добавляет новый канал в список каналов в меню <strong>Избранное</strong> Internet Explorer и на панель <strong>каналов</strong> на рабочем столе.<br /><blockquote>[!Note]<br />этот метод больше не поддерживается в Windows Vista. В этой операционной системе возвращается E_NOTIMPL.</blockquote><br /> | 
| <a href="shelluihelper-adddesktopcomponent.md"><strong>адддесктопкомпонент</strong></a> | Добавляет элемент в активный рабочий стол.<br /> | 
| <a href="shelluihelper-addfavorite.md"><strong>аддфаворите</strong></a> | Отображает пользовательский интерфейс по умолчанию для создания элемента избранного. Пользовательский интерфейс инициализируется с указанными параметрами.<br /> | 
| <a href="shelluihelper-issubscribed.md"><strong>IsSubscribed</strong></a> | Указывает, подписан ли указанный URL-адрес на.<br /> | 




 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Ексдисп. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 




