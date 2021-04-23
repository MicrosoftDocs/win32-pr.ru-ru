---
description: Средства CryptoAPI — это инструменты для выполнения общих задач управления сертификатами.
ms.assetid: 29146de8-adae-444b-bc75-fa43a19ab8f9
title: Средства для создания, просмотра и управления сертификатами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2fb4595b7c7711b10271bd97a447a77f3a01c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817856"
---
# <a name="tools-to-create-view-and-manage-certificates"></a><span data-ttu-id="ba498-103">Средства для создания, просмотра и управления сертификатами</span><span class="sxs-lookup"><span data-stu-id="ba498-103">Tools to Create, View, and Manage Certificates</span></span>

<span data-ttu-id="ba498-104">Средства CryptoAPI — это инструменты для выполнения общих задач управления сертификатами.</span><span class="sxs-lookup"><span data-stu-id="ba498-104">CryptoAPI Tools are tools to perform common certificate management tasks.</span></span>



| <span data-ttu-id="ba498-105">Средство</span><span class="sxs-lookup"><span data-stu-id="ba498-105">Tool</span></span>                                | <span data-ttu-id="ba498-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba498-106">Remarks</span></span>                                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba498-107">Программой</span><span class="sxs-lookup"><span data-stu-id="ba498-107">MakeCert</span></span>](makecert.md)<br/> | <span data-ttu-id="ba498-108">Создает тестовый сертификат [*X. 509*](../secgloss/x-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ba498-108">Creates a test [*X.509*](../secgloss/x-gly.md) certificate.</span></span><br/>                                                                                |
| [<span data-ttu-id="ba498-109">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="ba498-109">Cert2SPC</span></span>](cert2spc.md)<br/> | <span data-ttu-id="ba498-110">Создает тестовый [*сертификат издателя программного обеспечения*](../secgloss/s-gly.md) (SPC).</span><span class="sxs-lookup"><span data-stu-id="ba498-110">Creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC).</span></span><br/>           |
| [<span data-ttu-id="ba498-111">CertMgr</span><span class="sxs-lookup"><span data-stu-id="ba498-111">CertMgr</span></span>](certmgr.md)<br/>   | <span data-ttu-id="ba498-112">Управляет сертификатами, [*списками CTL и отзывами сертификатов*](../secgloss/c-gly.md) (CRL).</span><span class="sxs-lookup"><span data-stu-id="ba498-112">Manages certificates, CTLs, and [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs).</span></span><br/> |



 

<span data-ttu-id="ba498-113">Все введенные пользователем данные для этих средств не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="ba498-113">All user input to these tools is case insensitive.</span></span> <span data-ttu-id="ba498-114">Для имени [*пары ключей*](../secgloss/k-gly.md) и файла [*закрытого ключа*](../secgloss/p-gly.md) теперь существуют отдельные параметры.</span><span class="sxs-lookup"><span data-stu-id="ba498-114">Separate options now exist for the [*key pair*](../secgloss/k-gly.md) name and the [*private key*](../secgloss/p-gly.md) file.</span></span>

## <a name="additional-tools"></a><span data-ttu-id="ba498-115">Дополнительные средства</span><span class="sxs-lookup"><span data-stu-id="ba498-115">Additional Tools</span></span>

<span data-ttu-id="ba498-116">Certutil.exe — это программа командной строки, которая устанавливается в составе служб сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ba498-116">Certutil.exe is a command-line tool that is installed as part of Certificate Services.</span></span> <span data-ttu-id="ba498-117">Certutil.exe можно использовать для дампа и просмотра сведений о конфигурации [*центра сертификации*](../secgloss/c-gly.md) (ЦС), настройки служб сертификатов, резервного копирования и восстановления компонентов ЦС, а также для проверки [*сертификатов*](../secgloss/c-gly.md), [*пар ключей*](../secgloss/k-gly.md)и цепочек сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ba498-117">You can use Certutil.exe to dump and display [*certification authority*](../secgloss/c-gly.md) (CA) configuration information, configure Certificate Services, back up and restore CA components, and verify [*certificates*](../secgloss/c-gly.md), [*key pairs*](../secgloss/k-gly.md), and certificate chains.</span></span> <span data-ttu-id="ba498-118">Дополнительные сведения о программе certutil см. в разделе [certutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732443(v=ws.11)) статьи Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="ba498-118">For more information about Certutil, see the [Certutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732443(v=ws.11)) topic on Microsoft TechNet.</span></span>

 

 
