---
title: Класс Ксекуречаннелсервер
description: Класс Ксекуречаннелсервер
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Диспетчер устройств Windows Media, класс Ксекуречаннелсервер
- Диспетчер устройств, класс Ксекуречаннелсервер
- поставщики услуг, класс Ксекуречаннелсервер
- Справочник по программированию, класс Ксекуречаннелсервер
- Справочник по диспетчер устройств Windows Media, класс Ксекуречаннелсервер
- Класс Ксекуречаннелсервер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792060"
---
# <a name="csecurechannelserver-class"></a><span data-ttu-id="a964b-109">Класс Ксекуречаннелсервер</span><span class="sxs-lookup"><span data-stu-id="a964b-109">CSecureChannelServer Class</span></span>

<span data-ttu-id="a964b-110">Класс **ксекуречаннелсервер** является вспомогательным классом (не интерфейсом), который позволяет поставщику услуг или безопасному поставщику содержимого проверять подлинность приложения с помощью интерфейса [**икомпонентаусентикате**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) , для шифрования и расшифровки данных, а также для создания подписей Mac.</span><span class="sxs-lookup"><span data-stu-id="a964b-110">The **CSecureChannelServer** class is a helper class (not an interface) that enables a service provider or secure content provider to authenticate an application using the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface, to encrypt and decrypt data, and to create MAC signatures.</span></span> <span data-ttu-id="a964b-111">Для процесса проверки подлинности требуется, чтобы приложение создает объект **ксекуречаннелклиент** , а поставщик услуг создает объект **ксекуречаннелсервер** .</span><span class="sxs-lookup"><span data-stu-id="a964b-111">The authentication process requires that the application create a **CSecureChannelClient** object and that the service provider create a **CSecureChannelServer** object.</span></span> <span data-ttu-id="a964b-112">Классы **ксекуречаннелклиент** и **ксекуречаннелсервер** объявляются в библиотеке статической компоновки мссачлп. lib.</span><span class="sxs-lookup"><span data-stu-id="a964b-112">The **CSecureChannelClient** and **CSecureChannelServer** classes are declared in the static link library, Mssachlp.lib.</span></span> <span data-ttu-id="a964b-113">Все методы диспетчер устройств Windows Media, поставщика услуг и интерфейсов безопасного содержимого могут возвращать ВМДМ \_ E \_ нотцертифиед, чтобы указать, что вызывающий объект не прошел проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="a964b-113">All methods of Windows Media Device Manager, service provider, and secure content provider interfaces can return WMDM\_E\_NOTCERTIFIED to indicate that the caller has not authenticated successfully.</span></span>

<span data-ttu-id="a964b-114">Класс **ксекуречаннелсервер** предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a964b-114">The **CSecureChannelServer** class exposes the following methods.</span></span>



