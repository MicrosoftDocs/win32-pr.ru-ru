---
description: Для упрощения и сокращения объема кода, необходимого для выполнения обычных задач обработки сообщений, предусмотрена группа функций высокого уровня.
ms.assetid: 7c1a4d6e-9b9d-43c8-b094-3c98b9a68490
title: Упрощенные сообщения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbacaac4dd8ef32b7bab1ff4e57ad04aa1263c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145766"
---
# <a name="simplified-messages"></a><span data-ttu-id="bc71e-103">Упрощенные сообщения</span><span class="sxs-lookup"><span data-stu-id="bc71e-103">Simplified Messages</span></span>

<span data-ttu-id="bc71e-104">Для упрощения и сокращения объема кода, необходимого для выполнения обычных задач обработки сообщений, предусмотрена группа функций высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="bc71e-104">A group of high-level functions has been provided to simplify and shorten the amount of code necessary to accomplish the usual message manipulation tasks.</span></span> <span data-ttu-id="bc71e-105">Эти функции называются "упрощенными функциями сообщений".</span><span class="sxs-lookup"><span data-stu-id="bc71e-105">These functions are called "simplified message functions."</span></span> <span data-ttu-id="bc71e-106">Имена всех упрощенных функций сообщений содержат слово «Message».</span><span class="sxs-lookup"><span data-stu-id="bc71e-106">The names of all simplified message functions contain the word "Message."</span></span>

<span data-ttu-id="bc71e-107">[*Упрощенные функции сообщений*](../secgloss/s-gly.md) имеют более высокий уровень, чем базовые криптографические функции или низкоуровневые функции сообщений.</span><span class="sxs-lookup"><span data-stu-id="bc71e-107">[*Simplified message functions*](../secgloss/s-gly.md) are at a higher level than the base cryptographic functions or the low-level message functions.</span></span> <span data-ttu-id="bc71e-108">Они заключают несколько базовых криптографических, низкоуровневых сообщений и функций сертификатов в одну функцию, которая выполняет определенную задачу особым образом, например шифровать \# сообщение PKCS 7 или подписывать сообщение.</span><span class="sxs-lookup"><span data-stu-id="bc71e-108">They wrap several of the base cryptographic, low-level message, and certificate functions into a single function that performs a specific task in a specific manner, such as encrypting a PKCS \#7 message or signing a message.</span></span> <span data-ttu-id="bc71e-109">Упрощенные функции сообщений позволяют быстро приступить к использованию CryptoAPI, уменьшая число вызовов функций, необходимых для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="bc71e-109">Simplified message functions provide a quick way to get started using CryptoAPI by reducing the number of function calls needed to accomplish a task.</span></span>

<span data-ttu-id="bc71e-110">В следующей таблице перечислены разделы, содержащие подробные описания процедур или примеры использования упрощенных функций сообщений.</span><span class="sxs-lookup"><span data-stu-id="bc71e-110">The following table list sections that contain detailed procedure descriptions or C program examples of using the simplified message functions.</span></span>



| <span data-ttu-id="bc71e-111">Section</span><span class="sxs-lookup"><span data-stu-id="bc71e-111">Section</span></span>                                                                                                                                         | <span data-ttu-id="bc71e-112">Содержимое</span><span class="sxs-lookup"><span data-stu-id="bc71e-112">Contents</span></span>                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc71e-113">Упрощенные функции сообщений</span><span class="sxs-lookup"><span data-stu-id="bc71e-113">Simplified Message Functions</span></span>](cryptography-functions.md)                                                         | <span data-ttu-id="bc71e-114">Содержит список упрощенных функций сообщений.</span><span class="sxs-lookup"><span data-stu-id="bc71e-114">Lists the simplified message functions.</span></span>                                                     |
| [<span data-ttu-id="bc71e-115">Создание подписанного сообщения</span><span class="sxs-lookup"><span data-stu-id="bc71e-115">Creating a Signed Message</span></span>](creating-a-signed-message.md)                                                                                      | <span data-ttu-id="bc71e-116">Подробно описывается процесс создания подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc71e-116">Details the process of creating a signed message.</span></span>                                           |
| [<span data-ttu-id="bc71e-117">Процедура для подписи данных</span><span class="sxs-lookup"><span data-stu-id="bc71e-117">Procedure for Signing Data</span></span>](procedure-for-signing-data.md)                                                                                    | <span data-ttu-id="bc71e-118">Предоставляет процедуру использования упрощенных функций сообщений для создания подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc71e-118">Provides a procedure for using the simplified message functions to create a signed message.</span></span> |
| [<span data-ttu-id="bc71e-119">Проверка подписанного сообщения</span><span class="sxs-lookup"><span data-stu-id="bc71e-119">Verifying A Signed Message</span></span>](verifying-a-signed-message.md)                                                                                    | <span data-ttu-id="bc71e-120">Подробное описание процесса проверки подписи подписанного сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc71e-120">Details a process for verifying the signature on a signed message.</span></span>                          |
| [<span data-ttu-id="bc71e-121">Шифрование сообщения</span><span class="sxs-lookup"><span data-stu-id="bc71e-121">Encrypting a Message</span></span>](../secauthn/encrypting-a-message.md)                                                                                           | <span data-ttu-id="bc71e-122">Сведения о задачах, необходимых для шифрования и расшифровки сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc71e-122">Details the tasks needed to encrypt and decrypt a message.</span></span>                                  |
| [<span data-ttu-id="bc71e-123">Расшифровка сообщения</span><span class="sxs-lookup"><span data-stu-id="bc71e-123">Decrypting a Message</span></span>](../secauthn/decrypting-a-message.md)                                                                                           | <span data-ttu-id="bc71e-124">Сведения о задачах, необходимых для расшифровки сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc71e-124">Details the tasks needed to decrypt a message.</span></span>                                              |
| [<span data-ttu-id="bc71e-125">Пример программы на C: использование Криптенкриптмессаже и Криптдекриптмессаже</span><span class="sxs-lookup"><span data-stu-id="bc71e-125">Example C Program: Using CryptEncryptMessage and CryptDecryptMessage</span></span>](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) | <span data-ttu-id="bc71e-126">Предоставляет процедуру и пример кода для шифрования и расшифровки сообщения.</span><span class="sxs-lookup"><span data-stu-id="bc71e-126">Provides a procedure and sample code for encrypting and decrypting a message.</span></span>               |



 

 

 
