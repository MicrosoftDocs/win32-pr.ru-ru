---
description: Защищенные данные хранятся в виде большого двоичного объекта в кодировке ASN. 1.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Формат защищенных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156146"
---
# <a name="protected-data-format"></a><span data-ttu-id="12a00-103">Формат защищенных данных</span><span class="sxs-lookup"><span data-stu-id="12a00-103">Protected Data Format</span></span>

<span data-ttu-id="12a00-104">Защищенные данные хранятся в виде большого двоичного объекта в кодировке ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="12a00-104">Protected data is stored as an ASN.1 encoded BLOB.</span></span> <span data-ttu-id="12a00-105">Данные форматируются как CMS (синтаксис сообщений сертификата) в виде упакованного содержимого.</span><span class="sxs-lookup"><span data-stu-id="12a00-105">The data is formatted as CMS (certificate message syntax) enveloped content.</span></span> <span data-ttu-id="12a00-106">Цифровой конверт содержит зашифрованное содержимое, сведения о получателе, содержащие зашифрованный ключ шифрования содержимого (CEK), и заголовок, содержащий сведения о содержимом, включая строку правила незашифрованного дескриптора защиты.</span><span class="sxs-lookup"><span data-stu-id="12a00-106">The digital envelope contains encrypted content, recipient information that contains an encrypted content encryption key (CEK), and a header that contains information about the content, including the unencrypted protection descriptor rule string.</span></span> <span data-ttu-id="12a00-107">Это показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="12a00-107">This is shown by the following diagram.</span></span>

![защищенные запечатанные данные](images/protecteddatablob.png)

## <a name="related-topics"></a><span data-ttu-id="12a00-109">См. также</span><span class="sxs-lookup"><span data-stu-id="12a00-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12a00-110">CNG DPAPI</span><span class="sxs-lookup"><span data-stu-id="12a00-110">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="12a00-111">Дескрипторы защиты</span><span class="sxs-lookup"><span data-stu-id="12a00-111">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> <dt>

[<span data-ttu-id="12a00-112">Поставщики защиты</span><span class="sxs-lookup"><span data-stu-id="12a00-112">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



