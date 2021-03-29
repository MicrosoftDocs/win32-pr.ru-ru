---
description: Чтобы подписать файл и создать каталог для него, сначала необходимо выполнить процесс подписывания файлов, сертификата и открытого ключа.
ms.assetid: 61337ea6-2d6b-4080-9128-5b8527512ce6
title: Создание подписанных файлов и каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1327ed2d64c6f7be9f14acc2c846cf8a887119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264823"
---
# <a name="creating-signed-files-and-catalogs"></a><span data-ttu-id="f11de-103">Создание подписанных файлов и каталогов</span><span class="sxs-lookup"><span data-stu-id="f11de-103">Creating Signed Files and Catalogs</span></span>

<span data-ttu-id="f11de-104">Чтобы подписать файл и создать каталог для него, сначала необходимо выполнить процесс подписывания файлов, сертификата и открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="f11de-104">To sign a file and create a catalog for it, you must first have a process for signing files, a certificate, and a public key.</span></span>

<span data-ttu-id="f11de-105">**Подписание файла и создание каталога**</span><span class="sxs-lookup"><span data-stu-id="f11de-105">**To sign a file and a create a catalog**</span></span>

1.  <span data-ttu-id="f11de-106">Чтобы извлечь [*маркер открытого ключа*](p-sbscs-gly.md) из файла сертификата, используйте [Pktextract.exe](pktextract-exe.md) .</span><span class="sxs-lookup"><span data-stu-id="f11de-106">Use [Pktextract.exe](pktextract-exe.md) to extract the [*public key token*](p-sbscs-gly.md) from the certificate file.</span></span> <span data-ttu-id="f11de-107">Файл сертификата должен присутствовать в том же каталоге, что и программа.</span><span class="sxs-lookup"><span data-stu-id="f11de-107">The certificate file must be present in the same directory as the utility.</span></span>
2.  <span data-ttu-id="f11de-108">Используйте значение токена открытого ключа, чтобы обновить атрибут **PublicKeyToken** элемента **assemblyIdentity** в файле манифеста.</span><span class="sxs-lookup"><span data-stu-id="f11de-108">Use the public key token value to update the **publicKeyToken** attribute of the **assemblyIdentity** element in the manifest file.</span></span>
3.  <span data-ttu-id="f11de-109">Используйте [MT.exe](mt-exe.md) для создания хэшей файлов, содержащихся в манифесте сборки, и для создания файла описания каталога (CDF-файлов).</span><span class="sxs-lookup"><span data-stu-id="f11de-109">Use [MT.exe](mt-exe.md) to generate hashes of files contained in the assembly manifest and to create the catalog description file (.cdf).</span></span>
4.  <span data-ttu-id="f11de-110">Чтобы создать каталог безопасности для сборки, используйте Makecat.exe с созданным CDF.</span><span class="sxs-lookup"><span data-stu-id="f11de-110">Use Makecat.exe with the generated .cdf to create the security catalog for the assembly.</span></span> <span data-ttu-id="f11de-111">Это средство входит в интерфейс CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="f11de-111">This tool is included in the CryptoAPI.</span></span>
5.  <span data-ttu-id="f11de-112">Используйте программу [SignTool](/windows/desktop/SecCrypto/signtool) для подписывания каталога, созданного с помощью сертификата, используемого на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="f11de-112">Use the [SignTool](/windows/desktop/SecCrypto/signtool) utility to sign the catalog generated with the certificate used in step 1.</span></span> <span data-ttu-id="f11de-113">. CDF из шагов 3 и 4 можно удалить после создания каталога.</span><span class="sxs-lookup"><span data-stu-id="f11de-113">The .cdf from steps 3 and 4 can be deleted once the catalog is created.</span></span>

<span data-ttu-id="f11de-114">См. также [пример подписывания сборки](assembly-signing-example.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-114">See also, [Assembly Signing Example](assembly-signing-example.md).</span></span>

 

 
