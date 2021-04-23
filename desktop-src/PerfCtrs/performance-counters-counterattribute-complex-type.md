---
description: Определяет атрибут счетчика, который указывает, как данные счетчика отображаются в приложении-потребителе.
ms.assetid: 3749501b-4f3e-42e5-b1d5-2700b6d4a48a
title: Сложный тип Каунтераттрибуте
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1b34a3a802f0f7c79815956c3a364522ce0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663201"
---
# <a name="counterattribute-complex-type"></a><span data-ttu-id="2a4d5-103">Сложный тип Каунтераттрибуте</span><span class="sxs-lookup"><span data-stu-id="2a4d5-103">counterAttribute Complex Type</span></span>

<span data-ttu-id="2a4d5-104">Определяет атрибут счетчика, который указывает, как данные счетчика отображаются в приложении-потребителе.</span><span class="sxs-lookup"><span data-stu-id="2a4d5-104">Defines an attribute of a counter that specifies how the counter data is displayed in a consumer application.</span></span>

``` syntax
<xs:complexType name="counterAttribute">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                use="required"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="xs:string"
                    >
                        <xs:enumeration
                            value="reference"
                         />
                        <xs:enumeration
                            value="noDisplay"
                         />
                        <xs:enumeration
                            value="noDigitGrouping"
                         />
                        <xs:enumeration
                            value="displayAsHex"
                         />
                        <xs:enumeration
                            value="displayAsReal"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="2a4d5-105">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2a4d5-105">Attributes</span></span>



| <span data-ttu-id="2a4d5-106">Имя</span><span class="sxs-lookup"><span data-stu-id="2a4d5-106">Name</span></span> | <span data-ttu-id="2a4d5-107">Тип</span><span class="sxs-lookup"><span data-stu-id="2a4d5-107">Type</span></span> | <span data-ttu-id="2a4d5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2a4d5-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a4d5-109">name</span><span class="sxs-lookup"><span data-stu-id="2a4d5-109">name</span></span> |      | <span data-ttu-id="2a4d5-110">Имя применяемого атрибута вывода.</span><span class="sxs-lookup"><span data-stu-id="2a4d5-110">The name of the display attribute to apply.</span></span> <span data-ttu-id="2a4d5-111">Можно указать одно из следующих имен:</span><span class="sxs-lookup"><span data-stu-id="2a4d5-111">You can specify one of the following names:</span></span><br/> <dl> <span data-ttu-id="2a4d5-112"><dt><span id="reference"></span><span id="REFERENCE"></span>IsReference</dt></span><span class="sxs-lookup"><span data-stu-id="2a4d5-112"><dt><span id="reference"></span><span id="REFERENCE"></span>reference</dt></span></span> <dd> <span data-ttu-id="2a4d5-113">Получите значение счетчика по ссылке, а не по значению.</span><span class="sxs-lookup"><span data-stu-id="2a4d5-113">Retrieve the value of the counter by reference as opposed to by value.</span></span><br/> </dd> <span data-ttu-id="2a4d5-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>не отображать</dt></span><span class="sxs-lookup"><span data-stu-id="2a4d5-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>noDisplay</dt></span></span> <dd> <span data-ttu-id="2a4d5-115">Не отображать значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="2a4d5-115">Do not display the counter value.</span></span> <span data-ttu-id="2a4d5-116">Как правило, этот атрибут используется, если данные счетчика используются в качестве входных данных для вычисления значения другого счетчика.</span><span class="sxs-lookup"><span data-stu-id="2a4d5-116">Typically, you use this attribute if the counter's data is used as input for calculating another counter's value.</span></span> <br/> </dd> <span data-ttu-id="2a4d5-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>нодигитграупинг</dt></span><span class="sxs-lookup"><span data-stu-id="2a4d5-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt></span></span> <dd> <span data-ttu-id="2a4d5-118">Приложения-потребитель или мониторинг не должны использовать разделители цифр при отображении значений счетчиков.</span><span class="sxs-lookup"><span data-stu-id="2a4d5-118">Consumer or monitoring applications should not use digit separators when displaying counter values.</span></span> <br/> </dd> <span data-ttu-id="2a4d5-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>дисплайашекс</dt></span><span class="sxs-lookup"><span data-stu-id="2a4d5-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt></span></span> <dd> <span data-ttu-id="2a4d5-120">Приложение-потребитель или монитор мониторинга должны отображать значение счетчика в шестнадцатеричном формате вместо целочисленного значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a4d5-120">Consumer or monitoring applications should display the counter value as a hexadecimal, instead of the default integer value.</span></span><br/> </dd> <span data-ttu-id="2a4d5-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>дисплайасреал</dt></span><span class="sxs-lookup"><span data-stu-id="2a4d5-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt></span></span> <dd> <span data-ttu-id="2a4d5-122">Потребительское приложение или приложения мониторинга должны отображать значение счетчика как вещественное число, а не целочисленное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a4d5-122">Consumer or monitoring applications should display the counter value as a real number, instead of the default integer value.</span></span> <br/> </dd> </dl> |



## <a name="requirements"></a><span data-ttu-id="2a4d5-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2a4d5-123">Requirements</span></span>



| <span data-ttu-id="2a4d5-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2a4d5-124">Requirement</span></span> | <span data-ttu-id="2a4d5-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2a4d5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2a4d5-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a4d5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2a4d5-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a4d5-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2a4d5-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a4d5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2a4d5-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a4d5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




