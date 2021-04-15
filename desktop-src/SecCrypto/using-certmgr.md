---
description: Используйте CertMgr для просмотра сертификатов, списков отзыва сертификатов и списков CTL из файла или хранилища сертификатов, копирования сертификатов в хранилище сертификатов, удаления сертификатов из хранилища сертификатов, а также для сохранения сертификатов в файлах.
ms.assetid: cc2424bf-e7ea-4484-9934-3aba02b63492
title: Использование CertMgr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7e22862184f87e1f070a4683d313cb1457e7d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662629"
---
# <a name="using-certmgr"></a><span data-ttu-id="938e3-103">Использование CertMgr</span><span class="sxs-lookup"><span data-stu-id="938e3-103">Using CertMgr</span></span>

<span data-ttu-id="938e3-104">[CertMgr](certmgr.md) можно использовать для просмотра [*сертификатов*](../secgloss/c-gly.md), [*списков отзыва сертификатов*](../secgloss/c-gly.md) (CRL) и [*списков доверия сертификатов*](../secgloss/c-gly.md) (CTL) из файла или хранилища сертификатов, для копирования сертификатов в [*хранилище сертификатов*](../secgloss/c-gly.md), для удаления сертификатов из хранилища сертификатов и для сохранения сертификатов в файлах.</span><span class="sxs-lookup"><span data-stu-id="938e3-104">[CertMgr](certmgr.md) can be used to view [*certificates*](../secgloss/c-gly.md), [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) from a file or a certificate store, to copy certificates into a [*certificate store*](../secgloss/c-gly.md), to delete certificates from a certificate store, and to save certificates to files.</span></span>

<span data-ttu-id="938e3-105">Если программа [CertMgr](certmgr.md) используется без параметров, то отображается мастер certmgr, который поможет пользователю выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="938e3-105">When [CertMgr](certmgr.md) is used without options, a CertMgr wizard appears to guide the user through the operation.</span></span>

<span data-ttu-id="938e3-106">Файл должен иметь один из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="938e3-106">The file must be one of the following types:</span></span>

-   <span data-ttu-id="938e3-107">Закодированный список CTL, списка отзыва сертификатов или файла сертификата (может быть в кодировке Base-64)</span><span class="sxs-lookup"><span data-stu-id="938e3-107">An encoded CTL, CRL, or certificate file (could be base-64 encoded)</span></span>
-   <span data-ttu-id="938e3-108">Файл PKCS \# 7</span><span class="sxs-lookup"><span data-stu-id="938e3-108">A PKCS \#7 file</span></span>
-   <span data-ttu-id="938e3-109">Файл SPC</span><span class="sxs-lookup"><span data-stu-id="938e3-109">An SPC file</span></span>
-   <span data-ttu-id="938e3-110">Подписанный документ</span><span class="sxs-lookup"><span data-stu-id="938e3-110">A signed document</span></span>
-   <span data-ttu-id="938e3-111">Сериализованный storeFile</span><span class="sxs-lookup"><span data-stu-id="938e3-111">A serialized storeFile</span></span>

<span data-ttu-id="938e3-112">В следующих примерах используются команды [CertMgr](certmgr.md) для выполнения общих задач с сертификатами.</span><span class="sxs-lookup"><span data-stu-id="938e3-112">The following examples use [CertMgr](certmgr.md) commands to perform common certificate tasks.</span></span>

-   <span data-ttu-id="938e3-113">Просмотр сертификатов, списков отзыва сертификатов и списков CTL из *MyFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="938e3-113">View the certificates, CRLs, and CTLs from *MyFile.ext*.</span></span>

    <span data-ttu-id="938e3-114">**CertMgr** *MyFile. ext*</span><span class="sxs-lookup"><span data-stu-id="938e3-114">**certmgr** *MyFile.ext*</span></span>

-   <span data-ttu-id="938e3-115">Просмотрите сертификаты, списки отзыва сертификатов и списки CTL из хранилища системы.</span><span class="sxs-lookup"><span data-stu-id="938e3-115">View the certificates, CRLs, and CTLs from the MY system store.</span></span>

    <span data-ttu-id="938e3-116">**certmgr-s My**</span><span class="sxs-lookup"><span data-stu-id="938e3-116">**certmgr -s my**</span></span>

