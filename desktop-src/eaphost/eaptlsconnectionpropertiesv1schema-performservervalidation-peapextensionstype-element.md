---
title: Перформсервервалидатион (Еаптипе)
description: Сведения об элементе Перформсервервалидатион. Этот элемент указывает, выполняется ли проверка сервера. | Перформсервервалидатион (Еаптипе)
ms.assetid: f6233bff-18e4-45b4-b598-839fa198f676
keywords:
- элемент EAPHost
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655379676bd117b89a6fe41a8d6895260e71a2bf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694041"
---
# <a name="performservervalidation-eaptype"></a><span data-ttu-id="027da-106">Перформсервервалидатион (Еаптипе)</span><span class="sxs-lookup"><span data-stu-id="027da-106">PerformServerValidation (EapType)</span></span>

<span data-ttu-id="027da-107">Элемент **перформсервервалидатион (еаптипе)** указывает, выполняется ли проверка сервера.</span><span class="sxs-lookup"><span data-stu-id="027da-107">The **PerformServerValidation (EapType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS:PerformServerValidation "
 />
```

<span data-ttu-id="027da-108">Элемент определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="027da-108">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="027da-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="027da-109">Remarks</span></span>

<span data-ttu-id="027da-110">Элемент **перформсервервалидатион** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="027da-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="027da-111">Требования</span><span class="sxs-lookup"><span data-stu-id="027da-111">Requirements</span></span>



| <span data-ttu-id="027da-112">Роль</span><span class="sxs-lookup"><span data-stu-id="027da-112">Role</span></span> | <span data-ttu-id="027da-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="027da-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="027da-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="027da-114">Client</span></span><br/> | <span data-ttu-id="027da-115">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="027da-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="027da-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="027da-116">Server</span></span><br/> | <span data-ttu-id="027da-117">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="027da-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="027da-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="027da-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="027da-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="027da-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="027da-120">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="027da-120">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="027da-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="027da-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="027da-122">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="027da-122">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="027da-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="027da-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="027da-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="027da-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="027da-125">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="027da-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="027da-126">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="027da-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="027da-127">**Перформсервервалидатион (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="027da-127">**PerformServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv2shema-tlsextensions-tlsextensionstype-element.md)
</dt> </dl>

 

 





