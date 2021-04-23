---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "105664841"
---
# <a name="cert2spc"></a><span data-ttu-id="e0d86-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="e0d86-103">Cert2SPC</span></span>

<span data-ttu-id="e0d86-104">Средство Cert2SPC создает тестовый [*сертификат издателя программного обеспечения*](../secgloss/s-gly.md) (SPC) с помощью существующих [*сертификатов*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e0d86-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="e0d86-105">Cert2SPC может заключить несколько сертификатов X. 509 в объект данных, подписанных [*PKCS \# 7*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e0d86-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="e0d86-106">Средство устанавливается в \\ папку bin пути установки пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e0d86-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="e0d86-107">Cert2SPC доступен в составе Windows SDK, который можно скачать из <https://go.microsoft.com/fwlink/p/?linkid=84091> .</span><span class="sxs-lookup"><span data-stu-id="e0d86-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="e0d86-108">Это средство предназначено только для тестирования.</span><span class="sxs-lookup"><span data-stu-id="e0d86-108">This tool is for test purposes only.</span></span> <span data-ttu-id="e0d86-109">Допустимый SPC получен из [*центра сертификации*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e0d86-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="e0d86-110">**Cert2SPC** *Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="e0d86-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="e0d86-111">*Output. SPC*</span><span class="sxs-lookup"><span data-stu-id="e0d86-111">*Output.spc*</span></span>

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d86-112">*Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="e0d86-112">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="e0d86-113">Имена сертификатов X. 509 для включения в SPC.</span><span class="sxs-lookup"><span data-stu-id="e0d86-113">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="e0d86-114">Каждое имя сертификата заканчивается расширением CER.</span><span class="sxs-lookup"><span data-stu-id="e0d86-114">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="e0d86-115">*Output. SPC*</span><span class="sxs-lookup"><span data-stu-id="e0d86-115">*Output.spc*</span></span>            | <span data-ttu-id="e0d86-116">Имя \# объекта PKCS 7, содержащего создаваемые сертификаты X. 509.</span><span class="sxs-lookup"><span data-stu-id="e0d86-116">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="e0d86-117">Имя выходного файла заканчивается расширением SPC.</span><span class="sxs-lookup"><span data-stu-id="e0d86-117">The output file name ends with the .spc extension.</span></span> |



 

 

 
