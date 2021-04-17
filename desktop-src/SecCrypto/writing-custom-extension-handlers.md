---
description: Чтобы создать пользовательские модули или закодировать сложное расширение, можно написать собственные обработчики расширений, которые экспортируют пользовательские интерфейсы.
ms.assetid: a33ac417-b5f9-4ad7-a26e-13cdb1e4ac1b
title: Написание пользовательских обработчиков расширений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c8c4380b11fd0b0b1a5484ba0a7ab80f69c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684157"
---
# <a name="writing-custom-extension-handlers"></a><span data-ttu-id="995d0-103">Написание пользовательских обработчиков расширений</span><span class="sxs-lookup"><span data-stu-id="995d0-103">Writing Custom Extension Handlers</span></span>

<span data-ttu-id="995d0-104">Чтобы создать пользовательские модули или закодировать сложное расширение, можно написать собственные обработчики расширений, которые экспортируют пользовательские интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="995d0-104">To create custom extensions or to encode a complex extension, you can write your own extension handlers that export custom interfaces.</span></span> <span data-ttu-id="995d0-105">Службы сертификации Майкрософт поставляются со следующими интерфейсами, которые можно использовать для кодирования различных типов данных расширения: [**ицертенкодеалтнаме**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ицертенкодебитстринг**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ицертенкодекрлдистинфо**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ицертенкодедатеаррай**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray)и [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span><span class="sxs-lookup"><span data-stu-id="995d0-105">Microsoft Certificate Services ships with the following interfaces which can be used to encode various types of extension data: [**ICertEncodeAltName**](/windows/desktop/api/Certenc/nn-certenc-icertencodealtname), [**ICertEncodeBitString**](/windows/desktop/api/Certenc/nn-certenc-icertencodebitstring), [**ICertEncodeCRLDistInfo**](/windows/desktop/api/Certenc/nn-certenc-icertencodecrldistinfo), [**ICertEncodeDateArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodedatearray), [**ICertEncodeLongArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodelongarray), and [**ICertEncodeStringArray**](/windows/desktop/api/Certenc/nn-certenc-icertencodestringarray).</span></span> <span data-ttu-id="995d0-106">Эти интерфейсы содержатся в Certenc.dll.</span><span class="sxs-lookup"><span data-stu-id="995d0-106">These interfaces are contained in Certenc.dll.</span></span> <span data-ttu-id="995d0-107">Кроме того, сведения о типе для этих интерфейсов содержатся в Certencl.dll, который содержится в пакете SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="995d0-107">Additionally, the type information for these interfaces is contained in Certencl.dll, which is contained in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="995d0-108">Дополнительные сведения о обработчиках расширений см. в разделе [обработчики расширений](extension-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="995d0-108">For more information about extension handlers, see [Extension Handlers](extension-handlers.md).</span></span>

 

 



