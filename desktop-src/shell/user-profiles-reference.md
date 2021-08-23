---
description: С профилями пользователей используются следующие элементы API.
title: Справочник по профилям пользователей
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4b064eefae4916576cb8ccc6b3dfe058ea4e2e34f960315b74d384194f61ec99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967839"
---
# <a name="user-profiles-reference"></a>Справочник по профилям пользователей

С профилями пользователей используются следующие элементы API.

## <a name="functions"></a>Функции



| Компонент                                                                   | Описание                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**креатинвиронментблокк**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | Извлекает переменные среды для указанного пользователя.                                                   |
| [**креатепрофиле**](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | Создает новый профиль пользователя. (только Windows Vista и более поздних версий.)                                                   |
| [**делетепрофиле**](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | Удаляет профиль пользователя и все параметры, связанные с пользователем, с указанного компьютера.                           |
| [**дестройенвиронментблокк**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | Освобождает переменные среды, созданные функцией [**креатинвиронментблокк**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) . |
| [**експанденвиронментстрингсфорусер**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | Развертывает исходную строку с помощью блока среды, установленного для указанного пользователя.                  |
| [**жеталлусерспрофиледиректори**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | Возвращает путь к корню профиля всех пользователей.                                                      |
| [**жетдефаултусерпрофиледиректори**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | Возвращает путь к корню профиля пользователя по умолчанию.                                                   |
| [**жетпрофилесдиректори**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | Возвращает путь к корневому каталогу, в котором хранятся все профили пользователей.                                  |
| [**жетпрофилетипе**](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | Возвращает тип профиля, загруженного для текущего пользователя.                                                    |
| [**жетусерпрофиледиректори**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | Возвращает путь к корневому каталогу указанного профиля пользователя.                                     |
| [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | Загружает профиль указанного пользователя.                                                                           |
| [**унлоадусерпрофиле**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | Выгружает профиль пользователя, который был загружен функцией [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .          |



 

Функция [**креатеусерпрофиликс**](createuserprofileex.md) не поддерживается.

## <a name="structures"></a>Структуры



| Структура                          | Описание                                |
|------------------------------------|--------------------------------------------|
| [**FILEINFO**](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | Содержит сведения о профиле пользователя. |



 

 

 



