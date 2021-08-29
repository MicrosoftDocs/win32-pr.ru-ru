---
description: с многоязычный пользовательский интерфейс (MUI) используются следующие функции.
ms.assetid: 918d1f04-78fe-4b60-bee7-08d2f131437e
title: многоязычный пользовательский интерфейс Функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507118ce04895c9b13f5c9d71fae69717a38e2d74186159fb2efcef7f45a0c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041224"
---
# <a name="multilingual-user-interface-functions"></a>многоязычный пользовательский интерфейс Функции

с многоязычный пользовательский интерфейс (MUI) используются следующие функции.



| Функция                                                                 | Описание                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**енумуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa)                               | Перечисляет языки пользовательского интерфейса, доступные в операционной системе.                                     |
| [**EnumUILanguagesProc**](/windows/win32/api/winnls/nc-winnls-uilanguage_enumproca)                       | Определяемая приложением функция, используемая с функцией [**енумуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .                      |
| [**фримуилибрари**](/windows/desktop/api/Muiload/nf-muiload-freemuilibrary)                                 | Уменьшает значение счетчика ссылок для модуля ресурсов, загруженного с помощью [ **лоадмуилибрари**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                  |
| [**жетфилемуиинфо**](/windows/desktop/api/Winnls/nf-winnls-getfilemuiinfo)                                 | Извлекает сведения о ресурсах для файла.                                                                    |
| [**жетфилемуипас**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)                                 | Извлекает путь к файлу ресурсов, связанному с конкретным языком, связанный с указанным LN-файлом.                           |
| [**жетпроцесспреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages) | Извлекает предпочтительные языки пользовательского интерфейса для процесса.                                                                           |
| [**жетсистемдефаултуилангуаже**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)         | возвращает идентификатор языка пользовательского интерфейса системы по умолчанию, известный как "язык установки" в Windows Vista. |
| [**жетсистемпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)   | Извлекает предпочтительные для системы языки пользовательского интерфейса.                                                                            |
| [**жетсреадпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)   | Возвращает предпочтительный для потока язык пользовательского интерфейса для текущего потока.                                                     |
| [**жетсреадуилангуаже**](/windows/desktop/api/Winnls/nf-winnls-getthreaduilanguage)                       | Возвращает идентификатор языка первого языка интерфейса пользователя для текущего потока.                            |
| [**жетуилангуажефаллбакклист**](/windows/desktop/api/Muiload/nf-muiload-getuilanguagefallbacklist)           | Возвращает резервный список языков пользовательского интерфейса, представленных в виде имен языков.                                         |
| [**жетуилангуажеинфо**](/windows/desktop/api/Winnls/nf-winnls-getuilanguageinfo)                           | Извлекает разнообразные сведения о языке пользовательского интерфейса.                                                     |
| [**жетусердефаултуилангуаже**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage)             | Возвращает идентификатор языка пользовательского интерфейса для текущего пользователя.                                          |
| [**жетусерпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)       | Получает предпочитаемый пользователем язык пользовательского интерфейса.                                                                              |
| [**лоадмуилибрари**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)                                 | Возвращает маркер зависящих от языка ресурсов, связанных с определенным языком (LN) файлом.            |
| [**сетпроцесспреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) | Задает предпочтительные языки интерфейса для процесса приложения.                                                    |
| [**сетсреадпреферредуилангуажес**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)   | Задает предпочтительный язык пользовательского интерфейса для потока.                                                                                 |
| [**сетсреадуилангуаже**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage)                       | Задает предпочтительный язык пользовательского интерфейса для текущего потока.                                                      |



 

 

 
