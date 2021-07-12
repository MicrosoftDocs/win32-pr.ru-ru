---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581982"
---
# <a name="cert2spc"></a><span data-ttu-id="1970a-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="1970a-103">Cert2SPC</span></span>

<span data-ttu-id="1970a-104">средство Cert2SPC создает тестовое [*программное обеспечение Publisher сертификате*](../secgloss/s-gly.md) (SPC) с использованием существующих [*сертификатов*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1970a-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="1970a-105">Cert2SPC может заключить несколько сертификатов X. 509 в объект данных, подписанных [*PKCS \# 7*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1970a-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="1970a-106">это средство устанавливается в \\ папку Bin установочного пакета Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1970a-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="1970a-107">Cert2SPC доступен в составе Windows SDK, который можно скачать из <https://go.microsoft.com/fwlink/p/?linkid=84091> .</span><span class="sxs-lookup"><span data-stu-id="1970a-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="1970a-108">Это средство предназначено только для тестирования.</span><span class="sxs-lookup"><span data-stu-id="1970a-108">This tool is for test purposes only.</span></span> <span data-ttu-id="1970a-109">Допустимый SPC получен из [*центра сертификации*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1970a-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="1970a-110">**Cert2SPC** *Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="1970a-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="1970a-111">*Output. SPC*</span><span class="sxs-lookup"><span data-stu-id="1970a-111">*Output.spc*</span></span>

 



| <span data-ttu-id="1970a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1970a-112">Parameters</span></span>              | <span data-ttu-id="1970a-113">Описание</span><span class="sxs-lookup"><span data-stu-id="1970a-113">Description</span></span>                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1970a-114">*Cert1. cer Cert2. cer* ...</span><span class="sxs-lookup"><span data-stu-id="1970a-114">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="1970a-115">Имена сертификатов X. 509 для включения в SPC.</span><span class="sxs-lookup"><span data-stu-id="1970a-115">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="1970a-116">Каждое имя сертификата заканчивается расширением CER.</span><span class="sxs-lookup"><span data-stu-id="1970a-116">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="1970a-117">*Output. SPC*</span><span class="sxs-lookup"><span data-stu-id="1970a-117">*Output.spc*</span></span>            | <span data-ttu-id="1970a-118">Имя \# объекта PKCS 7, содержащего создаваемые сертификаты X. 509.</span><span class="sxs-lookup"><span data-stu-id="1970a-118">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="1970a-119">Имя выходного файла заканчивается расширением SPC.</span><span class="sxs-lookup"><span data-stu-id="1970a-119">The output file name ends with the .spc extension.</span></span> |



 

 

 
