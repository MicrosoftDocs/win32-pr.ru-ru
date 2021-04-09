---
title: Согласованность при обмене файлами
description: Служба BITS гарантирует, что версия переданного файла будет согласована в зависимости от размера файла и метки времени, а не от содержимого (BITS не защищает от атак типа "злоумышленник в середине").
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887712"
---
# <a name="file-transfer-consistency"></a><span data-ttu-id="2bd73-103">Согласованность при обмене файлами</span><span class="sxs-lookup"><span data-stu-id="2bd73-103">File Transfer Consistency</span></span>

<span data-ttu-id="2bd73-104">Служба BITS гарантирует, что версия переданного файла будет согласована в зависимости от размера файла и метки времени, а не от содержимого (BITS не защищает от атак типа "злоумышленник в середине").</span><span class="sxs-lookup"><span data-stu-id="2bd73-104">BITS guarantees that the version of the file it transfers is consistent based on the file size and time stamp, not content (BITS does not protect against man-in-the-middle attacks).</span></span> <span data-ttu-id="2bd73-105">Чтобы проверить содержимое самостоятельно, можно использовать метод [**IBackgroundCopyFile3:: жеттемпораринаме**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) , чтобы получить имя файла, содержащего скачанное содержимое, проверить содержимое с помощью собственного механизма, а затем вызвать метод [**IBackgroundCopyFile3:: сетвалидатионстате**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) , чтобы указать BITS, если содержимое файла является допустимым.</span><span class="sxs-lookup"><span data-stu-id="2bd73-105">To verify the contents yourself, you can use the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method to get the name of the file that contains the downloaded content, verify the contents using your own mechanism, and then call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method to indicate to BITS if the contents of the file is valid.</span></span> <span data-ttu-id="2bd73-106">Если для состояния проверки задано **значение false** и содержимое находится с сервера-источника, задание переходит в состояние ошибки.</span><span class="sxs-lookup"><span data-stu-id="2bd73-106">If you set the validation state to **FALSE** and the content is from the origin server, the job goes into the error state.</span></span> <span data-ttu-id="2bd73-107">Если содержимое помещается из однорангового узла, BITS загружает его с сервера-источника.</span><span class="sxs-lookup"><span data-stu-id="2bd73-107">If the content is from a peer, BITS downloads the file from the origin server.</span></span>

<span data-ttu-id="2bd73-108">При загрузке, если размер файла или отметка времени изменяется во время передачи файла службой BITS, BITS перезапускает передачу только этого файла.</span><span class="sxs-lookup"><span data-stu-id="2bd73-108">For downloads, if the file size or time stamp changes while BITS is transferring the file, BITS restarts the transfer of that file only.</span></span> <span data-ttu-id="2bd73-109">Например, если задание загрузки содержит два файла и файлы обновляются на сервере, а BITS перемещает второй файл, BITS перезапускает передачу только второго файла.</span><span class="sxs-lookup"><span data-stu-id="2bd73-109">For example, if the download job contains two files and the files are updated on the server while BITS is transferring the second file, BITS restarts the transfer of the second file only.</span></span> <span data-ttu-id="2bd73-110">Первый файл, который уже успешно передавался, не обновляется в соответствии с новыми изменениями.</span><span class="sxs-lookup"><span data-stu-id="2bd73-110">The first file, which already transferred successfully, is not updated to reflect the new changes.</span></span>

<span data-ttu-id="2bd73-111">Обратите внимание, что если вы владеете файлом, загружаемым с сервера, необходимо создать новый URL-адрес для каждой новой версии файла.</span><span class="sxs-lookup"><span data-stu-id="2bd73-111">Note that if you own the file being downloaded from the server, you should create a new URL for each new version of the file.</span></span> <span data-ttu-id="2bd73-112">Если для новых версий файла используется один и тот же URL-адрес, некоторые прокси-серверы могут обрабатывать устаревшие данные из кэша, так как они не проверяют исходный сервер, если он устарел.</span><span class="sxs-lookup"><span data-stu-id="2bd73-112">If you use the same URL for new versions of the file, some proxy servers may serve stale data from their cache because they do not verify with the original server if the file is stale.</span></span>

<span data-ttu-id="2bd73-113">Для отправки, если размер файла или отметка времени изменяется во время передачи файла, BITS выдает ошибку, а задание помещается в \_ состояние ошибки задания BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2bd73-113">For uploads, if the file size or time stamp changes during the file transfer, BITS generates an error and the job is placed in the BG\_JOB\_STATE\_ERROR state.</span></span>

<span data-ttu-id="2bd73-114">Служба BITS не синхронизирует запросы на передачу, когда один или несколько пользователей запрашивают передачу одного и того же файла в одно и то же расположение.</span><span class="sxs-lookup"><span data-stu-id="2bd73-114">BITS does not synchronize transfer requests when one or more users request that the same file be transferred to the same location.</span></span> <span data-ttu-id="2bd73-115">BITS передает файл для каждого запроса отдельно.</span><span class="sxs-lookup"><span data-stu-id="2bd73-115">BITS transfers the file for each request separately.</span></span>

 

 




