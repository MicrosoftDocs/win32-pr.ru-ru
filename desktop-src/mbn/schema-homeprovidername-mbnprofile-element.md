---
description: Определяет имя поставщика услуг домашнего доступа для указанной SIM-карты или устройства.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Хомепровидернаме (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809617"
---
# <a name="homeprovidername-mbnprofile-element"></a><span data-ttu-id="ba3c7-103">Хомепровидернаме (Мбнпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="ba3c7-103">HomeProviderName (MBNProfile) Element</span></span>

<span data-ttu-id="ba3c7-104">Элемент **хомепровидернаме (мбнпрофиле)** определяет имя поставщика услуг домашнего доступа для указанной SIM-карты или устройства.</span><span class="sxs-lookup"><span data-stu-id="ba3c7-104">The **HomeProviderName (MBNProfile)** element identifies the name of Home provider for the given SIM/Device.</span></span>

<span data-ttu-id="ba3c7-105">Этот элемент является необязательным и задается службой мобильного широкополосного подключения для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="ba3c7-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="ba3c7-106">Приложение не должно задавать это поле при создании или обновлении профиля.</span><span class="sxs-lookup"><span data-stu-id="ba3c7-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

<span data-ttu-id="ba3c7-107">Элемент **хомепровидернаме** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ba3c7-107">The **HomeProviderName** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba3c7-108">Требования</span><span class="sxs-lookup"><span data-stu-id="ba3c7-108">Requirements</span></span>



| <span data-ttu-id="ba3c7-109">Требование</span><span class="sxs-lookup"><span data-stu-id="ba3c7-109">Requirement</span></span> | <span data-ttu-id="ba3c7-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ba3c7-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ba3c7-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba3c7-111">Minimum supported client</span></span><br/> | <span data-ttu-id="ba3c7-112">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ba3c7-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ba3c7-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba3c7-113">Minimum supported server</span></span><br/> | <span data-ttu-id="ba3c7-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ba3c7-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ba3c7-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba3c7-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba3c7-116">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ba3c7-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ba3c7-117">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="ba3c7-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="ba3c7-118">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ba3c7-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ba3c7-119">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="ba3c7-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




