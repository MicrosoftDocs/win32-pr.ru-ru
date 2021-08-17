---
description: Авторизация задает, к каким ресурсам у вас есть доступ.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Авторизация для веб-страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4f64cbbf3dd9ac38a13719cd8835a198f1fbb3b522e8ac368ffaf4e759fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141335"
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
2.  файлы CSS содержат Windows 8 стили, помогающие создать веб-страницу приложения для хранения Windows.
    -   уи-лигхт. css — она была получена из базовой таблицы стилей для Windows 8 элементов управления.
    -   Уи-вебаус. CSS — обеспечивает добавочное Оформление для оптимизации макета страниц веб-аутентификации.
    -   семе-Колорс. CSS — обеспечивает добавочный стиль для переопределения контрастных цветов по умолчанию для элементов управления с цветом торговой марки поставщика.

## <a name="summary-and-next-steps"></a>Сводка и дальнейшие действия

Сводный [учебник по проверке подлинности веб-страниц](tutorial-for-authenticating-web-pages.md)

Следующие рекомендации [по проектированию веб-страниц проверки подлинности](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Рекомендации по разработке веб-страниц](considerations-for-the-web-page-development.md)
</dt> <dt>

[Пример приложения SDK брокера веб-проверки подлинности](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
