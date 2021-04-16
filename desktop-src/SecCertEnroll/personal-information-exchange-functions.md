---
description: В каждом из следующих разделов описывается функция, экспортируемая Xenroll.dll для управления сообщениями обмена личной информацией (PFX).
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: Функции обмена личной информацией
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683950"
---
# <a name="personal-information-exchange-functions"></a><span data-ttu-id="849de-103">Функции обмена личной информацией</span><span class="sxs-lookup"><span data-stu-id="849de-103">Personal Information Exchange Functions</span></span>

<span data-ttu-id="849de-104">В каждом из следующих разделов описывается функция, экспортируемая Xenroll.dll для управления сообщениями обмена личной информацией (PFX).</span><span class="sxs-lookup"><span data-stu-id="849de-104">Each of the following sections discusses a function exported by Xenroll.dll to manage Personal Information Exchange (PFX) messages.</span></span> <span data-ttu-id="849de-105">В каждом разделе также обсуждается использование CertEnroll.dll для замены функции или указывает, что сопоставление между двумя библиотеками не существует.</span><span class="sxs-lookup"><span data-stu-id="849de-105">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="createfilepfxwstr"></a><span data-ttu-id="849de-106">креатефилепфксвстр</span><span class="sxs-lookup"><span data-stu-id="849de-106">createFilePFXWStr</span></span>

<span data-ttu-id="849de-107">Функция [**креатефилепфксвстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) в Xenroll.dll сохраняет цепочку сертификатов и [*закрытый ключ*](/windows/desktop/SecGloss/p-gly) в файле с помощью формата PFX.</span><span class="sxs-lookup"><span data-stu-id="849de-107">The [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) function in Xenroll.dll saves a certificate chain and [*private key*](/windows/desktop/SecGloss/p-gly) in a file by using the PFX format.</span></span>

<span data-ttu-id="849de-108">Библиотека CertEnroll.dll напрямую не реализует функции для копирования PFX-сообщения в файл.</span><span class="sxs-lookup"><span data-stu-id="849de-108">The CertEnroll.dll library does not directly implement functionality to copy the PFX message to a file.</span></span> <span data-ttu-id="849de-109">Однако можно использовать метод [**креатепфкс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) в интерфейсе [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) для создания закодированного сообщения PFX и написать пользовательскую функцию для сохранения сообщения в файле.</span><span class="sxs-lookup"><span data-stu-id="849de-109">You can, however, use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message and write a custom function to save the message in a file.</span></span>

## <a name="createpfxwstr"></a><span data-ttu-id="849de-110">креатепфксвстр</span><span class="sxs-lookup"><span data-stu-id="849de-110">createPFXWStr</span></span>

<span data-ttu-id="849de-111">Функция [**креатепфксвстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) в Xenroll.dll сохраняет цепочку сертификатов и закрытый ключ в строке формата PFX.</span><span class="sxs-lookup"><span data-stu-id="849de-111">The [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) function in Xenroll.dll saves a certificate chain and private key in a PFX format string.</span></span>

<span data-ttu-id="849de-112">Для создания закодированного сообщения PFX, содержащего цепочку сертификатов и ключ, можно использовать метод [**креатепфкс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) в интерфейсе [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .</span><span class="sxs-lookup"><span data-stu-id="849de-112">You can use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message that contains the certificate chain and key.</span></span> <span data-ttu-id="849de-113">Можно указать пароль, параметры экспорта и тип кодировки.</span><span class="sxs-lookup"><span data-stu-id="849de-113">You can specify a password, export options, and encoding type.</span></span> <span data-ttu-id="849de-114">Чтобы получить строку, эквивалентную возвращенной из [**креатепфксвстр**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), передайте \_ \_ \_ двоичный флаг кскн шифрования String в в параметре *Encoding* метода [**креатепфкс**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) .</span><span class="sxs-lookup"><span data-stu-id="849de-114">To retrieve a string that is equivalent to that returned from [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), pass the XCN\_CRYPT\_STRING\_BINARY flag in the in the *Encoding* parameter of the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="849de-115">См. также</span><span class="sxs-lookup"><span data-stu-id="849de-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="849de-116">Сопоставление Xenroll.dll CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="849de-116">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="849de-117">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="849de-117">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
