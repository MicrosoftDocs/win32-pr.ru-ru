---
title: Сложный тип Хеадерфиелдстипе
description: Определяет элементы, указывающие поля для заголовка электронной почты.
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- планировщик задач сложного типа Хеадерфиелдстипе
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edb783972217d0455eb2ee25fed31cf20e5b774b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489855"
---
# <a name="headerfieldstype-complex-type"></a><span data-ttu-id="cdb32-104">Сложный тип Хеадерфиелдстипе</span><span class="sxs-lookup"><span data-stu-id="cdb32-104">headerFieldsType Complex Type</span></span>

<span data-ttu-id="cdb32-105">Определяет элементы, указывающие поля для заголовка электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cdb32-105">Defines the elements that specify the fields for an email header.</span></span>

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cdb32-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cdb32-106">Child elements</span></span>



| <span data-ttu-id="cdb32-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="cdb32-107">Element</span></span>                                                                         | <span data-ttu-id="cdb32-108">Тип</span><span class="sxs-lookup"><span data-stu-id="cdb32-108">Type</span></span>                                                                       | <span data-ttu-id="cdb32-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cdb32-109">Description</span></span>                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="cdb32-110">**хеадерфиелд**</span><span class="sxs-lookup"><span data-stu-id="cdb32-110">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="cdb32-111">**хеадерфиелдтипе**</span><span class="sxs-lookup"><span data-stu-id="cdb32-111">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="cdb32-112">Задает поле в заголовке сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cdb32-112">Specifies a field in an email header.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="cdb32-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cdb32-113">Requirements</span></span>



| <span data-ttu-id="cdb32-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cdb32-114">Requirement</span></span> | <span data-ttu-id="cdb32-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cdb32-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cdb32-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdb32-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cdb32-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cdb32-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cdb32-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdb32-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cdb32-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cdb32-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





