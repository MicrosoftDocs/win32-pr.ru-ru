---
title: Кредентиалсблоб (Еафостусеркредентиалс), элемент
description: Используется, когда конфигурация метода является двоичным BLOB-объектом, а не в текстовом формате XML.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Элемент Кредентиалсблоб EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135471"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a><span data-ttu-id="4106d-104">Кредентиалсблоб (Еафостусеркредентиалс), элемент</span><span class="sxs-lookup"><span data-stu-id="4106d-104">CredentialsBlob (EapHostUserCredentials) Element</span></span>

<span data-ttu-id="4106d-105">Элемент **кредентиалсблоб (еафостусеркредентиалс)** используется, когда конфигурация метода является двоичным BLOB-объектом, а не в ТЕКСТОВОМ формате XML.</span><span class="sxs-lookup"><span data-stu-id="4106d-105">The **CredentialsBlob (EapHostUserCredentials)** element is used when the method configuration is a binary BLOB instead of in XML text format.</span></span>

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="4106d-106">Элемент **кредентиалсблоб** определяется элементом [**еафостусеркредентиалс**](eaphostusercredentialsschema-eaphostusercredentials-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4106d-106">The **CredentialsBlob** element is defined by the [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4106d-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4106d-107">Remarks</span></span>

<span data-ttu-id="4106d-108">Элементы [**Credential**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) и **кредентиалсблоб** не могут одновременно использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="4106d-108">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and **CredentialsBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="4106d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="4106d-109">Requirements</span></span>



| <span data-ttu-id="4106d-110">Требование</span><span class="sxs-lookup"><span data-stu-id="4106d-110">Requirement</span></span> | <span data-ttu-id="4106d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4106d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4106d-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4106d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4106d-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4106d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4106d-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4106d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4106d-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4106d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4106d-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4106d-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="4106d-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="4106d-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4106d-118">**еафостусеркредентиалс**</span><span class="sxs-lookup"><span data-stu-id="4106d-118">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

<span data-ttu-id="4106d-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="4106d-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4106d-120">**еафостусеркредентиалс**</span><span class="sxs-lookup"><span data-stu-id="4106d-120">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[<span data-ttu-id="4106d-121">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="4106d-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4106d-122">Схема еафостусеркредентиалс</span><span class="sxs-lookup"><span data-stu-id="4106d-122">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





