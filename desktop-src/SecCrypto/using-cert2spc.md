---
description: Следующая команда заключает в оболочку сертификат X. 509, MyCert. cer, в тестовый \# сертификат издателя по PKCS 7 (SPC), именуемый MyCert. SPC.
ms.assetid: c3287289-d2bf-4d1d-80f0-e7dd41a3cbe3
title: Использование Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca10b0ab121e283a181c84b056b63ce10ece385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543519"
---
# <a name="using-cert2spc"></a><span data-ttu-id="25e6d-103">Использование Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="25e6d-103">Using Cert2SPC</span></span>

<span data-ttu-id="25e6d-104">Следующая команда заключает в оболочку сертификат [*X. 509*](../secgloss/x-gly.md) , *MyCert*. cer, в тестовый \# [*сертификат издателя по*](../secgloss/s-gly.md) PKCS 7 (SPC), именуемый *MyCert*. SPC.</span><span class="sxs-lookup"><span data-stu-id="25e6d-104">The following command wraps an [*X.509*](../secgloss/x-gly.md) certificate, *MyCert*.cer, into a test PKCS \#7 [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC), called *MyCert*.spc.</span></span> <span data-ttu-id="25e6d-105">Созданный SPC будет использоваться только в целях тестирования.</span><span class="sxs-lookup"><span data-stu-id="25e6d-105">The SPC created is to be used for test purposes only.</span></span> <span data-ttu-id="25e6d-106">SPC, используемый для фактического подписывания кода, который необходимо распространить на общедоступную службу, должен быть получен от ГТЕ, VeriSign, Inc. или другого доверенного [*центра сертификации*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="25e6d-106">An SPC used to actually sign code to be distributed to the public must be obtained from GTE, VeriSign, Inc., or another trusted [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="25e6d-107">**Cert2SPC** \*MyCert \* *. cer* \*  *MyCert \* \* *. SPC**</span><span class="sxs-lookup"><span data-stu-id="25e6d-107">**Cert2SPC** *MyCert\*\*\*.cer*\* *MyCert\*\*\*.spc*\*</span></span>

 

 
