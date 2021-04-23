---
description: Используйте криптографические технологии для шифрования открытых ключей, алгоритмов шифрования, шифрования RSA и цифровых сертификатов.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Шифрование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662314"
---
# <a name="cryptography"></a><span data-ttu-id="ce525-103">Шифрование</span><span class="sxs-lookup"><span data-stu-id="ce525-103">Cryptography</span></span>

## <a name="purpose"></a><span data-ttu-id="ce525-104">Назначение</span><span class="sxs-lookup"><span data-stu-id="ce525-104">Purpose</span></span>

<span data-ttu-id="ce525-105">Шифрование — это использование кодов для преобразования данных, чтобы только конкретный получатель мог прочесть его с помощью ключа.</span><span class="sxs-lookup"><span data-stu-id="ce525-105">Cryptography is the use of codes to convert data so that only a specific recipient will be able to read it, using a key.</span></span>

<span data-ttu-id="ce525-106">К технологиям шифрования Майкрософт относятся CryptoAPI, поставщики служб шифрования (CSP), средства CryptoAPI, CAPICOM, Винтруст, выдача и управление сертификатами и разработка настраиваемых инфраструктур открытых ключей.</span><span class="sxs-lookup"><span data-stu-id="ce525-106">Microsoft cryptographic technologies include CryptoAPI, Cryptographic Service Providers (CSP), CryptoAPI Tools, CAPICOM, WinTrust, issuing and managing certificates, and developing customizable public key infrastructures.</span></span> <span data-ttu-id="ce525-107">Также описаны регистрация сертификатов и смарт-карт, Управление сертификатами и разработка пользовательских модулей.</span><span class="sxs-lookup"><span data-stu-id="ce525-107">Certificate and smart card enrollment, certificate management, and custom module development are also described.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ce525-108">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="ce525-108">Developer audience</span></span>

<span data-ttu-id="ce525-109">Интерфейс CryptoAPI предназначен для использования разработчиками приложений Windows, которые позволяют пользователям создавать и обмениваться документами и другими данными в безопасной среде, особенно на незащищенных носителях, таких как Интернет.</span><span class="sxs-lookup"><span data-stu-id="ce525-109">CryptoAPI is intended for use by developers of Windows-based applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="ce525-110">Разработчики должны быть знакомы с языками программирования C и C++ и средой программирования Windows.</span><span class="sxs-lookup"><span data-stu-id="ce525-110">Developers should be familiar with the C and C++ programming languages and the Windows programming environment.</span></span> <span data-ttu-id="ce525-111">Хотя это и не является обязательным, рекомендуется понимать вопросы, связанные с шифрованием или безопасностью.</span><span class="sxs-lookup"><span data-stu-id="ce525-111">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="ce525-112">CAPICOM — это 32-разрядный компонент, предназначенный для использования разработчиками, создающими приложения с использованием языка программирования Visual Basic Scripting Edition (VBScript) или языка программирования C++.</span><span class="sxs-lookup"><span data-stu-id="ce525-112">CAPICOM is a 32-bit only component that is intended for use by developers who are creating applications using Visual Basic Scripting Edition (VBScript) programming language or the C++ programming language.</span></span> <span data-ttu-id="ce525-113">Элемент CAPICOM доступен для использования в операционных системах, указанных в Run-Time требованиях.</span><span class="sxs-lookup"><span data-stu-id="ce525-113">CAPICOM is available for use in the operating systems specified in Run-Time Requirements.</span></span> <span data-ttu-id="ce525-114">Для будущей разработки рекомендуется использовать платформа .NET Framework для реализации функций безопасности.</span><span class="sxs-lookup"><span data-stu-id="ce525-114">For future development, we recommend that you use the .NET Framework to implement security features.</span></span> <span data-ttu-id="ce525-115">Дополнительные сведения см. [в разделе альтернативы использованию элемента CAPICOM](alternatives-to-using-capicom.md).</span><span class="sxs-lookup"><span data-stu-id="ce525-115">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ce525-116">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="ce525-116">Run-time requirements</span></span>

<span data-ttu-id="ce525-117">Сведения о требованиях времени выполнения для определенного программного элемента см. в разделе "требования" на странице справочника по этому элементу.</span><span class="sxs-lookup"><span data-stu-id="ce525-117">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="ce525-118">CAPICOM 2.1.0.2 поддерживается в следующих операционных системах и версиях:</span><span class="sxs-lookup"><span data-stu-id="ce525-118">CAPICOM 2.1.0.2 is supported on the following operating systems and versions:</span></span>

-   <span data-ttu-id="ce525-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce525-119">Windows Server 2003</span></span>
-   <span data-ttu-id="ce525-120">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ce525-120">Windows XP</span></span>

<span data-ttu-id="ce525-121">CAPICOM доступен в виде распространяемого файла, который можно скачать из [распространяемого пакета Platform SDK: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span><span class="sxs-lookup"><span data-stu-id="ce525-121">CAPICOM is available as a redistributable file that can be downloaded from [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span></span>

<span data-ttu-id="ce525-122">Для служб сертификации требуются следующие версии этих операционных систем:</span><span class="sxs-lookup"><span data-stu-id="ce525-122">Certificate Services requires the following versions of these operating systems:</span></span>

-   <span data-ttu-id="ce525-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ce525-123">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="ce525-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce525-124">Windows Server 2008</span></span>
-   <span data-ttu-id="ce525-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce525-125">Windows Server 2003</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ce525-126">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="ce525-126">In this section</span></span>



| <span data-ttu-id="ce525-127">Раздел</span><span class="sxs-lookup"><span data-stu-id="ce525-127">Topic</span></span>                                                           | <span data-ttu-id="ce525-128">Описание</span><span class="sxs-lookup"><span data-stu-id="ce525-128">Description</span></span>                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce525-129">О шифровании</span><span class="sxs-lookup"><span data-stu-id="ce525-129">About Cryptography</span></span>](about-cryptography.md)<br/>         | <span data-ttu-id="ce525-130">Основные понятия криптографических концепций и высокоуровневое представление технологий криптографии Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ce525-130">Key cryptography concepts and a high-level view of Microsoft cryptography technologies.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="ce525-131">Использование шифрования</span><span class="sxs-lookup"><span data-stu-id="ce525-131">Using Cryptography</span></span>](using-cryptography.md)<br/>         | <span data-ttu-id="ce525-132">Криптографические процессы, процедуры и расширенные примеры программ C и Visual Basic с использованием функций CryptoAPI и CAPICOM Objects.</span><span class="sxs-lookup"><span data-stu-id="ce525-132">Cryptography processes, procedures, and extended samples of C and Visual Basic programs using CryptoAPI functions and CAPICOM objects.</span></span><br/>                                                                            |
| [<span data-ttu-id="ce525-133">Справочник по шифрованию</span><span class="sxs-lookup"><span data-stu-id="ce525-133">Cryptography Reference</span></span>](cryptography-reference.md)<br/> | <span data-ttu-id="ce525-134">Подробное описание функций криптографии, интерфейсов, объектов, структур и других программных элементов шифрования Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ce525-134">Detailed descriptions of the Microsoft cryptography functions, interfaces, objects, structures, and other programming elements.</span></span> <span data-ttu-id="ce525-135">Содержит справочные описания API для работы с цифровыми сертификатами.</span><span class="sxs-lookup"><span data-stu-id="ce525-135">Includes reference descriptions of the API for working with digital certificates.</span></span><br/> |



 

 

 




