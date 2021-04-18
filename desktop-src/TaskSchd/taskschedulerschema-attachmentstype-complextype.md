---
title: Сложный тип Аттачментстипе
description: Определяет элементы, используемые для указания вложений, отправляемых с сообщением электронной почты.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- планировщик задач сложного типа Аттачментстипе
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682010"
---
# <a name="attachmentstype-complex-type"></a><span data-ttu-id="d9f4d-104">Сложный тип Аттачментстипе</span><span class="sxs-lookup"><span data-stu-id="d9f4d-104">attachmentsType Complex Type</span></span>

<span data-ttu-id="d9f4d-105">Определяет элементы, используемые для указания вложений, отправляемых с сообщением электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d9f4d-105">Defines the elements used to specify an attachment sent with an email message.</span></span>

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d9f4d-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d9f4d-106">Child elements</span></span>



| <span data-ttu-id="d9f4d-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="d9f4d-107">Element</span></span>                                                          | <span data-ttu-id="d9f4d-108">Тип</span><span class="sxs-lookup"><span data-stu-id="d9f4d-108">Type</span></span>                                                                    | <span data-ttu-id="d9f4d-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d9f4d-109">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9f4d-110">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d9f4d-110">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="d9f4d-111">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="d9f4d-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="d9f4d-112">Указывает путь к файлу, который отправляется в виде вложения в сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d9f4d-112">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d9f4d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d9f4d-113">Requirements</span></span>



| <span data-ttu-id="d9f4d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d9f4d-114">Requirement</span></span> | <span data-ttu-id="d9f4d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d9f4d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d9f4d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9f4d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d9f4d-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9f4d-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d9f4d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9f4d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d9f4d-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d9f4d-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