| <span data-ttu-id="a964b-115">Метод</span><span class="sxs-lookup"><span data-stu-id="a964b-115">Method</span></span>                                                            | <span data-ttu-id="a964b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a964b-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a964b-117">[**декриптпарам**](/previous-versions/bb231598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a964b-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span></span>         | <span data-ttu-id="a964b-118">Расшифровывает данные, содержащиеся в параметре.</span><span class="sxs-lookup"><span data-stu-id="a964b-118">Decrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="a964b-119">[**енкриптпарам**](/previous-versions/ms868509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a964b-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span></span>         | <span data-ttu-id="a964b-120">Шифрует данные, содержащиеся в параметре.</span><span class="sxs-lookup"><span data-stu-id="a964b-120">Encrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="a964b-121">[**фисаусентикатед**](/previous-versions/bb231600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a964b-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span></span> | <span data-ttu-id="a964b-122">Проверяет, успешно ли установлен безопасный канал проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a964b-122">Verifies that a secure authentication channel has been successfully established.</span></span>            |
| <span data-ttu-id="a964b-123">[**жетаппсек**](/previous-versions/bb231601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a964b-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span></span>               | <span data-ttu-id="a964b-124">Извлекает уровни безопасности приложения для локальных и удаленных компонентов.</span><span class="sxs-lookup"><span data-stu-id="a964b-124">Retrieves the application security levels of the local and remote components.</span></span>               |
| <span data-ttu-id="a964b-125">[**жетсессионкэй**](/previous-versions/bb231602(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a964b-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span></span>       | <span data-ttu-id="a964b-126">Извлекает текущий ключ сеанса.</span><span class="sxs-lookup"><span data-stu-id="a964b-126">Retrieves the current session key.</span></span>                                                          |
| <span data-ttu-id="a964b-127">[**макфинал**](/previous-versions/ms868513(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a964b-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span></span>                 | <span data-ttu-id="a964b-128">Освобождает канал кода проверки подлинности сообщений (MAC) и получает конечное значение MAC.</span><span class="sxs-lookup"><span data-stu-id="a964b-128">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>     |
| <span data-ttu-id="a964b-129">[**маЦинит**](/previous-versions/ms868514(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a964b-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span></span>                   | <span data-ttu-id="a964b-130">Получает канал кода проверки подлинности сообщений (MAC).</span><span class="sxs-lookup"><span data-stu-id="a964b-130">Acquires a message authentication code (MAC) channel.</span></span>                                       |
| <span data-ttu-id="a964b-131">[**макупдате**](/previous-versions/ms868515(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a964b-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span></span>               | <span data-ttu-id="a964b-132">Обновляет значение кода проверки подлинности сообщения (MAC) значением параметра.</span><span class="sxs-lookup"><span data-stu-id="a964b-132">Updates the message authentication code (MAC) value with a parameter value.</span></span>                 |
| <span data-ttu-id="a964b-133">[**сакаус**](/previous-versions/ms868516(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a964b-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span></span>                   | <span data-ttu-id="a964b-134">Устанавливает безопасный канал с проверкой подлинности между компонентами.</span><span class="sxs-lookup"><span data-stu-id="a964b-134">Establishes a secure authenticated channel between components.</span></span>                              |
| <span data-ttu-id="a964b-135">[**сакжетпротоколс**](/previous-versions/ms868517(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a964b-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span></span>   | <span data-ttu-id="a964b-136">Сообщает о протоколах, поддерживаемых компонентом.</span><span class="sxs-lookup"><span data-stu-id="a964b-136">Reports the protocols supported by a component.</span></span>                                             |
| <span data-ttu-id="a964b-137">[**сетцертификате**](/previous-versions/ms868518(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a964b-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span></span>     | <span data-ttu-id="a964b-138">Указывает сертификат и закрытый ключ сервера защищенного канала (SAC).</span><span class="sxs-lookup"><span data-stu-id="a964b-138">Specifies the certificate and private key of the secure authenticated channel (SAC) server.</span></span> |
| <span data-ttu-id="a964b-139">[**сетсессионкэй**](/previous-versions/ms868519(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a964b-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span></span>       | <span data-ttu-id="a964b-140">Задает ключ сеанса, используемый для взаимодействия с другим компонентом.</span><span class="sxs-lookup"><span data-stu-id="a964b-140">Sets the session key that is used to communicate with another component.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="a964b-141">См. также</span><span class="sxs-lookup"><span data-stu-id="a964b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a964b-142">**Класс Ксекуречаннелклиент**</span><span class="sxs-lookup"><span data-stu-id="a964b-142">**CSecureChannelClient Class**</span></span>](csecurechannelclient-class.md)
</dt> <dt>

[<span data-ttu-id="a964b-143">**Интерфейс Икомпонентаусентикате**</span><span class="sxs-lookup"><span data-stu-id="a964b-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="a964b-144">**Интерфейсы для поставщиков услуг**</span><span class="sxs-lookup"><span data-stu-id="a964b-144">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> <dt>

[<span data-ttu-id="a964b-145">**Использование защищенных каналов с проверкой подлинности**</span><span class="sxs-lookup"><span data-stu-id="a964b-145">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 