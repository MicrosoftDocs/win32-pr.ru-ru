---
description: Объясняет, как использовать средство SignTool для проверки подписи файла.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Использование средства SignTool для проверки подписи файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8161d4c890400f3aa33b415e7ac16a5306aa094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662625"
---
# <a name="using-signtool-to-verify-a-file-signature"></a><span data-ttu-id="4a92a-103">Использование средства SignTool для проверки подписи файла</span><span class="sxs-lookup"><span data-stu-id="4a92a-103">Using SignTool to Verify a File Signature</span></span>

<span data-ttu-id="4a92a-104">Следующая команда проверяет подпись файла с именем *MyControl.exe*:</span><span class="sxs-lookup"><span data-stu-id="4a92a-104">The following command verifies the signature of a file named *MyControl.exe*:</span></span>

<span data-ttu-id="4a92a-105">**Проверка средства SignTool** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="4a92a-105">**SignTool verify** *MyControl.exe*</span></span>

<span data-ttu-id="4a92a-106">Если предыдущий пример завершается сбоем, то в сигнатуре может использоваться сертификат подписи кода.</span><span class="sxs-lookup"><span data-stu-id="4a92a-106">If the preceding example fails, it could be that the signature used a code-signing certificate.</span></span> <span data-ttu-id="4a92a-107">По умолчанию средство [SignTool](signtool.md) имеет политику драйвера Windows для проверки.</span><span class="sxs-lookup"><span data-stu-id="4a92a-107">[SignTool](signtool.md) defaults to the Windows driver policy for verification.</span></span>

<span data-ttu-id="4a92a-108">Следующая команда проверяет подпись с помощью политики проверки подлинности по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="4a92a-108">The following command verifies the signature, using the Default Authentication Verification Policy:</span></span>

<span data-ttu-id="4a92a-109">Средство **SignTool Verify/па** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="4a92a-109">**SignTool verify /pa** *MyControl.exe*</span></span>

<span data-ttu-id="4a92a-110">Следующая команда проверяет системный файл, который может быть подписан в каталоге:</span><span class="sxs-lookup"><span data-stu-id="4a92a-110">The following command verifies a system file that may be signed in a catalog:</span></span>

<span data-ttu-id="4a92a-111">Средство **SignTool Verify/a** *SysFile.dll*</span><span class="sxs-lookup"><span data-stu-id="4a92a-111">**SignTool verify /a** *SysFile.dll*</span></span>

<span data-ttu-id="4a92a-112">Следующая команда проверяет системный файл, подписанный в каталоге с именем *MyCat.Cat*:</span><span class="sxs-lookup"><span data-stu-id="4a92a-112">The following command verifies a system file that is signed in a catalog named *MyCat.cat*:</span></span>

<span data-ttu-id="4a92a-113">Средство **SignTool Verify/c** *MyCat.catMyFile.ini*</span><span class="sxs-lookup"><span data-stu-id="4a92a-113">**SignTool verify /c** *MyCat.catMyFile.ini*</span></span>

<span data-ttu-id="4a92a-114">Для любой проверки [SignTool](signtool.md) можно получить сведения о подписавшем сертификата.</span><span class="sxs-lookup"><span data-stu-id="4a92a-114">For any [SignTool](signtool.md) verification, you can retrieve the signer of the certificate.</span></span> <span data-ttu-id="4a92a-115">Следующая команда проверяет системный файл и отображает сертификат подписавших:</span><span class="sxs-lookup"><span data-stu-id="4a92a-115">The following command verifies a system file and displays the signer certificate:</span></span>

<span data-ttu-id="4a92a-116">Средство **SignTool проверка/v** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="4a92a-116">**SignTool verify /v** *MyControl.exe*</span></span>

<span data-ttu-id="4a92a-117">Средство [SignTool](signtool.md) возвращает текст командной строки, который указывает результат проверки подписи.</span><span class="sxs-lookup"><span data-stu-id="4a92a-117">[SignTool](signtool.md) returns command-line text that states the result of the signature check.</span></span> <span data-ttu-id="4a92a-118">Кроме того, средство SignTool возвращает нулевой код выхода для успешного выполнения, один для неудачного выполнения и два для выполнения, которые завершились с предупреждениями.</span><span class="sxs-lookup"><span data-stu-id="4a92a-118">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="4a92a-119">Дополнительные сведения о [SignTool](signtool.md)см. в разделе [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="4a92a-119">For more information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 



