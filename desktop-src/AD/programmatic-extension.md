---
title: Программное расширение
description: В программных расширениях есть несколько непрозрачных приложений; Администратор должен доверять документации, входящей в состав приложения установки.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Программное расширение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773118"
---
# <a name="programmatic-extension"></a><span data-ttu-id="10c5a-104">Программное расширение</span><span class="sxs-lookup"><span data-stu-id="10c5a-104">Programmatic Extension</span></span>

<span data-ttu-id="10c5a-105">Преимуществом LDIF-файла является то, что администратор может проверить свою функцию.</span><span class="sxs-lookup"><span data-stu-id="10c5a-105">The benefit of an LDIF file is that the administrator can examine its function.</span></span> <span data-ttu-id="10c5a-106">Однако схему также можно расширить программным способом.</span><span class="sxs-lookup"><span data-stu-id="10c5a-106">However, the schema can also be extended programmatically.</span></span> <span data-ttu-id="10c5a-107">Программные расширения имеют несколько разрешений, но приложение непрозрачно; Администратор должен доверять документации, входящей в состав приложения установки.</span><span class="sxs-lookup"><span data-stu-id="10c5a-107">Programmatic extensions have several merits, but an application is opaque; the administrator must trust the documentation included with the setup application.</span></span> <span data-ttu-id="10c5a-108">Использование программных расширений схемы может быть препятствием для развертывания приложений, которые их используют.</span><span class="sxs-lookup"><span data-stu-id="10c5a-108">Use of programmatic schema extensions may be a barrier to deployment for applications that use them.</span></span> <span data-ttu-id="10c5a-109">Программное расширение является инвариантным; Это исполняемый файл Windows NT.</span><span class="sxs-lookup"><span data-stu-id="10c5a-109">A programmatic extension is invariant; it is a Windows NT executable.</span></span> <span data-ttu-id="10c5a-110">Двоичный файл не может быть изменен, в отличие от LDIF-или CSV-файла, который может быть изменен случайно или злонамеренно.</span><span class="sxs-lookup"><span data-stu-id="10c5a-110">The binary cannot be tampered with, unlike an LDIF or .csv file, which can be edited inadvertently or maliciously.</span></span>

<span data-ttu-id="10c5a-111">Ниже перечислены преимущества LDIF-файла.</span><span class="sxs-lookup"><span data-stu-id="10c5a-111">Benefits of an LDIF file include:</span></span>

-   <span data-ttu-id="10c5a-112">Приложения могут обнаруживать и восстанавливать ошибки, а также предоставлять отзывы пользователей.</span><span class="sxs-lookup"><span data-stu-id="10c5a-112">Applications can detect and recover from errors and provide user feedback.</span></span>
-   <span data-ttu-id="10c5a-113">Приложения могут работать в Юникоде без необходимости кодирования в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="10c5a-113">Applications can handle Unicode without resorting to Base64 encoding.</span></span>
-   <span data-ttu-id="10c5a-114">Приложения могут использовать установщик Windows API установки.</span><span class="sxs-lookup"><span data-stu-id="10c5a-114">Applications can leverage Windows Installer setup APIs.</span></span>
-   <span data-ttu-id="10c5a-115">Для установления подлинности приложения могут подписываться.</span><span class="sxs-lookup"><span data-stu-id="10c5a-115">Applications can be signed to establish authenticity.</span></span>

 

 




