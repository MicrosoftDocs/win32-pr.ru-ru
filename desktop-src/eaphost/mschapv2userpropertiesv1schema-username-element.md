---
title: Элемент username (CHAP)
description: Сведения об элементе username, определяющем пользователя, для которого выполняется проверка подлинности. См. пример синтаксиса и Просмотр дополнительных доступных ресурсов.
ms.assetid: 3dd12864-5e0a-492c-a2c3-28118d21a0f2
keywords:
- Элемент username, EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29065a59e150d2a4295e91b41862250d58e017b5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987884"
---
# <a name="username-element-chap"></a><span data-ttu-id="94c80-105">Элемент username (CHAP)</span><span class="sxs-lookup"><span data-stu-id="94c80-105">Username element (CHAP)</span></span>

<span data-ttu-id="94c80-106">Элемент **username** определяет пользователя, для которого выполняется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="94c80-106">The **Username** element identifies the user being authenticated.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="remarks"></a><span data-ttu-id="94c80-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94c80-107">Remarks</span></span>

<span data-ttu-id="94c80-108">Если элемент **username** отсутствует, имя пользователя получается из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="94c80-108">If the **Username** element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="94c80-109">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="94c80-109">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="94c80-110">Требования</span><span class="sxs-lookup"><span data-stu-id="94c80-110">Requirements</span></span>



| <span data-ttu-id="94c80-111">Роль</span><span class="sxs-lookup"><span data-stu-id="94c80-111">Role</span></span> | <span data-ttu-id="94c80-112">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="94c80-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="94c80-113">Клиент</span><span class="sxs-lookup"><span data-stu-id="94c80-113">Client</span></span><br/> | <span data-ttu-id="94c80-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94c80-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94c80-115">Сервер</span><span class="sxs-lookup"><span data-stu-id="94c80-115">Server</span></span><br/> | <span data-ttu-id="94c80-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94c80-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94c80-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94c80-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94c80-118">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="94c80-118">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="94c80-119">Схема mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="94c80-119">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





