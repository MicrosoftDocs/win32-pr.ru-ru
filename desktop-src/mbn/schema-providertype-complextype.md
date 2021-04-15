---
description: Указывает сведения о сети сотовой связи.
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: Сложный тип providerType (мобильное широкополосное подключение)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662411"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="36f35-103">Сложный тип providerType</span><span class="sxs-lookup"><span data-stu-id="36f35-103">providerType Complex Type</span></span>

<span data-ttu-id="36f35-104">Сложный тип **ProviderType** указывает сведения о сети сотовой связи.</span><span class="sxs-lookup"><span data-stu-id="36f35-104">The **providerType** complex type specifies information about a cellular network.</span></span>

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="36f35-105">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="36f35-105">Child elements</span></span>



| <span data-ttu-id="36f35-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="36f35-106">Element</span></span>                                                          | <span data-ttu-id="36f35-107">Тип</span><span class="sxs-lookup"><span data-stu-id="36f35-107">Type</span></span>                                                           | <span data-ttu-id="36f35-108">Описание</span><span class="sxs-lookup"><span data-stu-id="36f35-108">Description</span></span>               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="36f35-109">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="36f35-109">**ProviderID**</span></span>](schema-providerid-providertype-element.md)     | [<span data-ttu-id="36f35-110">**провидеридтипе**</span><span class="sxs-lookup"><span data-stu-id="36f35-110">**providerIdType**</span></span>](schema-provideridtype-simpletype.md)     | <span data-ttu-id="36f35-111">Идентификатор поставщика.</span><span class="sxs-lookup"><span data-stu-id="36f35-111">Provider ID.</span></span><br/>   |
| [<span data-ttu-id="36f35-112">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="36f35-112">**ProviderName**</span></span>](schema-providername-providertype-element.md) | [<span data-ttu-id="36f35-113">**провидернаметипе**</span><span class="sxs-lookup"><span data-stu-id="36f35-113">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="36f35-114">Имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="36f35-114">Provider name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="36f35-115">Требования</span><span class="sxs-lookup"><span data-stu-id="36f35-115">Requirements</span></span>



| <span data-ttu-id="36f35-116">Требование</span><span class="sxs-lookup"><span data-stu-id="36f35-116">Requirement</span></span> | <span data-ttu-id="36f35-117">Значение</span><span class="sxs-lookup"><span data-stu-id="36f35-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="36f35-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36f35-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36f35-119">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="36f35-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="36f35-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36f35-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36f35-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="36f35-121">None supported</span></span><br/>                         |



 

 




