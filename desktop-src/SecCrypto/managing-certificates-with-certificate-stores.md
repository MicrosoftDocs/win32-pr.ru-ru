---
description: Использование функций CryptoAPI для управления хранилищами сертификатов и сертификатами, списками отзыва сертификатов и списками доверия сертификатов в этих магазинах.
ms.assetid: 6a56c355-8f24-41cc-88d9-2a02d9863ccf
title: Управление сертификатами с помощью хранилищ сертификатов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98abb2b612f77db3f1c59e53fb9c7bf0f34cefb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552345"
---
# <a name="managing-certificates-with-certificate-stores"></a><span data-ttu-id="66845-103">Управление сертификатами с помощью хранилищ сертификатов</span><span class="sxs-lookup"><span data-stu-id="66845-103">Managing Certificates with Certificate Stores</span></span>

<span data-ttu-id="66845-104">В течение определенного периода времени [*Сертификаты*](../secgloss/c-gly.md) будут накапливаться на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="66845-104">Over a period of time, [*certificates*](../secgloss/c-gly.md) will accumulate on a user's computer.</span></span> <span data-ttu-id="66845-105">Для управления этими сертификатами требуются средства.</span><span class="sxs-lookup"><span data-stu-id="66845-105">Tools are required to manage these certificates.</span></span> <span data-ttu-id="66845-106">Интерфейс [*CryptoAPI*](../secgloss/c-gly.md) предоставляет эти средства как функции для хранения, извлечения, удаления, перечисления и проверки сертификатов.</span><span class="sxs-lookup"><span data-stu-id="66845-106">[*CryptoAPI*](../secgloss/c-gly.md) provides those tools as functions to store, retrieve, delete, list (enumerate), and verify certificates.</span></span> <span data-ttu-id="66845-107">CryptoAPI также предоставляет средства для присоединения сертификатов к сообщениям.</span><span class="sxs-lookup"><span data-stu-id="66845-107">CryptoAPI also provides the means to attach certificates to messages.</span></span>

<span data-ttu-id="66845-108">CryptoAPI предлагает две основные категории функций для управления сертификатами: функции, управляющие [*хранилищами сертификатов*](../secgloss/c-gly.md), и функции, которые работают с сертификатами, [*списками отзыва сертификатов*](../secgloss/c-gly.md) (CRL) и [*списками доверия сертификатов*](../secgloss/c-gly.md) (CTL) в этих магазинах.</span><span class="sxs-lookup"><span data-stu-id="66845-108">CryptoAPI offers two main categories of functions for managing certificates: functions that manage [*certificate stores*](../secgloss/c-gly.md), and functions that work with the certificates, [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) within those stores.</span></span>

<span data-ttu-id="66845-109">Функции, управляющие [*хранилищами сертификатов*](../secgloss/c-gly.md) , включают функции для работы с логическими или [*виртуальными хранилищами*](../secgloss/v-gly.md), [*удаленными*](../secgloss/r-gly.md)хранилищами, [*внешними хранилищами*](../secgloss/e-gly.md)и хранилищами, которые могут быть перемещены.</span><span class="sxs-lookup"><span data-stu-id="66845-109">The functions that manage [*certificate stores*](../secgloss/c-gly.md) include functions for working with logical or [*virtual stores*](../secgloss/v-gly.md), [*remote stores*](../secgloss/r-gly.md), [*external stores*](../secgloss/e-gly.md), and stores that can be relocated.</span></span>

