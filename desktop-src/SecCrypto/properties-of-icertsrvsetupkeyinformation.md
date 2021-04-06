---
description: Следующие свойства определяются интерфейсом Ицертсрвсетупкэйинформатион.
ms.assetid: d805a011-8728-4687-8e4a-ad331617abe7
title: Свойства Ицертсрвсетупкэйинформатион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2a41647c06015c011d4d7a36cddfd81466b3b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910072"
---
# <a name="properties-of-icertsrvsetupkeyinformation"></a><span data-ttu-id="c5008-103">Свойства Ицертсрвсетупкэйинформатион</span><span class="sxs-lookup"><span data-stu-id="c5008-103">Properties of ICertSrvSetupKeyInformation</span></span>

<span data-ttu-id="c5008-104">Следующие свойства определяются интерфейсом [**ицертсрвсетупкэйинформатион**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) .</span><span class="sxs-lookup"><span data-stu-id="c5008-104">The following properties are defined by the [**ICertSrvSetupKeyInformation**](/windows/desktop/api/Casetup/nn-casetup-icertsrvsetupkeyinformation) interface.</span></span>



| <span data-ttu-id="c5008-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="c5008-105">Property</span></span>                                                                           | <span data-ttu-id="c5008-106">Описание</span><span class="sxs-lookup"><span data-stu-id="c5008-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5008-107">**ContainerName**</span><span class="sxs-lookup"><span data-stu-id="c5008-107">**ContainerName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_containername)                 | <span data-ttu-id="c5008-108">Возвращает или задает имя, используемое [*поставщиком служб шифрования*](../secgloss/c-gly.md) (CSP) для создания, хранения ключа или доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="c5008-108">Gets or sets the name used by the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to generate, store, or access the key.</span></span>                                                                       |
| [<span data-ttu-id="c5008-109">**Существующий**</span><span class="sxs-lookup"><span data-stu-id="c5008-109">**Existing**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existing)                           | <span data-ttu-id="c5008-110">Возвращает или задает значение, указывающее, существует ли уже закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="c5008-110">Gets or sets a value that indicates whether the private key already exists.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="c5008-111">**ексистингкацертификате**</span><span class="sxs-lookup"><span data-stu-id="c5008-111">**ExistingCACertificate**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_existingcacertificate) | <span data-ttu-id="c5008-112">Возвращает или задает двоичное значение, закодированное с помощью [*distinguished Encoding Rules*](../secgloss/d-gly.md) (Der) и представляющее собой двоичное значение сертификата ЦС, соответствующего существующему ключу.</span><span class="sxs-lookup"><span data-stu-id="c5008-112">Gets or sets the binary value that has been encoded by using [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER) and that is the binary value of the CA certificate that corresponds to an existing key.</span></span> |
| [<span data-ttu-id="c5008-113">**HashAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="c5008-113">**HashAlgorithm**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_hashalgorithm)                 | <span data-ttu-id="c5008-114">Возвращает или задает имя хэш-алгоритма, используемого для подписания или проверки сертификата ЦС для ключа.</span><span class="sxs-lookup"><span data-stu-id="c5008-114">Gets or sets the name of the hash algorithm used to sign or verify the CA certificate for the key.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="c5008-115">**Длина**</span><span class="sxs-lookup"><span data-stu-id="c5008-115">**Length**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_length)                               | <span data-ttu-id="c5008-116">Возвращает или задает стойкость ключа к одному из значений, поддерживаемых CSP.</span><span class="sxs-lookup"><span data-stu-id="c5008-116">Gets or sets the strength of the key to one of the values supported by the CSP.</span></span>                                                                                                                                                                                                                   |
| [<span data-ttu-id="c5008-117">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="c5008-117">**ProviderName**</span></span>](/windows/desktop/api/Casetup/nf-casetup-icertsrvsetupkeyinformation-get_providername)                   | <span data-ttu-id="c5008-118">Возвращает или задает имя CSP, используемого для создания или хранения закрытого ключа.</span><span class="sxs-lookup"><span data-stu-id="c5008-118">Gets or sets the name of the CSP that is used to generate or store the private key.</span></span>                                                                                                                                                                                                               |



 

 

 
