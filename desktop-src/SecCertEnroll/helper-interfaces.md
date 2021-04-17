---
description: API регистрации сертификатов поддерживают следующие интерфейсы общего использования.
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Вспомогательные интерфейсы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a0c6948e9b0fe09aee0b983d230f53bc8e76b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684185"
---
# <a name="helper-interfaces"></a><span data-ttu-id="d52d1-103">Вспомогательные интерфейсы</span><span class="sxs-lookup"><span data-stu-id="d52d1-103">Helper Interfaces</span></span>

<span data-ttu-id="d52d1-104">API регистрации сертификатов поддерживают следующие интерфейсы общего использования.</span><span class="sxs-lookup"><span data-stu-id="d52d1-104">The following general use interfaces are supported by the Certificate Enrollment API.</span></span>



| <span data-ttu-id="d52d1-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="d52d1-105">Interface</span></span>                                                                    | <span data-ttu-id="d52d1-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d52d1-106">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d52d1-107">**ибинариконвертер**</span><span class="sxs-lookup"><span data-stu-id="d52d1-107">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | <span data-ttu-id="d52d1-108">Создает строку в кодировке Юникод из массива байтов, создает массив байтов из строки в кодировке Юникод и изменяет тип кодировки Юникода, применяемый к строке.</span><span class="sxs-lookup"><span data-stu-id="d52d1-108">Creates a Unicode-encoded string from a byte array, creates a byte array from a Unicode-encoded string, and modifies the type of Unicode encoding applied to a string.</span></span> |
| [<span data-ttu-id="d52d1-109">**ицертификатеаттестатиончалленже**</span><span class="sxs-lookup"><span data-stu-id="d52d1-109">**ICertificateAttestationChallenge**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | <span data-ttu-id="d52d1-110">Поддерживает проблемы аттестации сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d52d1-110">Supports certificate attestation challenges.</span></span>                                                                                                                           |
| [<span data-ttu-id="d52d1-111">**иобжектид**</span><span class="sxs-lookup"><span data-stu-id="d52d1-111">**IObjectId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | <span data-ttu-id="d52d1-112">Представляет идентификатор объекта.</span><span class="sxs-lookup"><span data-stu-id="d52d1-112">Represents an object identifier.</span></span>                                                                                                                                       |
| [<span data-ttu-id="d52d1-113">**иобжектидс**</span><span class="sxs-lookup"><span data-stu-id="d52d1-113">**IObjectIds**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | <span data-ttu-id="d52d1-114">Управляет коллекцией объектов [**иобжектид**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) .</span><span class="sxs-lookup"><span data-stu-id="d52d1-114">Manages a collection of [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) objects.</span></span>                                                                                                        |
| [<span data-ttu-id="d52d1-115">**IX500DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="d52d1-115">**IX500DistinguishedName**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | <span data-ttu-id="d52d1-116">Представляет различающееся имя X. 500.</span><span class="sxs-lookup"><span data-stu-id="d52d1-116">Represents an X.500 distinguished name.</span></span>                                                                                                                                |
| [<span data-ttu-id="d52d1-117">**IX509EndorsementKey**</span><span class="sxs-lookup"><span data-stu-id="d52d1-117">**IX509EndorsementKey**</span></span>](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | <span data-ttu-id="d52d1-118">Интерфейс ключа подтверждения X. 509</span><span class="sxs-lookup"><span data-stu-id="d52d1-118">X.509 Endorsement Key Interface</span></span>                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="d52d1-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d52d1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d52d1-120">Интерфейсы Цертенролл</span><span class="sxs-lookup"><span data-stu-id="d52d1-120">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