-   <span data-ttu-id="938e3-117">Скопируйте все сертификаты, списки отзыва сертификатов и списки CTL в файл с именем *MyFile. ext* в новый файл, именуемый *NewFile. ext*.</span><span class="sxs-lookup"><span data-stu-id="938e3-117">Copy all the certificates, CRLs, and CTLs in a file named *MyFile.ext* to a new file, called *NewFile.ext*.</span></span>

    <span data-ttu-id="938e3-118">**CertMgr-Add-ALL-c** *MyFile. ext* *NewFile. ext*</span><span class="sxs-lookup"><span data-stu-id="938e3-118">**certmgr -add -all -c** *MyFile.ext* *NewFile.ext*</span></span>

-   <span data-ttu-id="938e3-119">Скопируйте все сертификаты, списки отзыва сертификатов и списки CTL из хранилища системы в файл с именем *невмифиле. ext*.</span><span class="sxs-lookup"><span data-stu-id="938e3-119">Copy all the certificates, CRLs, and CTLs from the MY system store to a file called *NewMyFile.ext*.</span></span>

    <span data-ttu-id="938e3-120">**CertMgr-Add-все-c-s My** *невмифиле. ext*</span><span class="sxs-lookup"><span data-stu-id="938e3-120">**certmgr -add -all -c -s my** *NewMyFile.ext*</span></span>

-   <span data-ttu-id="938e3-121">Скопируйте сертификат с общим именем *MyCert* в моем системном хранилище в файл с именем *невцерт. cer*.</span><span class="sxs-lookup"><span data-stu-id="938e3-121">Copy a certificate with the common name *MyCert* in the MY system store to a file called *NewCert.cer*.</span></span>

    <span data-ttu-id="938e3-122">**CertMgr-Add-c-n** *MyCert* **-s My** *невцерт. cer*</span><span class="sxs-lookup"><span data-stu-id="938e3-122">**certmgr -add -c -n** *MyCert* **-s my** *NewCert.cer*</span></span>

-   <span data-ttu-id="938e3-123">Удалите все сертификаты из хранилища системы.</span><span class="sxs-lookup"><span data-stu-id="938e3-123">Delete all the certificates from the MY system store.</span></span>

    <span data-ttu-id="938e3-124">**certmgr-del-все-c-s My**</span><span class="sxs-lookup"><span data-stu-id="938e3-124">**certmgr -del -all -c -s my**</span></span>

-   <span data-ttu-id="938e3-125">Удалите все списки CTL из хранилища системы и сохраните полученное хранилище в файл с именем *невсторе. str*.</span><span class="sxs-lookup"><span data-stu-id="938e3-125">Delete all the CTLs from the MY system store and save the resulting store to a file called *NewStore.str*.</span></span>

    <span data-ttu-id="938e3-126">**CertMgr-del-ALL-CTL-s моя** *невсторе. str*</span><span class="sxs-lookup"><span data-stu-id="938e3-126">**certmgr -del -all -ctl -s my** *NewStore.str*</span></span>

-   <span data-ttu-id="938e3-127">Сохраните в файл с именем *невцерт. cer*, сертификат, который является сертификатом в кодировке [*X. 509*](../secgloss/x-gly.md) с общим именем *MyCert* и расположен в корневом хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="938e3-127">Save, to a file called *NewCert.cer*, a certificate that is an [*X.509*](../secgloss/x-gly.md) encoded certificate, that has the common name *MyCert*, and that is located in the Root certificate store.</span></span>

    <span data-ttu-id="938e3-128">**CertMgr-разместил-c-n** *MyCert* **-s root** *невцерт. cer*</span><span class="sxs-lookup"><span data-stu-id="938e3-128">**certmgr -put -c -n** *MyCert* **-s root** *NewCert.cer*</span></span>

## <a name="related-topics"></a><span data-ttu-id="938e3-129">См. также</span><span class="sxs-lookup"><span data-stu-id="938e3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="938e3-130">CertMgr</span><span class="sxs-lookup"><span data-stu-id="938e3-130">CertMgr</span></span>](certmgr.md)
</dt> </dl>

 

 
