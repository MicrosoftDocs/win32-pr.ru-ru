---
description: Приложению может потребоваться запросить имя пользователя и пароль, чтобы избежать сохранения пароля администратора или убедиться в том, что маркер имеет соответствующие привилегии.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Запрос учетных данных для пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9b9941be168a307e35b3575f4d12241dc624553686a61b232f2c5ba86e9c0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480494"
---
# <a name="asking-the-user-for-credentials"></a>Запрос учетных данных для пользователя

Приложению может потребоваться запросить имя пользователя и пароль, чтобы избежать сохранения пароля администратора или убедиться в том, что маркер имеет соответствующие привилегии.

Тем не менее, просто запрашивать учетные данные могут научить пользователей передавать их в любое случайное, неопределенное диалоговое окно, отображаемое на экране. Чтобы уменьшить этот результат обучения, рекомендуется выполнить следующую процедуру.

**Для правильного получения учетных данных пользователя**

1.  Уведомлять пользователя, используя сообщение, которое очевидно является частью приложения, в котором отображается диалоговое окно, в котором запрашиваются имя пользователя и пароль. Кроме того, можно использовать [**структуру \_ сведений CREDUI**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) для вызова [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) , чтобы передать идентифицирующие данные или сообщение.
2.  Вызовите [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa). Обратите внимание, что максимальное число символов, указанное для сведений об имени пользователя и пароле, содержит завершающий нуль символ.
3.  Вызовите [**кредуипарсеусернаме**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) и [**кредуиконфирмкредентиалс**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) , чтобы убедиться, что получены соответствующие учетные данные.

В следующем примере показано, как вызвать [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) , чтобы запросить у пользователя имя пользователя и пароль. Сначала он заполняет \_ структуру CREDUI info информацией о том, какие запросы использовать. Затем код заполняет два буфера с нулями. Это делается для того, чтобы в функцию не передавалась никакая информация, которая может раскрывать пользователю старое имя пользователя или пароль. Вызов **CredUIPromptForCredentials** открывает диалоговое окно. В целях безопасности в этом примере используется флаг CREDUI \_ Флаги \_ \_ не \_ сохраняются, чтобы операционная система не сохраняла пароль, так как он может быть открыт. Если ошибок нет, **CredUIPromptForCredentials** заполняет переменные PszName и псзпвд и возвращает ноль. Когда приложение завершит использование учетных данных, оно должно подать нули в буферах, чтобы предотвратить случайное расстановку информации.


```C++
CREDUI_INFO cui;
TCHAR pszName[CREDUI_MAX_USERNAME_LENGTH+1];
TCHAR pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1];
BOOL fSave;
DWORD dwErr;
 
cui.cbSize = sizeof(CREDUI_INFO);
cui.hwndParent = NULL;
//  Ensure that MessageText and CaptionText identify what credentials
//  to use and which application requires them.
cui.pszMessageText = TEXT("Enter administrator account information");
cui.pszCaptionText = TEXT("CredUITest");
cui.hbmBanner = NULL;
fSave = FALSE;
SecureZeroMemory(pszName, sizeof(pszName));
SecureZeroMemory(pszPwd, sizeof(pszPwd));
dwErr = CredUIPromptForCredentials( 
    &cui,                         // CREDUI_INFO structure
    TEXT("TheServer"),            // Target for credentials
                                  //   (usually a server)
    NULL,                         // Reserved
    0,                            // Reason
    pszName,                      // User name
    CREDUI_MAX_USERNAME_LENGTH+1, // Max number of char for user name
    pszPwd,                       // Password
    CREDUI_MAX_PASSWORD_LENGTH+1, // Max number of char for password
    &fSave,                       // State of save check box
    CREDUI_FLAGS_GENERIC_CREDENTIALS |  // flags
    CREDUI_FLAGS_ALWAYS_SHOW_UI |
    CREDUI_FLAGS_DO_NOT_PERSIST);  

if(!dwErr)
{
    //  Put code that uses the credentials here.
 
    //  When you have finished using the credentials,
    //  erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**кредуикмдлинепромптфоркредентиалс**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[**CREDUI \_ уинфо**](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
