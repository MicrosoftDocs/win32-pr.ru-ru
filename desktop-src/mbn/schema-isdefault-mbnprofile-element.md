---
description: Указывает, является ли этот профиль профилем по умолчанию для устройства.
ms.assetid: 024ef936-ddf4-41f6-81c9-5c8a632690a0
title: Default (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsDefault
api_type:
- Schema
ms.openlocfilehash: a59001e385fa7007d188daf2c1348d1a00c3a074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497373"
---
# <a name="isdefault-mbnprofile-element"></a><span data-ttu-id="3e657-103">Default (Мбнпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="3e657-103">IsDefault (MBNProfile) Element</span></span>

<span data-ttu-id="3e657-104">Элемент **Default (мбнпрофиле)** указывает, является ли этот профиль профилем по умолчанию для устройства.</span><span class="sxs-lookup"><span data-stu-id="3e657-104">The **IsDefault (MBNProfile)** element specifies if this is the default profile for the device.</span></span>

<span data-ttu-id="3e657-105">Это необязательный элемент. Если он не указан, профиль не будет установлен в качестве профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e657-105">This is an optional element and if it is not specified then the profile will not be set as the default profile.</span></span>

<span data-ttu-id="3e657-106">Профиль по умолчанию используется службой мобильной широкополосной связи для следующих целей.</span><span class="sxs-lookup"><span data-stu-id="3e657-106">The default profile is used by the Mobile Broadband service for following purposes</span></span>

-   <span data-ttu-id="3e657-107">Служба мобильной широкополосной связи использует параметры подключения из профиля по умолчанию при выполнении автоматических сетевых подключений.</span><span class="sxs-lookup"><span data-stu-id="3e657-107">The Mobile Broadband service uses connection settings from the default profile when performing automatic network connections.</span></span> <span data-ttu-id="3e657-108">Эти параметры включают имя точки доступа, имя пользователя, пароль и т. д.</span><span class="sxs-lookup"><span data-stu-id="3e657-108">These settings include access point name, user name, password, etc.</span></span>
-   <span data-ttu-id="3e657-109">Политика автоматического подключения для мобильного высокоскоростного устройства берется из профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e657-109">Auto connection policy for a Mobile Broadband device is taken from it's default profile.</span></span>
-   <span data-ttu-id="3e657-110">В пользовательском интерфейсе сетевого подключения операционной системы также используются данные подключения из профиля по умолчанию для операций подключения.</span><span class="sxs-lookup"><span data-stu-id="3e657-110">The operating system network connection UI also uses connection data from the default profile for connection operations.</span></span>

<span data-ttu-id="3e657-111">Поставщики услуг сотовой связи могут предоставлять сведения о подключении в профиле и настраивать этот профиль в качестве профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3e657-111">Cellular service providers can provide the connection details in a profile and configure that profile as a default profile.</span></span> <span data-ttu-id="3e657-112">Служба мобильной широкополосной связи будет использовать эти параметры подключения без запроса дополнительных сведений о пользователе.</span><span class="sxs-lookup"><span data-stu-id="3e657-112">The Mobile Broadband service will use these connection settings without prompting user for details.</span></span>

``` syntax
<xs:element name="IsDefault"
    type="boolean"
 />
```

<span data-ttu-id="3e657-113">Элемент **Default** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3e657-113">The **IsDefault** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e657-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3e657-114">Requirements</span></span>



| <span data-ttu-id="3e657-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3e657-115">Requirement</span></span> | <span data-ttu-id="3e657-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3e657-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="3e657-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e657-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e657-118">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="3e657-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="3e657-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e657-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e657-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3e657-120">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="3e657-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e657-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e657-122">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="3e657-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3e657-123">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="3e657-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="3e657-124">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="3e657-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3e657-125">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="3e657-125">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




