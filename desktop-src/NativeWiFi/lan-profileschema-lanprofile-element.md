---
description: Содержит профиль проводной сети.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Ланпрофиле, элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 58ad88c9f975455bdd2d77a0ef8ee028d9027d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265405"
---
# <a name="lanprofile-element"></a><span data-ttu-id="7c8e7-103">Ланпрофиле, элемент</span><span class="sxs-lookup"><span data-stu-id="7c8e7-103">LANProfile Element</span></span>

<span data-ttu-id="7c8e7-104">Элемент Ланпрофиле содержит профиль проводной сети.</span><span class="sxs-lookup"><span data-stu-id="7c8e7-104">The LANProfile element contains a wired network profile.</span></span> <span data-ttu-id="7c8e7-105">Этот элемент является уникальным корневым элементом для профиля проводной сети.</span><span class="sxs-lookup"><span data-stu-id="7c8e7-105">This element is the unique root element for a wired network profile.</span></span>

<span data-ttu-id="7c8e7-106">Целевое пространство имен для элемента Ланпрофиле — `https://www.microsoft.com/networking/LAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="7c8e7-106">The target namespace for the LANProfile element is `https://www.microsoft.com/networking/LAN/profile/v1`.</span></span>

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="MSM">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="security">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OneXEnforced"
                                        type="boolean"
                                     />
                                    <xs:element name="OneXEnabled"
                                        type="boolean"
                                     />
                                    <xs:any
                                        processContents="lax"
                                        minOccurs="0"
                                        maxOccurs="unbounded"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="7c8e7-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7c8e7-107">Child elements</span></span>



| <span data-ttu-id="7c8e7-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="7c8e7-108">Element</span></span>                                                                 | <span data-ttu-id="7c8e7-109">Тип</span><span class="sxs-lookup"><span data-stu-id="7c8e7-109">Type</span></span>    | <span data-ttu-id="7c8e7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7c8e7-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c8e7-111">**MSM**</span><span class="sxs-lookup"><span data-stu-id="7c8e7-111">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)                 |         | <span data-ttu-id="7c8e7-112">Содержит параметры модуля для конкретных носителей (MSM).</span><span class="sxs-lookup"><span data-stu-id="7c8e7-112">Contains media-specific module (MSM) settings.</span></span> <br/>                                                                               |
| [<span data-ttu-id="7c8e7-113">**онексенаблед**</span><span class="sxs-lookup"><span data-stu-id="7c8e7-113">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="7c8e7-114">Логическое</span><span class="sxs-lookup"><span data-stu-id="7c8e7-114">boolean</span></span> | <span data-ttu-id="7c8e7-115">Указывает, будет ли служба автоматической настройки для проводных сетей попытаться выполнить проверку подлинности через порт 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="7c8e7-115">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="7c8e7-116">**онексенфорцед**</span><span class="sxs-lookup"><span data-stu-id="7c8e7-116">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="7c8e7-117">Логическое</span><span class="sxs-lookup"><span data-stu-id="7c8e7-117">boolean</span></span> | <span data-ttu-id="7c8e7-118">Указывает, требует ли служба автоматической настройки для проводных сетей использование 802.1 X для проверки подлинности портов.</span><span class="sxs-lookup"><span data-stu-id="7c8e7-118">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="7c8e7-119">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="7c8e7-119">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="7c8e7-120">Содержит параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="7c8e7-120">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="7c8e7-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c8e7-121">Remarks</span></span>

<span data-ttu-id="7c8e7-122">Сведения о просмотре списка дочерних элементов в древовидной структуре см. в разделе [ \_ элементы схемы профиля локальной сети](lan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="7c8e7-122">To view the list of child elements in a tree-like structure, see [LAN\_profile Schema Elements](lan-profileschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c8e7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7c8e7-123">Requirements</span></span>



| <span data-ttu-id="7c8e7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7c8e7-124">Requirement</span></span> | <span data-ttu-id="7c8e7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7c8e7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7c8e7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c8e7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7c8e7-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c8e7-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7c8e7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c8e7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7c8e7-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7c8e7-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




