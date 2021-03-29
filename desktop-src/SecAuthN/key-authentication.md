---
description: Многие виды проверки подлинности основаны на идее того, что сущность может доказать свою личность, если она может доказать, что она знает ключ, например пароль, который может быть известен только ему.
ms.assetid: e17e4eb7-133e-46a0-8247-00a58b88bf61
title: Проверка подлинности с использованием ключа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deaadfdb61340955209ded22b5302e5436271ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264819"
---
# <a name="key-authentication"></a><span data-ttu-id="444b2-103">Проверка подлинности с использованием ключа</span><span class="sxs-lookup"><span data-stu-id="444b2-103">Key Authentication</span></span>

<span data-ttu-id="444b2-104">Многие виды проверки подлинности основаны на идее того, что сущность может доказать свою личность, если она может доказать, что она знает ключ, например пароль, который может быть известен только ему.</span><span class="sxs-lookup"><span data-stu-id="444b2-104">Many forms of authentication are based on the idea that an entity can prove its identity if it can prove it knows a key, such as a password, that only it can know.</span></span>

<span data-ttu-id="444b2-105">Методы проверки подлинности, которые используют секрет, например пароль, должны иметь способ защитить секрет от получения общедоступного набора знаний.</span><span class="sxs-lookup"><span data-stu-id="444b2-105">Authentication techniques that rely on a secret, such as a password, need to have a way to keep the secret from becoming public knowledge.</span></span> <span data-ttu-id="444b2-106">Владелец пароля не может пройти до двери и ввести пароль.</span><span class="sxs-lookup"><span data-stu-id="444b2-106">A password owner cannot walk up to a door and give the password.</span></span> <span data-ttu-id="444b2-107">Кто-то, помимо дуркипер, может прослушиваться; или это может быть неверный дверца.</span><span class="sxs-lookup"><span data-stu-id="444b2-107">Someone besides the doorkeeper might be listening; or it might be the wrong door.</span></span> <span data-ttu-id="444b2-108">Для сохранения секрета должен быть способ подтвердить, что пользователь знает пароль, не раскрывая пароль.</span><span class="sxs-lookup"><span data-stu-id="444b2-108">In order to keep a secret, there must be a way to prove a user knows the password without revealing the password.</span></span> <span data-ttu-id="444b2-109">Это идея проверки подлинности секретного ключа, метода проверки, используемого по всему [*протоколу Kerberos*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="444b2-109">That is the idea behind secret key authentication, a method of verification used throughout the [*Kerberos protocol*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="444b2-110">Обратите внимание, что «секрет» в проверке подлинности с помощью секретного ключа заключается в том, что процесс проверки подлинности выполняется в секрете, то есть без фактического разглашения содержимого ключа.</span><span class="sxs-lookup"><span data-stu-id="444b2-110">Notice that the "secret" in secret key authentication is that the authentication process takes place "in secret;" that is, without ever actually revealing the content of the key.</span></span>

<span data-ttu-id="444b2-111">Чтобы проверка подлинности с помощью секретного ключа работала, две стороны транзакции должны совместно использовать криптографический [*ключ сеанса*](../secgloss/s-gly.md) , который также известен только для них и не может быть другим.</span><span class="sxs-lookup"><span data-stu-id="444b2-111">For secret key authentication to work, the two parties to a transaction must share a cryptographic [*session key*](../secgloss/s-gly.md) which is also secret, known only to them and to no others.</span></span> <span data-ttu-id="444b2-112">Ключ является [*симметричным*](../secgloss/s-gly.md); Это единственный ключ, используемый для шифрования и расшифровки.</span><span class="sxs-lookup"><span data-stu-id="444b2-112">The key is [*symmetric*](../secgloss/s-gly.md); that is, it is a single key used for both encryption and decryption.</span></span> <span data-ttu-id="444b2-113">Одна сторона в процессе проверки подлинности подтверждает знание ключа, шифруя сообщение.</span><span class="sxs-lookup"><span data-stu-id="444b2-113">One party in the authentication process proves its knowledge of the key by encrypting a message.</span></span> <span data-ttu-id="444b2-114">Другая сторона подтверждает свои знания о ключе, расшифровании сообщения.</span><span class="sxs-lookup"><span data-stu-id="444b2-114">The other party proves its knowledge of the key by decrypting the message.</span></span>

 

 
