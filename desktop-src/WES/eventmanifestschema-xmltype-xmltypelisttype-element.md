---
title: xmlType (Ксмлтипелисттипе), элемент
description: Определяет тип XML.
ms.assetid: 4443963f-f47a-4371-87d8-58f508ba15d6
keywords:
- Журнал событий элемента xmlType
topic_type:
- apiref
api_name:
- xmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5aa37214c5efc0dee9e788ad10ed2f437e3df19f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691824"
---
# <a name="xmltype-xmltypelisttype-element"></a><span data-ttu-id="825f7-104">xmlType (Ксмлтипелисттипе), элемент</span><span class="sxs-lookup"><span data-stu-id="825f7-104">xmlType (XmlTypeListType) Element</span></span>

<span data-ttu-id="825f7-105">Определяет тип XML.</span><span class="sxs-lookup"><span data-stu-id="825f7-105">Defines an XML type.</span></span>

``` syntax
<xs:element name="xmlType">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="XmlType"
            >
                <xs:attribute name="name"
                    type="QName"
                    use="required"
                 />
                <xs:attribute name="value"
                    type="string"
                    use="required"
                 />
                <xs:attribute name="symbol"
                    type="string"
                    use="required"
                 />
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="825f7-106">Элемент **xmlType** определяется сложным типом [**ксмлтипелисттипе**](eventmanifestschema-xmltypelisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="825f7-106">The **xmlType** element is defined by the [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="825f7-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="825f7-107">Attributes</span></span>



| <span data-ttu-id="825f7-108">Имя</span><span class="sxs-lookup"><span data-stu-id="825f7-108">Name</span></span>   | <span data-ttu-id="825f7-109">Тип</span><span class="sxs-lookup"><span data-stu-id="825f7-109">Type</span></span>      | <span data-ttu-id="825f7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="825f7-110">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="825f7-111">name</span><span class="sxs-lookup"><span data-stu-id="825f7-111">name</span></span>   | <span data-ttu-id="825f7-112">**QName**</span><span class="sxs-lookup"><span data-stu-id="825f7-112">**QName**</span></span> | <span data-ttu-id="825f7-113">Имя типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="825f7-113">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="825f7-114">символ</span><span class="sxs-lookup"><span data-stu-id="825f7-114">symbol</span></span> | <span data-ttu-id="825f7-115">строка</span><span class="sxs-lookup"><span data-stu-id="825f7-115">string</span></span>    | <span data-ttu-id="825f7-116">Символ, используемый для ссылки на тип выходных данных в приложении.</span><span class="sxs-lookup"><span data-stu-id="825f7-116">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="825f7-117">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для типа выходных данных в файле заголовка, создаваемом компилятором.</span><span class="sxs-lookup"><span data-stu-id="825f7-117">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="825f7-118">value</span><span class="sxs-lookup"><span data-stu-id="825f7-118">value</span></span>  | <span data-ttu-id="825f7-119">строка</span><span class="sxs-lookup"><span data-stu-id="825f7-119">string</span></span>    | <span data-ttu-id="825f7-120">Целочисленное значение, уникально идентифицирующее тип вывода в списке определяемых типов выходных данных.</span><span class="sxs-lookup"><span data-stu-id="825f7-120">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="825f7-121">Требования</span><span class="sxs-lookup"><span data-stu-id="825f7-121">Requirements</span></span>



| <span data-ttu-id="825f7-122">Требование</span><span class="sxs-lookup"><span data-stu-id="825f7-122">Requirement</span></span> | <span data-ttu-id="825f7-123">Значение</span><span class="sxs-lookup"><span data-stu-id="825f7-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="825f7-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="825f7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="825f7-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="825f7-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="825f7-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="825f7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="825f7-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="825f7-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="825f7-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="825f7-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="825f7-129">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="825f7-129">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="825f7-130">**Ксмлтипес (Типелисттипе)**</span><span class="sxs-lookup"><span data-stu-id="825f7-130">**xmlTypes (TypeListType)**</span></span>](eventmanifestschema-xmltypes-typelisttype-element.md)
</dt> </dl>

 

 





