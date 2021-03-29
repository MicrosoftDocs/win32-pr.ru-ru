---
description: Приложению может потребоваться запросить имя пользователя и пароль, чтобы избежать сохранения пароля администратора или убедиться в том, что маркер имеет соответствующие привилегии.
ms.assetid: 966de0cc-63de-4430-843f-668de2dfe0a6
title: Запрос учетных данных для пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adb315837d86a9f1dda4075b8d89db33f0dd22e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664140"
---
# <a name="asking-the-user-for-credentials"></a><span data-ttu-id="2e233-103">Запрос учетных данных для пользователя</span><span class="sxs-lookup"><span data-stu-id="2e233-103">Asking the User for Credentials</span></span>

<span data-ttu-id="2e233-104">Приложению может потребоваться запросить имя пользователя и пароль, чтобы избежать сохранения пароля администратора или убедиться в том, что маркер имеет соответствующие привилегии.</span><span class="sxs-lookup"><span data-stu-id="2e233-104">Your application may need to prompt the user for user name and password information to avoid storing an administrator password or to verify that the token holds the appropriate privileges.</span></span>

<span data-ttu-id="2e233-105">Тем не менее, просто запрашивать учетные данные могут научить пользователей передавать их в любое случайное, неопределенное диалоговое окно, отображаемое на экране.</span><span class="sxs-lookup"><span data-stu-id="2e233-105">However, simply prompting for credentials may train users to supply those to any random, unidentified dialog box that appears on the screen.</span></span> <span data-ttu-id="2e233-106">Чтобы уменьшить этот результат обучения, рекомендуется выполнить следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="2e233-106">The following procedure is recommended to reduce that training effect.</span></span>

<span data-ttu-id="2e233-107">**Для правильного получения учетных данных пользователя**</span><span class="sxs-lookup"><span data-stu-id="2e233-107">**To properly acquire user credentials**</span></span>

1.  <span data-ttu-id="2e233-108">Уведомлять пользователя, используя сообщение, которое очевидно является частью приложения, в котором отображается диалоговое окно, в котором запрашиваются имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="2e233-108">Inform the user, by using a message that is clearly part of your application, that they will see a dialog box that requests their user name and password.</span></span> <span data-ttu-id="2e233-109">Кроме того, можно использовать [**структуру \_ сведений CREDUI**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) для вызова [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) , чтобы передать идентифицирующие данные или сообщение.</span><span class="sxs-lookup"><span data-stu-id="2e233-109">You can also use the [**CREDUI\_INFO**](/windows/desktop/api/wincred/ns-wincred-credui_infoa) structure on the call to [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to convey identifying data or a message.</span></span>
2.  <span data-ttu-id="2e233-110">Вызовите [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span><span class="sxs-lookup"><span data-stu-id="2e233-110">Call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).</span></span> <span data-ttu-id="2e233-111">Обратите внимание, что максимальное число символов, указанное для сведений об имени пользователя и пароле, содержит завершающий нуль символ.</span><span class="sxs-lookup"><span data-stu-id="2e233-111">Note that the maximum number of characters specified for user name and password information includes the terminating null character.</span></span>
3.  <span data-ttu-id="2e233-112">Вызовите [**кредуипарсеусернаме**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) и [**кредуиконфирмкредентиалс**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) , чтобы убедиться, что получены соответствующие учетные данные.</span><span class="sxs-lookup"><span data-stu-id="2e233-112">Call [**CredUIParseUserName**](/windows/desktop/api/wincred/nf-wincred-creduiparseusernamea) and [**CredUIConfirmCredentials**](/windows/desktop/api/wincred/nf-wincred-creduiconfirmcredentialsa) to verify that you obtained appropriate credentials.</span></span>

<span data-ttu-id="2e233-113">В следующем примере показано, как вызвать [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) , чтобы запросить у пользователя имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="2e233-113">The following example shows how to call [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) to ask the user for a user name and password.</span></span> <span data-ttu-id="2e233-114">Сначала он заполняет \_ структуру CREDUI info информацией о том, какие запросы использовать.</span><span class="sxs-lookup"><span data-stu-id="2e233-114">It begins by filling in a CREDUI\_INFO structure with information about what prompts to use.</span></span> <span data-ttu-id="2e233-115">Затем код заполняет два буфера с нулями.</span><span class="sxs-lookup"><span data-stu-id="2e233-115">Next, the code fills two buffers with zeros.</span></span> <span data-ttu-id="2e233-116">Это делается для того, чтобы в функцию не передавалась никакая информация, которая может раскрывать пользователю старое имя пользователя или пароль.</span><span class="sxs-lookup"><span data-stu-id="2e233-116">This is done to ensure that no information gets passed to the function that might reveal an old user name or password to the user.</span></span> <span data-ttu-id="2e233-117">Вызов **CredUIPromptForCredentials** открывает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="2e233-117">The call to **CredUIPromptForCredentials** brings up the dialog box.</span></span> <span data-ttu-id="2e233-118">В целях безопасности в этом примере используется флаг CREDUI \_ Флаги \_ \_ не \_ сохраняются, чтобы операционная система не сохраняла пароль, так как он может быть открыт.</span><span class="sxs-lookup"><span data-stu-id="2e233-118">For security reasons, this example uses the CREDUI\_FLAGS\_DO\_NOT\_PERSIST flag to prevent the operating system from storing the password because it might then be exposed.</span></span> <span data-ttu-id="2e233-119">Если ошибок нет, **CredUIPromptForCredentials** заполняет переменные PszName и псзпвд и возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="2e233-119">If there are no errors, **CredUIPromptForCredentials** fills in the pszName and pszPwd variables and returns zero.</span></span> <span data-ttu-id="2e233-120">Когда приложение завершит использование учетных данных, оно должно подать нули в буферах, чтобы предотвратить случайное расстановку информации.</span><span class="sxs-lookup"><span data-stu-id="2e233-120">When the application has finished using the credentials, it should put zeros in the buffers to prevent the information from being accidentally revealed.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2e233-121">См. также</span><span class="sxs-lookup"><span data-stu-id="2e233-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e233-122">**кредуикмдлинепромптфоркредентиалс**</span><span class="sxs-lookup"><span data-stu-id="2e233-122">**CredUICmdLinePromptForCredentials**</span></span>](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa)
</dt> <dt>

[<span data-ttu-id="2e233-123">**CREDUI \_ уинфо**</span><span class="sxs-lookup"><span data-stu-id="2e233-123">**CREDUI\_UINFO**</span></span>](/windows/desktop/api/wincred/ns-wincred-credui_infoa)
</dt> </dl>

 

 
