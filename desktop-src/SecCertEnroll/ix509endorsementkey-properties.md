---
description: Интерфейс IX509EndorsementKey предоставляет следующие свойства.
ms.assetid: 9E93622B-56E9-4F2F-9EFA-4F63D45EDCB6
title: Свойства IX509EndorsementKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4bbdbc464803988f5b1100ac42fc0e3697fb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647464"
---
# <a name="ix509endorsementkey-properties"></a><span data-ttu-id="149c9-103">Свойства IX509EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="149c9-103">IX509EndorsementKey Properties</span></span>

<span data-ttu-id="149c9-104">Интерфейс [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) предоставляет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="149c9-104">The [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="149c9-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="149c9-105">In this section</span></span>



| <span data-ttu-id="149c9-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="149c9-106">Topic</span></span>                                                                        | <span data-ttu-id="149c9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="149c9-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="149c9-108">**Свойство Length**</span><span class="sxs-lookup"><span data-stu-id="149c9-108">**Length property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_length)<br/>             | <span data-ttu-id="149c9-109">Битовая длина ключа подтверждения.</span><span class="sxs-lookup"><span data-stu-id="149c9-109">The bit length of the endorsement key.</span></span> <span data-ttu-id="149c9-110">Доступ к этому свойству можно получить только после вызова метода [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="149c9-110">You can only access this property after the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been called.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="149c9-111">**Открытое свойство**</span><span class="sxs-lookup"><span data-stu-id="149c9-111">**Opened property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_opened)<br/>             | <span data-ttu-id="149c9-112">Указывает, был ли успешно вызван метод [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="149c9-112">Indicates whether the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method has been successfully called.</span></span><br/>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="149c9-113">**ProviderName, свойство**</span><span class="sxs-lookup"><span data-stu-id="149c9-113">**ProviderName property**</span></span>](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername)<br/> | <span data-ttu-id="149c9-114">Имя поставщика шифрования.</span><span class="sxs-lookup"><span data-stu-id="149c9-114">The name of the encryption provider.</span></span> <span data-ttu-id="149c9-115">По умолчанию используется поставщик криптографии платформы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="149c9-115">The default is the Microsoft Platform Crypto Provider.</span></span> <span data-ttu-id="149c9-116">Свойство [**providerName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) необходимо задать до вызова метода [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) .</span><span class="sxs-lookup"><span data-stu-id="149c9-116">You must set the [**ProviderName**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-get_providername) property before you call the [**Open**](/windows/desktop/api/Certenroll/nf-certenroll-ix509endorsementkey-open) method.</span></span> <span data-ttu-id="149c9-117">Невозможно изменить свойство **providerName** после вызова метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="149c9-117">You cannot change the **ProviderName** property after you have called the **Open** method.</span></span><br/> |



 

 

 




