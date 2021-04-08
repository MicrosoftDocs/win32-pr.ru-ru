---
description: Установщик Windows могут использовать цифровые подписи для обнаружения поврежденных ресурсов.
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: Цифровые подписи и внешние CAB-файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10e921b324a43a919a417f47953c0a44e4777ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910956"
---
# <a name="digital-signatures-and-external-cabinet-files"></a><span data-ttu-id="191dd-103">Цифровые подписи и внешние CAB-файлы</span><span class="sxs-lookup"><span data-stu-id="191dd-103">Digital Signatures and External Cabinet Files</span></span>

<span data-ttu-id="191dd-104">Установщик Windows могут использовать цифровые подписи для обнаружения поврежденных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="191dd-104">Windows Installer can use digital signatures to detect corrupted resources.</span></span> <span data-ttu-id="191dd-105">При установке внешнего ресурса сертификат для подписи, принадлежащий ресурсу, может быть проверен на соответствие сертификату подписания, созданному в пакете.</span><span class="sxs-lookup"><span data-stu-id="191dd-105">When installing an external resource, the signer certificate belonging to the resource may be verified against a reference signer certificate authored in the package.</span></span> <span data-ttu-id="191dd-106">Установщик не может проверить подписи для внутренних ящиков.</span><span class="sxs-lookup"><span data-stu-id="191dd-106">The installer cannot verify signatures for internal cabinets.</span></span> <span data-ttu-id="191dd-107">Проверять цифровые подписи можно только с помощью [таблицы мсидигиталсигнатуре](msidigitalsignature-table.md) и [таблицы мсидигиталцертификате](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="191dd-107">It can only verify digital signatures by using the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>

<span data-ttu-id="191dd-108">При установке файла, хранящегося во внешнем CAB-файле, установщик Windows выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="191dd-108">Windows Installer does the following when installing a file stored in an external cabinet:</span></span>

-   <span data-ttu-id="191dd-109">Установщик проверяет, присутствует ли запись носителя для этого внешнего CAB-файла в [таблице мсидигиталсигнатуре](msidigitalsignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="191dd-109">The installer checks to see whether the media entry for that external cabinet is listed in the [MsiDigitalSignature table](msidigitalsignature-table.md).</span></span> <span data-ttu-id="191dd-110">Файл, хранящийся во внешнем CAB-файле, определяется с помощью записи в столбце CAB-файла [таблицы мультимедиа](media-table.md) , которая не является префиксом \# символа "".</span><span class="sxs-lookup"><span data-stu-id="191dd-110">A file stored in an external cabinet is identified by having an entry in the Cabinet column of the [Media table](media-table.md) that is not prefixed by a '\#' character.</span></span>
-   <span data-ttu-id="191dd-111">Перед открытием внешнего CAB-файла установщик вызывает WinVerifyTrust для извлечения текущего сертификата и хэш-информации.</span><span class="sxs-lookup"><span data-stu-id="191dd-111">Before opening the external cabinet, the installer calls WinVerifyTrust to extract the current certificate and hash information.</span></span> <span data-ttu-id="191dd-112">В случае несоответствия между текущими сведениями о подписи в CAB-файле и сведениями о подписи, созданными в пакете, установка завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="191dd-112">If there is a mismatch between the current signature information on the cabinet and the signature information authored in the package, the installation fails.</span></span> <span data-ttu-id="191dd-113">Установка завершается сбоем, так как CAB-файл может быть скомпрометирован и не может быть доверенным.</span><span class="sxs-lookup"><span data-stu-id="191dd-113">The installation fails because the cabinet may have been compromised and cannot be trusted.</span></span>

<span data-ttu-id="191dd-114">Дополнительные сведения об использовании цифровых подписей, цифровых сертификатов и [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)см. в разделе " [Безопасность](https://msdn.microsoft.com/library/cc527452.aspx) " пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="191dd-114">For more information regarding the use of digital signatures, digital certificates, and [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), see the [Security](https://msdn.microsoft.com/library/cc527452.aspx) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="191dd-115">Дополнительные сведения см. в разделе [**мсижетфилесигнатуреинформатион**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [Мсидигиталцертификате Table](msidigitalcertificate-table.md)и [мсидигиталсигнатуре Table](msidigitalsignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="191dd-115">For more information, see [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [MsiDigitalCertificate table](msidigitalcertificate-table.md), and [MsiDigitalSignature table](msidigitalsignature-table.md).</span></span>

 

 
