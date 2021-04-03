---
title: Сложный тип Процессинжеррордататипе
description: Определяет ошибку, которая произошла во время отображения данных события для события.
ms.assetid: fd1cc78c-1da5-43c5-8c4b-8abe7e1dc1e1
keywords:
- Журнал событий сложных типов Процессинжеррордататипе
topic_type:
- apiref
api_name:
- ProcessingErrorDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcc9d2beed4050a8eed34925f30e52f67d129b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136898"
---
# <a name="processingerrordatatype-complex-type"></a><span data-ttu-id="b8cb1-104">Сложный тип Процессинжеррордататипе</span><span class="sxs-lookup"><span data-stu-id="b8cb1-104">ProcessingErrorDataType Complex Type</span></span>

<span data-ttu-id="b8cb1-105">Определяет ошибку, которая произошла во время отображения данных события для события.</span><span class="sxs-lookup"><span data-stu-id="b8cb1-105">Defines an error that occurred while rendering the event data for the event.</span></span> <span data-ttu-id="b8cb1-106">Это может произойти, если данные события не соответствуют определению шаблона данных события в манифесте.</span><span class="sxs-lookup"><span data-stu-id="b8cb1-106">This can occur if the event data does not match the event data template definition in the manifest.</span></span>

``` syntax
<xs:complexType name="ProcessingErrorDataType">
    <xs:sequence>
        <xs:element name="ErrorCode"
            type="unsignedInt"
         />
        <xs:element name="DataItemName"
            type="string"
         />
        <xs:element name="EventPayload"
            type="hexBinary"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b8cb1-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b8cb1-107">Child elements</span></span>



| <span data-ttu-id="b8cb1-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="b8cb1-108">Element</span></span>                                                                          | <span data-ttu-id="b8cb1-109">Тип</span><span class="sxs-lookup"><span data-stu-id="b8cb1-109">Type</span></span>        | <span data-ttu-id="b8cb1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b8cb1-110">Description</span></span>                                                                          |
|----------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8cb1-111">**DataItemName**</span><span class="sxs-lookup"><span data-stu-id="b8cb1-111">**DataItemName**</span></span>](eventschema-dataitemname-processingerrordatatype-element.md) | <span data-ttu-id="b8cb1-112">строка</span><span class="sxs-lookup"><span data-stu-id="b8cb1-112">string</span></span>      | <span data-ttu-id="b8cb1-113">Имя элемента данных события, вызвавшего ошибку.</span><span class="sxs-lookup"><span data-stu-id="b8cb1-113">The name of the event data item that caused the error.</span></span><br/>                    |
| [<span data-ttu-id="b8cb1-114">**Код ошибки**</span><span class="sxs-lookup"><span data-stu-id="b8cb1-114">**ErrorCode**</span></span>](eventschema-errorcode-processingerrordatatype-element.md)       | <span data-ttu-id="b8cb1-115">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b8cb1-115">unsignedInt</span></span> | <span data-ttu-id="b8cb1-116">Код ошибки ошибки, произошедшей при отображении данных события.</span><span class="sxs-lookup"><span data-stu-id="b8cb1-116">The error code of the error that occurred while rendering the event data.</span></span><br/> |
| [<span data-ttu-id="b8cb1-117">**евентпайлоад**</span><span class="sxs-lookup"><span data-stu-id="b8cb1-117">**EventPayload**</span></span>](eventschema-eventpayload-processingerrordatatype-element.md) | <span data-ttu-id="b8cb1-118">hexBinary</span><span class="sxs-lookup"><span data-stu-id="b8cb1-118">hexBinary</span></span>   | <span data-ttu-id="b8cb1-119">Двоичный BLOB-объект, содержащий все данные события.</span><span class="sxs-lookup"><span data-stu-id="b8cb1-119">A binary blob that contains the entire event data.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="b8cb1-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b8cb1-120">Requirements</span></span>



| <span data-ttu-id="b8cb1-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b8cb1-121">Requirement</span></span> | <span data-ttu-id="b8cb1-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b8cb1-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b8cb1-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b8cb1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b8cb1-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8cb1-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b8cb1-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b8cb1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b8cb1-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b8cb1-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





