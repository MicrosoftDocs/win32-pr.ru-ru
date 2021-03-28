---
description: 'Этот раздел по типам файлов и сопоставлению файлов организован следующим образом:'
ms.assetid: 45d8b729-1e9d-40c0-8306-9a475262ac40
title: Типы файлов и сопоставления файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf84bbf44475d32768d2359d3723952ada843c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264438"
---
# <a name="file-types-and-file-associations"></a>Типы файлов и сопоставления файлов

Этот раздел по типам файлов и сопоставлению файлов организован следующим образом:

-   [Регистрация приложения](app-registration.md)
-   [Типы файлов](fa-file-types.md)
-   [Выбор расширения типа файлов](how-to-choose-a-file-type-extension.md)
-   [Определение атрибутов типа файла](how-to-define-file-type-attributes.md)
-   [Включение приложения в диалоговое окно «Открыть с помощью»](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [Исключение приложения из диалогового окна "Открыть с помощью" для несвязанных типов файлов](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)
-   [Как работают сопоставления файлов](fa-how-work.md)
-   [Представление содержимого по типу или виду файла](prophand-content-view.md)
-   [Регистрация пользовательских свойств и макета для типа файлов](how-to-register-custom-properties-and-layout-for-your-file-type.md)
-   [Средство проверки типов файлов](file-type-verifier.md)
-   [Использование средства проверки типов файлов](how-to-use-the-file-type-verifier.md)
-   [Обработчики типов файлов](fa-file-extensions.md)
-   [Программные идентификаторы](fa-progids.md)
-   [Как зарегистрировать тип файла для нового приложения](how-to-register-a-file-type-for-a-new-application.md)
-   [Наблюдаемые типы](fa-perceivedtypes.md)
-   [Массивы ассоциаций](fa-associationarray.md)

## <a name="additional-resources"></a>Дополнительные ресурсы

-   Настройка доступа к программам и параметров по умолчанию (SPAD) — это панель управления Windows, которая позволяет пользователям с правами администратора задавать значение по умолчанию для компьютера, а также скрывать или отображать приложение. Примерами приложений, зарегистрированных в SPAD, являются мультимедиа, почта, браузер, Messenger и приложения Java. Установка программ по умолчанию (SYDP) — это панель управления Windows, которая работает с ограниченными привилегиями и позволяет пользователям задавать значения по умолчанию. Любое приложение может зарегистрироваться в SYDP. Сведения о регистрации приложений в SPAD и SYDP см. в разделе [рекомендации по сопоставлению файлов и программам по умолчанию](appguide-fa-defpro.md), [настройке доступа к программам и по умолчанию для компьютеров (SPAD)](cpl-setprogramaccess.md).
-   Связанные концептуальные концепции см. в разделе [Обзор команд и сопоставлений файлов](fa-verbs.md).
-   Сведения о создании хранилища данных оболочки см. в разделе [реализация базовых интерфейсов объекта папки](nse-implement.md).

Сопутствующую справочную документацию см. в следующих разделах:

-   Инструкции по выполнению команды для элемента оболочки см. в описании метода [**инвокеверб**](folderitem-invokeverb.md) .
-   Чтобы получить коллекцию команд, которые могут быть выполнены в элементе оболочки, см. метод [**Verbs**](folderitem-verbs.md) .
-   Сведения о выполнении операции с указанным файлом см. в разделе функции [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .
-   Список распознанных типов по умолчанию см. в разделе [**воспринимаемое**](/windows/win32/api/shtypes/ne-shtypes-perceived) перечисление.
-   Чтобы получить распознанный тип файла на основе его расширения, см. раздел Функция [**ассокжетперцеиведтипе**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .

 

 



