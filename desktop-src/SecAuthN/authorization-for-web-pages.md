---
description: Авторизация задает, к каким ресурсам у вас есть доступ.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Авторизация для веб-страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c26e9bc8333d74d18989c5c581cc54054a29ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898302"
---
# <a name="authorization-for-web-pages"></a>Авторизация для веб-страниц

Авторизация задает, к каким ресурсам у вас есть доступ.

**Цель:** Чтобы разрешить пользователям доступ к приложению.

## <a name="prerequisites"></a>Предварительные требования

Нет

**Время на выполнение:** 2 минуты.

## <a name="instructions"></a>Инструкции

### <a name="1-authorization"></a>1. Авторизация

Когда пользователь вводит свои учетные данные и нажимает кнопку "вход", отображается страница разрешений. Эта страница лучше позволяет пользователям управлять детализированными разрешениями, предоставляя приложению доступ к данным contoso. ![Страница разрешений Contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. Использование примера

Необходимо знать следующие файлы HTML и CSS.

1.  Следующие HTML-файлы соответствуют двум страницам в потоке веб-авторизации.
    -   WebAuthLogin.html — пример HTML-кода для страницы входа
    -   WebAuthPermissions.html — пример HTML-кода для страницы разрешений
2.  Файлы CSS содержат стили Windows 8, помогающие создать веб-страницу приложения для Магазина Windows.
    -   Уи-Лигхт. CSS — она была получена из базовой таблицы стилей для элементов управления Windows 8.
    -   Уи-вебаус. CSS — обеспечивает добавочное Оформление для оптимизации макета страниц веб-аутентификации.
    -   семе-Колорс. CSS — обеспечивает добавочный стиль для переопределения контрастных цветов по умолчанию для элементов управления с цветом торговой марки поставщика.

## <a name="summary-and-next-steps"></a>Сводка и дальнейшие действия

Сводный [учебник по проверке подлинности веб-страниц](tutorial-for-authenticating-web-pages.md)

Следующие рекомендации [по проектированию веб-страниц проверки подлинности](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Рекомендации по разработке веб-страниц](considerations-for-the-web-page-development.md)
</dt> <dt>

[Пример приложения SDK брокера веб-проверки подлинности](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
