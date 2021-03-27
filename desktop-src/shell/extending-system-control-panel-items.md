---
description: Некоторые из системных элементов, найденных на панели управления, являются расширяемыми. Чтобы установить расширение панели управления, зарегистрируйте расширение оболочки следующим образом, где name — это предопределенное имя системного элемента (см. таблицу ниже).
title: Расширение элементов панели управления "система"
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b8b18b71-c95f-4c71-8df4-fe9342ce0165
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9b0f6628d7bc75378915c1d9f3e20327478742df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997302"
---
# <a name="extending-system-control-panel-items"></a>Расширение элементов панели управления "система"

Некоторые из системных элементов, найденных на панели управления, являются расширяемыми. Чтобы установить расширение панели управления, зарегистрируйте расширение оболочки следующим образом, где *Name* — это предопределенное имя системного элемента (см. таблицу ниже).

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Controls Folder
                  name
                     shellex
                        PropertySheetHandlers
```

Это похоже на способ регистрации расширения для предопределенного объекта оболочки. Поскольку единственными расширениями оболочки, поддерживаемыми элементами панели управления, являются страницы свойств, регистрация должна находиться в подразделе **шеллекс** \\ **пропертишисандлерс** .



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Элемент панели управления</th>
<th><em>name</em></th>
<th>Примечания</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Отображение</td>
<td>Поддержки</td>
<td>Также поддерживает замену страницы <strong>рабочего стола</strong> .
<blockquote>
[!Note]<br />
В Windows Vista эта поддержка больше не поддерживается.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Дополнительные параметры экрана</td>
<td>Устройство</td>
<td>Дополнительные свойства, не зависящие от оборудования.
<blockquote>
[!Note]<br />
В Windows Vista эта поддержка больше не поддерживается.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Дополнительные параметры экрана</td>
<td>Отображение</td>
<td>Дополнительные свойства, относящиеся к оборудованию.
<blockquote>
[!Note]<br />
В Windows Vista эта поддержка больше не поддерживается.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Свойства браузера</td>
<td>Интернет</td>
<td>Максимальное число страниц расширения — 18.</td>
</tr>
<tr class="odd">
<td>Keyboard (Клавиатура)</td>
<td>Keyboard (Клавиатура)</td>
<td>Максимальное число страниц расширения — 30.</td>
</tr>
<tr class="even">
<td>Мышь</td>
<td>Мышь</td>
<td>Также поддерживает замену стандартных страниц. Максимальное число страниц расширения — 8.</td>
</tr>
<tr class="odd">
<td>Параметры электропитания</td>
<td>Мощный</td>
<td>Максимальное число страниц, включая стандартные страницы, равно 18.</td>
</tr>
<tr class="even">
<td>Система</td>
<td>Система</td>
<td>Максимальное число страниц расширения — 8.
<blockquote>
[!Note]<br />
В Windows Vista эта поддержка больше не поддерживается.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Элемент **Установка и удаление программ** на панели управления Windows XP не является страницей свойств и поэтому не может быть расширен методами, обсуждаемыми здесь. Вместо этого его содержимое получает издательы приложений. Дополнительные сведения о добавлении содержимого для **установки и удаления программ** см. в [**разделе иапппублишер**](/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher), [**иенумпублишедаппс**](/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps)и [**ипублишедапп**](/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Элементы панели управления](control-panel-applications.md)
</dt> <dt>

[Руководство по работе пользователей](user-experience-guidelines.md)
</dt> <dt>

[Регистрация элементов панели управления](registering-control-panel-items.md)
</dt> <dt>

[Использование Кплапплет](using-cplapplet.md)
</dt> <dt>

[Обработка сообщений в панели управления](message-processing.md)
</dt> <dt>

[Исполнение элементов панели управления](executing-control-panel-items.md)
</dt> <dt>

[Назначение категорий панели управления](assigning-control-panel-categories.md)
</dt> <dt>

[Создание ссылок на задачи с возможностью поиска для элемента панели управления](creating-searchable-task-links.md)
</dt> <dt>

[Доступ к панели управления в защищенном режиме в Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




