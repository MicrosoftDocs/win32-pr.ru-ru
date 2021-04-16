---
title: Сложный тип Ксмлтипелисттипе
description: Определяет выходные типы списка, которые служба использует для определения способа визуализации входного типа данных.
ms.assetid: d90b32cc-a0b5-44d1-8083-781aa5e10783
keywords:
- Журнал событий сложных типов Ксмлтипелисттипе
topic_type:
- apiref
api_name:
- XmlTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 388161572ec9c84ed46d5b40987df5fb8d1ed077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340795"
---
# <a name="xmltypelisttype-complex-type"></a><span data-ttu-id="a8dee-104">Сложный тип Ксмлтипелисттипе</span><span class="sxs-lookup"><span data-stu-id="a8dee-104">XmlTypeListType Complex Type</span></span>

<span data-ttu-id="a8dee-105">Определяет выходные типы списка, которые служба использует для определения способа визуализации входного типа данных.</span><span class="sxs-lookup"><span data-stu-id="a8dee-105">Defines a list output types that the service uses to determine how to render an input data type.</span></span>

``` syntax
<xs:complexType name="XmlTypeListType">
    <xs:sequence>
        <xs:element name="xmlType"
            minOccurs="0"
            maxOccurs="unbounded"
        >
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
                            type="CSymbolType"
                            use="required"
                         />
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a8dee-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a8dee-106">Child elements</span></span>



| <span data-ttu-id="a8dee-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="a8dee-107">Element</span></span>                                                                | <span data-ttu-id="a8dee-108">Тип</span><span class="sxs-lookup"><span data-stu-id="a8dee-108">Type</span></span> | <span data-ttu-id="a8dee-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a8dee-109">Description</span></span>                      |
|------------------------------------------------------------------------|------|----------------------------------|
| [<span data-ttu-id="a8dee-110">**xmlType**</span><span class="sxs-lookup"><span data-stu-id="a8dee-110">**xmlType**</span></span>](eventmanifestschema-xmltype-xmltypelisttype-element.md) |      | <span data-ttu-id="a8dee-111">Определяет тип XML.</span><span class="sxs-lookup"><span data-stu-id="a8dee-111">Defines an XML type.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="a8dee-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a8dee-112">Attributes</span></span>



| <span data-ttu-id="a8dee-113">Имя</span><span class="sxs-lookup"><span data-stu-id="a8dee-113">Name</span></span>   | <span data-ttu-id="a8dee-114">Тип</span><span class="sxs-lookup"><span data-stu-id="a8dee-114">Type</span></span>                                                              | <span data-ttu-id="a8dee-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a8dee-115">Description</span></span>                                                                                                                                                                                                                                                |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8dee-116">name</span><span class="sxs-lookup"><span data-stu-id="a8dee-116">name</span></span>   | <span data-ttu-id="a8dee-117">**QName**</span><span class="sxs-lookup"><span data-stu-id="a8dee-117">**QName**</span></span>                                                         | <span data-ttu-id="a8dee-118">Имя типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a8dee-118">The name of the output type.</span></span><br/>                                                                                                                                                                                                                    |
| <span data-ttu-id="a8dee-119">символ</span><span class="sxs-lookup"><span data-stu-id="a8dee-119">symbol</span></span> | [<span data-ttu-id="a8dee-120">**ксимболтипе**</span><span class="sxs-lookup"><span data-stu-id="a8dee-120">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="a8dee-121">Символ, используемый для ссылки на тип выходных данных в приложении.</span><span class="sxs-lookup"><span data-stu-id="a8dee-121">The symbol to use to reference the output type in your application.</span></span> <span data-ttu-id="a8dee-122">[**Компилятор сообщений (MC.exe)**](message-compiler--mc-exe-.md) использует символ, чтобы создать константу для типа выходных данных в файле заголовка, создаваемом компилятором.</span><span class="sxs-lookup"><span data-stu-id="a8dee-122">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the output type in the header file that the compiler generates.</span></span><br/> |
| <span data-ttu-id="a8dee-123">value</span><span class="sxs-lookup"><span data-stu-id="a8dee-123">value</span></span>  | <span data-ttu-id="a8dee-124">строка</span><span class="sxs-lookup"><span data-stu-id="a8dee-124">string</span></span>                                                            | <span data-ttu-id="a8dee-125">Целочисленное значение, уникально идентифицирующее тип вывода в списке определяемых типов выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a8dee-125">An integer value that uniquely identifies the output type in the list of output types that you define.</span></span><br/>                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="a8dee-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8dee-126">Remarks</span></span>

<span data-ttu-id="a8dee-127">\\Файл Include \\Winmeta.xml, включенный в Windows SDK, содержит список предопределенных типов вывода.</span><span class="sxs-lookup"><span data-stu-id="a8dee-127">The \\Include\\Winmeta.xml file, which is included in the Windows SDK, contains a list of predefined output types.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8dee-128">Требования</span><span class="sxs-lookup"><span data-stu-id="a8dee-128">Requirements</span></span>



| <span data-ttu-id="a8dee-129">Требование</span><span class="sxs-lookup"><span data-stu-id="a8dee-129">Requirement</span></span> | <span data-ttu-id="a8dee-130">Значение</span><span class="sxs-lookup"><span data-stu-id="a8dee-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8dee-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8dee-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a8dee-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8dee-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8dee-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8dee-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a8dee-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8dee-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





