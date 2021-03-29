---
description: Используйте команды MakeCert для создания тестовых сертификатов с помощью параметров, доступных в Internet Explorer версии 4,0 или более поздней.
ms.assetid: 5dbcc8d0-ffd1-4418-adf6-a9805280ee6d
title: Использование MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 068b10d5ce50141ff657379f9c5106cf2733d969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811236"
---
# <a name="using-makecert"></a><span data-ttu-id="46b74-103">Использование MakeCert</span><span class="sxs-lookup"><span data-stu-id="46b74-103">Using MakeCert</span></span>

<span data-ttu-id="46b74-104">В следующих примерах используются команды [MakeCert](makecert.md) для создания тестовых сертификатов с помощью параметров, доступных в Internet Explorer версии 4,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="46b74-104">The following examples use [MakeCert](makecert.md) commands to create test certificates using options available with Internet Explorer version 4.0 or later.</span></span>

-   <span data-ttu-id="46b74-105">Создайте сертификат, выданный тестовым корнем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46b74-105">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="46b74-106">Сохраните сертификат в файл.</span><span class="sxs-lookup"><span data-stu-id="46b74-106">Save the certificate to a file.</span></span>

    <span data-ttu-id="46b74-107">**MakeCert** *Минев. cer*</span><span class="sxs-lookup"><span data-stu-id="46b74-107">**MakeCert** *MyNew.cer*</span></span>

-   <span data-ttu-id="46b74-108">Создайте сертификат, выданный тестовым корнем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46b74-108">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="46b74-109">Сохраните его в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="46b74-109">Save it to a certificate store.</span></span>

    <span data-ttu-id="46b74-110">**MakeCert-СС** *миневсторе*</span><span class="sxs-lookup"><span data-stu-id="46b74-110">**MakeCert -ss** *MyNewStore*</span></span>

-   <span data-ttu-id="46b74-111">Создайте сертификат, выданный тестовым корнем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46b74-111">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="46b74-112">Создайте контейнер ключей и сохраните сертификат как в хранилище, так и в файл.</span><span class="sxs-lookup"><span data-stu-id="46b74-112">Create a key container and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="46b74-113">**MakeCert-SK** *миневкэй* **-SS** *миневсторе* *Минев. cer*</span><span class="sxs-lookup"><span data-stu-id="46b74-113">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="46b74-114">Создайте сертификат, выданный тестовым корнем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46b74-114">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="46b74-115">Создайте файл закрытого ключа и сохраните сертификат как в хранилище, так и в файл.</span><span class="sxs-lookup"><span data-stu-id="46b74-115">Create a private key file and save the certificate to both a store and a file.</span></span>

    <span data-ttu-id="46b74-116">**MakeCert-SV** *микэйфиле* **-СС** *миневсторе* *Минев. cer*</span><span class="sxs-lookup"><span data-stu-id="46b74-116">**MakeCert -sv** *MyKeyFile* **-ss** *MyNewStore* *MyNew.cer*</span></span>

-   <span data-ttu-id="46b74-117">Создайте сертификат, выданный тестовым корнем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46b74-117">Make a certificate issued by the default test root.</span></span> <span data-ttu-id="46b74-118">Создайте контейнер ключей, сохраните сертификат как в хранилище, так и в файле, а затем сделайте закрытый ключ экспортируемым.</span><span class="sxs-lookup"><span data-stu-id="46b74-118">Create a key container, save the certificate to both a store and a file, and make the private key exportable.</span></span>

    <span data-ttu-id="46b74-119">**MakeCert-SK** *миневкэй* **-SS** *миневсторе* *Минев. cer* **-PE**</span><span class="sxs-lookup"><span data-stu-id="46b74-119">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* *MyNew.cer* **-pe**</span></span>

-   <span data-ttu-id="46b74-120">Создайте сертификат, используя тестовый корень по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46b74-120">Make a certificate by using the default test root.</span></span> <span data-ttu-id="46b74-121">Сохраните сертификат в хранилище.</span><span class="sxs-lookup"><span data-stu-id="46b74-121">Save the certificate to a store.</span></span> <span data-ttu-id="46b74-122">Затем создайте другой сертификат, выданный созданным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="46b74-122">Then make another certificate issued by the newly created certificate.</span></span> <span data-ttu-id="46b74-123">Сохраните второй сертификат в другом хранилище.</span><span class="sxs-lookup"><span data-stu-id="46b74-123">Save the second certificate to another store.</span></span>

    <span data-ttu-id="46b74-124">**MakeCert-SK** *миневкэй* **-SS** *миневсторе* **MakeCert —** *миневсторе* **-SS** *аносерсторе*</span><span class="sxs-lookup"><span data-stu-id="46b74-124">**MakeCert -sk** *MyNewKey* **-ss** *MyNewStore* **MakeCert -is** *MyNewStore* **-ss** *AnotherStore*</span></span>

-   <span data-ttu-id="46b74-125">Создайте сертификат, используя тестовый корень по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46b74-125">Make a certificate by using the default test root.</span></span> <span data-ttu-id="46b74-126">Сохраните сертификат в хранилище MY.</span><span class="sxs-lookup"><span data-stu-id="46b74-126">Save the certificate to the MY store.</span></span> <span data-ttu-id="46b74-127">Затем создайте другой сертификат, используя только что созданный сертификат.</span><span class="sxs-lookup"><span data-stu-id="46b74-127">Then make another certificate by using the newly created certificate.</span></span> <span data-ttu-id="46b74-128">Если в хранилище MY существует несколько сертификатов, сертификат должен быть идентифицирован с помощью его общего имени.</span><span class="sxs-lookup"><span data-stu-id="46b74-128">If there is more than one certificate in the MY store, the certificate must be identified by using its common name.</span></span>

    <span data-ttu-id="46b74-129">**MakeCert-SK** *миневкэй* **-n "CN = Ксксззии"-SS My MAKECERT-является моим "ксксззии"-SS** *аносерсторе*</span><span class="sxs-lookup"><span data-stu-id="46b74-129">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my MakeCert -is my -in "XXZZYY" -ss** *AnotherStore*</span></span>

-   <span data-ttu-id="46b74-130">Создайте сертификат, используя тестовый корень по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="46b74-130">Make a certificate by using the default test root.</span></span> <span data-ttu-id="46b74-131">Сохраните сертификат в хранилище MY и в файле.</span><span class="sxs-lookup"><span data-stu-id="46b74-131">Save the certificate to the MY store and to a file.</span></span> <span data-ttu-id="46b74-132">Затем создайте другой сертификат, используя только что созданный сертификат *Минев* .</span><span class="sxs-lookup"><span data-stu-id="46b74-132">Then make another certificate by using the newly created *MyNew* certificate.</span></span> <span data-ttu-id="46b74-133">Если в хранилище MY имеется несколько сертификатов, однозначно Идентифицируйте первый сертификат с помощью имени файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="46b74-133">If there is more than one certificate in the MY store, uniquely identify the first certificate by using the certificate file name.</span></span>

    <span data-ttu-id="46b74-134">**MakeCert-SK** *миневкэй* **-n "CN = ксксззии"-SS My** *Минев. cer* **MakeCert-является My-МФ** *Минев. cer* **-SS** *аносерсторе*</span><span class="sxs-lookup"><span data-stu-id="46b74-134">**MakeCert -sk** *MyNewKey* **-n "CN=XXZZYY" -ss my** *MyNew.cer* **MakeCert -is my -ic** *MyNew.cer* **-ss** *AnotherStore*</span></span>

 

 



