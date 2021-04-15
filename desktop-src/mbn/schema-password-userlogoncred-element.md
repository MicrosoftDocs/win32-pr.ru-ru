---
description: Указывает пароль, используемый для проверки подлинности пользователя.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Password (Усерлогонкред), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662397"
---
# <a name="password-userlogoncred-element"></a><span data-ttu-id="c3ea2-103">Password (Усерлогонкред), элемент</span><span class="sxs-lookup"><span data-stu-id="c3ea2-103">Password (UserLogonCred) Element</span></span>

<span data-ttu-id="c3ea2-104">Элемент [**Password (усерлогонкред)**](schema-ignorepassword-userlogoncred-element.md) указывает пароль, используемый для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="c3ea2-104">The [**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) element specifies the password used to authenticate a user.</span></span>

<span data-ttu-id="c3ea2-105">Элемент представляет собой строку длиной до 255 символов.</span><span class="sxs-lookup"><span data-stu-id="c3ea2-105">The element is a string of up to 255 characters.</span></span>

<span data-ttu-id="c3ea2-106">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="c3ea2-106">This element is optional.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="c3ea2-107">Элемент **Password** определяется элементом [**усерлогонкред**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c3ea2-107">The **Password** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ea2-108">Требования</span><span class="sxs-lookup"><span data-stu-id="c3ea2-108">Requirements</span></span>



| <span data-ttu-id="c3ea2-109">Требование</span><span class="sxs-lookup"><span data-stu-id="c3ea2-109">Requirement</span></span> | <span data-ttu-id="c3ea2-110">Значение</span><span class="sxs-lookup"><span data-stu-id="c3ea2-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c3ea2-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3ea2-111">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ea2-112">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="c3ea2-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c3ea2-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3ea2-113">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ea2-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c3ea2-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="c3ea2-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3ea2-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3ea2-116">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="c3ea2-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c3ea2-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="c3ea2-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="c3ea2-118">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="c3ea2-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c3ea2-119">**Усерлогонкред (contextType)**</span><span class="sxs-lookup"><span data-stu-id="c3ea2-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




