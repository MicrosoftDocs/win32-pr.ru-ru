---
title: Сложный тип Нетворксеттингстипе
description: Определяет элементы, которые предоставляют параметры, которые служба планировщик задач использует для получения сетевого профиля.
ms.assetid: e5df1dda-b691-47ff-a956-50ff1ce9c7cc
keywords:
- планировщик задач сложного типа Нетворксеттингстипе
topic_type:
- apiref
api_name:
- networkSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb2a8389b1e1f368bedf03fa38dce9c8e262a401
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988869"
---
# <a name="networksettingstype-complex-type"></a><span data-ttu-id="05f69-104">Сложный тип Нетворксеттингстипе</span><span class="sxs-lookup"><span data-stu-id="05f69-104">networkSettingsType Complex Type</span></span>

<span data-ttu-id="05f69-105">Определяет элементы, которые предоставляют параметры, которые служба планировщик задач использует для получения сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="05f69-105">Defines the elements that provide the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

``` syntax
<xs:complexType name="networkSettingsType">
    <xs:all>
        <xs:element name="Name"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="Id"
            type="guidType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="05f69-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="05f69-106">Child elements</span></span>



| <span data-ttu-id="05f69-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="05f69-107">Element</span></span>                                                              | <span data-ttu-id="05f69-108">Тип</span><span class="sxs-lookup"><span data-stu-id="05f69-108">Type</span></span>                                                        | <span data-ttu-id="05f69-109">Описание</span><span class="sxs-lookup"><span data-stu-id="05f69-109">Description</span></span>                                                                                 |
|----------------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05f69-110">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="05f69-110">**Id**</span></span>](taskschedulerschema-id-networksettingstype-element.md)     | [<span data-ttu-id="05f69-111">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="05f69-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md) | <span data-ttu-id="05f69-112">Указывает значение идентификатора GUID, определяющее сетевой профиль.</span><span class="sxs-lookup"><span data-stu-id="05f69-112">Specifies a GUID value that identifies a network profile.</span></span> <br/>                       |
| [<span data-ttu-id="05f69-113">**Имя**</span><span class="sxs-lookup"><span data-stu-id="05f69-113">**Name**</span></span>](taskschedulerschema-name-networksettingstype-element.md) | <span data-ttu-id="05f69-114">нонемптистринг</span><span class="sxs-lookup"><span data-stu-id="05f69-114">nonEmptyString</span></span>                                              | <span data-ttu-id="05f69-115">Указывает имя сетевого профиля.</span><span class="sxs-lookup"><span data-stu-id="05f69-115">Specifies the name of a network profile.</span></span> <span data-ttu-id="05f69-116">Имя используется в целях показа.</span><span class="sxs-lookup"><span data-stu-id="05f69-116">The name is used for display purposes.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="05f69-117">Требования</span><span class="sxs-lookup"><span data-stu-id="05f69-117">Requirements</span></span>



| <span data-ttu-id="05f69-118">Требование</span><span class="sxs-lookup"><span data-stu-id="05f69-118">Requirement</span></span> | <span data-ttu-id="05f69-119">Значение</span><span class="sxs-lookup"><span data-stu-id="05f69-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05f69-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05f69-120">Minimum supported client</span></span><br/> | <span data-ttu-id="05f69-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05f69-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05f69-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05f69-122">Minimum supported server</span></span><br/> | <span data-ttu-id="05f69-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05f69-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





