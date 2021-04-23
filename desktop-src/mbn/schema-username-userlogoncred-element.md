---
description: Указывает имя пользователя для входа.
ms.assetid: a312de24-2a81-4fac-9c23-4e67e171e692
title: Элемент UserName (Усерлогонкред)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserName
api_type:
- Schema
ms.openlocfilehash: 53ad1bde74f2d2a1649fa5fdee23ef70ab53b09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662391"
---
# <a name="username-userlogoncred-element"></a><span data-ttu-id="fd1a3-103">Элемент UserName (Усерлогонкред)</span><span class="sxs-lookup"><span data-stu-id="fd1a3-103">UserName (UserLogonCred) Element</span></span>

<span data-ttu-id="fd1a3-104">Элемент **username (усерлогонкред)** указывает имя пользователя для входа.</span><span class="sxs-lookup"><span data-stu-id="fd1a3-104">The **UserName (UserLogonCred)** element specifies the user name for logon.</span></span>

<span data-ttu-id="fd1a3-105">Элемент представляет собой строку, которая не может быть длиннее 255 символов.</span><span class="sxs-lookup"><span data-stu-id="fd1a3-105">The element is a string with a maximum of 255 characters.</span></span>

<span data-ttu-id="fd1a3-106">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="fd1a3-106">This element is optional.</span></span>

``` syntax
<xs:element name="UserName"
    type="nameType"
 />
```

<span data-ttu-id="fd1a3-107">Элемент **username** определяется элементом [**усерлогонкред**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fd1a3-107">The **UserName** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd1a3-108">Требования</span><span class="sxs-lookup"><span data-stu-id="fd1a3-108">Requirements</span></span>



| <span data-ttu-id="fd1a3-109">Требование</span><span class="sxs-lookup"><span data-stu-id="fd1a3-109">Requirement</span></span> | <span data-ttu-id="fd1a3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="fd1a3-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="fd1a3-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd1a3-111">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1a3-112">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="fd1a3-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="fd1a3-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd1a3-113">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1a3-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fd1a3-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="fd1a3-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd1a3-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd1a3-116">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="fd1a3-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fd1a3-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="fd1a3-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="fd1a3-118">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="fd1a3-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fd1a3-119">**Усерлогонкред (contextType)**</span><span class="sxs-lookup"><span data-stu-id="fd1a3-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




