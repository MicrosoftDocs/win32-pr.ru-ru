---
description: XML — это промышленный стандарт для описания структурированных данных. Цифровая подпись XML — это XML-представление цифровой подписи, которое обеспечивает возможность проверки происхождения и целостности XML-документа и данных, на которые имеются ссылки.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Общие сведения о цифровой подписи XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683485"
---
# <a name="xml-digital-signature-overview"></a><span data-ttu-id="35084-104">Общие сведения о цифровой подписи XML</span><span class="sxs-lookup"><span data-stu-id="35084-104">XML Digital Signature Overview</span></span>

<span data-ttu-id="35084-105">XML — это промышленный стандарт для описания структурированных данных.</span><span class="sxs-lookup"><span data-stu-id="35084-105">XML is an industry standard for describing structured data.</span></span> <span data-ttu-id="35084-106">Цифровая подпись XML — это XML-представление [*цифровой подписи*](../secgloss/d-gly.md) , которое обеспечивает возможность проверки происхождения и целостности XML-документа и данных, на которые имеются ссылки.</span><span class="sxs-lookup"><span data-stu-id="35084-106">An XML Digital Signature is an XML representation of a [*digital signature*](../secgloss/d-gly.md) that provides the ability to verify the origin and integrity of XML document and externally referenced data.</span></span> <span data-ttu-id="35084-107">Цифровые подписи XML можно использовать для подписывания произвольных данных, включая XML-документ или фрагмент, HTML-страницу, обычный текст или данные в двоичном формате, такие как JPEG-файл.</span><span class="sxs-lookup"><span data-stu-id="35084-107">XML digital signatures can be used to sign arbitrary data, including an XML document or fragment, an HTML page, plain text, or binary-encoded data such as a JPEG file.</span></span>

<span data-ttu-id="35084-108">Формат цифровой подписи XML, поддерживаемый API цифровых подписей Криптксмл, определяется синтаксисом подписи XML и обработкой (второй выпуск) консорциума W3C.</span><span class="sxs-lookup"><span data-stu-id="35084-108">The XML digital signature format supported by the CryptXML digital signature API is specified by the XML Signature Syntax and Processing (Second Edition) W3C recommendation.</span></span>

<span data-ttu-id="35084-109">Цифровая подпись Криптксмл реализует поддержку требуемых типов сигнатур, алгоритмов шифрования, алгоритмов канонизации и заданное преобразование с оболочкой.</span><span class="sxs-lookup"><span data-stu-id="35084-109">The CryptXML digital signature implements support for the required signature types, cryptographic algorithms, canonicalization algorithms, and the specified enveloped transform.</span></span>

<span data-ttu-id="35084-110">Разработчики могут расширить набор алгоритмов шифрования по умолчанию, поддерживаемых Криптксмл, путем создания библиотек DLL расширения шифрования.</span><span class="sxs-lookup"><span data-stu-id="35084-110">Developers can extend the default set of cryptographic algorithms supported by CryptXML by creating cryptographic extension DLLs.</span></span> <span data-ttu-id="35084-111">Разработчики также могут создавать собственные пользовательские преобразования и алгоритмы Канонизации на основе API Криптксмл.</span><span class="sxs-lookup"><span data-stu-id="35084-111">Developers can also create their own custom transforms and canonicalization algorithms on top of CryptXML API.</span></span> <span data-ttu-id="35084-112">Разработчики могут использовать API Криптксмл с API-интерфейсами сертификатов Windows.</span><span class="sxs-lookup"><span data-stu-id="35084-112">Developers can use the CryptXML APIs with the Windows certificate APIs.</span></span>

 

 
