---
title: Класс Ксекуречаннелклиент
description: Класс Ксекуречаннелклиент
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Диспетчер устройств Windows Media, класс Ксекуречаннелклиент
- Диспетчер устройств, класс Ксекуречаннелклиент
- Классические приложения, класс Ксекуречаннелклиент
- Справочник по программированию, класс Ксекуречаннелклиент
- Справочник по диспетчер устройств Windows Media, класс Ксекуречаннелклиент
- Класс Ксекуречаннелклиент
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691540"
---
# <a name="csecurechannelclient-class"></a><span data-ttu-id="8c97f-109">Класс Ксекуречаннелклиент</span><span class="sxs-lookup"><span data-stu-id="8c97f-109">CSecureChannelClient Class</span></span>

<span data-ttu-id="8c97f-110">Класс **ксекуречаннелклиент** является вспомогательным классом (не интерфейсом), который позволяет приложениям проходить проверку подлинности, шифровать и расшифровывать данные, а также создавать компьютеры Макинтош.</span><span class="sxs-lookup"><span data-stu-id="8c97f-110">The **CSecureChannelClient** class is a helper class (not an interface) that enables applications to authenticate themselves, encrypt and decrypt data, and create MACs.</span></span>

<span data-ttu-id="8c97f-111">Класс **ксекуречаннелклиент** предоставляет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8c97f-111">The **CSecureChannelClient** class exposes the following methods.</span></span>



| <span data-ttu-id="8c97f-112">Метод</span><span class="sxs-lookup"><span data-stu-id="8c97f-112">Method</span></span>                                                            | <span data-ttu-id="8c97f-113">Описание</span><span class="sxs-lookup"><span data-stu-id="8c97f-113">Description</span></span>                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c97f-114">[**Хождения**](/previous-versions/ms983906(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8c97f-114">[**Authenticate**](/previous-versions/ms983906(v=msdn.10))</span></span>         | <span data-ttu-id="8c97f-115">Активирует обмен сертификатами между компонентами для установления отношения доверия.</span><span class="sxs-lookup"><span data-stu-id="8c97f-115">Triggers the exchange of certificates between components to establish trust.</span></span>                                              |
| <span data-ttu-id="8c97f-116">[**декриптпарам**](/previous-versions/bb231586(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c97f-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span></span>         | <span data-ttu-id="8c97f-117">Расшифровывает данные, полученные с помощью параметра.</span><span class="sxs-lookup"><span data-stu-id="8c97f-117">Decrypts data received through a parameter.</span></span>                                                                               |
| <span data-ttu-id="8c97f-118">[**енкриптпарам**](/previous-versions/bb231587(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c97f-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span></span>         | <span data-ttu-id="8c97f-119">Шифрует данные, отправляемые через параметр.</span><span class="sxs-lookup"><span data-stu-id="8c97f-119">Encrypts data being sent out through a parameter.</span></span>                                                                         |
| <span data-ttu-id="8c97f-120">[**фисаусентикатед**](/previous-versions/ms868497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8c97f-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span></span> | <span data-ttu-id="8c97f-121">Проверяет, успешно ли установлен безопасный канал проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8c97f-121">Verifies that a secure authentication channel has been successfully established.</span></span> <span data-ttu-id="8c97f-122">Этот метод не используется приложениями.</span><span class="sxs-lookup"><span data-stu-id="8c97f-122">This method is not used by applications.</span></span> |
| <span data-ttu-id="8c97f-123">[**жетаппсек**](/previous-versions/ms868498(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8c97f-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span></span>               | <span data-ttu-id="8c97f-124">Извлекает уровни безопасности приложения для локальных и удаленных компонентов.</span><span class="sxs-lookup"><span data-stu-id="8c97f-124">Retrieves the application security levels of the local and remote components.</span></span>                                             |
| <span data-ttu-id="8c97f-125">[**жетсессионкэй**](/previous-versions/bb231590(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c97f-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span></span>       | <span data-ttu-id="8c97f-126">Извлекает текущий ключ сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c97f-126">Retrieves the current session key.</span></span> <span data-ttu-id="8c97f-127">Этот метод не используется приложениями.</span><span class="sxs-lookup"><span data-stu-id="8c97f-127">This method is not used by applications.</span></span>                                               |
| <span data-ttu-id="8c97f-128">[**макфинал**](/previous-versions/bb231591(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c97f-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span></span>                 | <span data-ttu-id="8c97f-129">Освобождает канал кода проверки подлинности сообщений (MAC) и получает конечное значение MAC.</span><span class="sxs-lookup"><span data-stu-id="8c97f-129">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>                                   |
| <span data-ttu-id="8c97f-130">[**маЦинит**](/previous-versions/bb231592(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c97f-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span></span>                   | <span data-ttu-id="8c97f-131">Получает канал кода проверки подлинности сообщений (MAC).</span><span class="sxs-lookup"><span data-stu-id="8c97f-131">Acquires a message authentication code (MAC) channel.</span></span>                                                                     |
| <span data-ttu-id="8c97f-132">[**макупдате**](/previous-versions/bb231593(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c97f-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span></span>               | <span data-ttu-id="8c97f-133">Добавляет значение в код проверки подлинности сообщения (MAC).</span><span class="sxs-lookup"><span data-stu-id="8c97f-133">Adds a value to a message authentication code (MAC).</span></span>                                                                      |
| <span data-ttu-id="8c97f-134">[**сетцертификате**](/previous-versions/ms868504(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8c97f-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span></span>     | <span data-ttu-id="8c97f-135">Указывает сертификат и закрытый ключ клиента безопасного канала с проверкой подлинности (SAC).</span><span class="sxs-lookup"><span data-stu-id="8c97f-135">Specifies the certificate and private key of the secure authenticated channel (SAC) client.</span></span>                               |
| <span data-ttu-id="8c97f-136">[**сетинтерфаце**](/previous-versions/bb231595(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c97f-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span></span>         | <span data-ttu-id="8c97f-137">Выбирает интерфейс, используемый для обмена данными по безопасному каналу с проверкой подлинности (SAC).</span><span class="sxs-lookup"><span data-stu-id="8c97f-137">Selects the interface used for secure authenticated channel (SAC) communications.</span></span>                                         |
| <span data-ttu-id="8c97f-138">[**сетсессионкэй**](/previous-versions/ms868506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8c97f-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span></span>       | <span data-ttu-id="8c97f-139">Задает ключ сеанса, используемый для взаимодействия с другим компонентом.</span><span class="sxs-lookup"><span data-stu-id="8c97f-139">Sets the session key that is used to communicate with another component.</span></span> <span data-ttu-id="8c97f-140">Этот метод не используется приложениями.</span><span class="sxs-lookup"><span data-stu-id="8c97f-140">This method is not used by applications.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="8c97f-141">См. также</span><span class="sxs-lookup"><span data-stu-id="8c97f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c97f-142">**Класс Ксекуречаннелсервер**</span><span class="sxs-lookup"><span data-stu-id="8c97f-142">**CSecureChannelServer Class**</span></span>](csecurechannelserver-class.md)
</dt> <dt>

[<span data-ttu-id="8c97f-143">**Интерфейс Икомпонентаусентикате**</span><span class="sxs-lookup"><span data-stu-id="8c97f-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="8c97f-144">**Интерфейсы для приложений**</span><span class="sxs-lookup"><span data-stu-id="8c97f-144">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> </dl>

 

 