<span data-ttu-id="66845-110">Сертификаты, [*списки отзыва*](../secgloss/c-gly.md)сертификатов и [*списки CTL*](../secgloss/c-gly.md) можно хранить и поддерживать в [*хранилищах сертификатов*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="66845-110">Certificates, [*CRLs*](../secgloss/c-gly.md), and [*CTLs*](../secgloss/c-gly.md) can be kept and maintained in [*certificate stores*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="66845-111">Их можно получить из магазина, в котором они были сохранены для использования в процессах проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="66845-111">They can be retrieved from a store where they have been persisted for use in authentication processes.</span></span>

<span data-ttu-id="66845-112">[*Хранилище сертификатов*](../secgloss/c-gly.md) является центральным для всех функций сертификатов.</span><span class="sxs-lookup"><span data-stu-id="66845-112">The [*certificate store*](../secgloss/c-gly.md) is central to all certificate functionality.</span></span> <span data-ttu-id="66845-113">Управление сертификатами осуществляется в хранилище с помощью функций с префиксом "CERT".</span><span class="sxs-lookup"><span data-stu-id="66845-113">The certificates are managed in the store using functions with a "Cert" prefix.</span></span> <span data-ttu-id="66845-114">Типичным хранилищем сертификатов является связанный список [*сертификатов*](../secgloss/c-gly.md) , как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="66845-114">A typical certificate store is a linked list of [*certificates*](../secgloss/c-gly.md) as shown in the following illustration.</span></span>

![хранилище сертификатов](images/certstore1.png)

<span data-ttu-id="66845-116">На предыдущем рисунке показана:</span><span class="sxs-lookup"><span data-stu-id="66845-116">The preceding illustration shows:</span></span>

-   <span data-ttu-id="66845-117">Каждое [*хранилище сертификатов*](../secgloss/c-gly.md) имеет указатель на первый блок сертификата в этом хранилище.</span><span class="sxs-lookup"><span data-stu-id="66845-117">Each [*certificate store*](../secgloss/c-gly.md) has a pointer to the first certificate block in that store.</span></span>
-   <span data-ttu-id="66845-118">Блок сертификата включает указатель на данные этого сертификата и указатель "Далее" на следующий блок сертификата в хранилище.</span><span class="sxs-lookup"><span data-stu-id="66845-118">A certificate block includes a pointer to that certificate's data and a "next" pointer to the next certificate block in the store.</span></span>
-   <span data-ttu-id="66845-119">Указатель "Далее" в последнем блоке сертификата имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="66845-119">The "next" pointer in the last certificate block is set to **NULL**.</span></span>
-   <span data-ttu-id="66845-120">Блок данных сертификата содержит контекст сертификата только для чтения и все расширенные свойства сертификата.</span><span class="sxs-lookup"><span data-stu-id="66845-120">The data block of a certificate contains the read-only certificate context and any extended properties of the certificate.</span></span>
-   <span data-ttu-id="66845-121">Блок данных каждого сертификата содержит [*счетчик ссылок*](../secgloss/r-gly.md) , который отслеживает количество указателей на существующий сертификат.</span><span class="sxs-lookup"><span data-stu-id="66845-121">The data block of each certificate contains a [*reference count*](../secgloss/r-gly.md) that keeps track of the number of pointers to the certificate that exist.</span></span>

<span data-ttu-id="66845-122">Сертификаты в [*хранилище сертификатов*](../secgloss/c-gly.md) обычно хранятся в определенном постоянном хранилище, таком как файл на диске или системный реестр.</span><span class="sxs-lookup"><span data-stu-id="66845-122">Certificates in a [*certificate store*](../secgloss/c-gly.md) are normally kept in some kind of permanent storage such as a disk file or the system registry.</span></span> <span data-ttu-id="66845-123">Хранилища сертификатов также можно создавать и открывать строго в памяти.</span><span class="sxs-lookup"><span data-stu-id="66845-123">Certificate stores can also be created and opened strictly in memory.</span></span> <span data-ttu-id="66845-124">Хранилище памяти предоставляет временное хранилище сертификатов для работы с сертификатами, которые не нужно хранить.</span><span class="sxs-lookup"><span data-stu-id="66845-124">A memory store provides temporary certificate storage for working with certificates that do not need to be kept.</span></span>

<span data-ttu-id="66845-125">Дополнительные расположения магазинов позволяют сохранять и искать Магазины в различных частях реестра локального компьютера или с соответствующими наборами разрешений в реестре на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="66845-125">Additional store locations allow stores to be kept and searched in various parts of a local computer's registry or, with proper permissions set, in the registry on a remote computer.</span></span>

<span data-ttu-id="66845-126">У каждого пользователя есть личное хранилище My Store, в котором хранятся сертификаты этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="66845-126">Each user has a personal My store where that user's certificates are stored.</span></span> <span data-ttu-id="66845-127">Хранилище My может находиться в любом из нескольких физических расположений, включая реестр на локальном или удаленном компьютере, файл на диске, базу данных, службу каталогов, [*смарт-карту*](../secgloss/s-gly.md)или другое расположение.</span><span class="sxs-lookup"><span data-stu-id="66845-127">The My store can be at any one of many physical locations, including the registry on a local or remote computer, a disk file, a database, directory service, a [*smart card*](../secgloss/s-gly.md), or another location.</span></span> <span data-ttu-id="66845-128">Хотя любой сертификат может храниться в хранилище My, это хранилище должно быть зарезервировано для персональных сертификатов пользователя: сертификаты, используемые для подписывания и расшифровки сообщений этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="66845-128">While any certificate can be stored in the My store, this store should be reserved for a user's personal certificates: those certificates used for signing and decrypting that user's messages.</span></span>

<span data-ttu-id="66845-129">Использование сертификатов для проверки подлинности зависит от наличия сертификатов, выданных издателем доверенных сертификатов.</span><span class="sxs-lookup"><span data-stu-id="66845-129">Using certificates for authentication depends on having certificates issued by some trusted certificate issuer.</span></span> <span data-ttu-id="66845-130">Сертификаты для издателей доверенных сертификатов обычно хранятся в корневом хранилище, которое в настоящее время хранится в подразделе реестра.</span><span class="sxs-lookup"><span data-stu-id="66845-130">Certificates for trusted certificate issuers are typically kept in the Root store, which is currently persisted to a registry subkey.</span></span> <span data-ttu-id="66845-131">В контексте CryptoAPI защищено корневое хранилище, а диалоговые окна пользовательского интерфейса напоминают пользователю о необходимости поместить в это хранилище только доверенные сертификаты.</span><span class="sxs-lookup"><span data-stu-id="66845-131">In the CryptoAPI context, the Root store is protected, and user interface dialog boxes remind the user to place only trusted certificates into that store.</span></span> <span data-ttu-id="66845-132">В случае корпоративной сети сертификаты могут быть отправлены (скопированы) системным администратором с компьютера контроллера домена в корневые хранилища на клиентских компьютерах.</span><span class="sxs-lookup"><span data-stu-id="66845-132">In enterprise network situations, certificates might be pushed (copied) by a system administrator from the domain controller computer to the Root stores on client computers.</span></span> <span data-ttu-id="66845-133">Этот процесс предоставляет все члены домена с аналогичными списками доверия.</span><span class="sxs-lookup"><span data-stu-id="66845-133">This process provides all members of a domain with similar trust lists.</span></span>

<span data-ttu-id="66845-134">Другие сертификаты могут храниться в системном хранилище [*центра сертификации*](../secgloss/c-gly.md) (ЦС) или в созданных пользователем файловых хранилищах.</span><span class="sxs-lookup"><span data-stu-id="66845-134">Other certificates can be stored in the [*certification authority*](../secgloss/c-gly.md) (CA) system store or in user-created, file-based stores.</span></span>

<span data-ttu-id="66845-135">Списки функций для использования и обслуживания хранилищ сертификатов см. в разделе [функции хранилища сертификатов](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="66845-135">For lists of functions for using and maintaining certificate stores, see [Certificate Store Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="66845-136">Пример, в котором используются некоторые из этих функций, см. в разделе [Пример программы C: операции с хранилищем сертификатов](example-c-program-certificate-store-operations.md).</span><span class="sxs-lookup"><span data-stu-id="66845-136">For an example that uses some of these functions, see [Example C Program: Certificate Store Operations](example-c-program-certificate-store-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="66845-137">См. также</span><span class="sxs-lookup"><span data-stu-id="66845-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66845-138">Управление состоянием хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="66845-138">Managing a Certificate Store State</span></span>](managing-a-certificate-store-state.md)
</dt> <dt>

[<span data-ttu-id="66845-139">Работа с сертификатами в хранилищах сертификатов</span><span class="sxs-lookup"><span data-stu-id="66845-139">Working with Certificates in Certificate Stores</span></span>](working-with-certificates-in-certificate-stores.md)
</dt> <dt>

[<span data-ttu-id="66845-140">Ссылки на сертификаты</span><span class="sxs-lookup"><span data-stu-id="66845-140">Certificate Links</span></span>](certificate-links.md)
</dt> <dt>

[<span data-ttu-id="66845-141">Хранилища коллекций</span><span class="sxs-lookup"><span data-stu-id="66845-141">Collection Stores</span></span>](collection-stores.md)
</dt> <dt>

[<span data-ttu-id="66845-142">Логические и физические хранилища</span><span class="sxs-lookup"><span data-stu-id="66845-142">Logical and Physical Stores</span></span>](logical-and-physical-stores.md)
</dt> <dt>

[<span data-ttu-id="66845-143">Расположения системных хранилищ</span><span class="sxs-lookup"><span data-stu-id="66845-143">System Store Locations</span></span>](system-store-locations.md)
</dt> <dt>

[<span data-ttu-id="66845-144">Перенос хранилища сертификатов</span><span class="sxs-lookup"><span data-stu-id="66845-144">Certificate Store Migration</span></span>](certificate-store-migration.md)
</dt> </dl>

 

 
