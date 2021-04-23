---
description: Указывает способ управления паролями при обновлении профилей.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Игнорепассворд (Усерлогонкред), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711161"
---
# <a name="ignorepassword-userlogoncred-element"></a><span data-ttu-id="ad2cb-103">Игнорепассворд (Усерлогонкред), элемент</span><span class="sxs-lookup"><span data-stu-id="ad2cb-103">IgnorePassword (UserLogonCred) Element</span></span>

<span data-ttu-id="ad2cb-104">Элемент **игнорепассворд (усерлогонкред)** определяет способ управления паролями при обновлении профилей.</span><span class="sxs-lookup"><span data-stu-id="ad2cb-104">The **IgnorePassword (UserLogonCred)** element specifies how to handle passwords when upgrading profiles.</span></span>

<span data-ttu-id="ad2cb-105">Если задано значение **true** и профиль с тем же именем существует во время операции обновления, то пароль из этого профиля будет создан и сохранен в новом профиле.</span><span class="sxs-lookup"><span data-stu-id="ad2cb-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in new profile.</span></span>

<span data-ttu-id="ad2cb-106">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ad2cb-106">This element is optional.</span></span>

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

<span data-ttu-id="ad2cb-107">Элемент **игнорепассворд** определяется элементом [**усерлогонкред**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ad2cb-107">The **IgnorePassword** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad2cb-108">Требования</span><span class="sxs-lookup"><span data-stu-id="ad2cb-108">Requirements</span></span>



| <span data-ttu-id="ad2cb-109">Требование</span><span class="sxs-lookup"><span data-stu-id="ad2cb-109">Requirement</span></span> | <span data-ttu-id="ad2cb-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ad2cb-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ad2cb-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad2cb-111">Minimum supported client</span></span><br/> | <span data-ttu-id="ad2cb-112">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ad2cb-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ad2cb-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad2cb-113">Minimum supported server</span></span><br/> | <span data-ttu-id="ad2cb-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ad2cb-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ad2cb-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad2cb-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad2cb-116">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ad2cb-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ad2cb-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="ad2cb-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="ad2cb-118">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ad2cb-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ad2cb-119">**Усерлогонкред (contextType)**</span><span class="sxs-lookup"><span data-stu-id="ad2cb-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




