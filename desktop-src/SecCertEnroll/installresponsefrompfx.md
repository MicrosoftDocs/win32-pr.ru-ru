---
description: Устанавливает зарегистрированный сертификат из файла обмена личной информацией (PFX) в хранилище сертификатов.
ms.assetid: f42379d0-b80e-4d95-ab34-9bb35fde06fd
title: инсталлреспонсефромпфкс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db435b3d61f5b2e53a9838024f4080bb8028ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999223"
---
# <a name="installresponsefrompfx"></a><span data-ttu-id="cf3de-103">инсталлреспонсефромпфкс</span><span class="sxs-lookup"><span data-stu-id="cf3de-103">installResponseFromPFX</span></span>

<span data-ttu-id="cf3de-104">Пример Инсталлреспонсефромпфкс устанавливает зарегистрированный сертификат из файла обмена личной информацией (PFX) в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cf3de-104">The installResponseFromPFX sample installs an enrolled certificate from a Personal Information Exchange (PFX) file to the certificate store.</span></span>

## <a name="location"></a><span data-ttu-id="cf3de-105">Расположение</span><span class="sxs-lookup"><span data-stu-id="cf3de-105">Location</span></span>

<span data-ttu-id="cf3de-106">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows этот образец устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ инсталлреспонсефромпфкс.</span><span class="sxs-lookup"><span data-stu-id="cf3de-106">When you install the Microsoft Windows Software Development Kit (SDK), the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\installResponseFromPFX folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="cf3de-107">Разговор</span><span class="sxs-lookup"><span data-stu-id="cf3de-107">Discussion</span></span>

<span data-ttu-id="cf3de-108">Пример Инсталлреспонсефромпфкс:</span><span class="sxs-lookup"><span data-stu-id="cf3de-108">The installResponseFromPFX sample:</span></span>

1.  <span data-ttu-id="cf3de-109">Обрабатывает аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="cf3de-109">Processes the command line arguments.</span></span> <span data-ttu-id="cf3de-110">Командная строка должна содержать:</span><span class="sxs-lookup"><span data-stu-id="cf3de-110">The command line should contain:</span></span>
    -   <span data-ttu-id="cf3de-111">Имя образца.</span><span class="sxs-lookup"><span data-stu-id="cf3de-111">The name of the sample.</span></span>
    -   <span data-ttu-id="cf3de-112">Имя PFX-файла, содержащего зарегистрированный сертификат.</span><span class="sxs-lookup"><span data-stu-id="cf3de-112">The name of the PFX file that contains the enrolled certificate.</span></span>
    -   <span data-ttu-id="cf3de-113">Пароль, связанный с PFX-файлом.</span><span class="sxs-lookup"><span data-stu-id="cf3de-113">A password associated with the PFX file.</span></span>
2.  <span data-ttu-id="cf3de-114">Считывает PFX-файл, сначала пытается выполнить формат Base64, а двоичный формат — в случае сбоя Base64.</span><span class="sxs-lookup"><span data-stu-id="cf3de-114">Reads the PFX file, trying the base64 format first and the binary format if base64 fails.</span></span> <span data-ttu-id="cf3de-115">Функция Декодефилев () определена в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="cf3de-115">The DecodeFileW() function is defined in enrollCommon.cpp.</span></span>
3.  <span data-ttu-id="cf3de-116">Преобразует зарегистрированный сертификат в **BSTR** и использует его для инициализации объекта [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) .</span><span class="sxs-lookup"><span data-stu-id="cf3de-116">Converts the enrolled certificate to a **BSTR** and uses it to initialize an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object.</span></span> <span data-ttu-id="cf3de-117">Функция Конвертвсзтобстр определена в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="cf3de-117">The convertWszToBstr function is defined in enrollCommon.cpp.</span></span>
4.  <span data-ttu-id="cf3de-118">Устанавливает сертификат в хранилище сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cf3de-118">Installs the certificate in the certificate store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf3de-119">См. также</span><span class="sxs-lookup"><span data-stu-id="cf3de-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf3de-120">енроллеобокмк</span><span class="sxs-lookup"><span data-stu-id="cf3de-120">enrollEOBOCMC</span></span>](enrolleobocmc.md)
</dt> <dt>

[<span data-ttu-id="cf3de-121">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="cf3de-121">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



