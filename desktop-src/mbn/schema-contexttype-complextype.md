---
description: Указывает контекст конненктион мобильного широкополосного устройства.
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: Сложный тип contextType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 63d221c6bd388196abfb73a8ac38a26de516d0df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656115"
---
# <a name="contexttype-complex-type"></a><span data-ttu-id="438aa-103">Сложный тип contextType</span><span class="sxs-lookup"><span data-stu-id="438aa-103">contextType Complex Type</span></span>

<span data-ttu-id="438aa-104">Сложный тип **ContextType** указывает контекст Конненктион мобильного широкополосного устройства.</span><span class="sxs-lookup"><span data-stu-id="438aa-104">The **contextType** complex type specifies the connenction context of a Mobile Broadband device.</span></span>

``` syntax
<xs:complexType name="contextType">
    <xs:sequence>
        <xs:element name="AccessString"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:minLength
                        value="1"
                     />
                    <xs:maxLength
                        value="100"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="UserLogonCred"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="UserName"
                        type="nameType"
                     />
                    <xs:element name="IgnorePassword"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:element name="Compression"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="DISABLE"
                     />
                    <xs:enumeration
                        value="ENABLE"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="AuthProtocol"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="NONE"
                     />
                    <xs:enumeration
                        value="PAP"
                     />
                    <xs:enumeration
                        value="CHAP"
                     />
                    <xs:enumeration
                        value="MsCHAPv2"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="438aa-105">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="438aa-105">Child elements</span></span>



| <span data-ttu-id="438aa-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="438aa-106">Element</span></span>                                                               | <span data-ttu-id="438aa-107">Тип</span><span class="sxs-lookup"><span data-stu-id="438aa-107">Type</span></span>                                           | <span data-ttu-id="438aa-108">Описание</span><span class="sxs-lookup"><span data-stu-id="438aa-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="438aa-109">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="438aa-109">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)       |                                                | <span data-ttu-id="438aa-110">Имя точки доступа или строка вызова, используемые для установки подключения к данным</span><span class="sxs-lookup"><span data-stu-id="438aa-110">APN or dial string to be used to establish a data connection</span></span><br/>                        |
| [<span data-ttu-id="438aa-111">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="438aa-111">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)       |                                                | <span data-ttu-id="438aa-112">Протокол проверки подлинности, используемый для активации контекста PDP.</span><span class="sxs-lookup"><span data-stu-id="438aa-112">Authentication protocol to be used for activating a PDP context.</span></span><br/>                    |
| [<span data-ttu-id="438aa-113">**Сжатие**</span><span class="sxs-lookup"><span data-stu-id="438aa-113">**Compression**</span></span>](schema-compression-contexttype-element.md)         |                                                | <span data-ttu-id="438aa-114">Указывает, будет ли использоваться сжатие по каналу данных для заголовка и передачи данных</span><span class="sxs-lookup"><span data-stu-id="438aa-114">Specifies if compression will be used at the data link for header and data transfer</span></span><br/> |
| [<span data-ttu-id="438aa-115">**игнорепассворд**</span><span class="sxs-lookup"><span data-stu-id="438aa-115">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="438aa-116">Логическое</span><span class="sxs-lookup"><span data-stu-id="438aa-116">boolean</span></span>                                        | <span data-ttu-id="438aa-117">Как работать с паролями при обновлении профилей.</span><span class="sxs-lookup"><span data-stu-id="438aa-117">How to handle passwords when upgrading profiles.</span></span><br/>                                    |
| [<span data-ttu-id="438aa-118">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="438aa-118">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="438aa-119">строка</span><span class="sxs-lookup"><span data-stu-id="438aa-119">string</span></span>                                         | <span data-ttu-id="438aa-120">Пароль, используемый для проверки подлинности пользователя</span><span class="sxs-lookup"><span data-stu-id="438aa-120">Password used to authenticate a user</span></span><br/>                                                |
| [<span data-ttu-id="438aa-121">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="438aa-121">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)     |                                                | <span data-ttu-id="438aa-122">Учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="438aa-122">Log on credentials for a connection.</span></span><br/>                                                |
| [<span data-ttu-id="438aa-123">**Имен**</span><span class="sxs-lookup"><span data-stu-id="438aa-123">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="438aa-124">**наметипе**</span><span class="sxs-lookup"><span data-stu-id="438aa-124">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="438aa-125">Имя пользователя для входа</span><span class="sxs-lookup"><span data-stu-id="438aa-125">User name for logon</span></span><br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="438aa-126">Требования</span><span class="sxs-lookup"><span data-stu-id="438aa-126">Requirements</span></span>



| <span data-ttu-id="438aa-127">Требование</span><span class="sxs-lookup"><span data-stu-id="438aa-127">Requirement</span></span> | <span data-ttu-id="438aa-128">Значение</span><span class="sxs-lookup"><span data-stu-id="438aa-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="438aa-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="438aa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="438aa-130">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="438aa-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="438aa-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="438aa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="438aa-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="438aa-132">None supported</span></span><br/>                         |



 

 




