---
description: Функции целостности изображений управляют набором сертификатов в файле образа.
ms.assetid: db77b8af-3c36-4e01-88e0-4c44ef8504ff
title: Функции целостности изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a11678dbb12bcb9f29950589b60a84e00960b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072426"
---
# <a name="image-integrity-functions"></a><span data-ttu-id="342a4-103">Функции целостности изображений</span><span class="sxs-lookup"><span data-stu-id="342a4-103">Image Integrity Functions</span></span>

<span data-ttu-id="342a4-104">Функции целостности изображений управляют набором сертификатов в файле образа.</span><span class="sxs-lookup"><span data-stu-id="342a4-104">The image integrity functions manage the set of certificates in an image file.</span></span> <span data-ttu-id="342a4-105">Предоставляются подпрограммы для добавления, удаления и запроса сертификатов.</span><span class="sxs-lookup"><span data-stu-id="342a4-105">Routines are provided to add, remove, and query certificates.</span></span> <span data-ttu-id="342a4-106">Кроме того, существует функция, позволяющая получить поток байтов файла изображения, необходимый для вычисления дайджеста сообщения файла изображения.</span><span class="sxs-lookup"><span data-stu-id="342a4-106">There is also a function available for obtaining the byte stream of an image file required to calculate a message digest of the image file.</span></span> <span data-ttu-id="342a4-107">Это необходимо для создания сертификатов подписи.</span><span class="sxs-lookup"><span data-stu-id="342a4-107">This is needed to create signature certificates.</span></span>

<span data-ttu-id="342a4-108">Каждый сертификат в файле имеет индекс, который может изменяться при удалении сертификатов.</span><span class="sxs-lookup"><span data-stu-id="342a4-108">Every certificate in a file has an index which can change as certificates are removed.</span></span> <span data-ttu-id="342a4-109">Новые сертификаты всегда будут добавляться в конец списка существующих сертификатов.</span><span class="sxs-lookup"><span data-stu-id="342a4-109">New certificates will always be added "at the end" of the list of existing certificates.</span></span> <span data-ttu-id="342a4-110">То есть им будут назначены индексы, превышающие индекс, который используется в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="342a4-110">That is, they will be assigned indices that are greater than any index currently in use.</span></span> <span data-ttu-id="342a4-111">Как правило, приложение не должно рассчитывать, что у данного сертификата тот же индекс, что и при последнем обращении.</span><span class="sxs-lookup"><span data-stu-id="342a4-111">In general, an application should not assume that a given certificate has the same index it had the last time it was referenced.</span></span>

-   [<span data-ttu-id="342a4-112">**дижестфунктион**</span><span class="sxs-lookup"><span data-stu-id="342a4-112">**DigestFunction**</span></span>](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)
-   [<span data-ttu-id="342a4-113">**имажеаддцертификате**</span><span class="sxs-lookup"><span data-stu-id="342a4-113">**ImageAddCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)
-   [<span data-ttu-id="342a4-114">**имажеенумератецертификатес**</span><span class="sxs-lookup"><span data-stu-id="342a4-114">**ImageEnumerateCertificates**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)
-   [<span data-ttu-id="342a4-115">**имажежетцертификатедата**</span><span class="sxs-lookup"><span data-stu-id="342a4-115">**ImageGetCertificateData**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)
-   [<span data-ttu-id="342a4-116">**имажежетцертификатехеадер**</span><span class="sxs-lookup"><span data-stu-id="342a4-116">**ImageGetCertificateHeader**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)
-   [<span data-ttu-id="342a4-117">**имажежетдижестстреам**</span><span class="sxs-lookup"><span data-stu-id="342a4-117">**ImageGetDigestStream**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)
-   [<span data-ttu-id="342a4-118">**имажеремовецертификате**</span><span class="sxs-lookup"><span data-stu-id="342a4-118">**ImageRemoveCertificate**</span></span>](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)

 

 



